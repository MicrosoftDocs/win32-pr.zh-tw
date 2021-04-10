---
title: UI_PKEY_RecentColorsCategoryLabel
description: 識別 UI \_ PKEY \_ RecentColorsCategoryLabel 屬性。
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bcb2e3f5df1ba66204a8df6b088ca3a2808ced
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674220"
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

下列螢幕擷取畫面顯示 `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)。

![dropdowncolorpicker 專案的螢幕擷取畫面，其中 colortemplate 屬性設定為 themecolors。](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[色彩選擇器屬性](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




