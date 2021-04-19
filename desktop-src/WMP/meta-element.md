---
title: 中繼元素
description: 中繼元素會指定適用于整個播放清單的中繼資料。
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- 中繼元素 Windows Media Player
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998610"
---
# <a name="meta-element"></a><span data-ttu-id="0ee1c-104">中繼元素</span><span class="sxs-lookup"><span data-stu-id="0ee1c-104">meta Element</span></span>

<span data-ttu-id="0ee1c-105">**中繼** 元素會指定適用于整個播放清單的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="0ee1c-105">The **meta** element specifies metadata that applies to the entire playlist.</span></span>

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a><span data-ttu-id="0ee1c-106">屬性</span><span class="sxs-lookup"><span data-stu-id="0ee1c-106">Attributes</span></span>



| <span data-ttu-id="0ee1c-107">詞彙</span><span class="sxs-lookup"><span data-stu-id="0ee1c-107">Term</span></span>                                                                       | <span data-ttu-id="0ee1c-108">描述</span><span class="sxs-lookup"><span data-stu-id="0ee1c-108">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee1c-109"><span id="name"></span><span id="NAME"></span>**名字**</span><span class="sxs-lookup"><span data-stu-id="0ee1c-109"><span id="name"></span><span id="NAME"></span>**name**</span></span><br/>          | <span data-ttu-id="0ee1c-110">中繼資料專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ee1c-110">The name of an item of metadata.</span></span><br/>                                                                                       |
| <span data-ttu-id="0ee1c-111"><span id="content"></span><span id="CONTENT"></span>**內容**</span><span class="sxs-lookup"><span data-stu-id="0ee1c-111"><span id="content"></span><span id="CONTENT"></span>**content**</span></span><br/> | <span data-ttu-id="0ee1c-112">中繼資料專案的值。</span><span class="sxs-lookup"><span data-stu-id="0ee1c-112">The value of an item of metadata.</span></span> <span data-ttu-id="0ee1c-113">例如，如果 name 屬性為 "content-type"，則內容屬性可能是 "搖滾"。</span><span class="sxs-lookup"><span data-stu-id="0ee1c-113">For example, if the name attribute is "Genre" the content attribute could be "Rock".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="0ee1c-114">父/子項目</span><span class="sxs-lookup"><span data-stu-id="0ee1c-114">Parent/Child Elements</span></span>



| <span data-ttu-id="0ee1c-115">階層</span><span class="sxs-lookup"><span data-stu-id="0ee1c-115">Hierarchy</span></span> | <span data-ttu-id="0ee1c-116">元素</span><span class="sxs-lookup"><span data-stu-id="0ee1c-116">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="0ee1c-117">父代</span><span class="sxs-lookup"><span data-stu-id="0ee1c-117">Parent</span></span>    | [<span data-ttu-id="0ee1c-118">頭</span><span class="sxs-lookup"><span data-stu-id="0ee1c-118">head</span></span>](head-element.md) |
| <span data-ttu-id="0ee1c-119">子系</span><span class="sxs-lookup"><span data-stu-id="0ee1c-119">Child</span></span>     | <span data-ttu-id="0ee1c-120">無</span><span class="sxs-lookup"><span data-stu-id="0ee1c-120">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="0ee1c-121">備註</span><span class="sxs-lookup"><span data-stu-id="0ee1c-121">Remarks</span></span>

<span data-ttu-id="0ee1c-122">Windows Media 播放清單的建立者可以將中繼元素的 name 屬性設定為任何字串。</span><span class="sxs-lookup"><span data-stu-id="0ee1c-122">The creator of a Windows Media Playlist can set the name attribute of a meta element to any string.</span></span> <span data-ttu-id="0ee1c-123">下列清單顯示在 Windows Media Player 和其他 Microsoft 元件所建立的 Windows Media 播放清單中找到的一些典型名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="0ee1c-123">The following list shows some typical name attributes that are found in Windows Media Playlists created by Windows Media Player and other Microsoft components.</span></span>

-   <span data-ttu-id="0ee1c-124">作者</span><span class="sxs-lookup"><span data-stu-id="0ee1c-124">Author</span></span>
-   <span data-ttu-id="0ee1c-125">類別</span><span class="sxs-lookup"><span data-stu-id="0ee1c-125">Category</span></span>
-   <span data-ttu-id="0ee1c-126">Genre</span><span class="sxs-lookup"><span data-stu-id="0ee1c-126">Genre</span></span>
-   <span data-ttu-id="0ee1c-127">UserName</span><span class="sxs-lookup"><span data-stu-id="0ee1c-127">UserName</span></span>
-   <span data-ttu-id="0ee1c-128">UserRating</span><span class="sxs-lookup"><span data-stu-id="0ee1c-128">UserRating</span></span>
-   <span data-ttu-id="0ee1c-129">Generator</span><span class="sxs-lookup"><span data-stu-id="0ee1c-129">Generator</span></span>

## <a name="examples"></a><span data-ttu-id="0ee1c-130">範例</span><span class="sxs-lookup"><span data-stu-id="0ee1c-130">Examples</span></span>


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="0ee1c-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ee1c-131">Requirements</span></span>



| <span data-ttu-id="0ee1c-132">需求</span><span class="sxs-lookup"><span data-stu-id="0ee1c-132">Requirement</span></span> | <span data-ttu-id="0ee1c-133">值</span><span class="sxs-lookup"><span data-stu-id="0ee1c-133">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="0ee1c-134">版本</span><span class="sxs-lookup"><span data-stu-id="0ee1c-134">Version</span></span><br/> | <span data-ttu-id="0ee1c-135">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="0ee1c-135">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ee1c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ee1c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee1c-137">**head 元素**</span><span class="sxs-lookup"><span data-stu-id="0ee1c-137">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="0ee1c-138">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="0ee1c-138">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





