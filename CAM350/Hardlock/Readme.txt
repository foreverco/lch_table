                               Sentinel Drivers
                                 Version 5.15

This readme file describes the installation procedures for all Sentinel
system drivers.  See the appropriate section for the procedure about the
driver that you are installing.

-----------------------------------
        README File Contents
-----------------------------------

        1.0     File List
        2.0     Changes Since Last General Release
        2.1     Changes Since Windows 95 Beta Release
        3.0     Windows NT Driver Installation Procedure
        3.1     Windows NT Driver Configuration
        3.2     Windows NT Driver Un-install
        3.3     Windows NT - DOS Device Driver
        4.0     Windows 3.x Driver Installation Procedure
        4.1     Windows 3.x Driver Configuration
        5.0     OS/2 Driver Installation Procedure
        5.1     OS/2 Driver Configuration
        6.0     Windows 95 Driver Installation Procedure
        6.1     Windows 95 Driver Configuration
        6.2     Windows 95 Driver Un-install
                        
-----------------------------------
1.0     File List
-----------------------------------

 README.TXT          - This file.
 SENTINEL.DDP        - OS/2 installation script file.
 DOS\SENTDOS.SYS     - DOS Device Driver for use with some interfaces under
                       Windows NT.
 OS2\INSTALL.CMD     - OS/2 installation command file.
 OS2\SENTINEL.SYS    - OS/2 Sentinel Driver.
 WIN_31\INSTALL.EXE  - Install program for Windows 3.x Sentinel Driver.
 WIN_31\SENTINEL.386 - Windows 3.x Sentinel Driver.
 WIN_NT\INSTALL.BAT  - Batch file to invoke appropriate Win NT installation
                       program under different hardware platform.
 WIN_NT\SETUPAXP.EXE - Sentinel Driver installation program for Windows NT
                       on ALPHA platforms.
 WIN_NT\SETUPX86.EXE - Sentinel Driver installation program for Windows NT
                       on INTEL platforms.
 WIN_NT\SETUPMPS.EXE - Sentinel Driver installation program for Windows NT
                       on MIPS platforms.
 WIN_NT\SETUPPPC.EXE - Sentinel Driver installation program for Windows NT
                       on Power PC platforms.
 WIN_NT\SNTI386.DLL  - Sentinel Driver setup for Windows NT on Intel platforms.
 WIN_NT\SNTMIPS.DLL  - Sentinel Driver setup for Windows NT on MIPS platforms.
 WIN_NT\SNTALPHA.DLL - Sentinel Driver setup for Windows NT on Alpha platforms.
 WIN_NT\SNTPPC.DLL   - Sentinel Driver setup for Windows NT on Power PC platforms.
 WIN_NT\SENTINEL.WRI - Windows NT Sentinel Driver User's Guide
                       in Windows Write format.
 WIN_NT\I386\SENTTEMP.HLP  - Help file for the WinNT Sentinel Driver setup dll.
 WIN_NT\I386\SENTTEMP.SYS  - WinNT Sentinel Driver for x86 systems.
 WIN_NT\I386\RNBOVTMP.DLL  - WinNT Sentinel Virtual Device Driver for x86
                             systems.
 WIN_NT\MIPS\SENTTEMP.HLP  - Help file for the WinNT Sentinel Driver setup dll.
 WIN_NT\MIPS\SENTTEMP.SYS  - WinNT Sentinel Driver for MIPS systems.
 WIN_NT\MIPS\RNBOVTMP.DLL  - WinNT Sentinel Virtual Device Driver for MIPS
                             systems.
 WIN_NT\ALPHA\SENTTEMP.HLP - Help file for the WinNT Sentinel Driver setup dll.
 WIN_NT\ALPHA\SENTTEMP.SYS - WinNT Sentinel Driver for Alpha systems.
 WIN_NT\ALPHA\RNBOVTMP.DLL - WinNT Sentinel Virtual Device Driver for ALPHA
                             systems.
 WIN_NT\PPC\SENTTEMP.HLP   - Help file for the WinNT Sentinel Driver setup dll.
 WIN_NT\PPC\SENTTEMP.SYS   - WinNT Sentinel Driver for Power PC systems.
 WIN_NT\PPC\RNBOVTMP.DLL   - WinNT Sentinel Virtual Device Driver for Power PC
                             systems.
 WIN_95\SENTINEL.VXD - Windows 95 Sentinel Driver.
 WIN_95\SENTW95.EXE  - Sentinel Driver installation program for Windows 95.
 WIN_95\SENTW95.DLL  - Sentinel Driver installation DLL.
 WIN_95\SENTW95.HLP  - Windows help file used by the DLL.
 WIN_95\SENTSTRT.EXE - Program used to initialize the VxD.

