---
title: head 元素
description: Head 元素包含適用于整個播放清單的中繼資料。
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- head 元素 Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976105"
---
# <a name="head-element"></a><span data-ttu-id="0e00c-104">head 元素</span><span class="sxs-lookup"><span data-stu-id="0e00c-104">head Element</span></span>

<span data-ttu-id="0e00c-105">**Head** 元素包含適用于整個播放清單的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="0e00c-105">The **head** element contains metadata that applies to the entire playlist.</span></span>

``` syntax
<head>
</head>
```

## <a name="attributes"></a><span data-ttu-id="0e00c-106">屬性</span><span class="sxs-lookup"><span data-stu-id="0e00c-106">Attributes</span></span>

<span data-ttu-id="0e00c-107">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="0e00c-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="0e00c-108">父/子項目</span><span class="sxs-lookup"><span data-stu-id="0e00c-108">Parent/Child Elements</span></span>



| <span data-ttu-id="0e00c-109">階層</span><span class="sxs-lookup"><span data-stu-id="0e00c-109">Hierarchy</span></span> | <span data-ttu-id="0e00c-110">元素</span><span class="sxs-lookup"><span data-stu-id="0e00c-110">Elements</span></span>                                                  |
|-----------|-----------------------------------------------------------|
| <span data-ttu-id="0e00c-111">父代</span><span class="sxs-lookup"><span data-stu-id="0e00c-111">Parent</span></span>    | [<span data-ttu-id="0e00c-112">Smil</span><span class="sxs-lookup"><span data-stu-id="0e00c-112">smil</span></span>](smil-element.md)                                  |
| <span data-ttu-id="0e00c-113">子系</span><span class="sxs-lookup"><span data-stu-id="0e00c-113">Child</span></span>     | <span data-ttu-id="0e00c-114">[標題](title-element--wpl.md)、 [中繼](meta-element.md)</span><span class="sxs-lookup"><span data-stu-id="0e00c-114">[title](title-element--wpl.md), [meta](meta-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0e00c-115">備註</span><span class="sxs-lookup"><span data-stu-id="0e00c-115">Remarks</span></span>

<span data-ttu-id="0e00c-116">**標頭** 專案通常包含 **標題** 專案，以及一個或多個定義播放清單全域特性的 **中繼** 元素。</span><span class="sxs-lookup"><span data-stu-id="0e00c-116">Typically the **head** element contains a **title** element and one or more **meta** elements that define global characteristics of the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="0e00c-117">範例</span><span class="sxs-lookup"><span data-stu-id="0e00c-117">Examples</span></span>


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="0e00c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e00c-118">Requirements</span></span>



| <span data-ttu-id="0e00c-119">需求</span><span class="sxs-lookup"><span data-stu-id="0e00c-119">Requirement</span></span> | <span data-ttu-id="0e00c-120">值</span><span class="sxs-lookup"><span data-stu-id="0e00c-120">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="0e00c-121">版本</span><span class="sxs-lookup"><span data-stu-id="0e00c-121">Version</span></span><br/> | <span data-ttu-id="0e00c-122">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="0e00c-122">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e00c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e00c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e00c-124">**中繼元素**</span><span class="sxs-lookup"><span data-stu-id="0e00c-124">**meta Element**</span></span>](meta-element.md)
</dt> <dt>

[<span data-ttu-id="0e00c-125">**.WPL) 的 title 元素 (**</span><span class="sxs-lookup"><span data-stu-id="0e00c-125">**title Element (WPL)**</span></span>](title-element--wpl.md)
</dt> <dt>

[<span data-ttu-id="0e00c-126">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="0e00c-126">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





