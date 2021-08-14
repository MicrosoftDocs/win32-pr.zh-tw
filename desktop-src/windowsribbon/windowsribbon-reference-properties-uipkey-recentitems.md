---
title: UI_PKEY_RecentItems
description: 識別 UI \_ PKEY \_ RecentItems 屬性。
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04e18400f297edae1f9a1eda54bccbcd6c31c9f1d9b40408e243b6c275a83ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437954"
---
# <a name="ui_pkey_recentitems"></a>UI \_ PKEY \_ RecentItems

識別 UI \_ PKEY \_ RecentItems 屬性。

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a>備註

[UI \_應用 \_ ](windowsribbon-reference-properties-uipkey-pinned.md) 程式會使用 PKEY 釘選來查詢 [應用程式功能表](windowsribbon-controls-applicationmenu.md)的最近使用 (MRU) items 集合中的專案陣列。 每個 MRU 專案的資訊封裝在 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) 物件中，並包含下列三個屬性索引鍵：

-   [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)
-   [UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [UI \_ PKEY \_ 釘選](windowsribbon-reference-properties-uipkey-pinned.md)

MRU 專案的清單會以 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)指標的形式傳遞至功能區主機應用程式，以供主應用程式 **中的個別** 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[狀態屬性](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 