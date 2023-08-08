**Cisco CLI** is the command line interface used to interact with Cisco devices

**Cisco IOS** is the operating system that runs on Cisco devices and is configured through different modes[^1]

User Exec Mode
```
Switch>
```
- Default Prompt
- Has a limited number of commands
- Cannot be used to change configuration


Privileged Exec Mode
```
Switch>enable
Switch#
```
- Has more commands that User Exec Mode
- Used to save config by running:
	- `write memory` or
	- `copy running-config startup-config`
- Can run command `show running-config`
- Can be password protected
- Cannot be used to change configuration

Global configuration Mode
```
Switch#configure terminal
Swtich(config)#
```
- Is used to configure Cisco device
- Has access to Privileged Exec commands by prefixing `do` before command
- Can set access control for users

## Other Commands

Interface Configuration Mode
```
Switch(config)#int fastethernet 0/1
Switch(config-if)#
```
- Used to add configuration to a specific interface

Configure device hostname
```
Switch(config)#hostname NewSwitchName
NewSwitchName(config)#
```

Running the `?` is used to get help on command.

Running `show version` gives detailed information about the Cisco device 

## References
[^1]:Understanding Cisco IOS Command Line Modes [[https://www.mustbegeek.com/understanding-cisco-ios-command-line-modes/]]
