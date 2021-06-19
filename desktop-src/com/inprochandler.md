---
title: InprocHandler
description: InprocHandler 指定應用程式是否在 HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID 登錄機碼中使用自訂處理常式。
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- InprocHandler 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404731"
---
# <a name="inprochandler"></a><span data-ttu-id="5a196-104">InprocHandler</span><span class="sxs-lookup"><span data-stu-id="5a196-104">InprocHandler</span></span>

<span data-ttu-id="5a196-105">指定應用程式是否使用自訂處理常式。</span><span class="sxs-lookup"><span data-stu-id="5a196-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5a196-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="5a196-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="5a196-107">備註</span><span class="sxs-lookup"><span data-stu-id="5a196-107">Remarks</span></span>

<span data-ttu-id="5a196-108">這是 **REG \_ SZ** 值，可指定應用程式所使用的自訂處理常式。</span><span class="sxs-lookup"><span data-stu-id="5a196-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="5a196-109">如果未使用自訂處理常式，則應該將專案設定為 Ole32.dll。</span><span class="sxs-lookup"><span data-stu-id="5a196-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="5a196-110">如果容器正在搜尋自訂處理常式的登錄，16位版本的優先順序會和16位容器相同，且32位版本的優先順序會與32位容器相同。</span><span class="sxs-lookup"><span data-stu-id="5a196-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a196-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a196-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a196-112">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="5a196-112">**InprocHandler32**</span></span>](inprochandler32.md)
</dt> </dl>

 

 




