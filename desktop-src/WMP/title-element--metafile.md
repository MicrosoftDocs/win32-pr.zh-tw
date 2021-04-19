---
title: '中繼檔 (TITLE 元素) '
description: TITLE 元素會定義文字字串，以指定 ASX 或 ENTRY 專案的標題。
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- " (中繼檔的 TITLE 元素) Windows Media Player"
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984808"
---
# <a name="title-element-metafile"></a><span data-ttu-id="46ece-104">中繼檔 (TITLE 元素) </span><span class="sxs-lookup"><span data-stu-id="46ece-104">TITLE Element (metafile)</span></span>

<span data-ttu-id="46ece-105">**TITLE** 元素會定義文字字串，以指定 **ASX** 或 **ENTRY 專案** 的標題。</span><span class="sxs-lookup"><span data-stu-id="46ece-105">The **TITLE** element defines a text string specifying the title for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a><span data-ttu-id="46ece-106">屬性</span><span class="sxs-lookup"><span data-stu-id="46ece-106">Attributes</span></span>

<span data-ttu-id="46ece-107">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="46ece-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="46ece-108">父/子項目</span><span class="sxs-lookup"><span data-stu-id="46ece-108">Parent/Child Elements</span></span>



| <span data-ttu-id="46ece-109">階層</span><span class="sxs-lookup"><span data-stu-id="46ece-109">Hierarchy</span></span>       | <span data-ttu-id="46ece-110">元素</span><span class="sxs-lookup"><span data-stu-id="46ece-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="46ece-111">父元素</span><span class="sxs-lookup"><span data-stu-id="46ece-111">Parent elements</span></span> | <span data-ttu-id="46ece-112">**ASX**， **進入**</span><span class="sxs-lookup"><span data-stu-id="46ece-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="46ece-113">子元素</span><span class="sxs-lookup"><span data-stu-id="46ece-113">Child elements</span></span>  | <span data-ttu-id="46ece-114">無</span><span class="sxs-lookup"><span data-stu-id="46ece-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="46ece-115">備註</span><span class="sxs-lookup"><span data-stu-id="46ece-115">Remarks</span></span>

<span data-ttu-id="46ece-116">這個元素會定義文字字串，以指定 **ASX** 或 **ENTRY 專案** 的標題。</span><span class="sxs-lookup"><span data-stu-id="46ece-116">This element defines a text string that specifies the title of an **ASX** or **ENTRY** element.</span></span> <span data-ttu-id="46ece-117">標題會顯示在 [顯示面板] 和 [ **屬性** ] 對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="46ece-117">The title is displayed in the display panel and **Properties** dialog box.</span></span>

<span data-ttu-id="46ece-118">當這個元素出現在 **ASX** 元素內時，文字會顯示為 [ **顯示** 資訊]。</span><span class="sxs-lookup"><span data-stu-id="46ece-118">When this element appears within an **ASX** element, the text is displayed as **Show** information.</span></span> <span data-ttu-id="46ece-119">當這個專案出現在 **ENTRY 專案** 中時，文字會顯示為 **剪輯** 資訊。</span><span class="sxs-lookup"><span data-stu-id="46ece-119">When this element appears within an **ENTRY** element, the text is displayed as **Clip** information.</span></span>

<span data-ttu-id="46ece-120">如果 **MOREINFO** 專案也與相關聯的 (父) 元素一起使用，則它是使用者按一下以存取 **MOREINFO** 專案中定義之 URL 的標題文字。</span><span class="sxs-lookup"><span data-stu-id="46ece-120">If a **MOREINFO** element is also used with the associated (parent) element, it is the title text that the user clicks to access the URL defined in the **MOREINFO** element.</span></span>

<span data-ttu-id="46ece-121">每個父 **ASX** 和 **ENTRY** 元素最多隻能包含一個子 **標題** 元素。</span><span class="sxs-lookup"><span data-stu-id="46ece-121">Each parent **ASX** and **ENTRY** element should contain at most one child **TITLE** element.</span></span> <span data-ttu-id="46ece-122">第一個專案之後的多個 **TITLE** 元素將會被忽略，而且不會顯示。</span><span class="sxs-lookup"><span data-stu-id="46ece-122">Multiple **TITLE** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="46ece-123">範例</span><span class="sxs-lookup"><span data-stu-id="46ece-123">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="46ece-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="46ece-124">Requirements</span></span>



| <span data-ttu-id="46ece-125">需求</span><span class="sxs-lookup"><span data-stu-id="46ece-125">Requirement</span></span> | <span data-ttu-id="46ece-126">值</span><span class="sxs-lookup"><span data-stu-id="46ece-126">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="46ece-127">版本</span><span class="sxs-lookup"><span data-stu-id="46ece-127">Version</span></span><br/> | <span data-ttu-id="46ece-128">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="46ece-128">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46ece-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46ece-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ece-130">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="46ece-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="46ece-131">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="46ece-131">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





