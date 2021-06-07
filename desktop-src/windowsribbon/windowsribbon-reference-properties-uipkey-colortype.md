---
title: UI_PKEY_ColorType
description: 識別 UI \_ PKEY \_ ColorType 屬性。
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443889"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="47fe8-103">UI \_ PKEY \_ ColorType</span><span class="sxs-lookup"><span data-stu-id="47fe8-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="47fe8-104">識別 UI \_ PKEY \_ ColorType 屬性。</span><span class="sxs-lookup"><span data-stu-id="47fe8-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="47fe8-105">備註</span><span class="sxs-lookup"><span data-stu-id="47fe8-105">Remarks</span></span>

<span data-ttu-id="47fe8-106">\_ \_ 應用程式會使用 UI PKEY ColorType 來查詢 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)控制項的色彩設定。</span><span class="sxs-lookup"><span data-stu-id="47fe8-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="47fe8-107">屬性值來自 [**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) 列舉。</span><span class="sxs-lookup"><span data-stu-id="47fe8-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|    <span data-ttu-id="47fe8-108">屬性</span><span class="sxs-lookup"><span data-stu-id="47fe8-108">Property</span></span>                            |    <span data-ttu-id="47fe8-109">描述</span><span class="sxs-lookup"><span data-stu-id="47fe8-109">Description</span></span>                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47fe8-110">UI \_ SWATCHCOLORTYPE \_ NOCOLOR</span><span class="sxs-lookup"><span data-stu-id="47fe8-110">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="47fe8-111">應用程式應該將色彩設定視為透明。</span><span class="sxs-lookup"><span data-stu-id="47fe8-111">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="47fe8-112">通常與 [ **無色彩** 色彩] 設定搭配使用。</span><span class="sxs-lookup"><span data-stu-id="47fe8-112">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="47fe8-113">UI \_ SWATCHCOLORTYPE \_ 自動</span><span class="sxs-lookup"><span data-stu-id="47fe8-113">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="47fe8-114">應用程式應該查詢 [GetSysColor (COLOR \_ WINDOWTEXT) ](/windows/win32/api/winuser/nf-winuser-getsyscolor)。</span><span class="sxs-lookup"><span data-stu-id="47fe8-114">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="47fe8-115">通常與 **自動** 色彩設定一起使用。</span><span class="sxs-lookup"><span data-stu-id="47fe8-115">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="47fe8-116">UI \_ SWATCHCOLORTYPE \_ RGB</span><span class="sxs-lookup"><span data-stu-id="47fe8-116">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="47fe8-117">應用程式應該查詢色彩設定的 [UI \_ PKEY \_ 色彩](windowsribbon-reference-properties-uipkey-color.md) 。</span><span class="sxs-lookup"><span data-stu-id="47fe8-117">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="47fe8-118">\_ \_ 在 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)中選取色彩樣本時，UI PKEY ColorType 會傳遞至 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)回呼方法。</span><span class="sxs-lookup"><span data-stu-id="47fe8-118">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="47fe8-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="47fe8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47fe8-120">色彩選擇器屬性</span><span class="sxs-lookup"><span data-stu-id="47fe8-120">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 