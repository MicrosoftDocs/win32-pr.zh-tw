---
title: UI_PKEY_RecentItems
description: 識別 UI \_ PKEY \_ RecentItems 屬性。
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07410d3152fb49b55460ec15c6914c53f3b6850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967904"
---
# <a name="ui_pkey_recentitems"></a><span data-ttu-id="26150-103">UI \_ PKEY \_ RecentItems</span><span class="sxs-lookup"><span data-stu-id="26150-103">UI\_PKEY\_RecentItems</span></span>

<span data-ttu-id="26150-104">識別 UI \_ PKEY \_ RecentItems 屬性。</span><span class="sxs-lookup"><span data-stu-id="26150-104">Identifies the UI\_PKEY\_RecentItems property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a><span data-ttu-id="26150-105">備註</span><span class="sxs-lookup"><span data-stu-id="26150-105">Remarks</span></span>

<span data-ttu-id="26150-106">[UI \_應用 \_ ](windowsribbon-reference-properties-uipkey-pinned.md) 程式會使用 PKEY 釘選來查詢 [應用程式功能表](windowsribbon-controls-applicationmenu.md)的最近使用 (MRU) items 集合中的專案陣列。</span><span class="sxs-lookup"><span data-stu-id="26150-106">[UI\_PKEY\_Pinned](windowsribbon-reference-properties-uipkey-pinned.md) is used by an application to query the array of items in the most recently used (MRU) items collection of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="26150-107">每個 MRU 專案的資訊封裝在 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) 物件中，並包含下列三個屬性索引鍵：</span><span class="sxs-lookup"><span data-stu-id="26150-107">The information for each MRU item is encapsulated in an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object and includes the following three property keys:</span></span>

-   [<span data-ttu-id="26150-108">UI \_ PKEY \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="26150-108">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
-   [<span data-ttu-id="26150-109">UI \_ PKEY \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="26150-109">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [<span data-ttu-id="26150-110">UI \_ PKEY \_ 釘選</span><span class="sxs-lookup"><span data-stu-id="26150-110">UI\_PKEY\_Pinned</span></span>](windowsribbon-reference-properties-uipkey-pinned.md)

<span data-ttu-id="26150-111">MRU 專案的清單會以 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)指標的形式傳遞至功能區主機應用程式，以供主應用程式 **中的個別** 執行。</span><span class="sxs-lookup"><span data-stu-id="26150-111">The list of MRU items is passed to the Ribbon host application as a **SAFEARRAY** of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pointers to respective implementations in the host application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26150-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="26150-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26150-113">狀態屬性</span><span class="sxs-lookup"><span data-stu-id="26150-113">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 