------------------------------------------------
2.0     Changes Since Last General Release
------------------------------------------------

  1.  Added Windows 95 VxD.

  2.  Added Windows NT support for PowerPC.

  3.  Added Quiet Mode and Path options to the Windows NT install program.  
      (See section 3.0 below.)

  4.  Added the ability to specify parallel port type in teh Windows NT
      configuration program.

  5.  Fixed a problem that caused SentinelSuperPro errors on very busy 
      systems running Windows NT.

  6.  Fixed a problem with the Enhanced Superpro where the ACTIVATE command
      would return a UNIT NOT FOUND error.

------------------------------------------------
2.1     Changes Since Windows 95 Beta Release
------------------------------------------------

  1.  Added dynamic load capability for the Windows 95 VxD when used with
      Win32 applications.

  2.  Enhanced the install program.

  3.  Fixed a problem where if the Windows 3.x VxD was loaded via the 
      system.ini file under Windows 95, the system would crash.


------------------------------------------------
3.0     Windows NT Driver Installation Procedure
------------------------------------------------
 
  1.  Make a backup copy of the diskette.

  2.  Under the Microsoft Windows NT Main group, double click on 
      "Command Prompt".

  3.  Change drive to the floppy drive contains the Portable Driver Diskette.
      In case of the floppy diskette distribution, change the current
      directory to \WIN_NT.  In case of the CD-ROM distribution, change the
      current directory to \PRODUCT\DRIVERS\WIN_NT.

  4.  Type "INSTALL.BAT" at the command prompt.
      There are two command line options:
        (See the INSTALL.BAT file for examples.)
        1.  /q     Quiet mode.  
                   Normal dialogs described below are not displayed.
                   Error messages are displayed.
        2.  /pxxx  Path, where xxx is the path of files to be installed.
                   Specify the path of files to be installed.
                   Otherwise, files will be copied from the default
                   directory.

  5.  A window with the title bar "Sentinel Driver Setup Program" is
      displayed.

  6.  Select "Functions" and then "Install Sentinel Driver" from the menu bar.

  7.  A dialog box with the default path for the NT driver is displayed.
      Change the drive letter if necessary and click "OK".

  8.  The Sentinel Driver and associated files are copied to the hard disk.
      One of the DLLs, SNTI386.DLL, SNTMIPS.DLL, SNTALPHA.DLL, or SNTPPC.DLL
      and SENTTEMP.HLP are copied to \%SYSTEMROOT%\SYSTEM32. SENTTEMP.SYS
      is copied to the file  \%SYSTEMROOT%\SYSTEM32\DRIVERS\SENTINEL.SYS.
      %SYSTEMROOT% is the directory where Microsoft Windows NT has been
      installed.

  9.  If the driver installation is successful, a dialog box with the message
      "Sentinel Driver Files Copied Successfully" is displayed.

 10.  When complete, a dialog box with the message "Driver Installed! Restart
      your system" is displayed.

 11.  Click "OK" to continue.

 12.  Restart your computer.

Manual Installation of Sentinel System Driver for Windows NT
------------------------------------------------------------
  We highly recommend that you install the Sentinel System Driver for 
  Windows NT with our installer.  If you decide to install it manually 
  or wish to integrate our driver installation into your application setup,
  review the install.bat file in the WIN_NT directory for an example of how 
  invoke our Windows NT install program. 
  

-------------------------------------------------
3.1     Windows NT Driver Configuration Procedure
-------------------------------------------------
If your system setting has been changed and you would like to reconfigure
the Sentinel Driver, perform the following steps.

  1.  Under the Microsoft Windows NT Main group, double click on
      "Control Panel".

  2.  Under the Control Panel double click on "Drivers".

  3.  Select "Sentinel for i386 System" in the installed driver list box.

  4.  Click the "Setup" button.

  5.  Click the "Edit" button to edit an existing parallel port setting
      or click the "Add" button to add a new parallel port setting.
      Select "OK" after you finish the port configuration.

  6.  A dialog box with the message "Your driver setting has changed" is
      displayed.  You will need to exit and restart Windows NT so that the
      new setting can take effect."

  7.  If you have any other application running at the background with
      unsaved data, choose "Don't Restart Now". Quit all the application
      and restart Windows NT, Otherwise select "Restart Now".


------------------------------------------------
3.2     Windows NT Driver Un-install
------------------------------------------------

  1.  Under the Microsoft Windows NT Main group, double click on
      "Command Prompt".

  2.  Change drive to the floppy drive contains the Portable Driver Diskette.
      In case of the floppy diskette distribution, change the current
      directory to \WIN_NT.  In case of the CD-ROM distribution, change the
      current directory to \PRODUCT\DRIVERS\WIN_NT.

  3.  Run "INSTALL.BAT" from the command prompt.
      1. Use Command-line options: (See the INSTALL.BAT file for examples.)
                      /q /u -   Quietly removes the existing driver.

      2. Via Pull-down menu -   Run INSTALL.BAT and select "Remove Sentinel
                                Driver" from the "Function" menu.

  4.  When complete, a dialog box with the message "Sentinel Driver Removed"
      is displayed.

  5.  Click "OK" to continue.

  Note:  Some files may not be removed until you restart your computer.

