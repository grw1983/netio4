# NETIO4
My Koukaam NETIO4 is locked in a beeping loop of agony.

I was able to attach to the serial port of the MT7620.
Obviously there is a problem with the MMC flash which damaged
the Linux kernel.

Unfortunately the U-Boot bootloader is locked with a passwort. I was able
to read out the SPI-NOR Flash out found the following:
password=00b4f2bb08a214ddbcdfe090a11df5155afd94b738e097bd8aea5bd8bbd4409c$ce2acc
Sadly I'm not able to decipher which hash algo is used and what the part after the dollar (ce2acc)
stands for. If I were able to generate a new password hash I could inject a known password
and then unlock the bootloader.
