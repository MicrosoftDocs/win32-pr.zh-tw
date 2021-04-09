---
title: InprocServer
description: 指定同進程伺服器 DLL 的路徑。
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932201"
---
# <a name="inprocserver"></a><span data-ttu-id="bc688-104">InprocServer</span><span class="sxs-lookup"><span data-stu-id="bc688-104">InprocServer</span></span>

<span data-ttu-id="bc688-105">指定同進程伺服器 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="bc688-105">Specifies the path to the in-process server DLL.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="bc688-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="bc688-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a><span data-ttu-id="bc688-107">備註</span><span class="sxs-lookup"><span data-stu-id="bc688-107">Remarks</span></span>

<span data-ttu-id="bc688-108">**InprocServer** 專案對可插入的類別而言相當罕見。</span><span class="sxs-lookup"><span data-stu-id="bc688-108">The **InprocServer** entry is relatively rare for insertable classes.</span></span>

<span data-ttu-id="bc688-109">同進程伺服器目前使用 **InprocServer** 登錄專案註冊。</span><span class="sxs-lookup"><span data-stu-id="bc688-109">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="bc688-110">32位和64位的同進程伺服器應該使用 [**InprocServer32**](inprocserver32.md) 專案。</span><span class="sxs-lookup"><span data-stu-id="bc688-110">The 32-bit and 64-bit in-process servers should use the [**InprocServer32**](inprocserver32.md) entry.</span></span> <span data-ttu-id="bc688-111">如果容器正在搜尋內含式伺服器的登錄，16位版本的優先順序會是16位容器，而32位版本的優先順序會與32位容器相同。</span><span class="sxs-lookup"><span data-stu-id="bc688-111">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc688-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc688-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc688-113">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="bc688-113">**InprocServer32**</span></span>](inprocserver32.md)
</dt> </dl>

 

 




