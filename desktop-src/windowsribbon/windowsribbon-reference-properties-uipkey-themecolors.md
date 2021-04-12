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
# <a name="ui_pkey_themecolors"></a><span data-ttu-id="7dc4d-103">UI \_ PKEY \_ ThemeColors</span><span class="sxs-lookup"><span data-stu-id="7dc4d-103">UI\_PKEY\_ThemeColors</span></span>

<span data-ttu-id="7dc4d-104">識別 UI \_ PKEY \_ ThemeColors 屬性。</span><span class="sxs-lookup"><span data-stu-id="7dc4d-104">Identifies the UI\_PKEY\_ThemeColors property.</span></span>

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a><span data-ttu-id="7dc4d-105">備註</span><span class="sxs-lookup"><span data-stu-id="7dc4d-105">Remarks</span></span>

<span data-ttu-id="7dc4d-106">\_ \_ 應用程式會使用 UI PKEY ThemeColors 來查詢 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)的色彩樣本值。</span><span class="sxs-lookup"><span data-stu-id="7dc4d-106">UI\_PKEY\_ThemeColors is used by an application to query the color swatch values of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="7dc4d-107">每個 [COLORREF](../gdi/colorref.md) 值會對應至 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) 中的色彩樣本，其中 `ThemeColors` 指定為 **ColorTemplate** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="7dc4d-107">Each [COLORREF](../gdi/colorref.md) value corresponds to a color swatch in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute.</span></span>

<span data-ttu-id="7dc4d-108">屬性值是 [COLORREF](../gdi/colorref.md) 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="7dc4d-108">The property value is an array of [COLORREF](../gdi/colorref.md) values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dc4d-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="7dc4d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dc4d-110">色彩選擇器屬性</span><span class="sxs-lookup"><span data-stu-id="7dc4d-110">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 