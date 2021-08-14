---
title: UI_PKEY_FontProperties_Family
description: 識別 UI \_ PKEY \_ FontProperties \_ 系列屬性。
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0574ea4fb104cff29b58c8b1f649bd9287672acef677e3ea4cdc6ad5f91367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438657"
---
# <a name="ui_pkey_fontproperties_family"></a>UI \_ PKEY \_ FontProperties \_ 系列

識別 UI \_ PKEY \_ FontProperties \_ 系列屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>備註

\_ \_ \_ 應用程式會使用 UI PKEY FontProperties 系列來查詢 [**字型家族**] 下拉式清單庫的值。

UI \_ PKEY \_ FontProperties 系列的值 \_ 符合使用[>enumfontfamilies 函數](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa)或[EnumFontFamiliesEx 函數](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)抓取的[Windows GDI 字型系列](../gdi/font-families.md)名稱。

預設值為空字串。

如果為 UI PKEY FontProperties 系列的值提供空字串 \_ \_ ，則 \_ 會清除字型選取範圍。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 