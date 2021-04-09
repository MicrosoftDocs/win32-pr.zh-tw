---
description: 下列 Winternl 定義是作用中終端機服務主控台會話識別碼的靜態記憶體位址。 此使用中的主控台會話識別碼並非在 Windows XP 之前的 Microsoft Windows 作業系統版本中定義。
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: 取得使用中的主控台會話識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936db3f8038348864fc90fc55eeb4287a67c45d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847230"
---
# <a name="getting-the-active-console-session-id"></a><span data-ttu-id="b2026-104">取得使用中的主控台會話識別碼</span><span class="sxs-lookup"><span data-stu-id="b2026-104">Getting the Active Console Session ID</span></span>

<span data-ttu-id="b2026-105">下列 Winternl 定義是作用中終端機服務主控台會話識別碼的靜態記憶體位址。</span><span class="sxs-lookup"><span data-stu-id="b2026-105">The following Winternl.h definition is the static memory address of the active Terminal Services console session ID.</span></span> <span data-ttu-id="b2026-106">此使用中的主控台會話識別碼並非在 Windows XP 之前的 Microsoft Windows 作業系統版本中定義。</span><span class="sxs-lookup"><span data-stu-id="b2026-106">This active console session ID is not defined in versions of the Microsoft Windows operating system earlier than Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="b2026-107">這項定義在未來的 Windows 版本中可能會變更。</span><span class="sxs-lookup"><span data-stu-id="b2026-107">This definition may change in future releases of Windows.</span></span> <span data-ttu-id="b2026-108">為確保您的應用程式會在未來繼續正常執行，您的應用程式必須呼叫 [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid)。</span><span class="sxs-lookup"><span data-stu-id="b2026-108">To ensure that your application will continue to run correctly in the future, your application must call [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span></span>

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
