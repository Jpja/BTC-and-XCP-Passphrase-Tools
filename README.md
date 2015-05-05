##BTC and XCP Passphrase Tools##


###Paperwallet###

Outputs a printer friendly paper wallet.

It prints the list of Bitcoin/Counterparty addresses and (optionally) private keys derived from a passphrase. The passphrase is compatible with Counterwallet, XCP Wallet for Chrome, and GetGems Messenger.

 * The code is forked from Blockscan's key generation tool. All changes are cosmetic.
 * The html file can run offline. All code is included in this file, so you do not need to unzip the directory to run it.
 * I cannot guarantee that the code is bug free. I encourage other to review the code and potentially improve/fork it.


###Vanity-address###

Finds a passphrase with vanity addresses. Specify vanity patterns for up to three addresses. The pattern starts with 1 followed by one or more characters. When specifying a pattern, consider this:

 * The algorithm tries random passphrases until it finds the desired pattern. This can take a long time. Your browser may freeze.
 * By default it stops searching after 1000 iterations but you can ovverrule this by typing *inf* at the begining of the random text input string.
 * Around 10 passphrases are tested per second. The probability of an address starting with 1A is 1/22. Therefore it takes a couple of seconds to find an address which starts with 1A. If you want both the first two addresses to start with 1A, the probability is squared; 1/484. Be prepared to wait around a minute. If all three addresses shall start with 1A, the proability is cubed and you'll likely have to wait around twenty minutes.
 * Addresses starting with 12,...,19,1A,...,1P are the easiest to find.
 * For subsequent characters the probability is approx. 1/58. Therefore by adding one character to one address you'll expext to wait 58 times longer!
 * Example: To make one address start with 1CP, expect to wait 2-3 minutes; p = 1/(22*58).
 * Example: To make one address start with 1XP, expect to wait a couple of hours. This is slow because 1X is rare; p=1/(1353*58).
 * Example: To make both the first two addresses start with 1A, expect to wait less than a minute; p=1/22^2.
 * Example: To make all the first three address start with 1A, expect to wait around twenty minutes; p=1/22^3.


###Brain-passphrase###

Generates a 12-word passphrase from a text input. The passphrase can be used in Counterwallet, XCP Chrome Wallet and GetGems Messenger.

 * It can be used as a sort of brain wallet. I advice against using it as such, but feel free to play around.


**Tools are experimental. Pending security audit. Use at own risk!**
