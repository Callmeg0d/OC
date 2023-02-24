#!/bin/bash

current_pcent=$(df --output=pcent /LOG)
current_pcent=${current_pcent//[^0-9]/}
pcent_limit = 70
echo "used $current_pcent%"

if [ $current_pcent -gt $pcent_limit ]
then
	sudo tar -cf /BACKUP/archive1.tar.gz /LOG
	sudo rm /LOG/*
fi
