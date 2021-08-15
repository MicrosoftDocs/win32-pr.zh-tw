---
title: UI_PKEY_RecentColorsCategoryLabel
description: 識別 UI \_ PKEY \_ RecentColorsCategoryLabel 屬性。
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f3a7a513afb50f01ee3a03c3a3240a2eae7a6ed7b6b8228c4a49e7343e052e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031470"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a>UI \_ PKEY \_ RecentColorsCategoryLabel

識別 UI \_ PKEY \_ RecentColorsCategoryLabel 屬性。

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 UI PKEY RecentColorsCategoryLabel 來查詢與 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)**最新色彩** 分類相關聯的標籤值。

UI \_ PKEY \_ RecentColorsCategoryLabel 只適用于 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) ，其中 `ThemeColors` 指定為 **ColorTemplate** 屬性的值 (這是唯一包含加上標籤之類別) 的範本。

下列螢幕擷取畫面顯示 `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)。

![dropdowncolorpicker 專案的螢幕擷取畫面，其中 colortemplate 屬性設定為 themecolors。](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[色彩選擇器屬性](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




