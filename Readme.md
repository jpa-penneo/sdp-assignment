# Processing SDP files

The file sdp.txt contains an example of some SDP (Session Description Protocol) messages. An SDP message contains information about a telephony session and defines: IP address, UDP port and codecs used.

Each SDP message is separated by a new line

## Assignment 1

Create an application that processes the file and identifies each different message, printing on the output screen the following information:

```
the.ip.address
thePort
["Codec1", "Codec2", "..."]
```

- IP comes from `c=` line
- Port comes from `m=` line
- Codecs come from `a=rtpmap` lines

Example of a message

```
v=0
o=- 0 0 IN IP4 43.173.154.12
s=session
b=CT:1098
m=audio 15082 RTP/AVP 9 0
c=IN IP4 154.195.20.236
a=rtpmap:9 G722/8000
a=rtpmap:0 PCMU/8000
a=encryption:optional
```

```
154.195.20.236
15082
["G722", "PCMU"]
```

## Assignment 2

Consider the file can have several thousands of messages, and instead of printing each message we need to store them in an external storage, like a database.

What optimizations or changes you would implement in order to improve the performance?