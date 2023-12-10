# SSH Agent start on login

Add this to your `~/.bash_profile`

```
export SSH_AUTH_SOCK=${HOME}/.ssh/agent.socket

if ! pgrep -u ${USER} ssh-agent > /dev/null; then
    rm -f ${SSH_AUTH_SOCK}
fi

if [ ! -S ${SSH_AUTH_SOCK} ]; then
    eval $(ssh-agent -a ${SSH_AUTH_SOCK} 2> /dev/null)
fi
```
