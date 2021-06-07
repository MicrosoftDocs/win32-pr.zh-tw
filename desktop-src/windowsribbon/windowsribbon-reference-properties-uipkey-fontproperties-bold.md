---
title: UI_PKEY_FontProperties_Bold
description: 識別 UI \_ PKEY \_ FontProperties \_ Bold 屬性。
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444379"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="03bd0-103">UI \_ PKEY \_ FontProperties \_ Bold</span><span class="sxs-lookup"><span data-stu-id="03bd0-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="03bd0-104">識別 UI \_ PKEY \_ FontProperties \_ Bold 屬性。</span><span class="sxs-lookup"><span data-stu-id="03bd0-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="03bd0-105">備註</span><span class="sxs-lookup"><span data-stu-id="03bd0-105">Remarks</span></span>

<span data-ttu-id="03bd0-106">UI \_ PKEY \_ FontProperties \_ bold 是由應用程式用來查詢 **粗體** 按鈕的狀態。</span><span class="sxs-lookup"><span data-stu-id="03bd0-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="03bd0-107">屬性值來自 [**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) 列舉。</span><span class="sxs-lookup"><span data-stu-id="03bd0-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="03bd0-108">預設值是 `UI_FONTPROPERTIES_NOTSET`。</span><span class="sxs-lookup"><span data-stu-id="03bd0-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="03bd0-109">下表描述屬性和 UI 結果。</span><span class="sxs-lookup"><span data-stu-id="03bd0-109">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="03bd0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="03bd0-110">Property</span></span>                    |    <span data-ttu-id="03bd0-111">UI 結果</span><span class="sxs-lookup"><span data-stu-id="03bd0-111">UI Result</span></span>                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="03bd0-112">**粗體** 按鈕已停用，而且只能由應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="03bd0-112">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="03bd0-113">未選取 [**粗體**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="03bd0-113">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="03bd0-114">已選取 [**粗體**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="03bd0-114">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="03bd0-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="03bd0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03bd0-116">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="03bd0-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="03bd0-117">**UI \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="03bd0-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="03bd0-118">字型控制項</span><span class="sxs-lookup"><span data-stu-id="03bd0-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 