# :smiling_imp: Trojan Cockroach

[![Gitter](https://badges.gitter.im/MinhasKamal/TrojanCockroach.svg)](https://gitter.im/MinhasKamal/TrojanCockroach?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

#### A Stealthy Trojan Spyware

<a href="https://MinhasKamal.github.io/TrojanCockroach">This program</a> is a **Trojan Virus** that steals data (ID, password; every key stroke) from PC (Windows XP or later) and emails it back to the author. It spreads among PCs through USB drives. It is almost undetectable to any antivirus software.

This project is created only for learning purpose.

### Intro
- [TrojanCockroach.cpp](https://github.com/MinhasKamal/TrojanCockroach/blob/master/com/minhaskamal/trojanCockroach/TrojanCockroach.cpp)- logs user's data, sends data through Transmit.exe, infects portable drive.
- [Infect.cpp](https://github.com/MinhasKamal/TrojanCockroach/blob/master/com/minhaskamal/trojanCockroach/Infect.cpp)- installs the virus into computer.
- [Transmit.exe](https://github.com/MinhasKamal/TrojanCockroach/blob/master/com/minhaskamal/trojanCockroach/Transmit.exe)-  emails data back.
- [TrojanCockroach.lnk](https://github.com/MinhasKamal/TrojanCockroach/blob/master/com/minhaskamal/trojanCockroach/TrojanCockroach.lnk)- resides in the startup folder of PC and activates TrojanCockroach.exe.
- [Infect.lnk](https://github.com/MinhasKamal/TrojanCockroach/blob/master/com/minhaskamal/trojanCockroach/Infect.lnk)- takes different attractive names in the infected portable drive, activates Infect.exe when clicked.
- [DecodeMessage.cpp](https://github.com/MinhasKamal/TrojanCockroach/blob/master/com/minhaskamal/trojanCockroach/DecodeMessage.cpp)- used to decode received email.

### Setup
1. Preparation
  1. Change the method **sendData()** of TrojanCockroach.cpp- place your email and password in the command.
  2. Compile **TrojanCockroach.cpp** & **Infect.cpp**. **Transmit.exe** is actually the executable distribution of [curl](https://curl.haxx.se) for Windows.
  3. Place **TrojanCockroach.exe**, **Infect.exe**, **Transmit.exe**, **Infect.lnk** & **TrojanCockroach.lnk** in the same folder.
  
    Here, I have changed all the file names (you do not wish to keep these- 'TrojanCockroach', 'Infect'; right? the code will need to be changed a little too) and this is how they look-
  <div align="center">
    <img src="https://cloud.githubusercontent.com/assets/5456665/18255358/cbaf8484-73ca-11e6-99a0-a5a52f65f8a0.PNG" alt="Key-Logger"/>
  </div>

  4. Now run **TrojanCockroach.exe** and insert a pendrive (see the magic!). You will get a hidden folder and link file in your pendrive. The hidden folder contains the full package, & the link file is actually renamed form of Infect.lnk.
  
2. Attack
  1. Now, insert the USB-Drive in the subject's PC (Yes, you have to start the spreading process from somewhere!)
  2. Run the shortcut and the spyware will be injected. Now (after a restart) every time any USB-Drive is inserted in the affected PC, the virus will copy itself in that, and the cycle will start again!

3. Data Collection
  1. You need to wait several days (depending on the number of power on/off of the PC), before getting any data.
  2. After getting the email copy the full message to a text file. As the message has come through email certain characters are converted. To resolve that --- --- ---. 
  3. Now, run **DecodeMessage.exe** for decoding the message as plain text. In this phase, you can look for specific patterns in the text, and thus get rid of most of the useless parts (like- mouse click, or same key-group press as happens during gaming). 

### Further 
You may read [TrojanCockroachStory](https://github.com/MinhasKamal/TrojanCockroach/blob/master/TrojanCockroachStory.md) to get an overview of how the program works. You will get a clearer understanding of the project from its pre-project- **[StupidKeyLogger](https://github.com/MinhasKamal/StupidKeyLogger)**.

The project is perfectly runnable. But I do not want newbies to abuse my project, so I am **keeping some simple secrets unrevealed**. There are also some intentionally created holes in this 'README'. I have made some nonsense changes in the code too, so that no one can run it effectively without getting his hands dirty. I believe these plain obstacles can easily be overcome by actual programmers.

**Note:** I will not also take any responsibility of someone else's ill act with my program. But I do believe that a real learner will learn a lot from this.


### License
<a rel="license" href="https://opensource.org/licenses/MIT"><img alt="MIT License" src="https://cloud.githubusercontent.com/assets/5456665/18950087/fbe0681a-865f-11e6-9552-e59d038d5913.png" width="60em" height=auto/></a><br/><a href="https://github.com/MinhasKamal/TrojanCockroach">Trojan Cockroach</a> is licensed under <a rel="license" href="https://opensource.org/licenses/MIT">MIT License</a>.
