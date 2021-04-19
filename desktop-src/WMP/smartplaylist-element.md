---
title: smartPlaylist 元素
description: SmartPlaylist 元素包含動態定義的播放清單部分。
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- smartPlaylist 元素 Windows Media Player
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983169"
---
# <a name="smartplaylist-element"></a><span data-ttu-id="cbe94-104">smartPlaylist 元素</span><span class="sxs-lookup"><span data-stu-id="cbe94-104">smartPlaylist Element</span></span>

<span data-ttu-id="cbe94-105">**SmartPlaylist** 元素包含動態定義的播放清單部分。</span><span class="sxs-lookup"><span data-stu-id="cbe94-105">The **smartPlaylist** element contains the dynamically defined portion of a playlist.</span></span>

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a><span data-ttu-id="cbe94-106">屬性</span><span class="sxs-lookup"><span data-stu-id="cbe94-106">Attributes</span></span>



| <span data-ttu-id="cbe94-107">詞彙</span><span class="sxs-lookup"><span data-stu-id="cbe94-107">Term</span></span>                                                                                                                                   | <span data-ttu-id="cbe94-108">描述</span><span class="sxs-lookup"><span data-stu-id="cbe94-108">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe94-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>需要 (**版本**) </span><span class="sxs-lookup"><span data-stu-id="cbe94-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (required)</span></span> <br/> | <span data-ttu-id="cbe94-110">十進位數，代表智慧播放清單架構的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="cbe94-110">The decimal number representing the version number of the smart playlist schema.</span></span> <span data-ttu-id="cbe94-111">設定為1.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="cbe94-111">Set to 1.0.0.0.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="cbe94-112">父/子項目</span><span class="sxs-lookup"><span data-stu-id="cbe94-112">Parent/Child Elements</span></span>



| <span data-ttu-id="cbe94-113">階層</span><span class="sxs-lookup"><span data-stu-id="cbe94-113">Hierarchy</span></span> | <span data-ttu-id="cbe94-114">元素</span><span class="sxs-lookup"><span data-stu-id="cbe94-114">Elements</span></span>                                                       |
|-----------|----------------------------------------------------------------|
| <span data-ttu-id="cbe94-115">父代</span><span class="sxs-lookup"><span data-stu-id="cbe94-115">Parent</span></span>    | [<span data-ttu-id="cbe94-116">序列</span><span class="sxs-lookup"><span data-stu-id="cbe94-116">seq</span></span>](seq-element.md)                                         |
| <span data-ttu-id="cbe94-117">子系</span><span class="sxs-lookup"><span data-stu-id="cbe94-117">Child</span></span>     | <span data-ttu-id="cbe94-118">[querySet](queryset-element.md)， [篩選](filter-element.md)</span><span class="sxs-lookup"><span data-stu-id="cbe94-118">[querySet](queryset-element.md), [filter](filter-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cbe94-119">備註</span><span class="sxs-lookup"><span data-stu-id="cbe94-119">Remarks</span></span>

<span data-ttu-id="cbe94-120">**SmartPlaylist** 元素通常包含 **querySet** 專案，而且也可以包含 **篩選** 元素。</span><span class="sxs-lookup"><span data-stu-id="cbe94-120">A **smartPlaylist** element typically contains a **querySet** element and can also contain a **filter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="cbe94-121">範例</span><span class="sxs-lookup"><span data-stu-id="cbe94-121">Examples</span></span>


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
            name = "Music in my library">
                <fragment name = "Genre">
                    <argument name = "condition">Is</argument>
                    <argument name = "value">Rock</argument>
                </fragment>
                <fragment name = "Album Artist">
                    <argument name = "condition">Is Not</argument>
                    <argument name = "value">Brenda Diaz</argument>
                </fragment>
        </sourceFilter>
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
```



## <a name="requirements"></a><span data-ttu-id="cbe94-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbe94-122">Requirements</span></span>



| <span data-ttu-id="cbe94-123">需求</span><span class="sxs-lookup"><span data-stu-id="cbe94-123">Requirement</span></span> | <span data-ttu-id="cbe94-124">值</span><span class="sxs-lookup"><span data-stu-id="cbe94-124">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="cbe94-125">版本</span><span class="sxs-lookup"><span data-stu-id="cbe94-125">Version</span></span><br/> | <span data-ttu-id="cbe94-126">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="cbe94-126">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cbe94-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbe94-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe94-128">**引數元素**</span><span class="sxs-lookup"><span data-stu-id="cbe94-128">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="cbe94-129">**filter 元素**</span><span class="sxs-lookup"><span data-stu-id="cbe94-129">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="cbe94-130">**片段元素**</span><span class="sxs-lookup"><span data-stu-id="cbe94-130">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="cbe94-131">**querySet 元素**</span><span class="sxs-lookup"><span data-stu-id="cbe94-131">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="cbe94-132">**seq 元素**</span><span class="sxs-lookup"><span data-stu-id="cbe94-132">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="cbe94-133">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="cbe94-133">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





