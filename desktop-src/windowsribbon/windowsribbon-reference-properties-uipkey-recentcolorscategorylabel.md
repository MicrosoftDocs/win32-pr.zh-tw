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
# <a name="ui_pkey_recentcolorscategorylabel"></a><span data-ttu-id="c07bc-103">UI \_ PKEY \_ RecentColorsCategoryLabel</span><span class="sxs-lookup"><span data-stu-id="c07bc-103">UI\_PKEY\_RecentColorsCategoryLabel</span></span>

<span data-ttu-id="c07bc-104">識別 UI \_ PKEY \_ RecentColorsCategoryLabel 屬性。</span><span class="sxs-lookup"><span data-stu-id="c07bc-104">Identifies the UI\_PKEY\_RecentColorsCategoryLabel property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="c07bc-105">備註</span><span class="sxs-lookup"><span data-stu-id="c07bc-105">Remarks</span></span>

<span data-ttu-id="c07bc-106">\_ \_ 應用程式會使用 UI PKEY RecentColorsCategoryLabel 來查詢與 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)**最新色彩** 分類相關聯的標籤值。</span><span class="sxs-lookup"><span data-stu-id="c07bc-106">UI\_PKEY\_RecentColorsCategoryLabel is used by an application to query the value of the label associated with the **Recent Colors** category of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="c07bc-107">UI \_ PKEY \_ RecentColorsCategoryLabel 只適用于 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) ，其中 `ThemeColors` 指定為 **ColorTemplate** 屬性的值 (這是唯一包含加上標籤之類別) 的範本。</span><span class="sxs-lookup"><span data-stu-id="c07bc-107">UI\_PKEY\_RecentColorsCategoryLabel is valid only for a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute (this is the only template that contains labeled categories).</span></span>

<span data-ttu-id="c07bc-108">下列螢幕擷取畫面顯示 `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)。</span><span class="sxs-lookup"><span data-stu-id="c07bc-108">The following screen shot shows a `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

![dropdowncolorpicker 專案的螢幕擷取畫面，其中 colortemplate 屬性設定為 themecolors。](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a><span data-ttu-id="c07bc-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="c07bc-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c07bc-111">色彩選擇器屬性</span><span class="sxs-lookup"><span data-stu-id="c07bc-111">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