-------------------------------------------------
3.3     Windows NT - DOS Device Driver
-------------------------------------------------

  It is possible, though unlikely, that on some systems, applications using
  the Watcom C/C++ with Rational DOS/4G and Microsoft Visual C/C++ with Phar
  Lap TNT DOS Extender may be unable to communicate with our Windows NT
  Device Driver.  In the unlikely event that you experience problems running
  your application under Windows NT, a DOS Device Driver is provided which
  allows your application to communicate with the Windows NT Device Driver
  on systems where it otherwise could not.

  To install this device driver, do the following:

    1.      Copy the file SENTDOS.SYS to the target system's hard disk.
    2.      Add the following statement to the custom Config file used
            by your application's PIF file, or if your application does
            not use a custom Config file, to the system's CONFIG.NT file.

            device=%path%\sentdos.sys

            Where %path% is the actual path where SENTDOS.SYS resides.


-------------------------------------------------
4.0     Windows 3.x Driver Installation Procedure
-------------------------------------------------

  1.  Make a backup copy of the diskette.

  2.  Select File|Run under the Program Manager.

  3.  Type "A:\WIN_31\INSTALL.EXE" at the dialog box. Change the drive letter
      A: to the floppy disk drive where the Portable Driver Diskette is
      located if you are running from a drive other than A:
      In case of the CD-ROM distribution, Type
      {CD-ROM DRIVE}:\PRODUCT\DRIVERS\WIN_31\INSTALL.EXE where {CD-ROM DRIVE}
      is the drive letter corresponding to CD-ROM drive on your system.

  4.  Follow the installation instructions.

  5.  If you need to change any of the driver's default settings, modify the
      SYSTEM.INI file.  See the following section for details.

  6.  When the installation is complete, restart Windows.

Manual Installation of Sentinel System Driver for Windows
---------------------------------------------------------
  We highly recommend that you install the Sentinel System Driver for Windows
  with our installer.  If you decide to install it manually later on, you may
  do so by performing the following steps:

  1.  Copy SENTINEL.386 to the windows directory.

  2.  Add the following line under the [386Enh] section in your SYSTEM.INI
      file located in your windows directory.

      DEVICE=C:\WINDOWS\SENTINEL.386

  Make sure to refer to the correct directory if the windows directory
  is located in other than C:\WINDOWS.


----------------------------------------
4.1     Windows 3.x Driver Configuration
----------------------------------------

  The method of configuring the system driver under 16 bit Windows uses 
  fields defined within the SYSTEM.INI file. Data can be defined for all 
  ports up to a maximum of 4 ports. The section [SentinelSetup] contains 
  global configuration data, i.e. autotiming delay, interrupts to mask, etc. 
  The section names [SentinelSetupPortA] through [SentinelSetupPortZ] 
  contain per-port configuration data. The port address field must be 
  defined for the configuration data under these sections to be used.

