---
title: '著作權元素 (Msfeeds .h) '
description: 著作權元素會定義文字字串，以指定 ASX 或 ENTRY 元素的著作權資訊。
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- 著作權元素 Windows Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980113"
---
# <a name="copyright-element"></a><span data-ttu-id="16b84-104">著作權元素</span><span class="sxs-lookup"><span data-stu-id="16b84-104">COPYRIGHT Element</span></span>

<span data-ttu-id="16b84-105">**著作權** 元素會定義文字字串，以指定 **ASX** 或 **ENTRY** 元素的著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="16b84-105">The **COPYRIGHT** element defines a text string specifying the copyright information for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a><span data-ttu-id="16b84-106">屬性</span><span class="sxs-lookup"><span data-stu-id="16b84-106">Attributes</span></span>

<span data-ttu-id="16b84-107">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="16b84-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="16b84-108">父/子項目</span><span class="sxs-lookup"><span data-stu-id="16b84-108">Parent/Child Elements</span></span>



| <span data-ttu-id="16b84-109">階層</span><span class="sxs-lookup"><span data-stu-id="16b84-109">Hierarchy</span></span>       | <span data-ttu-id="16b84-110">元素</span><span class="sxs-lookup"><span data-stu-id="16b84-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="16b84-111">父元素</span><span class="sxs-lookup"><span data-stu-id="16b84-111">Parent elements</span></span> | <span data-ttu-id="16b84-112">**ASX**， **進入**</span><span class="sxs-lookup"><span data-stu-id="16b84-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="16b84-113">子元素</span><span class="sxs-lookup"><span data-stu-id="16b84-113">Child elements</span></span>  | <span data-ttu-id="16b84-114">無</span><span class="sxs-lookup"><span data-stu-id="16b84-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="16b84-115">備註</span><span class="sxs-lookup"><span data-stu-id="16b84-115">Remarks</span></span>

<span data-ttu-id="16b84-116">此元素會定義文字字串，以指定 **ASX** 或 **ENTRY 專案** 的著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="16b84-116">This element defines a text string that specifies the copyright information for an **ASX** or **ENTRY** element.</span></span>

<span data-ttu-id="16b84-117">當此元素出現在 **ASX** 元素內時，著作權字串只會顯示為 [ **顯示** 資訊]。</span><span class="sxs-lookup"><span data-stu-id="16b84-117">When this element appears within an **ASX** element, the copyright string is displayed only as **Show** information.</span></span> <span data-ttu-id="16b84-118">當這個專案出現在 **ENTRY 專案** 中時，文字會顯示為剪輯資訊。</span><span class="sxs-lookup"><span data-stu-id="16b84-118">When this element appears within an **ENTRY** element, the text is displayed as clip information.</span></span> <span data-ttu-id="16b84-119">每個父 **ASX** 和 **ENTRY** 元素最多隻能包含一個子 **著作權** 元素。</span><span class="sxs-lookup"><span data-stu-id="16b84-119">Each parent **ASX** and **ENTRY** element should contain at most one child **COPYRIGHT** element.</span></span> <span data-ttu-id="16b84-120">第一個的多個 **著作權** 元素會被忽略，且不會顯示。</span><span class="sxs-lookup"><span data-stu-id="16b84-120">Multiple **COPYRIGHT** elements after the first will be ignored and will not be displayed.</span></span>

<span data-ttu-id="16b84-121">如果未使用 UTF-8 編碼配置來編碼中繼檔，則著作權和商標注冊符號 ( 或 ) 的字元可能無法正確顯示。</span><span class="sxs-lookup"><span data-stu-id="16b84-121">The characters for copyright and trademark registration symbols (   or   ) may not display properly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="16b84-122">在此情況下，若要為所有使用者正確顯示這些符號的其中一個，您可以改用 ASCII 對等專案 (c) 和 (R) 。</span><span class="sxs-lookup"><span data-stu-id="16b84-122">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (R) instead.</span></span>

<span data-ttu-id="16b84-123">如果中繼檔是使用 UTF-8 編碼，則著作權和商標符號將會正確顯示。</span><span class="sxs-lookup"><span data-stu-id="16b84-123">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="16b84-124">範例</span><span class="sxs-lookup"><span data-stu-id="16b84-124">Examples</span></span>


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a><span data-ttu-id="16b84-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="16b84-125">Requirements</span></span>



| <span data-ttu-id="16b84-126">需求</span><span class="sxs-lookup"><span data-stu-id="16b84-126">Requirement</span></span> | <span data-ttu-id="16b84-127">值</span><span class="sxs-lookup"><span data-stu-id="16b84-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="16b84-128">版本</span><span class="sxs-lookup"><span data-stu-id="16b84-128">Version</span></span><br/> | <span data-ttu-id="16b84-129">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="16b84-129">Windows Media Player version 7.0 or later</span></span><br/>                                 |
| <span data-ttu-id="16b84-130">標頭</span><span class="sxs-lookup"><span data-stu-id="16b84-130">Header</span></span><br/>  | <dl> <span data-ttu-id="16b84-131"><dt>Msfeeds。h</dt></span><span class="sxs-lookup"><span data-stu-id="16b84-131"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16b84-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16b84-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b84-133">**將著作權字元新增至中繼檔**</span><span class="sxs-lookup"><span data-stu-id="16b84-133">**Adding Copyright Characters to Metafiles**</span></span>](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[<span data-ttu-id="16b84-134">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="16b84-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="16b84-135">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="16b84-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





