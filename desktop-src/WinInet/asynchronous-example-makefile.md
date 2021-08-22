---
title: 非同步範例 Makefile
description: 以下是非同步範例應用程式的 makefile。
ms.assetid: 5d5b5578-6a2e-4311-9bf7-9b7818eb23ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45dafe17b360c5b77c1594f5879d93d27dc9d26be1212c035e21f34845ee51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051846"
---
# <a name="asynchronous-example-makefile"></a>非同步範例 Makefile

以下是 [非同步範例應用程式](asynchronous-example-application.md)的 makefile。

``` syntax
#----- Include the SDK's WIN32.MAK to pick up defines-------------------
!include <win32.mak>

all:    $(OUTDIR) $(OUTDIR)\async.exe 

$(OUTDIR)\async.exe:     $(OUTDIR)\async.obj
    $(link) $(ldebug) /OUT:$(OUTDIR)\async.exe $(conlflags) /PDB:$(OUTDIR)\async.pdb /MACHINE:$(CPU) $(OUTDIR)\async.obj wininet.lib $(baselibs)

$(OUTDIR)\async.obj:    async.c
    $(cc) $(cflags) $(cdebug) $(cvars) /EHsc /Fo"$(OUTDIR)\\" /Fd"$(OUTDIR)\\" /D"_CONSOLE" /D"UNICODE" /D"_UNICODE" async.c
        
#----- If OUTDIR does not exist, then create directory
$(OUTDIR) :
    if not exist "$(OUTDIR)/$(NULL)" mkdir $(OUTDIR)

clean:
     $(CLEANUP)
```

 

 