;Windows 3.x System Driver Sample SYSTEM.INI File settings
;
;
; Sentinel Device Driver Configuration Options for Windows 3.x drivers.
;
; ---------------------------
; GENERAL CONFIGURATION DATA:
; ---------------------------
;
; General driver configuration and parameters are defined as follows:
;
; Section Name: [SentinelSetup]
;
; Parameters  :
;
;         MachineType - Defines the machine type the driver is to be 
;                       configured for. The valid values are:
;                        
;              * 0 - Autodetect machine type.
;                1 - Defines IBM and IBM compatible machines.
;                2 - Defines NEC PC-9800 series machines.
;                3 - Defines Fujitsu FMR series machines. 
;
;              * Default.
;
;                Example:
;
;                [SentinelSetup]
;                MachineType = 1        ; Configure driver for IBM machines.
;
;         Delay - Defines the number of machine loops to use to 
;                 create a 2 microsecond delay. The valid values
;                 are:
;
;              * 0 - Use autotiming.
;                1 through 65535 - Number of loops to use to create a 
;                                  2us delay.
;
;              * Default.
;
;                Example:
;                
;                [SentinelSetup]
;                Delay = 100                ; Use 100 loops to create a 2us 
;                                           ; delay.
;
;         MaskInterrupts - Defines the set of interrupts to mask when 
;                          accessing the port (used for port contention).
;                          This is defined as a hexadecimal bit mask with
;                          the following values:
;
;                0 - Disable interrupt masking.
;              * 1 - Mask LPT1 printer interrupt.
;                2 - Mask LPT2 printer interrupt.
;              * 4 - Mask TIMER interrupt.
;
;              * Default interrupts masked.
;
;                To disable a set of interrupts, add the individual 
;                bit masks together to form the result mask.
;
;                Example:
;
;                [SentinelSetup]
;                MaskInterrupts = 5        ; Mask LPT1 and TIMER interrupts.
;
; ------------------------
; PORT CONFIGURATION DATA:
; ------------------------
;
; Per-Port configuration and parameters are defined as follows:
;
; Section Name: [SentinelSetupPort?]
;
; where ? is the port to configure defined as A through Z. Any port
; configuration defined overrides the default port configuration for
; the driver. Only the first 4 port configuration records (starting
; alphabetically with A) are used. The PortAddress parameter must be
; defined for the port configuration record to be used.
;
; Parameters  :
;
;       PortAddress - Defines the base address for a port. The 
;                     parameter must be defined for the remaining
;                     parameters to be used. The value must be
;                     defined in hexadecimal. The valid values are:
;
;                0 - Disables setup record.
;                1 through FFFE - Used as actual port address.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC            ; Define the first port to use
;                                             ; as 0x03BC.
;
;       PortContentionMethod - Defines the contention method used to
;                              gain access to a port. This is defined as
;                              a hexadecimal bit mask with the following 
;                              values:
;
;                0 - Disable port all contention methods.
;                1 - Use system port contention handler if
;                             available. 
;                             (Not available for Windows 3.x).
;                4 - Disable system interrupts.
;                8 - Mask interrupts as defined by the
;                    MaskInterrupts parameter under the 
;                    [SentinelSetup] section (see above).
;               10 - Use windows critical section handler. 
;                    (Not available for OS/2).
;               20 - Poll the port for access.
;               40 - Enable collision detection.
;        * 8000000 - Use driver defined values.
;
;              * Default.
;
;                To enable a set of contention methods, add the individual 
;                bit masks together to form the resulting contention method.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC              ; Define the first port to use
;                                               ; as 0x03BC.
;                PortContentionMethod = 78      ; Enable the following: 
;                                               ; mask interrupts,
;                                               ; Windows critical section, 
;                                               ; port polling, and 
;                                               ; collision detection.
;
;       PortType - Defines the type of parallel port. The valid values are:
;
;              * 0 - Autodetect port type.
;                1 - NEC PC-9800 series parallel port. 
;                      (Only valid when MachineType = 2 (NEC PC9800)).
;                2 - Fujitsu FMR series parallel port.
;                      (Only valid when MachineType = 3 (Fujitsu)).
;                3 - IBM AT or PS/2 compatible parallel port
;                      (Only valid when MachineType = 1 (IBM)).
;                4 - IBM PS/2 compatible parallel port w/DMA
;                      (Only valid when MachineType = 1 (IBM)).
;
;              * Default.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC            ; Define the first port to use
;                                             ; as 0x03BC.
;                PortType = 3                 ; IBM AT type port.
;
;
;        PortContentionRetryInterval - Defines the number of milliseconds
;                                      to delay in-between retries on
;                                      contenting for a busy port. This
;                                      parameter is used in conjunction
;                                      with the PortContentionRetryCount
;                                      parameter (see below). The valid
;                                      values are:
;
;                0 through 65534 - number of milliseconds to 
;                                  delay in-between retries of
;                                  contenting for a busy
;                                  port.
;
;                -1 - indefinite retry interval.
;
;              * Default is 300.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC               ; Define the first port to
;                                                ; use as 0x03BC.
;                PortContentionRetryInterval = 5 ; Delay 5 milliseconds
;                                                ; between retries on
;                                                ; a busy port.
;
;         PortContentionRetryCount - Defines the number of retries
;                                    to perform on a busy port.
;                                    Used in conjunction with the
;                                    PortContentionRetryInterval
;                                    parameter (see above). The valid
;                                    values are:
;
;                0 through 65534 - Number of retries to perform on a busy 
;                                  port.
;
;                -1 - Indefinite retry count.
;
;              * Default is 100.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC              ; Define the first port to use
;                                               ; as 0x03BC.
;                PortContentionRetryInterval = 5; Delay 5 milliseconds
;                                               ; between retries on
;                                               ; a busy port.
;                                               ; port is owned
;                PortContentionRetryCount = -1  ; Indefinite retries.
;
;         DeviceRetryCount - Defines the number of retries
;                            to perform on a I/O request (query) if
;                            communications is interrupted (the
;                            collision detection contention method
;                            (see above) must be enabled for this parameter
;                            to be used). The valid values are:
;
;                0 through 65534 - Number of retries to perform.
;                             -1 - Indefinite retry count.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC              ; Define the first port to use
;                                               ; as 0x03BC.
;                DeviceRetryCount = -1          ; Indefinite retries.
;
;
;        ValidatePort - is a Boolean the defines whether the driver should
;                       validate the port's existence before using it. The
;                       valid values are:
;
;                0 - disable port validation.
;              * 1 - enable port validation.
;
;              * Default.
;***********************************************************************
[SentinelSetup]                                ; General config options
MachineType                 = 1                ; IBM machine
Delay                       = 0                ; Use autotiming
MaskInterrupts              = 0                ; Don't mask any interrupts

