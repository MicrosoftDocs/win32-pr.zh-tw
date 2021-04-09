---
title: UI_PKEY_StandardColorsCategoryLabel
description: 識別 UI \_ PKEY \_ StandardColorsCategoryLabel 屬性。
ms.assetid: 59452d4b-acc9-4a5f-a06c-a67b0e676a57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcaecc19213ab82ebafaa76dc2e88a0db836a97a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674216"
---
# <a name="ui_pkey_standardcolorscategorylabel"></a><span data-ttu-id="ef905-103">UI \_ PKEY \_ StandardColorsCategoryLabel</span><span class="sxs-lookup"><span data-stu-id="ef905-103">UI\_PKEY\_StandardColorsCategoryLabel</span></span>

<span data-ttu-id="ef905-104">識別 UI \_ PKEY \_ StandardColorsCategoryLabel 屬性。</span><span class="sxs-lookup"><span data-stu-id="ef905-104">Identifies the UI\_PKEY\_StandardColorsCategoryLabel property.</span></span>

```
propertyDescription
   name = UI_PKEY_StandardColorsCategoryLabel
   shellPKey = UI_PKEY_StandardColorsCategoryLabel
   formatID = 00000404-7363-696e-8441798acf5aebb7
   propID = 404
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="ef905-105">備註</span><span class="sxs-lookup"><span data-stu-id="ef905-105">Remarks</span></span>

<span data-ttu-id="ef905-106">\_ \_ 應用程式會使用 UI PKEY StandardColorsCategoryLabel 來查詢與 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)之 **標準色彩** 分類相關聯的標籤值。</span><span class="sxs-lookup"><span data-stu-id="ef905-106">UI\_PKEY\_StandardColorsCategoryLabel is used by an application to query the value of the label associated with the **Standard Colors** category of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="ef905-107">UI \_ PKEY \_ StandardColorsCategoryLabel 只適用于 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) ，其中 `ThemeColors` 指定為 **ColorTemplate** 屬性的值 (這是唯一包含加上標籤之類別) 的範本。</span><span class="sxs-lookup"><span data-stu-id="ef905-107">UI\_PKEY\_StandardColorsCategoryLabel is valid only for a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute (this is the only template that contains labeled categories).</span></span>

<span data-ttu-id="ef905-108">下列螢幕擷取畫面顯示 `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)。</span><span class="sxs-lookup"><span data-stu-id="ef905-108">The following screen shot shows a `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

![dropdowncolorpicker 專案的螢幕擷取畫面，其中 colortemplate 屬性設定為 themecolors。](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a><span data-ttu-id="ef905-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef905-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef905-111">色彩選擇器屬性</span><span class="sxs-lookup"><span data-stu-id="ef905-111">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




