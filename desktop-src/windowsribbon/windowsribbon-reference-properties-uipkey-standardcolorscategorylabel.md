---
title: UI_PKEY_StandardColorsCategoryLabel
description: 識別 UI \_ PKEY \_ StandardColorsCategoryLabel 屬性。
ms.assetid: 59452d4b-acc9-4a5f-a06c-a67b0e676a57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4301fe8874ef4eb3fae0ad931114a7ed305cbc4893ad12c58cf182babe8a16c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437919"
---
# <a name="ui_pkey_standardcolorscategorylabel"></a>UI \_ PKEY \_ StandardColorsCategoryLabel

識別 UI \_ PKEY \_ StandardColorsCategoryLabel 屬性。

```
propertyDescription
   name = UI_PKEY_StandardColorsCategoryLabel
   shellPKey = UI_PKEY_StandardColorsCategoryLabel
   formatID = 00000404-7363-696e-8441798acf5aebb7
   propID = 404
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 UI PKEY StandardColorsCategoryLabel 來查詢與 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)之 **標準色彩** 分類相關聯的標籤值。

UI \_ PKEY \_ StandardColorsCategoryLabel 只適用于 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) ，其中 `ThemeColors` 指定為 **ColorTemplate** 屬性的值 (這是唯一包含加上標籤之類別) 的範本。

下列螢幕擷取畫面顯示 `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)。

![dropdowncolorpicker 專案的螢幕擷取畫面，其中 colortemplate 屬性設定為 themecolors。](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[色彩選擇器屬性](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




