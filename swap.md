# Coisas relacionadas a uso de memória Swap:

## Top 10 dos processos que estão usando swap:

>``` find /proc -maxdepth 2 -path "/proc/[0-9]*/status" -readable -exec awk -v FS=":" -v TOTSWP="$(cat /proc/swaps 
| sed 1d | awk 'BEGIN{sum=0} {sum=sum+$(NF-2)} END{print sum}')" '{process[$1]=$2;sub(/^[ \t]+/,"",process[$1]);} 
END {if(process["VmSwap"] && process["VmSwap"] != "0 kB") {used_swap=process["VmSwap"];sub(/[ a-zA-Z]+/,"",used_swap);
percent=(used_swap/TOTSWP*100); printf "%10s %-30s %20s %6.2f%\n",process["Pid"],process["Name"],process["VmSwap"],percent} }' '{}' \;  | awk '{print $(NF-2),$0}' | sort -hr | head | cut -d " " -f2-```
