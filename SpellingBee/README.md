# Spelling Bee

So my kid got into a spelling bee. 
I read on Reddit that a good application was quizlet. 


Paid subscription only supports 2000 words

There is also an open source project NYT-Spelling-Bee-Cheat

Here is the wordlist

https://github.com/spswanz/NYT-Spelling-Bee-Cheat/blob/master/twl06.txt

There are hundreds of thousands of words

So I grabbed the big ones. There are over 3000 at-least-15 character words 

```
brew install coreutils #For shuf
cat ~/Downloads/twl06.txt | strings -n 15 | shuf | head -n 2000 > wordlist
```
