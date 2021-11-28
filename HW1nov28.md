<!--part 2, Nov 27-->
# Week 3 Note
###  **Compression in Linux**
- **Compression provides**
	- take smaller storage
    - save files as single package
    - encryption
- **Properties in compression**
  - compression **ratio** (extent of compression)
  - **compatibility** (how file compressed)
  - these effect **time of compression** and **file size**
#### Major Methods in Linux
1. **gzip** : fast, minimum compression applied
2. **bzip2**: fast compression for high ratio, slow decompression, medium size
3. **xz**: slow compression for high ratio, fast decompression, smallest size
#### Commands
**.gzip**
```bash
#compression
gzip ~
#decompression
gunzip ~.gz
gzip -d ~.gz
```
**.xz**
```bash
#compression
xz -z ~
#decompression
xz -d ~.xz
```
**tar.gz**
```bash
#compression
tar -zcvf ~.tar.gz 
tar -zcvf ~.tar.gz
```
---
### **Other commands in Linux**
#### find : File Searching 
```bash
find usr/local/bin -ls -name '*.txt' 
```
##### find [path][option][action] ~

- option
  - size
  - name
  - type
  - user
- action
  - ls
  - print
- other
  - -a
  - -n
  - -p

#### cat : Read File from Beginning
```bash
cat -n test.py >> homework.py
```
##### cat [option] ~
- -n
- \>
- \>>
#### tac : Read File from Ending
```bash
tac -s ',' 2021112801.log
```
##### tac [option] ~
- -r
- -s
#### more : Read File by Pages
```bash
more test.py
```
##### more [option] ~
- option : read file from ( ) line

#### head : Take ~ lines from Beginning
```bash
head -n 5 test.py
```
#### tail : Take ~ lines from Ending
```bash
tail -n 5 test.py
```
---
### Network Model and Structure
#### TCP/IP & OSI Model
 TCP/IP: 4 layers, OSI: 7 layers
  - Application Layer
    - Application
    - Presentation
    - Session
  - Transport Layer
  - Internet Layer
  - Network Access Layer
    - Data Link
    - Physical

#### TCP & UDP protocals
- TCP : 3 way handshake
  - request -> 
  - <- respond
  - confirm -> 
  - **communication established**
  - end of conversation ->
- UDP : connectionless hand shake
  - request ->
  - <- respond
  - **communication established**
  - end of conversation

#### Port : entance of message
- from 0 ~ 65535
- open/closed by device
- transportations are established on different ports

#### Commands for Network Information
- **route**
  - set up rule for network
- **netstats**
  - list current network information
- **ping**
  - send a request to specific location
