---
title: 編譯和連結
description: 下列 makefile 顯示編譯用戶端和伺服器應用程式所需的檔案之間的相依性，並將其連結至 RPC 執行時間程式庫和 standard C 執行時間程式庫。
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- 遠端程序呼叫 RPC、工作、編譯和連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1991e39cc028c01066cd8f13344765787374fa08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932276"
---
# <a name="compiling-and-linking"></a><span data-ttu-id="2e90c-104">編譯和連結</span><span class="sxs-lookup"><span data-stu-id="2e90c-104">Compiling and Linking</span></span>

<span data-ttu-id="2e90c-105">下列 makefile 顯示編譯用戶端和伺服器應用程式所需的檔案之間的相依性，並將其連結至 RPC 執行時間程式庫和 standard C 執行時間程式庫。</span><span class="sxs-lookup"><span data-stu-id="2e90c-105">The following makefile shows the dependencies among the files needed to compile the client and server applications and link them to the RPC run-time library and the standard C run-time library.</span></span>

<span data-ttu-id="2e90c-106">這個 makefile 可以用來從本教學課程的原始程式碼建立用戶端和伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="2e90c-106">This makefile can be used to build client and server applications from the source code in this tutorial.</span></span> <span data-ttu-id="2e90c-107">此處顯示的存根和標頭是以 MIDL 2.0 版產生的。</span><span class="sxs-lookup"><span data-stu-id="2e90c-107">The stubs and headers shown here were generated with MIDL version 2.0.</span></span> <span data-ttu-id="2e90c-108">編譯器和連結器命令和引數可能會因您的電腦設定而有所不同。</span><span class="sxs-lookup"><span data-stu-id="2e90c-108">The compiler and linker commands and arguments may be different for your computer configuration.</span></span> <span data-ttu-id="2e90c-109">如需詳細資訊，請參閱編譯器的檔。</span><span class="sxs-lookup"><span data-stu-id="2e90c-109">See your compiler documentation for more information.</span></span>

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

 

 




