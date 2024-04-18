---
published: true
date: 2024-04-18
title: testing if assembly works on this
url: 0xN1ghtStalker.github.io
---
```assembly
                                                        **************************************************************
                             *                          FUNCTION                          *
                             **************************************************************
                             undefined something_weird()
                               assume FS_OFFSET = 0xffdff000
             undefined         AL:1           <RETURN>
             undefined4        ESI:4          mysterious_url                          XREF[1]:     00408155(W)  
             undefined1        Stack[-0x1]:1  local_1                                 XREF[1]:     00408177(W)  
             undefined2        Stack[-0x3]:2  local_3                                 XREF[1]:     0040816c(W)  
             undefined4        Stack[-0x7]:4  local_7                                 XREF[1]:     00408168(W)  
             undefined4        Stack[-0xb]:4  local_b                                 XREF[1]:     00408164(W)  
             undefined4        Stack[-0xf]:4  local_f                                 XREF[1]:     00408160(W)  
             undefined4        Stack[-0x13]:4 local_13                                XREF[1]:     0040815c(W)  
             undefined4        Stack[-0x17]:4 local_17                                XREF[1]:     00408158(W)  
             undefined1        Stack[-0x50]:1 local_50                                XREF[1]:     0040814f(*)  
                             something_weird                                 XREF[1]:     entry:00409b45(c)  
        00408140 83 ec 50        SUB        ESP,0x50
        00408143 56              PUSH       ESI
        00408144 57              PUSH       EDI
        00408145 b9 0e 00        MOV        ECX,0xe
                 00 00
        0040814a be d0 13        MOV        ESI,s_http://www.iuqerfsodp9ifjaposdfj_004313d0  = "http://www.iuqerfsodp9ifjapos
                 43 00
        0040814f 8d 7c 24 08     LEA        EDI=>local_50,[ESP + 0x8]
        00408153 33 c0           XOR        EAX,EAX
        00408155 f3 a5           MOVSD.REP  ES:EDI,mysterious_url                            = "http://www.iuqerfsodp9ifjapos
        00408157 a4              MOVSB      ES:EDI,mysterious_url=>s_http://www.iuqerfsodp   = "http://www.iuqerfsodp9ifjapos
        00408158 89 44 24 41     MOV        dword ptr [ESP + local_17],EAX
        0040815c 89 44 24 45     MOV        dword ptr [ESP + local_13],EAX
        00408160 89 44 24 49     MOV        dword ptr [ESP + local_f],EAX
        00408164 89 44 24 4d     MOV        dword ptr [ESP + local_b],EAX
        00408168 89 44 24 51     MOV        dword ptr [ESP + local_7],EAX
        0040816c 66 89 44        MOV        word ptr [ESP + local_3],AX
                 24 55
        00408171 50              PUSH       EAX
        00408172 50              PUSH       EAX
        00408173 50              PUSH       EAX
        00408174 6a 01           PUSH       0x1
        00408176 50              PUSH       EAX
        00408177 88 44 24 6b     MOV        byte ptr [ESP + local_1],AL
        0040817b ff 15 34        CALL       dword ptr [->WININET.DLL::InternetOpenA]         = 0000a7dc
                 a1 40 00
        00408181 6a 00           PUSH       0x0
        00408183 68 00 00        PUSH       0x84000000
                 00 84
        00408188 6a 00           PUSH       0x0
        0040818a 8d 4c 24 14     LEA        ECX,[ESP + 0x14]
        0040818e 8b f0           MOV        mysterious_url,EAX
        00408190 6a 00           PUSH       0x0
        00408192 51              PUSH       ECX
        00408193 56              PUSH       mysterious_url
        00408194 ff 15 38        CALL       dword ptr [->WININET.DLL::InternetOpenUrlA]      = 0000a7c8
                 a1 40 00
        0040819a 8b f8           MOV        EDI,EAX
        0040819c 56              PUSH       mysterious_url
        0040819d 8b 35 3c        MOV        mysterious_url,dword ptr [->WININET.DLL::Inter   = 0000a7b2
                 a1 40 00
        004081a3 85 ff           TEST       EDI,EDI
        004081a5 75 15           JNZ        LAB_004081bc
        004081a7 ff d6           CALL       mysterious_url=>WININET.DLL::InternetCloseHandle
        004081a9 6a 00           PUSH       0x0
        004081ab ff d6           CALL       mysterious_url=>WININET.DLL::InternetCloseHandle
        004081ad e8 de fe        CALL       FUN_00408090                                     undefined FUN_00408090()
                 ff ff
        004081b2 5f              POP        EDI
 
```