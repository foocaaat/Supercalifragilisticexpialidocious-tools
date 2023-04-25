#!/usr/bin/bash
if [ ! -f .cache/morning ]; then
    date '+%Y-%m-%d' > .cache/morning
else
    if [ "$(cat .cache/morning)" == "" ];then
        date '+%Y-%m-%d' -d "$(cat $HOME/.cache/morning | awk '{print $1;}')" > .cache/morning
    else
        todate=$(date -d $(date '+%Y-%m-%d') +%s)
        cond=$(date -d $(cat $HOME/.cache/morning | awk '{print $1;}') +%s )

        if [ $todate -gt $cond ];
        then
            echo $(date '+%Y-%m-%d' -d "$(cat $HOME/.cache/morning | awk '{print $1;}') + 1 days") $(date +%s) > .cache/morning
        else
            echo Yu have travel to the end of time 
        fi  

    fi
fi

