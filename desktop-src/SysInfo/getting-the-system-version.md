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
# <a name="getting-the-system-version"></a><span data-ttu-id="09aaa-103">取得系統版本</span><span class="sxs-lookup"><span data-stu-id="09aaa-103">Getting the System Version</span></span>

<span data-ttu-id="09aaa-104">下列範例會使用 [版本 API](version-helper-apis.md) 協助程式函式來判斷目前作業系統的版本（如果它是伺服器或用戶端版本），然後將這項資訊顯示在主控台中。</span><span class="sxs-lookup"><span data-stu-id="09aaa-104">The following example uses the [Version API Helper functions](version-helper-apis.md) to determine the version of the current operating system, if it is a Server or Client release, and then displays this information to the console.</span></span> <span data-ttu-id="09aaa-105">如果相容性模式有效，此範例會顯示為 [應用程式相容性](/previous-versions/bb757005(v=msdn.10))選取的作業系統。</span><span class="sxs-lookup"><span data-stu-id="09aaa-105">If compatibility mode is in effect, the example displays the operating system selected for [application compatibility](/previous-versions/bb757005(v=msdn.10)).</span></span>

<span data-ttu-id="09aaa-106">依賴版本資訊並不是測試功能的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="09aaa-106">Relying on version information is not the best way to test for a feature.</span></span> <span data-ttu-id="09aaa-107">請改為參考感興趣之功能的檔。</span><span class="sxs-lookup"><span data-stu-id="09aaa-107">Instead, refer to the documentation for the feature of interest.</span></span> <span data-ttu-id="09aaa-108">如需功能偵測常見技術的詳細資訊，請參閱 [作業系統版本](operating-system-version.md)。</span><span class="sxs-lookup"><span data-stu-id="09aaa-108">For more information on common techniques for feature detection, see [Operating System Version](operating-system-version.md).</span></span>


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



 

 
