1. Connection to internalhost with one command from localhost

`$ ssh -t -i ~/.ssh/appuser -A appuser@35.205.217.189 ssh -A internalhost`

2. Shortcut command. To

$ ssh internalhost

Add this

`Host internalhost
    User appuser
    Hostname internalhost
    ProxyCommand ssh -Al appuser 35.205.217.189 nc %h %p 2> /dev/null`
    
to `~/.ssh/config` file

 
