# homebrew-airsnare

Homebrew tap for [AirSnare](https://github.com/rtulke/airsnare) — WPA handshake
capture with deauthentication and PMKID extraction.

## Install

```sh
brew tap rtulke/airsnare
brew install airsnare
```

## Upgrade

```sh
brew update && brew upgrade airsnare
```

## Usage

AirSnare requires root. Basic examples:

```sh
# Capture handshakes on channel 6, passive mode
sudo airsnare -i en0 -c 6 -n -w out.pcap

# Active mode: send deauth frames to trigger handshakes
sudo airsnare -i en0 -c 6 -b AA:BB:CC:DD:EE:FF -w out.pcap

# Replay an existing capture
airsnare -r capture.pcap -n
```

See `man airsnare` or `airsnare --help` for all options, and the
[full documentation](https://github.com/rtulke/airsnare#readme) for
macOS-specific notes (channel switching, Apple Silicon limitations).

## Source

Formula source: [rtulke/airsnare](https://github.com/rtulke/airsnare/blob/master/Formula/airsnare.rb)