[SentinelSetupPortA]                           ; First port setup record
PortAddress                 = 3bc              ; port address to use
PortContentionMethod        = 80000000         ; use driver defined methods
PortType                    = 3                ; IBM AT type port
PortContentionRetryCount    = 0                ; disable contention rc
PortContentionRetryInterval = 0                ; disable contention ri
DeviceRetryCount            = -1               ; indefinite device rc
ValidatePort                = 0                ; don't validate the port

[SentinelSetupPortB]                           ; Second port setup record
;PortAddress                = 278              ; port address to use
PortAddress                 = 0                ; ignore this setup record
PortContentionMethod        = 80000000         ; use driver defined
                                               ; contention methods when
                                               ; accessing this port
PortType                    = 4                ; IBM PS/2 DMA type port
PortContentionRetryCount    = 0                ; disable contention rc
PortContentionRetryInterval = 0                ; disable contention ri
DeviceRetryCount            = -1               ; indefinite device rc
ValidatePort                = 0                ; don't validate the port

[SentinelSetupPortC]                           ; Second port setup record
PortAddress                 = 378              ; port address to use
PortContentionMethod        = 4                ; Disable system interrupts
                                               ; when accessing this port
PortType                    = 4                ; IBM PS/2 DMA type port


------------------------------------------
5.0     OS/2 Driver Installation Procedure
------------------------------------------

  1.  Make a backup copy of the diskette.

  2.  Start a OS/2 windows by double clicking on the OS/2 Windows icon in the
      Command prompt folder.

  3.  Type "A:\OS2\INSTALL.CMD" at the command prompt. Change the disk drive
      letter A: if the Sentinel Portable Driver Diskette is in a floppy disk 
      drive other than A:.

  4.  A dialog box with title "OS/2 Device Driver Installation" is displayed.

  5.  Change the source directory and destination directory if necessary.
      In case of the CD-ROM distribution, Change the source directory to
      {CD-ROM DRIVE}:\PRODUCT\DRIVERS where {CD-ROM DRIVE} is the drive
      letter corresponding to CD-ROM drive on your system.

  6.  Click on "Install".

  7.  Select the "Rainbow OS/2 Device Driver".

  8.  Click on "OK" button.

  9.  After the driver has been installed, click on "Exit" to exit.

 10.  Click on "Yes" button when the dialog box with message "Exit The 
      Program" appears.

 11.  Restart OS/2.
 
 12.  If you need to change any of the driver's default settings, modify the 
      DEVICE statement in the CONFIG.SYS file and create an .ini file 
      containing the required parameters.  See the following section for 
      details.


Manual Installation of Sentinel System Driver for OS/2
---------------------------------------------------------
  We highly recommend that you install the Sentinel System Driver for OS/2
  with our installer.  If you decide to install it manually later on, you may
  do so by performing the following steps:

  1.  Copy \OS2\SENTINEL.SYS to the OS2 subdirectory.

  2.  Add the following line to your CONFIG.SYS file:

      DEVICE=C:\OS2\SENTINEL.SYS


-----------------------------------
5.1     OS/2 Driver Configuration
-----------------------------------

  The method of configuring the system driver under OS/2 uses a 
  configuration file. The file name of the configuration file is passed 
  to the driver via a command line argument. The configuration file uses 
  syntax similar to that used by Windows for its INI files. The 
  configuration file uses the same section names as defined for the 
  Windows 3.x driver. Data can be defined for all ports up to a maximum 
  of 4 ports.  Configuration information can be written to a log file. 

