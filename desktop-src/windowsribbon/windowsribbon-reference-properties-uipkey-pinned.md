---
title: UI_PKEY_Pinned
description: 識別 UI \_ PKEY \_ 釘選屬性。
ms.assetid: 906b2ab9-1ed7-46a6-88bc-e8f9160ab60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8637f11404090313751647058ee41acbad3d9bf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183813"
---
# <a name="ui_pkey_pinned"></a><span data-ttu-id="71e62-103">UI \_ PKEY \_ 釘選</span><span class="sxs-lookup"><span data-stu-id="71e62-103">UI\_PKEY\_Pinned</span></span>

<span data-ttu-id="71e62-104">識別 UI \_ PKEY \_ 釘選屬性。</span><span class="sxs-lookup"><span data-stu-id="71e62-104">Identifies the UI\_PKEY\_Pinned property.</span></span>

```
propertyDescription
   name = UI_PKEY_Pinned
   shellPKey = UI_PKEY_Pinned
   formatID = 00000351-7363-696e-8441798acf5aebb7
   propID = 351
   typeInfo
      type = VT_BOOL
   booleanFormat
      formatAs = VARIANT_TRUE=-1, VARIANT_FALSE=0
```

## <a name="remarks"></a><span data-ttu-id="71e62-105">備註</span><span class="sxs-lookup"><span data-stu-id="71e62-105">Remarks</span></span>

<span data-ttu-id="71e62-106">\_ \_ 應用程式會使用已釘選的 UI PKEY 來查詢應用程式[功能表](windowsribbon-controls-applicationmenu.md)中的專案是在應用程式實例之間「釘選」還是持續性的。</span><span class="sxs-lookup"><span data-stu-id="71e62-106">UI\_PKEY\_Pinned is used by an application to query whether an item in the [Application Menu](windowsribbon-controls-applicationmenu.md) is "pinned", or persistent, across application instances.</span></span> <span data-ttu-id="71e62-107">例如，最近使用過的 (MRU) items 清單中的專案可供存取，且不會卸載 MRU 專案清單，直到它被「取消固定」為止。</span><span class="sxs-lookup"><span data-stu-id="71e62-107">For example, an item in the most recently used (MRU) items list is accessible and does not drop off the MRU items list until it is "unpinned".</span></span>

## <a name="related-topics"></a><span data-ttu-id="71e62-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="71e62-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71e62-109">狀態屬性</span><span class="sxs-lookup"><span data-stu-id="71e62-109">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> <dt>

[<span data-ttu-id="71e62-110">UI \_ PKEY \_ RecentItems</span><span class="sxs-lookup"><span data-stu-id="71e62-110">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md)
</dt> <dt>

[<span data-ttu-id="71e62-111">最近的項目</span><span class="sxs-lookup"><span data-stu-id="71e62-111">Recent Items</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 




