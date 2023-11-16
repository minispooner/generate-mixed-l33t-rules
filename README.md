# Generate Mixed L33t Rules
Python script to generate a list of mixed l33t rules for John the Ripper or Hashcat.

# Details
This tool generates mixed l33t rules for John the Ripper or Hashcat that result in mixed l33t permutations (example, 3xample, exampl3, 3xampl3), as opposed to the common replace-all l33t permutations (example, 3xampl3) that you often come across. Included by default is a customizable L33t Translations Table that holds the configuration for which characters should be replaced.

# How to Use
1. Configure the L33t Translation Table in the code to your liking
2. Run the script to generate your mixed l33t ruleset `python3 generate-mixed-l33t-rules.py`
3. Copy paste the output ruleset into your john.conf file
4. Try it out: `john -w:words.txt -rule:mixed_l33t --stdout | sort -u`

# Example Output
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
