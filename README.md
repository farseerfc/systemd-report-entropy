# systemd-report-entropy
report system entropy to journald during boot

## Why ?
Because it is hard to check available entropy during system boot,
and lack of entropy can cause delay in system boot process.

## How ?
Just start a systemd service early enough to report available entropy
to the journal, until systemd finished its booting.

## Ok, how to use it

1. Build and install the package 
```bash
makepkg -si
```

2. Enable the service
```bash
sudo systemctl enable systemd-report-entropy.service
```

3. reboot

4. check entropy report
```bash
journalctl -b0 -u systemd-report-entropy.service
```

## Example output:

```
-- Logs begin at Thu 2019-03-28 22:15:28 JST, end at Thu 2026-01-08 07:54:05 JST. --
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:40,039065879+09:00 22 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[275]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:40,528601478+09:00 24 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[287]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:40,583006383+09:00 25 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[298]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:40,635803013+09:00 26 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[311]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:40,709139758+09:00 27 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[322]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:40,780689390+09:00 28 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[332]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:40,868403187+09:00 31 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[342]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:40,958449758+09:00 33 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[352]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,037850641+09:00 34 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[362]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,124008337+09:00 36 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[372]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,210750558+09:00 38 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[382]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,293171454+09:00 40 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[392]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,377517725+09:00 40 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[403]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,449179832+09:00 41 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[413]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,506355838+09:00 42 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[423]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,565692194+09:00 45 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[433]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,643732202+09:00 51 sleeping 10.00000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[444]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,711799571+09:00 2235 sleeping 223.50000000000000000000 ms
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:41 fcgpdp systemd-report-entropy[458]: initializing
Nov 06 15:12:41 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:41,984222798+09:00 2237 sleeping 223.70000000000000000000 ms
Nov 06 15:12:42 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:42 fcgpdp systemd-report-entropy[471]: initializing
Nov 06 15:12:42 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:42,253016763+09:00 2238 sleeping 223.80000000000000000000 ms
Nov 06 15:12:42 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:42 fcgpdp systemd-report-entropy[483]: initializing
Nov 06 15:12:42 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:42,535630228+09:00 2238 sleeping 223.80000000000000000000 ms
Nov 06 15:12:42 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:42 fcgpdp systemd-report-entropy[494]: initializing
Nov 06 15:12:42 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:42,813681656+09:00 2238 sleeping 223.80000000000000000000 ms
Nov 06 15:12:43 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:43 fcgpdp systemd-report-entropy[519]: starting
Nov 06 15:12:43 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:43,137255276+09:00 2239 sleeping 223.90000000000000000000 ms
Nov 06 15:12:43 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:43 fcgpdp systemd-report-entropy[544]: starting
Nov 06 15:12:43 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:43,425112317+09:00 2239 sleeping 223.90000000000000000000 ms
Nov 06 15:12:43 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:43 fcgpdp systemd-report-entropy[559]: starting
Nov 06 15:12:43 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:43,701825695+09:00 2241 sleeping 224.10000000000000000000 ms
Nov 06 15:12:43 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:43 fcgpdp systemd-report-entropy[581]: starting
Nov 06 15:12:43 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:43,979455723+09:00 2243 sleeping 224.30000000000000000000 ms
Nov 06 15:12:44 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:44 fcgpdp systemd-report-entropy[631]: starting
Nov 06 15:12:44 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:44,274859590+09:00 2245 sleeping 224.50000000000000000000 ms
Nov 06 15:12:44 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:44 fcgpdp systemd-report-entropy[668]: starting
Nov 06 15:12:44 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:44,559586381+09:00 2246 sleeping 224.60000000000000000000 ms
Nov 06 15:12:44 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:44 fcgpdp systemd-report-entropy[728]: starting
Nov 06 15:12:44 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:44,833113558+09:00 2251 sleeping 225.10000000000000000000 ms
Nov 06 15:12:45 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:45 fcgpdp systemd-report-entropy[795]: starting
Nov 06 15:12:45 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:45,102937822+09:00 2252 sleeping 225.20000000000000000000 ms
Nov 06 15:12:45 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:45 fcgpdp systemd-report-entropy[856]: starting
Nov 06 15:12:45 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:45,395044639+09:00 2257 sleeping 225.70000000000000000000 ms
Nov 06 15:12:45 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:45 fcgpdp systemd-report-entropy[939]: starting
Nov 06 15:12:45 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:45,678205780+09:00 2258 sleeping 225.80000000000000000000 ms
Nov 06 15:12:45 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:45 fcgpdp systemd-report-entropy[1018]: starting
Nov 06 15:12:45 fcgpdp systemd-report-entropy[255]: ENTROPY 2020-11-06T15:12:45,950649382+09:00 2259 sleeping 225.90000000000000000000 ms
Nov 06 15:12:46 fcgpdp systemd-report-entropy[255]: is-system-running:
Nov 06 15:12:46 fcgpdp systemd-report-entropy[1061]: running
Nov 06 15:12:46 fcgpdp systemd-report-entropy[255]: REPORT ENTROPY systemd boot finished, quit.
```

