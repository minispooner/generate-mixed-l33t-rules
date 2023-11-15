# Generate Mixed L33t Rules
Python script to generate a list of mixed l33t rules for John the Ripper or Hashcat.

# Details
This tool generates mixed l33t rules (example, 3xample, exampl3, 3xampl3), as opposed to the common replace-all l33t rules (example, 3xampl3) that you often come across. The tool can be configured out support custom l33t translations as well (a=>4, s=>$, e=>3, ...). To do so, just alter the default L33t Translations Table to include characters you want translated and to what.

# How to Use
1. [optional] Configure the L33t Translation Table to your liking
2. Run the script to generate your mixed l33t ruleset `python3 generate_mixed_l33t.py`
3. Copy paste the output ruleset into your john.conf file
4. Try it out: `john -w:words.txt -rule:mixed_l33t --stdout | sort -u`

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
