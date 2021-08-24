These files will be different depending on your mud and which session handler you use,
but the below is for Legends of Kallisti.

For each account, you'll need something like this, named *accountname_kallisti.account*:
```
#nop Satori (Kallisti) account file
#nop this is my immortal account

#var account_name {account name}
#var account_password {redacted}

#nop Change the below to true if you want the kallisti module to remember
#nop your password.  It will need this to reconnect if you lose connection, but you are
#nop at risk of leaking it to the mud or others
#var account_dont_forget_password false

#nop vim: syntax=tt
```

For each player, you'll need something like this, named *playername_kallisti.player*:
```
#nop Kensho player file (imm)

#list modules_on_connect create layout kal_comms map;

#var account_name satori
#var char_name kensho
#var layout_preference full
#var comms-session com

#nop vim: syntax=tt
```
The account_name should match a valid .account file.  The modules_on_connect list are modules to load after
you enter the game.  The other two #vars are preference I'm pre-specifying until we have a working preferences
module.
