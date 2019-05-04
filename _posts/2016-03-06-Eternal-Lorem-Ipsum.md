Null meeting.

apache_logs.tar.gz

cat  access.log | cut -f 1 -d\ |sort |uniq |wc -l



delim

cat  access.log | cut -f 1 -d\ |sort |uniq -c|sort -rn | head -10

cat  access.log | cut -f 1 -d: |cut -f 2-3 -d/ |uniq -c | head


awk i used for small program better than delimiter
head access.log |awk '{print $4}'

head access.log |awk -F ':' '{print $1":"$4}'


head access.log |rev|cut -f 4 -d\" |rev

cat access.log |rev|cut -f 4 -d\" |rev | sort |uniq |wc

cat browser-uas.list |cut -f 1 -d\ browser-uas.list |sort |uniq -c |sort -rn |head

grep Mozilla browser-uas.list |cut -f 2 -d\ |sort |uniq -c|sort -rn


Jq


cat corrected_sample | jq '.states'

cat corrected_sample | jq '.outline.continent'

cat corrected_sample | jq '.details [0].UP[0].name'

cat corrected_sample | jq '.details [] |{'capitals': .UP[0].name}'

cat corrected_sample | jq '(.details[].UP[]?, .details[].MP[]?^C.details[].KA[]?).name'

cat corrected_sample |jq '(.details[].UP[]?, .details[].MP[]?).name, .details[].KA.name'



ls /root/Desktop/null_puliya_logs/cloudtrail/AWSLogs/872777666335/CloudTrail/us-west-2/2019/03/2* |grep json.gz |xargs -i ./abcd.sh {}