;OS/2 1.x/2.x/3.x System Driver Sample .ini File
;
;
; Sentinel Device Driver Configuration Options for OS/2 1.x/2.x driver.
;
; The OS/2 Sentinel Device Driver is installed through the OS/2 
; CONFIG.SYS file by adding a DEVICE statement as follows:
;
; DEVICE=[PATH]\SENTINEL.SYS
;
; where [PATH] is the drive and directory where the SENTINEL.SYS driver
; resides.
;
; -----------------------
; COMMAND LINE ARGUMENTS:
; -----------------------
;
; DEVICE=[PATH]\SENTINEL.SYS [[/Q] [/C=<config file>] [/L=<log file>]]
;
;        where:
;        
;                /Q  - Suppresses the sign-on banner.
;                /C= - Defines the configuration file to use. The format of
;                        a configuration file is defined below.
;                /L= - Defines the path and file name of where to log the
;                        driver's current configuration results to.
;
;
;        Example:
;
;        DEVICE=C:\SENTINEL.SYS /Q /C=C:\SENTINEL.INI /L=C:\SENTINEL.LOG
;
;        The above command line arguments perform the following functions:
;                Suppress the sign-on banner
;                Use the configuration parameters in C:\SENTINEL.INI
;                Log the current driver configuration to C:\SENTINEL.LOG
;
; --------------------------
; CONFIGURATION FILE FORMAT:
; --------------------------
;
; ---------------------------
; GENERAL CONFIGURATION DATA:
; ---------------------------
;
; General driver configuration and parameters are defined as follows:
;
; Section Name: [SentinelSetup]
;
; Parameters  :
;
;         LogFileName - Defines the path and file name used to log the
;                       configuration results of the driver during 
;                       installation. This parameter overrides the
;                       corresponding command line argument, /L=.
;
;                Example:
;
;                [SentinelSetup]
;                LogFileName = C:\SENTINEL.LOG ; log output results to
;                                                        ; this file.
;
;         SignOnMessage - A Boolean value defining whether the sign on
;                         banner should be displayed. This parameter 
;                         overrides the corresponding command line
;                         argument, /Q. The valid values are:
;
;                0 - disable banner display.
;                1 - enable banner display.
;
;                Example:
;
;                [SentinelSetup]
;                SignOnMessage = 1                    ; enable sign-on banner
;
;         MachineType - Defines the machine type the driver is to be 
;                       configured for. The valid values are:
;                        
;              * 0 - Autodetect machine type.
;                1 - Defines IBM and IBM compatible machines.
;                2 - Defines NEC PC-9800 series machines.
;                3 - Defines Fujitsu FMR series machines. 
;
;              * Default.
;
;                Example:
;
;                [SentinelSetup]
;                MachineType = 1        ; Configure driver for IBM machines.
;
;         Delay - Defines the number of machine loops to use to 
;                 create a 2 microsecond delay. The valid values
;                 are:
;
;              * 0 - Use autotiming.
;                1-65535 - Number of loops to use to create a 2us delay.
;
;              * Default.
;
;                Example:
;               
;                [SentinelSetup]
;                Delay = 100                ; Use 100 loops to create a 2us 
;                                           ; delay.
;
;        MaskInterrupts - Defines the set of interrupts to mask when 
;                         accessing the port (used for port contention).
;                         This is defined as a hexadecimal bit mask with the
;                         following values:
;
;                0 - Disable interrupt masking.
;              * 1 - Mask LPT1 printer interrupt.
;                2 - Mask LPT2 printer interrupt.
;              * 4 - Mask TIMER interrupt.
;
;              * Default interrupts masked.
;
;                To disable a set of interrupts, add the individual bit masks 
;                together to form the result mask.
;
;                Example:
;
;                [SentinelSetup]
;                MaskInterrupts = 5        ; Mask LPT1 and TIMER interrupts.
;
; ------------------------
; PORT CONFIGURATION DATA:
; ------------------------
;
; Per-Port configuration and parameters are defined as follows:
;
; Section Name: [SentinelSetupPort?]
;
; Where ? is the port to configure defined as A through Z. Any port
; configuration defined overrides the default port configuration for
; the driver. Only the first 4 port configuration records (starting
; alphabetically with A) are used. The PortAddress parameter must be
; defined for the port configuration record to be used.
;
; Parameters  :
;
;        PortAddress - Defines the base address for a port. The 
;                      parameter must be defined for the remaining
;                      parameters to be used. The value must be
;                      defined in hexadecimal. The valid values are:
;
;                             0 - Disables setup record.
;                1 through FFFE - Used as actual port address.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC              ; Define the first port to use
;                                               ; as 0x03BC.
;
;        PortContentionMethod - Defines the contention method used to
;                               gain access to a port. This is defined as
;                               a hexadecimal bit mask with the following ;                                         values:
;
;                 0 - Disable port all contention methods.
;                 1 - Use system port contention handler if available. 
;                     (Not available for Windows 3.x).
;                 4 - Disable system interrupts.
;                 8 - Mask interrupts as defined by the MaskInterrupts 
;                     parameter under the [SentinelSetup] section 
;                     (see above).
;                10 - Use windows critical section handler. 
;                     (Not available for OS/2).
;                20 - Poll the port for access.
;                40 - Enable collision detection.
;         * 8000000 - Use driver defined values.
;
;              * Default.
;
;                To enable a set of contention methods, add the
;                individual bit masks together to form the 
;                resulting contention method.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC              ; Define the first port to use
;                                               ; as 0x03BC.
;                PortContentionMethod = 79      ; Enable the following: 
;                                               ; mask interrupts,
;                                               ; Windows critical section, 
;                                               ; port polling,
;                                               ; collision detection, and
;                                               ; system port contention 
;                                               ; handler.
;
;        SystemPortNumber - Defines the logical port number to use
;                           for the defined port address when
;                           system contention driver is installed.
;                           The valid values are:
;
;
;                0-65534 - The logical port number to use.
;                   * -1 - Autodetect the logical port number. 
;
;              * Default.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC              ; Define the first port to use
;                                               ; as 0x03BC.
;                PortContentionMethod = 79      ; Enable the following: 
;                                               ; mask interrupts,
;                                               ; Windows critical section, 
;                                               ; port polling,
;                                               ; collision detection, and
;                                               ; system port contention 
;                                               ; handler.
;                SystemPortNumber = 0           ; First installed port.
;
;       PortDriver - Defines the system driver that handles system
;                    port contention for the parallel ports. This
;                    option is only available on version 2.11 and 
;                    above of OS/2. The valid value is a string 
;                    which length does not exceed 8 characters.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC               ; Define the first port to use
;                                                ; as 0x03BC.
;                PortContentionMethod = 1        ; Use system port contention
;                                                ; handler.
;                PortDriver = LPT1               ; Use the LPT1 driver for
;                                                ; system port contention.
;
;
;        PortType - Defines the type of parallel port. The valid values are:
;
;              * 0 - Autodetect port type.
;                1 - NEC PC-9800 series parallel port. 
;                    (Only valid when MachineType = 2 (NEC PC9800)).
;                2 - Fujitsu FMR series parallel port.
;                    (Only valid when MachineType = 3 (Fujitsu)).
;                3 - IBM AT or PS/2 compatible parallel port
;                    (Only valid when MachineType = 1 (IBM)).
;                4 - IBM PS/2 compatible parallel port w/DMA
;                    (Only valid when MachineType = 1 (IBM)).
;
;              * Default.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC               ; Define the first port to use
;                                                ; as 0x03BC.
;                PortType = 3                    ; IBM AT type port.
;
;        PortContentionRetryInterval - Defines the number of milliseconds
;                                      to delay in-between retries on
;                                      contenting for a busy port. This
;                                      parameter is used in conjunction
;                                      with the PortContentionRetryCount
;                                      parameter (see below). The valid
;                                      values are:
;
;                0 through 65534 - number of milliseconds to delay in-between 
;                                  retries of contending for a busy port.
;
;                             -1 - indefinite retry interval.
;
;              * Default is 300.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC               ; Define the first port to use
;                                                ; as 0x03BC.
;                PortContentionRetryInterval = 5 ; Delay 5 milliseconds
;                                                ; between retries on
;                                                ; a busy port.
;
;        PortContentionRetryCount - Defines the number of retries to perform 
;                                   on a busy port.  Used in conjunction with 
;                                   the PortContentionRetryInterval parameter 
;                                   (see above). The valid values are:
;
;                0-65534 - number of retries to perform on a busy port.
;
;                     -1 - indefinite retry count.
;
;              * Default is 100.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC               ; Define the first port to use
;                                                ; as 0x03BC.
;                PortContentionRetryInterval = 5 ; Delay 5 milliseconds
;                                                ; between retries on
;                                                ; a busy port.
;                                                ; port is owned
;                PortContentionRetryCount = -1   ; indefinite retries.
;
;        DeviceRetryCount - Defines the number of retries to perform on a I/O 
;                           request (query) if communications is interrupted 
;                           (the collision detection contention method
;                           (see above) must be enabled for this parameter
;                           to be used). The valid values are:
;
;                0 through 65534 - number of retries to perform.
;                             -1 - indefinite retry count.
;
;              * Default is 300.
;
;                Example:
;
;                [SentinelSetupPortA]
;                PortAddress = 3BC              ; Define the first port to use
;                                               ; as 0x03BC.
;                PortContentionMethod = 78      ; Enable the following: 
;                                               ; mask interrupts,
;                                               ; Windows critical section, 
;                                               ; port polling, and 
;                                               ; collision detection.
;                DeviceRetryCount     = -1      ; indefinite retries.
;
;
;        ValidatePort - is a Boolean the defines whether the driver should
;                       validate the port's existence before using it. The
;                       valid values are:
;
;                0 - disable port validation.
;              * 1 - enable port validation.
;
;              * Default.
;***********************************************************************
[SentinelSetup]                                    ; General config options
SignOnMessage                    = 1               ; Enable sign-on banner
LogFileName                      = C:\SENTINEL.LOG ; log current configuration
MachineType                      = 1               ; IBM machine
Delay                            = 0               ; Use autotiming
MaskInterrupts                   = 0               ; Don't mask any interrupts

