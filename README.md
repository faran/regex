REGEX

[\ -~] everything
[^] Negation
[a-zA-z0-9] Literal and Ranges
cat|dog Alteration with pipe
META Character
. for everything
if need to find . then use escape \.
\d all digits
\D negation of digits
\w all charachters
\W negation of character and digits
\t tabs
\n line break
\s any kind of space , tab or line break
\S negation
\ backslash space or just a space
\[\] match the bracket

QUANTIFIERS
 * = 0 or more time
+ = 1 or more time
http?:\/\/.*   
? makes quantifier less greedy so select in chunks rather one big stream
 
ITERATION
4{2,4}?
grabs 4 in pair of two also notice ? quantifier

GROUPS
\1 ,+, {2}


LOOKAROUNDS
+ive look ahead
cool(?=\ cat) matches cool where we have space and cat

-ive look ahead
cool(?!\ cat) matches cool everywhere but not where we have space and cat

+ive lookbehind
(?<=cool\ )cat

-ive look ahead
(?<!cool\ )cat


BOUNDARIES
woo\b matches only where the occurence of word woo is not in woohooo

ANCHORS
Start
^\w+
^This

End
\w+.$


MODIFIERS
m modifier
beginning word of ever line
(?m)^\w+

last word of every line
(?m)\w+$


i modifier case insensitive
(?i)[a-z]+

(?s).+
everything and lines as well

x modifier free space mode with comment enabled
(?x)
\w+ # t
