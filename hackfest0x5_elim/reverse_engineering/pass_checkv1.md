# Password Checker v1.0

> Get the correct password!\
> \
> Format Flag : `hackfest0x5{}`

A binary file is provided, so we have to decompile it using the IDA Pro application to analyze whether a suspicious string is found or not.\
![image](https://user-images.githubusercontent.com/41176663/170177546-5926fbe2-2edc-4762-a7b2-471e727e938c.png)
\
There is a suspicious variable, namely the supah_s3cret variable. Check the variable.\
![image](https://user-images.githubusercontent.com/41176663/170177625-15998be7-9358-4ad3-baaa-517df51b1be3.png)
\
And it turns out that there is actually a flag on that variable\
`hackfest0x5{the_strings_command_can_be_U5eful_but_dont_R3ly_0n_1t}`