[SentinelSetupPortA]                               ; First port setup record
PortAddress                      = 3bc             ; port address to use
PortContentionMethod             = 80000000        ; use driver defined methods
PortType                         = 3               ; IBM AT type port
PortContentionRetryCount         = 0               ; disable contention rc
PortContentionRetryInterval      = 0               ; disable contention ri
DeviceRetryCount                 = -1              ; indefinite device rc
SystemPortNumber                 = 0               ; system's logical port number
PortDriver                       = LPT1            ; system port contention drvr
ValidatePort                     = 0               ; don't validate the port

[SentinelSetupPortB]                               ; Second port setup record
;PortAddress                     = 278             ; port address to use
PortAddress                      = 0               ; ignore this setup record
PortContentionMethod             = 80000000        ; use driver defined
                                                   ; contention methods when
                                                   ; accessing this port
PortType                         = 4               ; IBM PS/2 DMA type port
PortContentionRetryCount         = 0               ; disable contention rc
PortContentionRetryInterval      = 0               ; disable contention ri
DeviceRetryCount                 = -1              ; indefinite device rc
ValidatePort                     = 0               ; don't validate the port

[SentinelSetupPortC]                               ; Second port setup record
PortAddress                      = 378             ; port address to use
PortContentionMethod             = 4               ; Disable system interrupts
                                                   ; when accessing this port
