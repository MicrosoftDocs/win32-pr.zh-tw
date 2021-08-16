---
title: UI_PKEY_StandardColors
description: 識別 UI \_ PKEY \_ StandardColors 屬性。
ms.assetid: fbdce7ba-4417-4f7f-928b-fba6af6eb396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2dd46462e9a123b0a8c64c3fd06fdfbc6ccbe3aa35274505dc4722dd2a40e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850069"
---
# <a name="ui_pkey_standardcolors"></a>UI \_ PKEY \_ StandardColors

識別 UI \_ PKEY \_ StandardColors 屬性。

```
propertyDescription
   name = UI_PKEY_StandardColors
   shellPKey = UI_PKEY_StandardColors
   formatID = 00000410-7363-696e-8441798acf5aebb7
   propID = 410
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 UI PKEY StandardColors 來查詢 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)的色彩樣本值。

無論針對 **ColorTemplate** 屬性指定的值為何，每個 [COLORREF](../gdi/colorref.md)值都會對應至 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)中的色彩樣本。

屬性值是 [COLORREF](../gdi/colorref.md) 值的陣列。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[色彩選擇器屬性](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 