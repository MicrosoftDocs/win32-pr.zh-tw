---
title: 媒體元件
description: 媒體元件會指定播放清單中的其中一個媒體專案。
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- 媒體元件 Windows Media Player
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988234"
---
# <a name="media-element"></a><span data-ttu-id="151fa-104">媒體元件</span><span class="sxs-lookup"><span data-stu-id="151fa-104">media Element</span></span>

<span data-ttu-id="151fa-105">**媒體** 元素會指定播放清單中的其中一個媒體專案。</span><span class="sxs-lookup"><span data-stu-id="151fa-105">The **media** element specifies one of the media items in a playlist.</span></span>

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a><span data-ttu-id="151fa-106">屬性</span><span class="sxs-lookup"><span data-stu-id="151fa-106">Attributes</span></span>



| <span data-ttu-id="151fa-107">詞彙</span><span class="sxs-lookup"><span data-stu-id="151fa-107">Term</span></span>                                                                                                                       | <span data-ttu-id="151fa-108">描述</span><span class="sxs-lookup"><span data-stu-id="151fa-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="151fa-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>需要 (**src**) </span><span class="sxs-lookup"><span data-stu-id="151fa-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (required)</span></span> <br/> | <span data-ttu-id="151fa-110">媒體專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="151fa-110">The URL of a media item.</span></span><br/>                                                              |
| <span data-ttu-id="151fa-111"><span id="cid"></span><span id="CID"></span>**Cid**</span><span class="sxs-lookup"><span data-stu-id="151fa-111"><span id="cid"></span><span id="CID"></span>**cid**</span></span><br/>                                                             | <span data-ttu-id="151fa-112">此媒體專案特有的內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="151fa-112">The content ID that is unique to this media item.</span></span><br/>                                     |
| <span data-ttu-id="151fa-113"><span id="tid"></span><span id="TID"></span>**tid**</span><span class="sxs-lookup"><span data-stu-id="151fa-113"><span id="tid"></span><span id="TID"></span>**tid**</span></span><br/>                                                             | <span data-ttu-id="151fa-114">可以用來追蹤此媒體專案之檔案系統物件的追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="151fa-114">The tracking ID that can be used to track the File System Object for this media item.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="151fa-115">父/子項目</span><span class="sxs-lookup"><span data-stu-id="151fa-115">Parent/Child Elements</span></span>



| <span data-ttu-id="151fa-116">階層</span><span class="sxs-lookup"><span data-stu-id="151fa-116">Hierarchy</span></span> | <span data-ttu-id="151fa-117">元素</span><span class="sxs-lookup"><span data-stu-id="151fa-117">Elements</span></span>               |
|-----------|------------------------|
| <span data-ttu-id="151fa-118">父代</span><span class="sxs-lookup"><span data-stu-id="151fa-118">Parent</span></span>    | [<span data-ttu-id="151fa-119">序列</span><span class="sxs-lookup"><span data-stu-id="151fa-119">seq</span></span>](seq-element.md) |
| <span data-ttu-id="151fa-120">子系</span><span class="sxs-lookup"><span data-stu-id="151fa-120">Child</span></span>     | <span data-ttu-id="151fa-121">無</span><span class="sxs-lookup"><span data-stu-id="151fa-121">None</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="151fa-122">備註</span><span class="sxs-lookup"><span data-stu-id="151fa-122">Remarks</span></span>

<span data-ttu-id="151fa-123">**Cid** 屬性 (內容識別碼) 是由 Windows Media Player 填入，以唯一識別媒體內容的一部分，即使其中繼資料屬性已變更也是一樣。</span><span class="sxs-lookup"><span data-stu-id="151fa-123">The **cid** attribute (the content ID) is populated by the Windows Media Player as a way to uniquely identify a piece of media content even if its metadata attributes have been changed.</span></span> <span data-ttu-id="151fa-124">這可讓您在電腦上共用播放清單，因為內容可以在另一部電腦上識別，而 Windows Media 播放清單可以「自動修復」內容的路徑。</span><span class="sxs-lookup"><span data-stu-id="151fa-124">This allows the sharing of playlists across computers, because the content can be identified on another computer, and the path to it can be "auto-repaired" by the Windows Media Playlist.</span></span> <span data-ttu-id="151fa-125">當檔案的名稱或位置變更時，) 使用 Windows 檔案系統來自動修復媒體的路徑，則 [ **tid** ] 屬性 (追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="151fa-125">The **tid** attribute (the tracking ID) uses the Windows file system to auto-repair the path to the media if the name or location of the file is changed.</span></span>

## <a name="examples"></a><span data-ttu-id="151fa-126">範例</span><span class="sxs-lookup"><span data-stu-id="151fa-126">Examples</span></span>


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a><span data-ttu-id="151fa-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="151fa-127">Requirements</span></span>



| <span data-ttu-id="151fa-128">需求</span><span class="sxs-lookup"><span data-stu-id="151fa-128">Requirement</span></span> | <span data-ttu-id="151fa-129">值</span><span class="sxs-lookup"><span data-stu-id="151fa-129">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="151fa-130">版本</span><span class="sxs-lookup"><span data-stu-id="151fa-130">Version</span></span><br/> | <span data-ttu-id="151fa-131">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="151fa-131">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="151fa-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="151fa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="151fa-133">**seq 元素**</span><span class="sxs-lookup"><span data-stu-id="151fa-133">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="151fa-134">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="151fa-134">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