PortType                         = 4               ; IBM PS/2 DMA type port


------------------------------------------------
6.0     Windows 95 Driver Installation Procedure
------------------------------------------------
  1.  Make a backup copy of the diskette.

  2.  Start Windows 95.  Select "Run" from the Taskbar and run the file
      SENTW95.EXE in the \WIN_95 subdirectory on the driver diskette.
      There are two command line options:
        1.  /q     Quiet mode.  
                   Normal dialogs described below are not displayed.
                   Error messages are displayed.
        2.  /pxxx  Path, where xxx is the path of files to be installed.
                   Specify the path of files to be installed.
                   Otherwise, files will be copied from the default
                   directory.

  3.  Select "Install Sentinel Driver" from the "Functions" menu.

  4.  Click "OK" when the "Driver installed!  Restart your system."
      message appears.  Restart Windows 95.

  5.  The following files have been created on your hard disk:
        WINDOWS\SYSTEM\SENTINEL.VXD
        WINDOWS\SYSTEM\RNBOSENT\SENTW95.EXE
        WINDOWS\SYSTEM\RNBOSENT\SENTW95.DLL
        WINDOWS\SYSTEM\RNBOSENT\SENTW95.HLP
        WINDOWS\SYSTEM\RNBOSENT\SENTINEL.SAV


Manual Installation of Sentinel System Driver for Windows 95
------------------------------------------------------------
We strongly recommend that you install the Sentinel System Driver for
Windows 95 with our installer.  If you decide to install it manually, you
may do so by performing the following steps:

  1.  Make a backup copy of the diskette.

  2.  If your application is a Win32 application, go to step 7.

  3.  Run Registry Editor (REGEDIT.EXE in Windows 95 root directory).

  4.  Select HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\RunServices.
     ( Clicking on the expansion box next to the item name expands the
     branch )

  5.  With RunServices highlighted, click on "Edit" menu and select "New",  
      then select "String Value" from its submenu.  Registry Editor 
      adds an entry "New Key #1" to the end of the list.
      Rename it to "RNBOStart".  ( To rename a key, click it with right mouse
      button, select Rename, and type the new name )
      Double-click on it to bring up "Edit String" dialog box.
      Type "%system_root%\system\rnbosent\sentstrt.exe" and click OK,
      where %system_root% is the name of the Windows 95 root directory.

  6.  Alternatively, the file sentstrt.exe can be copied to the
      %system_root%\startm~1\programs\startup subdirectory.

  7.  Copy the file "SENTINEL.VXD" from the "WIN_95\" directory on the
      Sentinel Driver diskette to the %system_root%\system directory.
      Create the subdirectory %system_root%\system\rnbosent.
      Copy all other files from the "WIN_95\" directory to the 
      %system_root%\system\rnbosent subdirectory.  Also copy "SENTINEL.VXD"
      to %system_root%\system\rnbosent as "SENTINEL.SAV", this is your
      back-up file to the system driver.

  8.  The installation is now complete. 
      To use the driver with Win32 applications, start the application.
      For all other applications, restart Windows 95.


------------------------------------------------
6.1     Windows 95 Driver Configuration
------------------------------------------------
  1.  Start Windows 95.  Select "Run" from the Taskbar and run the file
      SENTW95.EXE in the WINDOWS\SYSTEM\RNBOSENT subdirectory.

  2.  Select "Configure Sentinel Driver" from the "Functions" menu.

  3.  Click the "Edit" button to edit an existing parallel port setting
      or click the "Add" button to add a new parallel port setting.
      Select "OK" after you finish the port configuration.

  4.  Restart Windows 95 for the changes to take effect.


------------------------------------------------
6.2     Windows 95 Driver Un-install
------------------------------------------------

  1.  Start Windows 95.  Select "Run" from the Taskbar and run the file
      SENTW95.EXE in the WINDOWS\SYSTEM\RNBOSENT subdirectory (or from the
      original distribution media).  The driver can be removed via the
      command-line options or the pull-down menu.

      a. Command-line options:
           SENTW95 /q /u  -  Quietly removes the existing driver.

      b. Pull-down menu:
           Select "Remove Sentinel Driver" from the "Funtion" menu.

  2.  When complete, a dialog box with the message "Sentinel Driver Removed"
      is displayed.

  3.  Click "OK" to continue.
