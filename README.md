# Generate Mixed L33t Rules
Python script to generate a list of mixed l33t rules for John the Ripper or Hashcat.

# Details
I had the need for a mixed l33t rule (3xample), as opposed to the common replace-all l33t rules (3xampl3) that I often come across. I built on some Google results and came up with my own base rules template. Since there are many variations of l33t translations (s = 5 or $, T = 7, ...), I made the tool configurable, so you can simply enter in which characters you want translated and to what. A basic, default L33t Translation Table is already in place, but you can add other transltions as well.

# How to Use
1. Configure the L33t Translation Table to your liking
2. Run the script to generate your mixed l33t ruleset `python3 generate_mixed_l33t.py`
3. Copy paste the output ruleset into your john.conf file
4. Try it out: `john -w:words.txt -rule:mixed_l33t --stdout | sort | uniq`

# Example output
```
[List.Rules:mixed_l33t]
/a op[a4] %3s op[s$] %2s op[s$] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] %2s op[s$] /s op[s$] /e op[e3]
%2s op[s$] /s op[s$]
/a op[a4]
/a op[a4] %3e op[e3] %2e op[e3] /e op[e3]
%2a op[a4] /a op[a4]
%3a op[a4] %2a op[a4] /a op[a4] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] %2s op[s$] /s op[s$] %2e op[e3] /e op[e3]
%2a op[a4] /a op[a4] %3s op[s$] %2s op[s$] /s op[s$]
%2a op[a4] /a op[a4] /s op[s$] %2e op[e3] /e op[e3]
/s op[s$] /e op[e3]
%2a op[a4] /a op[a4] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] %2e op[e3] /e op[e3]
%2a op[a4] /a op[a4] %3s op[s$] %2s op[s$] /s op[s$] /e op[e3]
/a op[a4] %3s op[s$] %2s op[s$] /s op[s$] %2e op[e3] /e op[e3]
%2a op[a4] /a op[a4] /s op[s$] /e op[e3]
%2a op[a4] /a op[a4] %2s op[s$] /s op[s$]
%3a op[a4] %2a op[a4] /a op[a4] %2s op[s$] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] %2s op[s$] /s op[s$]
%3a op[a4] %2a op[a4] /a op[a4]
%3s op[s$] %2s op[s$] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
%3s op[s$] %2s op[s$] /s op[s$]
/a op[a4] %2e op[e3] /e op[e3]
%2e op[e3] /e op[e3]
/s op[s$]
%2a op[a4] /a op[a4] %2e op[e3] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] %3s op[s$] %2s op[s$] /s op[s$]
%3a op[a4] %2a op[a4] /a op[a4] /s op[s$]
/s op[s$] %2e op[e3] /e op[e3]
/a op[a4] %2s op[s$] /s op[s$] /e op[e3]
%2a op[a4] /a op[a4] %3s op[s$] %2s op[s$] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
/e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] %3s op[s$] %2s op[s$] /s op[s$] %2e op[e3] /e op[e3]
/a op[a4] %3s op[s$] %2s op[s$] /s op[s$] /e op[e3]
/a op[a4] /s op[s$]
%3e op[e3] %2e op[e3] /e op[e3]
%3s op[s$] %2s op[s$] /s op[s$] %2e op[e3] /e op[e3]
%2a op[a4] /a op[a4] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] %3s op[s$] %2s op[s$] /s op[s$] /e op[e3]
/s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
/a op[a4] /s op[s$] %2e op[e3] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] /s op[s$] /e op[e3]
%2a op[a4] /a op[a4] /s op[s$]
/a op[a4] /e op[e3]
%2a op[a4] /a op[a4] %2s op[s$] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
%2s op[s$] /s op[s$] %2e op[e3] /e op[e3]
%2a op[a4] /a op[a4] %3s op[s$] %2s op[s$] /s op[s$] %2e op[e3] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] /s op[s$] %2e op[e3] /e op[e3]
/a op[a4] /s op[s$] /e op[e3]
%2a op[a4] /a op[a4] %2s op[s$] /s op[s$] /e op[e3]
%2s op[s$] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
/a op[a4] %2s op[s$] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
%3s op[s$] %2s op[s$] /s op[s$] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
%2s op[s$] /s op[s$] /e op[e3]
/a op[a4] %2s op[s$] /s op[s$]
/a op[a4] %2s op[s$] /s op[s$] %2e op[e3] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] %3s op[s$] %2s op[s$] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
%3a op[a4] %2a op[a4] /a op[a4] %3e op[e3] %2e op[e3] /e op[e3]
/a op[a4] /s op[s$] %3e op[e3] %2e op[e3] /e op[e3]
%2a op[a4] /a op[a4] %2s op[s$] /s op[s$] %2e op[e3] /e op[e3]
%2a op[a4] /a op[a4] %3e op[e3] %2e op[e3] /e op[e3]
/a op[a4] %3s op[s$] %2s op[s$] /s op[s$]
```
