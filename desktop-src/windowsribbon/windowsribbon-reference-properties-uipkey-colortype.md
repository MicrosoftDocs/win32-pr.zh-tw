---
title: UI_PKEY_ColorType
description: 識別 UI \_ PKEY \_ ColorType 屬性。
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315700"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="a752c-103">UI \_ PKEY \_ ColorType</span><span class="sxs-lookup"><span data-stu-id="a752c-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="a752c-104">識別 UI \_ PKEY \_ ColorType 屬性。</span><span class="sxs-lookup"><span data-stu-id="a752c-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="a752c-105">備註</span><span class="sxs-lookup"><span data-stu-id="a752c-105">Remarks</span></span>

<span data-ttu-id="a752c-106">\_ \_ 應用程式會使用 UI PKEY ColorType 來查詢 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)控制項的色彩設定。</span><span class="sxs-lookup"><span data-stu-id="a752c-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="a752c-107">屬性值來自 [**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) 列舉。</span><span class="sxs-lookup"><span data-stu-id="a752c-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a752c-108">UI \_ SWATCHCOLORTYPE \_ NOCOLOR</span><span class="sxs-lookup"><span data-stu-id="a752c-108">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="a752c-109">應用程式應該將色彩設定視為透明。</span><span class="sxs-lookup"><span data-stu-id="a752c-109">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="a752c-110">通常與 [ **無色彩** 色彩] 設定搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a752c-110">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="a752c-111">UI \_ SWATCHCOLORTYPE \_ 自動</span><span class="sxs-lookup"><span data-stu-id="a752c-111">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="a752c-112">應用程式應該查詢 [GetSysColor (COLOR \_ WINDOWTEXT) ](/windows/win32/api/winuser/nf-winuser-getsyscolor)。</span><span class="sxs-lookup"><span data-stu-id="a752c-112">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="a752c-113">通常與 **自動** 色彩設定一起使用。</span><span class="sxs-lookup"><span data-stu-id="a752c-113">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="a752c-114">UI \_ SWATCHCOLORTYPE \_ RGB</span><span class="sxs-lookup"><span data-stu-id="a752c-114">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="a752c-115">應用程式應該查詢色彩設定的 [UI \_ PKEY \_ 色彩](windowsribbon-reference-properties-uipkey-color.md) 。</span><span class="sxs-lookup"><span data-stu-id="a752c-115">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="a752c-116">\_ \_ 在 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)中選取色彩樣本時，UI PKEY ColorType 會傳遞至 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)回呼方法。</span><span class="sxs-lookup"><span data-stu-id="a752c-116">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a752c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a752c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a752c-118">色彩選擇器屬性</span><span class="sxs-lookup"><span data-stu-id="a752c-118">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 