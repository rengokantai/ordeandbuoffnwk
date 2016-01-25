#### ordeandbuoffnwk
- cisco (switch initial config)
Do not show the initial config dialog.
```
show interface status
```
by default, the command line is like
```
switch>
```
we type
```
enable
```
and change the terminal prompt to
```
switch#
```
Then

```
switch#show running-config
```

Then config terminal
```
config terminal
```

create first host
```
hostname LAB1
vlan 10
name LAB-MAIN
state active
exit
interface vlan 10
```
We can see
```
LAB(config-if)#
```
type
```
interface fastethernet0/1
switchport access vlan 10
interface range fastethernet0/2-8
switchport access vlan 10
end
show interface status
```

type
```
?
```
to show help. (c? shows commands start from c)

```
LAB#conf terminal
```
First, let remote login
```
LAB(config)# line vty 0 15
password letmein
exit
```
enable password
```
enable secret securepassword
```

Finally
```
exit
write memory
```
