---
title: MiscStatus
description: 指定如何建立和顯示物件。
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- MiscStatus 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021676"
---
# <a name="miscstatus"></a><span data-ttu-id="d7f2d-104">MiscStatus</span><span class="sxs-lookup"><span data-stu-id="d7f2d-104">MiscStatus</span></span>

<span data-ttu-id="d7f2d-105">指定如何建立和顯示物件。</span><span class="sxs-lookup"><span data-stu-id="d7f2d-105">Specifies how to create and display an object.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d7f2d-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="d7f2d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a><span data-ttu-id="d7f2d-107">備註</span><span class="sxs-lookup"><span data-stu-id="d7f2d-107">Remarks</span></span>

<span data-ttu-id="d7f2d-108">如需詳細資訊，請參閱 [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) 列舉和 [**IOleObject：： GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)。</span><span class="sxs-lookup"><span data-stu-id="d7f2d-108">For more information, see the [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) enumeration and [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span></span>

<span data-ttu-id="d7f2d-109">如果找不到對應至 >DVASPECT 的子機碼，則會使用 **MiscStatus** 的預設值。</span><span class="sxs-lookup"><span data-stu-id="d7f2d-109">If no subkey that corresponds to a DVASPECT is found, the default value of **MiscStatus** is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7f2d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7f2d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7f2d-111">**IOleObject::GetMiscStatus**</span><span class="sxs-lookup"><span data-stu-id="d7f2d-111">**IOleObject::GetMiscStatus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




