---
title: ABSTRACT 元素
description: ABSTRACT 元素包含描述相關聯的 ASX、橫幅或 ENTRY 元素的文字。
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- ABSTRACT 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999440"
---
# <a name="abstract-element"></a><span data-ttu-id="adb0b-104">ABSTRACT 元素</span><span class="sxs-lookup"><span data-stu-id="adb0b-104">ABSTRACT Element</span></span>

<span data-ttu-id="adb0b-105">**ABSTRACT** 元素包含描述相關聯的 **ASX**、**橫幅** 或 **ENTRY** 元素的文字。</span><span class="sxs-lookup"><span data-stu-id="adb0b-105">The **ABSTRACT** element contains text that describes the associated **ASX**, **BANNER**, or **ENTRY** element.</span></span>

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a><span data-ttu-id="adb0b-106">屬性</span><span class="sxs-lookup"><span data-stu-id="adb0b-106">Attributes</span></span>

<span data-ttu-id="adb0b-107">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="adb0b-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="adb0b-108">父/子項目</span><span class="sxs-lookup"><span data-stu-id="adb0b-108">Parent/Child Elements</span></span>



| <span data-ttu-id="adb0b-109">階層</span><span class="sxs-lookup"><span data-stu-id="adb0b-109">Hierarchy</span></span> | <span data-ttu-id="adb0b-110">元素</span><span class="sxs-lookup"><span data-stu-id="adb0b-110">Elements</span></span>                       |
|-----------|--------------------------------|
| <span data-ttu-id="adb0b-111">父代</span><span class="sxs-lookup"><span data-stu-id="adb0b-111">Parent</span></span>    | <span data-ttu-id="adb0b-112">**ASX**、 **ENTRY**、 **橫幅**</span><span class="sxs-lookup"><span data-stu-id="adb0b-112">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="adb0b-113">子系</span><span class="sxs-lookup"><span data-stu-id="adb0b-113">Child</span></span>     | <span data-ttu-id="adb0b-114">無</span><span class="sxs-lookup"><span data-stu-id="adb0b-114">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="adb0b-115">備註</span><span class="sxs-lookup"><span data-stu-id="adb0b-115">Remarks</span></span>

<span data-ttu-id="adb0b-116">如果這個專案出現在 **ASX** 元素內，當滑鼠停留在顯示標題上時，文字會顯示為工具提示。</span><span class="sxs-lookup"><span data-stu-id="adb0b-116">If this element appears within an **ASX** element, the text displays as a ToolTip when the mouse hovers over the show title.</span></span>

<span data-ttu-id="adb0b-117">如果這個元素出現在 **ENTRY 專案** 中，當滑鼠停留在剪輯標題上時，文字會顯示為工具提示。</span><span class="sxs-lookup"><span data-stu-id="adb0b-117">If this element appears within an **ENTRY** element, the text displays as a ToolTip when the mouse hovers over the clip title.</span></span>

<span data-ttu-id="adb0b-118">如果這個元素出現在 **橫幅** 專案中，則文字會顯示為橫幅圖形的工具提示。</span><span class="sxs-lookup"><span data-stu-id="adb0b-118">If this element appears within a **BANNER** element, the text displays as a ToolTip for the banner graphic.</span></span>

<span data-ttu-id="adb0b-119">每個範圍只使用一個 **抽象** 元素。</span><span class="sxs-lookup"><span data-stu-id="adb0b-119">Use only one **ABSTRACT** element per scope.</span></span> <span data-ttu-id="adb0b-120">只有在處理中繼檔檔案時，才會使用另一個元素範圍內的第一個 **抽象** 元素。</span><span class="sxs-lookup"><span data-stu-id="adb0b-120">Only the first **ABSTRACT** element within the scope of another element is used when a metafile file is processed.</span></span> <span data-ttu-id="adb0b-121">該範圍中的任何後續 **抽象** 元素都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="adb0b-121">Any subsequent **ABSTRACT** elements in that scope are ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="adb0b-122">範例</span><span class="sxs-lookup"><span data-stu-id="adb0b-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="adb0b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="adb0b-123">Requirements</span></span>



| <span data-ttu-id="adb0b-124">需求</span><span class="sxs-lookup"><span data-stu-id="adb0b-124">Requirement</span></span> | <span data-ttu-id="adb0b-125">值</span><span class="sxs-lookup"><span data-stu-id="adb0b-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="adb0b-126">版本</span><span class="sxs-lookup"><span data-stu-id="adb0b-126">Version</span></span><br/> | <span data-ttu-id="adb0b-127">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="adb0b-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="adb0b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adb0b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb0b-129">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="adb0b-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="adb0b-130">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="adb0b-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





