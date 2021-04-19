---
title: seq 元素
description: Seq 元素包含定義靜態播放清單的元素，或定義智慧播放清單的元素。
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- seq 元素 Windows Media Player
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999143"
---
# <a name="seq-element"></a><span data-ttu-id="07875-104">seq 元素</span><span class="sxs-lookup"><span data-stu-id="07875-104">seq Element</span></span>

<span data-ttu-id="07875-105">**Seq** 元素包含定義靜態播放清單的元素，或定義智慧播放清單的元素。</span><span class="sxs-lookup"><span data-stu-id="07875-105">The **seq** element contains elements that define a static playlist or elements that define a smart playlist.</span></span>

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a><span data-ttu-id="07875-106">屬性</span><span class="sxs-lookup"><span data-stu-id="07875-106">Attributes</span></span>

<span data-ttu-id="07875-107">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="07875-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="07875-108">父/子項目</span><span class="sxs-lookup"><span data-stu-id="07875-108">Parent/Child Elements</span></span>



| <span data-ttu-id="07875-109">階層</span><span class="sxs-lookup"><span data-stu-id="07875-109">Hierarchy</span></span> | <span data-ttu-id="07875-110">元素</span><span class="sxs-lookup"><span data-stu-id="07875-110">Elements</span></span>                                                               |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="07875-111">父代</span><span class="sxs-lookup"><span data-stu-id="07875-111">Parent</span></span>    | [<span data-ttu-id="07875-112">body</span><span class="sxs-lookup"><span data-stu-id="07875-112">body</span></span>](body-element.md)                                               |
| <span data-ttu-id="07875-113">子系</span><span class="sxs-lookup"><span data-stu-id="07875-113">Child</span></span>     | <span data-ttu-id="07875-114">[media](media-element.md)、 [smartPlaylist](smartplaylist-element.md)</span><span class="sxs-lookup"><span data-stu-id="07875-114">[media](media-element.md), [smartPlaylist](smartplaylist-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="07875-115">備註</span><span class="sxs-lookup"><span data-stu-id="07875-115">Remarks</span></span>

<span data-ttu-id="07875-116">當 **seq** 元素只包含參考特定媒體專案的 **媒體** 專案時，播放清單會被視為靜態。</span><span class="sxs-lookup"><span data-stu-id="07875-116">When a **seq** element only contains **media** elements that reference specific media items, the playlist is considered to be static.</span></span> <span data-ttu-id="07875-117">當 **seq** 元素包含 **smartPlaylist** 元素時，它會被視為動態的「智慧型」播放清單。</span><span class="sxs-lookup"><span data-stu-id="07875-117">When a **seq** element contains a **smartPlaylist** element, it is considered to be a dynamic "smart" playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="07875-118">範例</span><span class="sxs-lookup"><span data-stu-id="07875-118">Examples</span></span>


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a><span data-ttu-id="07875-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="07875-119">Requirements</span></span>



| <span data-ttu-id="07875-120">需求</span><span class="sxs-lookup"><span data-stu-id="07875-120">Requirement</span></span> | <span data-ttu-id="07875-121">值</span><span class="sxs-lookup"><span data-stu-id="07875-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="07875-122">版本</span><span class="sxs-lookup"><span data-stu-id="07875-122">Version</span></span><br/> | <span data-ttu-id="07875-123">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="07875-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07875-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07875-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07875-125">**body 元素**</span><span class="sxs-lookup"><span data-stu-id="07875-125">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="07875-126">**媒體元件**</span><span class="sxs-lookup"><span data-stu-id="07875-126">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="07875-127">**smartPlaylist 元素**</span><span class="sxs-lookup"><span data-stu-id="07875-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="07875-128">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="07875-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





