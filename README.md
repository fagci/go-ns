# Netstalking things in GO

## Features

### Netrandom

- RTSP fuzzer
- random WAN IP generator
- random WAN IP port (range) scanner

## Build

```sh
go build
```

## Usage

Generate 5 random wan IPs:

```sh
./gons -gw 5
```

Netrandom find possible RTSP sources:

```sh
./gons -rtsp
```

Take snapshots from RTSP stream and write source URL in metadata:

```sh
./gons -rtsp -w 4096 -callback 'bash ./callbacks/capture.sh "{result}" "/sdcard/Pictures/RTSP/" "{slug}"'
```

Scan 1024 random WAN IPs for open VNC ports:

```sh
./gons -gw 1024 -ports 5900-5902
```

## Testing

```sh
go test -v ./...
```
