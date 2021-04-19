---
title: body 元素
description: Body 元素包含定義播放清單內容的元素。
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- body 元素 Windows Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995994"
---
# <a name="body-element"></a><span data-ttu-id="08d1e-104">body 元素</span><span class="sxs-lookup"><span data-stu-id="08d1e-104">body Element</span></span>

<span data-ttu-id="08d1e-105">**Body** 元素包含定義播放清單內容的元素。</span><span class="sxs-lookup"><span data-stu-id="08d1e-105">The **body** element contains the elements that define the contents of a playlist.</span></span>

``` syntax
<body>
</body>
```

## <a name="attributes"></a><span data-ttu-id="08d1e-106">屬性</span><span class="sxs-lookup"><span data-stu-id="08d1e-106">Attributes</span></span>

<span data-ttu-id="08d1e-107">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="08d1e-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="08d1e-108">父/子項目</span><span class="sxs-lookup"><span data-stu-id="08d1e-108">Parent/Child Elements</span></span>



| <span data-ttu-id="08d1e-109">階層</span><span class="sxs-lookup"><span data-stu-id="08d1e-109">Hierarchy</span></span> | <span data-ttu-id="08d1e-110">元素</span><span class="sxs-lookup"><span data-stu-id="08d1e-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="08d1e-111">父代</span><span class="sxs-lookup"><span data-stu-id="08d1e-111">Parent</span></span>    | [<span data-ttu-id="08d1e-112">Smil</span><span class="sxs-lookup"><span data-stu-id="08d1e-112">smil</span></span>](smil-element.md) |
| <span data-ttu-id="08d1e-113">子系</span><span class="sxs-lookup"><span data-stu-id="08d1e-113">Child</span></span>     | [<span data-ttu-id="08d1e-114">序列</span><span class="sxs-lookup"><span data-stu-id="08d1e-114">seq</span></span>](seq-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="08d1e-115">備註</span><span class="sxs-lookup"><span data-stu-id="08d1e-115">Remarks</span></span>

<span data-ttu-id="08d1e-116">播放清單的內容會組織在包含于 **body** 專案內的 **seq** 元素中。</span><span class="sxs-lookup"><span data-stu-id="08d1e-116">The contents of a playlist are organized within a **seq** element that is contained within the **body** element.</span></span> <span data-ttu-id="08d1e-117">一般來說，有一個 seq 元素定義了一組靜態的媒體專案，其中包含 **媒體** 專案，或是有一個定義一組動態媒體專案，並且包含 **smartPlaylist** 專案的 **seq** 專案。</span><span class="sxs-lookup"><span data-stu-id="08d1e-117">Typically there is either one **seq** element that defines a static set of media items and contains **media** elements, or there is one that defines a dynamic set of media items and contains a **smartPlaylist** element.</span></span>

## <a name="examples"></a><span data-ttu-id="08d1e-118">範例</span><span class="sxs-lookup"><span data-stu-id="08d1e-118">Examples</span></span>


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a><span data-ttu-id="08d1e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="08d1e-119">Requirements</span></span>



| <span data-ttu-id="08d1e-120">需求</span><span class="sxs-lookup"><span data-stu-id="08d1e-120">Requirement</span></span> | <span data-ttu-id="08d1e-121">值</span><span class="sxs-lookup"><span data-stu-id="08d1e-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="08d1e-122">版本</span><span class="sxs-lookup"><span data-stu-id="08d1e-122">Version</span></span><br/> | <span data-ttu-id="08d1e-123">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="08d1e-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08d1e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08d1e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d1e-125">**媒體元件**</span><span class="sxs-lookup"><span data-stu-id="08d1e-125">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="08d1e-126">**seq 元素**</span><span class="sxs-lookup"><span data-stu-id="08d1e-126">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="08d1e-127">**smartPlaylist 元素**</span><span class="sxs-lookup"><span data-stu-id="08d1e-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="08d1e-128">**smil 元素**</span><span class="sxs-lookup"><span data-stu-id="08d1e-128">**smil Element**</span></span>](smil-element.md)
</dt> <dt>

[<span data-ttu-id="08d1e-129">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="08d1e-129">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





