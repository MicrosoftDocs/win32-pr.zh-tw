---
title: UI_PKEY_FontProperties_BackgroundColorType
description: 識別 UI \_ PKEY \_ FontProperties \_ BackgroundColorType 屬性。
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463220"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="6277c-103">UI \_ PKEY \_ FontProperties \_ BackgroundColorType</span><span class="sxs-lookup"><span data-stu-id="6277c-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="6277c-104">識別 UI \_ PKEY \_ FontProperties \_ BackgroundColorType 屬性。</span><span class="sxs-lookup"><span data-stu-id="6277c-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="6277c-105">備註</span><span class="sxs-lookup"><span data-stu-id="6277c-105">Remarks</span></span>

<span data-ttu-id="6277c-106">UI \_ PKEY \_ FontProperties \_ BackgroundColorType 是由應用程式搭配 [ui \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)使用，以查詢 **文字反白顯示色彩** 圖庫的設定。</span><span class="sxs-lookup"><span data-stu-id="6277c-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="6277c-107">屬性值來自 [**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) 列舉。</span><span class="sxs-lookup"><span data-stu-id="6277c-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="6277c-108">預設值是 `UI_SWATCHCOLORTYPE_RGB`。</span><span class="sxs-lookup"><span data-stu-id="6277c-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="6277c-109">下表描述屬性值。</span><span class="sxs-lookup"><span data-stu-id="6277c-109">The following table describes the property values.</span></span>



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="6277c-110">應用程式應該針對色彩值查詢適當的系統計量，通常是以 GetSysColor (色彩視窗) 抓取的目前 Windows 主題 **視窗背景色彩** \_ 。</span><span class="sxs-lookup"><span data-stu-id="6277c-110">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="6277c-111">[**FontControl**](windowsribbon-element-fontcontrol.md)不支援。</span><span class="sxs-lookup"><span data-stu-id="6277c-111">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="6277c-112">應用程式應該查詢 [UI \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) 的色彩值。</span><span class="sxs-lookup"><span data-stu-id="6277c-112">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="6277c-113">[UI \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)的色彩值會顯示在 [文字 **反白顯示色彩**] 按鈕上，並在 [**文字反白顯示色彩**] 圖庫中選取。</span><span class="sxs-lookup"><span data-stu-id="6277c-113">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="6277c-114">\_當您 \_ \_ 在 [**FontControl**](windowsribbon-element-fontcontrol.md) **文字反白顯示色彩** 圖庫中選取色彩樣本時，UI PKEY FontProperties BackgroundColorType 會傳遞至 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)回呼方法。</span><span class="sxs-lookup"><span data-stu-id="6277c-114">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="6277c-115">強烈建議應用程式只設定初始 **文字反白顯示色彩** 值，而不會在資料指標在檔內重新置放時重新設定此值。</span><span class="sxs-lookup"><span data-stu-id="6277c-115">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="6277c-116">最後一個選取專案應維持不變，以避免需要重新選取所需的色彩。</span><span class="sxs-lookup"><span data-stu-id="6277c-116">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6277c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="6277c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6277c-118">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="6277c-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="6277c-119">**UI \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="6277c-119">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="6277c-120">字型控制項</span><span class="sxs-lookup"><span data-stu-id="6277c-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

