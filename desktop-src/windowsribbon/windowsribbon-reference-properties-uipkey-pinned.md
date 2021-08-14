---
title: UI_PKEY_Pinned
description: 識別 UI \_ PKEY \_ 釘選屬性。
ms.assetid: 906b2ab9-1ed7-46a6-88bc-e8f9160ab60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f1bfbbab458c12277c3ed881963005f80485b028a5291d42089d1ef431e3954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201483"
---
# <a name="ui_pkey_pinned"></a>UI \_ PKEY \_ 釘選

識別 UI \_ PKEY \_ 釘選屬性。

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

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用已釘選的 UI PKEY 來查詢應用程式[功能表](windowsribbon-controls-applicationmenu.md)中的專案是在應用程式實例之間「釘選」還是持續性的。 例如，最近使用過的 (MRU) items 清單中的專案可供存取，且不會卸載 MRU 專案清單，直到它被「取消固定」為止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[狀態屬性](windowsribbon-reference-properties-state.md)
</dt> <dt>

[UI \_ PKEY \_ RecentItems](windowsribbon-reference-properties-uipkey-recentitems.md)
</dt> <dt>

[最近的項目](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 




