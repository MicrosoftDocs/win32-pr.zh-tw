---
description: 當呼叫元件的 e 時，建議您在搜尋元件時使用相同的啟用內容。
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: 呼叫元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4742b19ea47e03fac5f7d0318248ea167182e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944468"
---
# <a name="calling-into-assemblies"></a><span data-ttu-id="a172e-103">呼叫元件</span><span class="sxs-lookup"><span data-stu-id="a172e-103">Calling Into Assemblies</span></span>

<span data-ttu-id="a172e-104">當呼叫元件的 e 時，建議您在搜尋元件時使用相同的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="a172e-104">When calling into the entrypoints of an assembly, it is recommended that you use the same activation context that was active when searching for the assembly.</span></span> <span data-ttu-id="a172e-105">至少要確定載入元件的元件不會不慎取得應用程式所使用的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="a172e-105">At minimum, ensure that the component loading the assembly does not accidentally get the activation context your application is using.</span></span> <span data-ttu-id="a172e-106">跨 DLL 界限洩漏啟用內容可能會導致非預期的相依性。</span><span class="sxs-lookup"><span data-stu-id="a172e-106">Leaking activation context across DLL boundaries can lead to unexpected dependencies.</span></span> <span data-ttu-id="a172e-107">如果您的應用程式已啟用隔離感知功能，這就不成問題， \_ \_ 因為在這種情況下，預設不會啟用啟用內容。</span><span class="sxs-lookup"><span data-stu-id="a172e-107">This is not a problem if your application compiles ISOLATION\_AWARE\_ENABLED because in that case no activation context is active by default.</span></span> <span data-ttu-id="a172e-108">如果您未在 \_ 定義啟用隔離感知的情況 \_ 下編譯，則應該啟用 **Null** 啟用內容或用來載入元件的相同啟用內容。</span><span class="sxs-lookup"><span data-stu-id="a172e-108">If you do not compile with ISOLATION\_AWARE\_ENABLED defined, you should activate the **NULL** activation context or the same activation context that was used to load the assembly.</span></span>

<span data-ttu-id="a172e-109">下列範例可確保裝載的 DLL 會在它所辨識的內容中執行：</span><span class="sxs-lookup"><span data-stu-id="a172e-109">The following example ensures that the hosted DLL runs in a context that it recognizes:</span></span>

``` syntax
ULONG_PTR ulpCookie;
ActivateActCtx(hTheActCtxForMyDll, &ulpCookie);
__try 
{
        MyDllIsolatedFunction();
    myDllIsolatedComInterface->Funct();
}
__finally 
{
    DeactivateActCtx(0, ulpCookie);
}
```

 

 



