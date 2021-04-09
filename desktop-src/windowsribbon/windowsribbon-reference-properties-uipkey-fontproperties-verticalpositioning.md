---
title: UI_PKEY_FontProperties_VerticalPositioning
description: 識別 UI \_ PKEY \_ FontProperties \_ VerticalPositioning 屬性。
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b67e2a099b7ce02b3c94f7c9d799fcdda5e881
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023944"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a><span data-ttu-id="f7852-103">UI \_ PKEY \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="f7852-103">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>

<span data-ttu-id="f7852-104">識別 UI \_ PKEY \_ FontProperties \_ VerticalPositioning 屬性。</span><span class="sxs-lookup"><span data-stu-id="f7852-104">Identifies the UI\_PKEY\_FontProperties\_VerticalPositioning property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a><span data-ttu-id="f7852-105">備註</span><span class="sxs-lookup"><span data-stu-id="f7852-105">Remarks</span></span>

<span data-ttu-id="f7852-106">UI \_ PKEY \_ FontProperties \_ VerticalPositioning 是由應用程式用來查詢 **上標** 和 **下標** 控制項的值。</span><span class="sxs-lookup"><span data-stu-id="f7852-106">UI\_PKEY\_FontProperties\_VerticalPositioning is used by an application to query the value of the **Superscript** and **Subscript** controls.</span></span>

<span data-ttu-id="f7852-107">屬性值來自 [**UI \_ FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) 列舉。</span><span class="sxs-lookup"><span data-stu-id="f7852-107">The property value is from the [**UI\_FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) enumeration.</span></span>

<span data-ttu-id="f7852-108">預設值是 `UI_FONTVERTICALPOSITION_NOTSET`。</span><span class="sxs-lookup"><span data-stu-id="f7852-108">The default value is `UI_FONTVERTICALPOSITION_NOTSET`.</span></span>

<span data-ttu-id="f7852-109">下列螢幕擷取畫面顯示功能區 [**FontControl**](windowsribbon-element-fontcontrol.md)的 **上標** 和 **下標** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f7852-109">The following screen shot shows the **Superscript** and **Subscript** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![fontcontrol 專案的螢幕擷取畫面，其中 richfont 屬性設定為 true。](images/markup/fontcontrol-subsuper.png)

<span data-ttu-id="f7852-111">下表描述屬性和 UI 結果。</span><span class="sxs-lookup"><span data-stu-id="f7852-111">The following table describes the properties and the UI result.</span></span>



|                                        |                                                                                                |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | <span data-ttu-id="f7852-112">**上標** 和 **下標** 按鈕已停用，而且只能由應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="f7852-112">**Superscript** and **Subscript** buttons are disabled and can only be set by the application.</span></span> |
| `UI_FONTVERTICALPOSITION_NOTSET`       | <span data-ttu-id="f7852-113">未選取 **上標** 和 **下標** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f7852-113">**Superscript** and **Subscript** buttons are not selected.</span></span>                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | <span data-ttu-id="f7852-114">選取 [**上標**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f7852-114">**Superscript** button is selected.</span></span>                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | <span data-ttu-id="f7852-115">已選取 [注 **標**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f7852-115">**Subscript** button is selected.</span></span>                                                              |



 

> [!Note]  
> <span data-ttu-id="f7852-116">無法同時選取 **上標** 和 **下標** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f7852-116">The **Superscript** and **Subscript** buttons cannot both be selected.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f7852-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7852-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7852-118">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="f7852-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="f7852-119">**UI \_ FONTVERTICALPOSITION**</span><span class="sxs-lookup"><span data-stu-id="f7852-119">**UI\_FONTVERTICALPOSITION**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[<span data-ttu-id="f7852-120">字型控制項</span><span class="sxs-lookup"><span data-stu-id="f7852-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 