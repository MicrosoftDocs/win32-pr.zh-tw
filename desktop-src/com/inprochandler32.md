---
title: InprocHandler32
description: 指定應用程式是否使用自訂處理常式。
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- InprocHandler32 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c918669aa3de1c8cf2622e3caf4acc9ae18f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371964"
---
# <a name="inprochandler32"></a><span data-ttu-id="543ad-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="543ad-104">InprocHandler32</span></span>

<span data-ttu-id="543ad-105">指定應用程式是否使用自訂處理常式。</span><span class="sxs-lookup"><span data-stu-id="543ad-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="543ad-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="543ad-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="543ad-107">備註</span><span class="sxs-lookup"><span data-stu-id="543ad-107">Remarks</span></span>

<span data-ttu-id="543ad-108">這是 **REG \_ SZ** 值，可指定應用程式所使用的自訂處理常式。</span><span class="sxs-lookup"><span data-stu-id="543ad-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="543ad-109">如果未使用自訂處理常式，則應該將專案設定為 Ole32.dll。</span><span class="sxs-lookup"><span data-stu-id="543ad-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="543ad-110">如果容器正在搜尋自訂處理常式的登錄，16位版本的優先順序會和16位容器相同，且32位版本的優先順序會與32位容器相同。</span><span class="sxs-lookup"><span data-stu-id="543ad-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="543ad-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="543ad-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="543ad-112">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="543ad-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




