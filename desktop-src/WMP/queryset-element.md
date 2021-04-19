---
title: querySet 元素
description: QuerySet 元素包含定義將從程式庫選取哪些媒體專案的元素。
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- querySet 元素 Windows Media Player
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996005"
---
# <a name="queryset-element"></a><span data-ttu-id="19134-104">querySet 元素</span><span class="sxs-lookup"><span data-stu-id="19134-104">querySet Element</span></span>

<span data-ttu-id="19134-105">**QuerySet** 元素包含定義將從程式庫選取哪些媒體專案的元素。</span><span class="sxs-lookup"><span data-stu-id="19134-105">The **querySet** element contains elements that define which media items will be selected from the library.</span></span>

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a><span data-ttu-id="19134-106">屬性</span><span class="sxs-lookup"><span data-stu-id="19134-106">Attributes</span></span>

<span data-ttu-id="19134-107">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="19134-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="19134-108">父/子項目</span><span class="sxs-lookup"><span data-stu-id="19134-108">Parent/Child Elements</span></span>



| <span data-ttu-id="19134-109">階層</span><span class="sxs-lookup"><span data-stu-id="19134-109">Hierarchy</span></span> | <span data-ttu-id="19134-110">元素</span><span class="sxs-lookup"><span data-stu-id="19134-110">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="19134-111">父代</span><span class="sxs-lookup"><span data-stu-id="19134-111">Parent</span></span>    | [<span data-ttu-id="19134-112">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="19134-112">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="19134-113">子系</span><span class="sxs-lookup"><span data-stu-id="19134-113">Child</span></span>     | [<span data-ttu-id="19134-114">sourceFilter</span><span class="sxs-lookup"><span data-stu-id="19134-114">sourceFilter</span></span>](sourcefilter-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="19134-115">備註</span><span class="sxs-lookup"><span data-stu-id="19134-115">Remarks</span></span>

<span data-ttu-id="19134-116">**QuerySet** 元素會指定應該從程式庫中選取哪些媒體專案，而不考慮結果集的大小。</span><span class="sxs-lookup"><span data-stu-id="19134-116">The **querySet** element specifies which media items should be selected from the library, without regard for the size of the result set.</span></span> <span data-ttu-id="19134-117">另一方面， **filter** 元素會限制結果集的大小。</span><span class="sxs-lookup"><span data-stu-id="19134-117">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="19134-118">範例</span><span class="sxs-lookup"><span data-stu-id="19134-118">Examples</span></span>


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a><span data-ttu-id="19134-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="19134-119">Requirements</span></span>



| <span data-ttu-id="19134-120">需求</span><span class="sxs-lookup"><span data-stu-id="19134-120">Requirement</span></span> | <span data-ttu-id="19134-121">值</span><span class="sxs-lookup"><span data-stu-id="19134-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="19134-122">版本</span><span class="sxs-lookup"><span data-stu-id="19134-122">Version</span></span><br/> | <span data-ttu-id="19134-123">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="19134-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19134-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19134-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19134-125">**引數元素**</span><span class="sxs-lookup"><span data-stu-id="19134-125">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="19134-126">**filter 元素**</span><span class="sxs-lookup"><span data-stu-id="19134-126">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="19134-127">**片段元素**</span><span class="sxs-lookup"><span data-stu-id="19134-127">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="19134-128">**smartPlaylist 元素**</span><span class="sxs-lookup"><span data-stu-id="19134-128">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="19134-129">**sourceFilter 元素**</span><span class="sxs-lookup"><span data-stu-id="19134-129">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="19134-130">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="19134-130">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





