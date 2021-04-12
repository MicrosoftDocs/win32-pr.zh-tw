---
title: UI_PKEY_ThemeColors
description: 識別 UI \_ PKEY \_ ThemeColors 屬性。
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5991ce5058de5a6f49ca8929de02e19657a610
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315358"
---
# <a name="ui_pkey_themecolors"></a>UI \_ PKEY \_ ThemeColors

識別 UI \_ PKEY \_ ThemeColors 屬性。

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 UI PKEY ThemeColors 來查詢 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)的色彩樣本值。

每個 [COLORREF](../gdi/colorref.md) 值會對應至 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) 中的色彩樣本，其中 `ThemeColors` 指定為 **ColorTemplate** 屬性的值。

屬性值是 [COLORREF](../gdi/colorref.md) 值的陣列。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[色彩選擇器屬性](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 