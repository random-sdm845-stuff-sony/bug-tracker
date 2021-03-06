Bug tracker for Dayes/Exers builds
=

How to add a bug report:

    Press "Issues" button
    Press the "Get started" button in the "Bug report" section
    Fill in the issue mentioning the needed informations
    Press "Submit new issue" button

How to get logs - by Nathan Chancellor
=

1   . Getting a dmesg:
    a. Either download a dmesg app and follow similar steps as above OR download a terminal emulator and continue on.

    b. Open your terminal emulator and type su to enter as the root user.

    c. Type dmesg > /sdcard/test.log

    d. Send the generated file (located in the head folder of your internal storage partition) to your developer, following the etiquette below.
    
################
# 2. USING ADB #
################

1.  Download the latest tools from Google:
    https://dl.google.com/android/repository/platform-tools-latest-linux.zip
    https://dl.google.com/android/repository/platform-tools-latest-darwin.zip
    https://dl.google.com/android/repository/platform-tools-latest-windows.zip

2.  Extract those to a folder and move into that folder:
    $ cd <folder_location>

3.  Plug in your device and accept the debugging prompt (turn on ADB in
    Settings > Developer Options if you don't see it).

4.  Verify your device is recognized.
    $ adb devices or $ ./adb devices

5.  Clear the logcat buffer.
    $ adb logcat -c or $ ./adb logcat -c

6.  Take your log:
    Logcat: $ adb logcat -d > test.log or $ ./adb logcat -d > test.log
    dmesg: $ adb shell dmesg > test.log or $ ./adb shell dmesg > test.log

7.  Give that log to the appropriate party with a proper report, following the etiquette below.


##################################
# PROPER BUG REPORTING ETIQUETTE #
##################################

1.  First and foremost, understand that for the vast majority of people, this is a hobby, not a job. It may take some time for your issue to be resolved. Being a jerk or bossy is likely to get you banned or at the least have your issue dismissed.

2.  Write in clear, concise manner what the issue is with steps to reproduce

    Bad: My phone is broken, help!
    Good: Whenever I open YouTube after a clean flash, it force closes.

3.  Explain what you have done. A developer should not have to ask what has already been attempted.

4.  Provide any scenarios/ROMs where it did work (was it working in a previous update, etc.)

5.  If you are technically inclined, provide commits that are either the issue or will resolve the issue. Developers love having a solution presented for them.

#
# Copyright (C) 2016-2017 Nathan Chancellor
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>
#
