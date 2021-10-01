# reconstructer.org
Legacy repo of my discontinued reconstructer.org website with some tools and papers from 2006 - 2013

Table of contents:
------------------

-> OfficeMalScanner.zip
   --------------------
   OfficeMalScanner is a Microsoft Office forensic tool to scan for malicious traces, like shellcode heuristics, PE-files or embedded OLE
   streams. Found files are being extracted to disk. It supports disassembly and hexview as well as an easy brute force mode to detect
   encrypted files. Next to this, an office file is being scanned for VB-macros code and if found, it will be extracted for further
   analysis.The "inflate" feature extracts Ms Office 2007 documents into a directory and marks potentially malicious files. 


-> ClassAndInterfaceToNames.zip
   -----------------------------
   This small IDAPython script scans an IDB file for class and interfaces UUIDs and creates the matching structure and its names.
   Unfortunately IDA doesn't do this automatically, thus this little helper. It can help you when reversing malware 
   using the COM interface, e.g. for IE-Browser or Outlook manipulation, BITS file transfer or dumping the protected storage. Make sure to
   copy interfaces.txt + classes.txt + ClassAndInterfaceToNames.py to IDADIR, e.g. C:\Program Files\IDA


-> VtablesStructuresFromPSDK2003R2.zip
  ------------------------------------
  This small IDAPython script includes all vtable structures that can be found in the files of the Microsoft PSDK 2003-R2. After running the
  script in IDA it adds these vtable structures to an IDB file. This will save time while reconstructing COM code.


-> Practical COM code reconstruction.swf
  -------------------------------------
  This COM reconstruction video tutorial (use Windows Media Player to view) is a practical guide to Microsoft COM code reconstruction. In 
  this tutorial a malware using COM is being dissected, which dumps the windows protected storage to steal credentials. After reconstruction 
  there is a far more readable code.
  
-> The big SoftICE howto.pdf
  -------------------------
  A comprehensive guide to the formerly best kernel debugger SoftICE by NuMega.


-> A Journey to the Center of the Rustock.B Rootkit.pdf
  ----------------------------------------------------
  Analysis of the Rustock.B rootkit. The rootkit used several proprietary obfuscation/packing methods to hide the native driver code from
  prying eyes. The paper is devided into two parts. The first part, which is divided in three stages, describes how to extract the
  native rootkit driver code without the use of kernel debuggers or other ring0 tools. The second part basically does the same, but much
  faster and with lesser efforts using the SoftICE kernel debugger.
  

-> Peacomm.C - Cracking the nutshell.pdf
  -------------------------------------
  Analysis of the malware Peacomm.C aka StormWorm. Learn about its XOR + TEA decryption, TIBS unpacking, defeating Anti-Debugging code, 
  files dropping, driver-code infection, VM-detection tricks and its rootkit features.
  

-> Rustock.C - When a myth comes true.pdf
  --------------------------------------
  Still one of the most impressive and hardest to analyze rootkits until today.
  

-> Hunting malware with Volatility v2.0.pdf
  ----------------------------------------
  Practical guide to show Volatility's powerful capabilities in malware forensics - One of most infamous rootkits like (e.g. TDL3, TDL4,
  Stuxnet, Zeroaccess, Rustock B. + C.) will be treated and how to find them in physical memory.


->Hunting rootkits with Windbg.pdf
  --------------------------------
  Practical guide how to analyze one of most infamous rootkits like (e.g. TDL3, TDL4, Stuxnet, Zeroacces, Rustock B. + C.) with the powerful 
  Windbg kernel debugger.


-> masTIFF - An in depth analysis of CVE-2013-3906.pdf
  ----------------------------------------------------
  Root Cause analysis of CVE-2013-3906 exploiting a TIFF bug inside a Microsoft Office Winword file. This bug was exploited in
  a targeted attack in November 2013.
  
