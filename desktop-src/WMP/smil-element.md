---
title: smil 元素
description: Smil 元素一律是 Windows Media 播放清單中的最上層元素， (.WPL) 檔。 它會指定檔案使用 SMIL (同步處理的多媒體整合語言) 語法和文法。
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- smil 元素 Windows Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996021"
---
# <a name="smil-element"></a><span data-ttu-id="51f06-105">smil 元素</span><span class="sxs-lookup"><span data-stu-id="51f06-105">smil Element</span></span>

<span data-ttu-id="51f06-106">**Smil** 元素一律是 Windows Media 播放清單中的最上層元素， (.wpl) 檔。</span><span class="sxs-lookup"><span data-stu-id="51f06-106">The **smil** element is always the top level element in a Windows Media Playlist (WPL) file.</span></span> <span data-ttu-id="51f06-107">它會指定檔案使用 SMIL (同步處理的多媒體整合語言) 語法和文法。</span><span class="sxs-lookup"><span data-stu-id="51f06-107">It specifies that the file uses SMIL (Synchronized Multimedia Integration Language) syntax and grammar.</span></span>

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a><span data-ttu-id="51f06-108">屬性</span><span class="sxs-lookup"><span data-stu-id="51f06-108">Attributes</span></span>

<span data-ttu-id="51f06-109">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="51f06-109">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="51f06-110">父/子項目</span><span class="sxs-lookup"><span data-stu-id="51f06-110">Parent/Child Elements</span></span>



| <span data-ttu-id="51f06-111">階層</span><span class="sxs-lookup"><span data-stu-id="51f06-111">Hierarchy</span></span> | <span data-ttu-id="51f06-112">元素</span><span class="sxs-lookup"><span data-stu-id="51f06-112">Elements</span></span>                                           |
|-----------|----------------------------------------------------|
| <span data-ttu-id="51f06-113">父代</span><span class="sxs-lookup"><span data-stu-id="51f06-113">Parent</span></span>    | <span data-ttu-id="51f06-114">無</span><span class="sxs-lookup"><span data-stu-id="51f06-114">None</span></span>                                               |
| <span data-ttu-id="51f06-115">子系</span><span class="sxs-lookup"><span data-stu-id="51f06-115">Child</span></span>     | <span data-ttu-id="51f06-116">[head](head-element.md)、 [body](body-element.md)</span><span class="sxs-lookup"><span data-stu-id="51f06-116">[head](head-element.md), [body](body-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="51f06-117">備註</span><span class="sxs-lookup"><span data-stu-id="51f06-117">Remarks</span></span>

<span data-ttu-id="51f06-118">每個 Windows Media 播放清單的根目錄都必須有 **smil** 元素。</span><span class="sxs-lookup"><span data-stu-id="51f06-118">Every Windows Media Playlist must have the **smil** element at its root.</span></span>

## <a name="examples"></a><span data-ttu-id="51f06-119">範例</span><span class="sxs-lookup"><span data-stu-id="51f06-119">Examples</span></span>


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a><span data-ttu-id="51f06-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="51f06-120">Requirements</span></span>



| <span data-ttu-id="51f06-121">需求</span><span class="sxs-lookup"><span data-stu-id="51f06-121">Requirement</span></span> | <span data-ttu-id="51f06-122">值</span><span class="sxs-lookup"><span data-stu-id="51f06-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="51f06-123">版本</span><span class="sxs-lookup"><span data-stu-id="51f06-123">Version</span></span><br/> | <span data-ttu-id="51f06-124">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="51f06-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51f06-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51f06-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f06-126">**body 元素**</span><span class="sxs-lookup"><span data-stu-id="51f06-126">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="51f06-127">**head 元素**</span><span class="sxs-lookup"><span data-stu-id="51f06-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="51f06-128">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="51f06-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





