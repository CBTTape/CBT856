# CBT856
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 856 is from Steve McColley and contains the Shared Spool  *   FILE 856
//*           Mods (previously known as the "Mellon Mods" for JES2) *   FILE 856
//*           which should be good for z/OS 1.9 thru z/OS 1.12.     *   FILE 856
//*           (They were tested on a z/OS 1.12 and z/OS 1.13        *   FILE 856
//*           system.)                                              *   FILE 856
//*                                                                 *   FILE 856
//*                Stephen McColley                                 *   FILE 856
//*                McColley Systems Group Inc.                      *   FILE 856
//*                SGMcColley@MVSProgrammer.com                     *   FILE 856
//*                http://WWW.MVSProgrammer.com                     *   FILE 856
//*                770-335-0478                                     *   FILE 856
//*                                                                 *   FILE 856
//*  Important                                                      *   FILE 856
//*    Note:    McColley Systems Group now produces a vendor        *   FILE 856
//*    ----     supported product called ESSM which supersedes      *   FILE 856
//*             the Mellon Mods.  For information about ESSM,       *   FILE 856
//*             please see members:  @ESSMDOC (MS Word), and        *   FILE 856
//*             @ESSMTXT (plain text without the table).            *   FILE 856
//*                                                                 *   FILE 856
//*          Please inquire about ESSM from the address above.      *   FILE 856
//*                                                                 *   FILE 856
//*       ------------------------------------------------          *   FILE 856
//*                                                                 *   FILE 856
//*               SSSS H   H  AAA  RRRR  EEEEE DDDD                 *   FILE 856
//*              S     H   H A   A R   R E     D   D                *   FILE 856
//*               SSS  HHHHH AAAAA RRRR  EEEE  D   D                *   FILE 856
//*                  S H   H A   A R  R  E     D   D                *   FILE 856
//*              SSSS  H   H A   A R   R EEEEE DDDD                 *   FILE 856
//*                                                                 *   FILE 856
//*                  SSSS PPPP   OOO   OOO  L                       *   FILE 856
//*                 S     P   P O   O O   O L                       *   FILE 856
//*                  SSS  PPPP  O   O O   O L                       *   FILE 856
//*                     S P     O   O O   O L                       *   FILE 856
//*                 SSSS  P      OOO   OOO  LLLLL                   *   FILE 856
//*                                                                 *   FILE 856
//*                    M   M  OOO  DDDD   SSSS                      *   FILE 856
//*                    MM MM O   O D   D S                          *   FILE 856
//*                    M M M O   O D   D  SSS                       *   FILE 856
//*                    M   M O   O D   D     S                      *   FILE 856
//*                    M   M  OOO  DDDD  SSSS                       *   FILE 856
//*                                                                 *   FILE 856
//*                  for jes2 1.10, 1.11 and 1.12                   *   FILE 856
//*                           and 1.13                              *   FILE 856
//*                                                                 *   FILE 856
//*      DISCLAIMER -                                               *   FILE 856
//*                                                                 *   FILE 856
//*    ***********************************************************  *   FILE 856
//*    *                                                         *  *   FILE 856
//*    *     THE MODS ON THIS TAPE HAVE BEEN USED SUCCESSFULLY   *  *   FILE 856
//*    *  AND TO THE BEST OF OUR KNOWLEDGE THEY ARE OPERATIONAL, *  *   FILE 856
//*    *  HOWEVER NO WARRANTY IS MADE TO THE ACCURACY OF THE     *  *   FILE 856
//*    *  MODS AND NO RESPONSIBILITY IS ASSUMED FOR ANY          *  *   FILE 856
//*    *  MODIFICATION DIRECTLY OR INDIRECTLY CAUSED BY THE USE  *  *   FILE 856
//*    *  OF THE MODIFICATIONS.  IT IS THE USERS RESPONSIBILITY  *  *   FILE 856
//*    *  TO EVALUATE THE USEFULLNESS OF THE MATERIAL.           *  *   FILE 856
//*    *                                                         *  *   FILE 856
//*    *     WE DO NOT GUARANTEE TO KEEP ANY MATERIAL PROVIDED   *  *   FILE 856
//*    *  UP TO DATE, NOR DO WE GUARANTEE TO PROVIDE ANY         *  *   FILE 856
//*    *  CORRECTIONS OR EXTENSIONS MADE IN THE FUTURE.          *  *   FILE 856
//*    *                                                         *  *   FILE 856
//*    ***********************************************************  *   FILE 856
//*                                                                 *   FILE 856
//*      This is the installation PDS for the Shared Spool Mods     *   FILE 856
//*     for JES2 1.10, 1.11, 1.12 and JES2 1.13.  The shared spool  *   FILE 856
//*     mods were formely known as the Mellon shared spool mods.    *   FILE 856
//*                                                                 *   FILE 856
//*      All who use the shared spool mods, owe a debt of           *   FILE 856
//*     gratitude to Mellon Bank for the original implementaion     *   FILE 856
//*     of the shared spool mods, but because it has been           *   FILE 856
//*     maintained outside of Mellon for over 15 years, and has     *   FILE 856
//*     been rewritten twice since then, we will refer to the       *   FILE 856
//*     mods as the SHARED SPOOL MODS from now on.  Once again -    *   FILE 856
//*                          THANK YOU MELLON BANK !                *   FILE 856
//*                                                                 *   FILE 856
//*      In this PDS you should find the following members.         *   FILE 856
//*                                                                 *   FILE 856
//*                    ( ADMINISTRATIVE MEMBERS )                   *   FILE 856
//*                                                                 *   FILE 856
//*    @@README -   That is this member, you are reading it.        *   FILE 856
//*                                                                 *   FILE 856
//*    DISCLAIM -   Our standard disclaimer - we guarentee /        *   FILE 856
//*                 warrant nothing!                                *   FILE 856
//*                                                                 *   FILE 856
//*                ( DOCUMENTATION - PDF AND DOC FORMAT MANUALS )   *   FILE 856
//*    SSMINSTP -   Shared Spool Mods installation manual - PDF     *   FILE 856
//*                 format (simply download to your PC as           *   FILE 856
//*                 ssminst.pdf - binary xfer)                      *   FILE 856
//*                                                                 *   FILE 856
//*    SSMINSTW -   Shared Spool Mods installation manual - Word    *   FILE 856
//*                 Document (simply download to your PC as         *   FILE 856
//*                 ssminst.doc - binary xfer)                      *   FILE 856
//*                                                                 *   FILE 856
//*    SSMUSERP -   Shared Spool Mods Users Guide - PDF format      *   FILE 856
//*                 (simply download to your PC as ssmuser.pdf -    *   FILE 856
//*                 binary xfer)                                    *   FILE 856
//*                                                                 *   FILE 856
//*    SSMUSERW -   Shared Spool Mods Users Buide - Word            *   FILE 856
//*                 Document (simply download to your PC as         *   FILE 856
//*                 ssmuser.doc - binary xfer)                      *   FILE 856
//*                                                                 *   FILE 856
//*    SSMOPSGP -   Shared Spool Mods Operations Guide - PDF        *   FILE 856
//*                 format (simply download to your PC as           *   FILE 856
//*                 ssmopsg.pdf - binary xfer)                      *   FILE 856
//*                                                                 *   FILE 856
//*    SSMOPSGW -   Shared Spool Mods Operations Guide - Word       *   FILE 856
//*                 Document (simply download to your PC as         *   FILE 856
//*                 ssmopsg.doc - binary xfer)                      *   FILE 856
//*                                                                 *   FILE 856
//*                   ( SMP INSTALLATION MEMBERS )                  *   FILE 856
//*                                                                 *   FILE 856
//*    LSES500  -   The SMP/e usermod needed to install the         *   FILE 856
//*                 entire package.                                 *   FILE 856
//*                                                                 *   FILE 856
//*    LSES500J -   Sample JCL to run the RECEIVE / APPLY Check     *   FILE 856
//*                 / APPLY (You must apply lses500 or use the      *   FILE 856
//*                 non-smp install method).                        *   FILE 856
//*                                                                 *   FILE 856
//*                 ( NON-SMP INSTALLATION MEMBERS )                *   FILE 856
//*                                                                 *   FILE 856
//*    ALOCLIBS -   NON-SMP STEP 1 - ALLOCATE NEW LIBRARIES.        *   FILE 856
//*                                                                 *   FILE 856
//*    COPYLIBS -   NON-SMP STEP 3 - POPULATE NEW LIBRARIES.        *   FILE 856
//*                                                                 *   FILE 856
//*                 ( COMMON JES2 PARMS NEEDED FOR PACKAGE )        *   FILE 856
//*                                                                 *   FILE 856
//*    JES2PARM -   SAMPLE JES2 PARMS NEEDED TO IMPLEMENT THE       *   FILE 856
//*                 PACKAGE.                                        *   FILE 856
//*                                                                 *   FILE 856
//*    *** THEN WE HAVE THE FOLLOWING FOUR MEMBERS - THEY ARE       *   FILE 856
//*    *** NOT REALLY PART OF THE SHARED SPOOL MODS - BUT WE        *   FILE 856
//*    *** HAVE BEEN DISTRIBUTING THEM, AND SOME FOLKS STILL        *   FILE 856
//*    *** NEED THEM.  IF YOU WANT TO USE THESE, YOU WILL HAVE      *   FILE 856
//*    *** TO APPLY THEM SEPARATELY FROM THE SHARED SPOOL MODS -    *   FILE 856
//*    *** WE JUST HAVE THE SOURCE - THEY ARE NOT SET UP AS         *   FILE 856
//*    *** USERMODS.                                                *   FILE 856
//*                                                                 *   FILE 856
//*                                                                 *   FILE 856
//*    STSCX01A -   OUR VERSION OF THE PAGE SEPARATOR EXIT.         *   FILE 856
//*                 (NOT PART OF SSM'S)                             *   FILE 856
//*                                                                 *   FILE 856
//*    STSCX05B -   PREVENT PURGING BY JOB RANGE. (NOT PART         *   FILE 856
//*                 OF SSM'S)                                       *   FILE 856
//*                                                                 *   FILE 856
//*    STSCX15A -   CAUSES FCBS TO BE RELOAD WITH EACH JOB          *   FILE 856
//*                 UNLESS STD FORMS.                               *   FILE 856
//*                                                                 *   FILE 856
//*    STSCX36A -   SAF PROCESSING FOR JOBS COMING IN FROM          *   FILE 856
//*                 RJE/NJE SOURCES.                                *   FILE 856
//*                                                                 *   FILE 856
//*                                                                 *   FILE 856
//*      THE DOCUMENTATION MEMBERS SUFFIXED WITH A 'P' I.E.         *   FILE 856
//*    SSMINSTP ARE PDF FORMAT DOCUMENTS.  TO USE THEM YOU WILL     *   FILE 856
//*    NEED TO TRANSFER THEM TO A PC USING YOUR FAVORITE FILE       *   FILE 856
//*    TRANSFER PROGRAM USING A BINARY OPTION - IE.  NO             *   FILE 856
//*    TRANSLATION.  YOU WILL PROBABLY NEED TO MAKE SURE THEY       *   FILE 856
//*    ARE TRANSFERRED TO A NEW FILE NAME THAT ENDS IN ".PDF",      *   FILE 856
//*    OR YOU MAY NOT BE ABLE TO READ THEM.                         *   FILE 856
//*                                                                 *   FILE 856
//*      IF YOU CAN NOT READ PDF DOCS THE ORIGINAL "WORD"           *   FILE 856
//*    FORMATTED DOCS ARE INCLUDED IN THE MEMBERS SUFFIXED WITH     *   FILE 856
//*    A "W" I.E. SSMINSTW.  YOU WILL PROBABLY NEED TO OFFLOAD      *   FILE 856
//*    THEM TO A PC FILE WITH A SUFFIX OF DOC TO READ THEM          *   FILE 856
//*    PROPERLY.                                                    *   FILE 856
//*                                                                 *   FILE 856
//*      THE THREE BASIC PIECES OF DOCUMENTATION ARE -              *   FILE 856
//*                                                                 *   FILE 856
//*    1 THE INSTALLATION GUIDE - GIVES BACKGROUND, INSTALLATION    *   FILE 856
//*      INSTRUCTIONS, AND OTHER INFORMATION NEEDED TO SETUP THE    *   FILE 856
//*      SHARED SPOOL MODS PACKAGE.                                 *   FILE 856
//*                                                                 *   FILE 856
//*    2 THE USERS GUIDE - GIVES DETAILED INFO ON JECL              *   FILE 856
//*      STATEMENTS AND IS AIMED AT THE END USERS - WHOEVER         *   FILE 856
//*      CODES AND USES JCL.                                        *   FILE 856
//*                                                                 *   FILE 856
//*    3 THE OPERATIONS GUIDE - GIVES DETAILED INFORMATIN ABOUT     *   FILE 856
//*      ALL OF THE NEW JES2 DISPLAY AND MODIFY COMMANDS            *   FILE 856
//*      AVAIALABLE WITH THE PACKAGE.                               *   FILE 856
//*                                                                 *   FILE 856
//*      ONCE YOU HAVE THE PACKAGE SET UP - PLEASE DROP ME A        *   FILE 856
//*      LINE AT                                                    *   FILE 856
//*                                                                 *   FILE 856
//*      email:    SGMCCOLLEY@ALLTEL.NET                            *   FILE 856
//*                STEPHEN.MCCOLLEY@MVSPROGRAMMER.COM               *   FILE 856
//*                                                                 *   FILE 856
//*      SO THAT I CAN ADD YOU TO THE MAILING LIST.  THAT WAY I     *   FILE 856
//*      CAN LET YOU KNOW ABOUT BUGS, FIXES, AND NEW RELEASES AS    *   FILE 856
//*      I MAKE THE AVAIALABLE.                                     *   FILE 856
//*                                                                 *   FILE 856
//*      IF YOU DROP ME YOUR REAL MAILING ADDRESS, I WILL SEND      *   FILE 856
//*      YOU A REAL "SHARED SPOOL MODS" COFFEE CUP - I STILL        *   FILE 856
//*      HAVE PLENTY OF THESE.                                      *   FILE 856
//*                                                                 *   FILE 856
```
