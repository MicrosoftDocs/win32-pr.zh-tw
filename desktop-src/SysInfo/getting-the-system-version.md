---
description: 下列範例會使用版本 API 協助程式函式來判斷目前作業系統的版本（如果它是伺服器或用戶端版本），然後將這項資訊顯示在主控台中。
ms.assetid: ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a
title: 取得系統版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0fa259378b81f9255846694927ee2b68e6f38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853095"
---
# <a name="getting-the-system-version"></a>取得系統版本

下列範例會使用 [版本 API](version-helper-apis.md) 協助程式函式來判斷目前作業系統的版本（如果它是伺服器或用戶端版本），然後將這項資訊顯示在主控台中。 如果相容性模式有效，此範例會顯示為 [應用程式相容性](/previous-versions/bb757005(v=msdn.10))選取的作業系統。

依賴版本資訊並不是測試功能的最佳方式。 請改為參考感興趣之功能的檔。 如需功能偵測常見技術的詳細資訊，請參閱 [作業系統版本](operating-system-version.md)。


```C++
#include <windows.h>
#include <stdio.h>
#include <VersionHelpers.h>

int 
__cdecl
wmain(
    __in int argc, 
    __in_ecount(argc) PCWSTR argv[]
    )
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

    if (IsWindowsXPOrGreater())
    {
        printf("XPOrGreater\n");
    }

    if (IsWindowsXPSP1OrGreater())
    {
        printf("XPSP1OrGreater\n");
    }

    if (IsWindowsXPSP2OrGreater())
    {
        printf("XPSP2OrGreater\n");
    }

    if (IsWindowsXPSP3OrGreater())
    {
        printf("XPSP3OrGreater\n");
    }

    if (IsWindowsVistaOrGreater())
    {
        printf("VistaOrGreater\n");
    }

    if (IsWindowsVistaSP1OrGreater())
    {
        printf("VistaSP1OrGreater\n");
    }

    if (IsWindowsVistaSP2OrGreater())
    {
        printf("VistaSP2OrGreater\n");
    }

    if (IsWindows7OrGreater())
    {
        printf("Windows7OrGreater\n");
    }

    if (IsWindows7SP1OrGreater())
    {
        printf("Windows7SP1OrGreater\n");
    }

    if (IsWindows8OrGreater())
    {
        printf("Windows8OrGreater\n");
    }

    if (IsWindows8Point1OrGreater())
    {
        printf("Windows8Point1OrGreater\n");
    }

    if (IsWindows10OrGreater())
    {
        printf("Windows10OrGreater\n");
    }

    if (IsWindowsServer())
    {
        printf("Server\n");
    }
    else
    {
        printf("Client\n");
    }
}
```



 

 
