---
title: UI_PKEY_FontProperties_ForegroundColorType
description: 識別 UI \_ PKEY \_ FontProperties \_ ForegroundColorType 屬性。
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f261256a36ee7a387c6c3a695d8c1182898690c2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444349"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a><span data-ttu-id="715e5-103">UI \_ PKEY \_ FontProperties \_ ForegroundColorType</span><span class="sxs-lookup"><span data-stu-id="715e5-103">UI\_PKEY\_FontProperties\_ForegroundColorType</span></span>

<span data-ttu-id="715e5-104">識別 UI \_ PKEY \_ FontProperties \_ ForegroundColorType 屬性。</span><span class="sxs-lookup"><span data-stu-id="715e5-104">Identifies the UI\_PKEY\_FontProperties\_ForegroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="715e5-105">備註</span><span class="sxs-lookup"><span data-stu-id="715e5-105">Remarks</span></span>

<span data-ttu-id="715e5-106">UI \_ PKEY \_ FontProperties \_ ForegroundColorType 是由應用程式搭配 [ui \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md)用來查詢 **文字顏色** 庫設定。</span><span class="sxs-lookup"><span data-stu-id="715e5-106">UI\_PKEY\_FontProperties\_ForegroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), to query **Text color** gallery settings.</span></span>

<span data-ttu-id="715e5-107">屬性值來自 [**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) 列舉。</span><span class="sxs-lookup"><span data-stu-id="715e5-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="715e5-108">預設值是 `UI_SWATCHCOLORTYPE_RGB`。</span><span class="sxs-lookup"><span data-stu-id="715e5-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="715e5-109">下表描述屬性值。</span><span class="sxs-lookup"><span data-stu-id="715e5-109">The following table describes the property values.</span></span>



|     <span data-ttu-id="715e5-110">值</span><span class="sxs-lookup"><span data-stu-id="715e5-110">Value</span></span>                           |     <span data-ttu-id="715e5-111">描述</span><span class="sxs-lookup"><span data-stu-id="715e5-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="715e5-112">[**FontControl**](windowsribbon-element-fontcontrol.md)不支援。</span><span class="sxs-lookup"><span data-stu-id="715e5-112">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="715e5-113">應用程式應該針對色彩值查詢適當的系統計量，通常是以 GetSysColor (COLOR WINDOWTEXT) 抓取的目前 Windows 主題 **文字色彩** \_ 。</span><span class="sxs-lookup"><span data-stu-id="715e5-113">Application should query the appropriate system metric for the color value typically the current Windows theme **text color** that is retrieved with GetSysColor(COLOR\_WINDOWTEXT).</span></span>                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="715e5-114">應用程式應該查詢 [UI \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) 的色彩值。</span><span class="sxs-lookup"><span data-stu-id="715e5-114">Application should query [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) for the color value.</span></span> <span data-ttu-id="715e5-115">[ [UI \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) ] 的色彩值會顯示在 **[文字色彩] 按鈕中** ，並在 [ **文字色彩** ] 圖庫中選取。</span><span class="sxs-lookup"><span data-stu-id="715e5-115">The color value of [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) is displayed on the **Text color** button and selected in the **Text color** gallery.</span></span><br/> |



 

<span data-ttu-id="715e5-116">\_ \_ \_ 當在 [**FontControl**](windowsribbon-element-fontcontrol.md) **文字色彩** 圖庫中選取色彩樣本時，UI PKEY FontProperties ForegroundColorType 會傳遞至 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)回呼方法。</span><span class="sxs-lookup"><span data-stu-id="715e5-116">UI\_PKEY\_FontProperties\_ForegroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="715e5-117">強烈建議應用程式只設定初始 **文字色彩** 值，而且不會在資料指標在檔內重新置放時重新設定此值。</span><span class="sxs-lookup"><span data-stu-id="715e5-117">It is highly recommended that the application only set an initial **Text color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="715e5-118">最後一個選取專案應維持不變，以避免需要重新選取所需的色彩。</span><span class="sxs-lookup"><span data-stu-id="715e5-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="715e5-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="715e5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="715e5-120">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="715e5-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="715e5-121">**UI \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="715e5-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="715e5-122">字型控制項</span><span class="sxs-lookup"><span data-stu-id="715e5-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

