---
title: " (WinNT 提供者的物件 SID) "
description: 您可以使用 objectSID 屬性來抓取使用者安全識別碼 (SID) 。 ObjectSID 會以形成 SID 字串的變異字元陣列形式傳回。
ms.assetid: 15845e6d-ea30-4d6c-9f35-b2abc1a564ba
ms.tgt_platform: multiple
keywords:
- WinNT 提供者 ADSI、使用者管理範例、物件 SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5d47e939770b9584a85e4e628c5c168901fc1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020796"
---
# <a name="object-sid-winnt-provider"></a><span data-ttu-id="6d303-105"> (WinNT 提供者的物件 SID) </span><span class="sxs-lookup"><span data-stu-id="6d303-105">Object SID (WinNT Provider)</span></span>

<span data-ttu-id="6d303-106">您可以使用 **objectSID** 屬性來抓取使用者安全識別碼 (SID) 。</span><span class="sxs-lookup"><span data-stu-id="6d303-106">The user security identifier (SID) can be retrieved using the **objectSID** attribute.</span></span> <span data-ttu-id="6d303-107">**ObjectSID** 會以形成 SID 字串的 **變異** 字元陣列形式傳回。</span><span class="sxs-lookup"><span data-stu-id="6d303-107">The **objectSID** is returned as a **VARIANT** array of characters that form the SID string.</span></span>

## <a name="example-code"></a><span data-ttu-id="6d303-108">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="6d303-108">Example Code</span></span>


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




