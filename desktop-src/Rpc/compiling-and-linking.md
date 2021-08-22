---
title: 編譯和連結
description: 下列 makefile 顯示編譯用戶端和伺服器應用程式所需的檔案之間的相依性，並將其連結至 RPC 執行時間程式庫和 standard C 執行時間程式庫。
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- 遠端程序呼叫 RPC、工作、編譯和連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2500a763db149eca914060dd7920548883fa57fbd5642485a41f5a55c65cd2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931711"
---
# <a name="compiling-and-linking"></a>編譯和連結

下列 makefile 顯示編譯用戶端和伺服器應用程式所需的檔案之間的相依性，並將其連結至 RPC 執行時間程式庫和 standard C 執行時間程式庫。

這個 makefile 可以用來從本教學課程的原始程式碼建立用戶端和伺服器應用程式。 此處顯示的存根和標頭是以 MIDL 2.0 版產生的。 編譯器和連結器命令和引數可能會因您的電腦設定而有所不同。 如需詳細資訊，請參閱編譯器的檔。

``` syntax
#makefile for helloc.exe and hellos.exe
#link refers to the linker
#conflags refers to flags for console applications
#conlibs refers to libraries for console applications
 
!include <ntwin32.mak>
 
all : helloc hellos
 
# Make the client side application helloc
helloc : helloc.exe
helloc.exe : helloc.obj hello_c.obj
    $(link) $(linkdebug) $(conflags) -out:helloc.exe \
        helloc.obj hello_c.obj \
        rpcrt4.lib $(conlibs)
 
# helloc main program
helloc.obj : helloc.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# helloc stub
hello_c.obj : hello_c.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# Make the server side application
hellos : hellos.exe
hellos.exe : hellos.obj hellop.obj hello_s.obj
    $(link) $(linkdebug) $(conflags) -out:hellos.exe \
        hellos.obj hello_s.obj hellop.obj \
        rpcrt4.lib $(conlibsmt)
 
# hello server main program
hellos.obj : hellos.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# remote procedures
hellop.obj : hellop.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# hellos stub file
hello_s.obj : hello_s.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# Stubs and header file from the IDL file
hello.h hello_c.c hello_s.c : hello.idl hello.acf
    midl hello.idl
```

 

 




