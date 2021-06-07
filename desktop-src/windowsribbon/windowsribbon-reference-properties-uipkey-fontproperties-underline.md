---
title: UI_PKEY_FontProperties_Underline
description: 識別 UI \_ PKEY \_ FontProperties 底線 \_ 屬性。
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066027e5f62416667619937eea7dbe493a3ff279
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443779"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="c9a20-103">UI \_ PKEY \_ FontProperties \_ 波浪線</span><span class="sxs-lookup"><span data-stu-id="c9a20-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="c9a20-104">識別 UI \_ PKEY \_ FontProperties 底線 \_ 屬性。</span><span class="sxs-lookup"><span data-stu-id="c9a20-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="c9a20-105">備註</span><span class="sxs-lookup"><span data-stu-id="c9a20-105">Remarks</span></span>

<span data-ttu-id="c9a20-106">\_ \_ \_ 應用程式會使用 UI PKEY FontProperties 底線來查詢底線按鈕的狀態。 </span><span class="sxs-lookup"><span data-stu-id="c9a20-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="c9a20-107">屬性值來自 [**UI \_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) 列舉。</span><span class="sxs-lookup"><span data-stu-id="c9a20-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="c9a20-108">預設值是 `UI_FONTUNDERLINE_NOTSET`。</span><span class="sxs-lookup"><span data-stu-id="c9a20-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="c9a20-109">下列螢幕擷取畫面顯示功能區 [**FontControl**](windowsribbon-element-fontcontrol.md)**的底線按鈕。**</span><span class="sxs-lookup"><span data-stu-id="c9a20-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![fontcontrol 專案的螢幕擷取畫面，其中 richfont 屬性設定為 true。](images/markup/fontcontrol-underline.png)

<span data-ttu-id="c9a20-111">下表描述屬性和 UI 結果。</span><span class="sxs-lookup"><span data-stu-id="c9a20-111">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="c9a20-112">屬性</span><span class="sxs-lookup"><span data-stu-id="c9a20-112">Property</span></span>                   |       <span data-ttu-id="c9a20-113">UI 結果</span><span class="sxs-lookup"><span data-stu-id="c9a20-113">UI Result</span></span>                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="c9a20-114">底線 **按鈕已** 停用，而且只能由應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="c9a20-114">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="c9a20-115">未選取 [底線 **] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="c9a20-115">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="c9a20-116">已選取 [底線 **] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="c9a20-116">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="c9a20-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="c9a20-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9a20-118">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="c9a20-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="c9a20-119">**UI \_ FONTUNDERLINE**</span><span class="sxs-lookup"><span data-stu-id="c9a20-119">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="c9a20-120">字型控制項</span><span class="sxs-lookup"><span data-stu-id="c9a20-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 