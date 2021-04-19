---
title: .WPL) 的 title 元素 (
description: Title 元素會指定播放清單的標題。
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- title 元素 (.WPL) Windows Media Player
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985771"
---
# <a name="title-element-wpl"></a><span data-ttu-id="7bb7c-104">.WPL) 的 title 元素 (</span><span class="sxs-lookup"><span data-stu-id="7bb7c-104">title Element (WPL)</span></span>

<span data-ttu-id="7bb7c-105">**Title** 元素會指定播放清單的標題。</span><span class="sxs-lookup"><span data-stu-id="7bb7c-105">The **title** element specifies a title for the playlist.</span></span>

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a><span data-ttu-id="7bb7c-106">屬性</span><span class="sxs-lookup"><span data-stu-id="7bb7c-106">Attributes</span></span>

<span data-ttu-id="7bb7c-107">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="7bb7c-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="7bb7c-108">父/子項目</span><span class="sxs-lookup"><span data-stu-id="7bb7c-108">Parent/Child Elements</span></span>



| <span data-ttu-id="7bb7c-109">階層</span><span class="sxs-lookup"><span data-stu-id="7bb7c-109">Hierarchy</span></span> | <span data-ttu-id="7bb7c-110">元素</span><span class="sxs-lookup"><span data-stu-id="7bb7c-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="7bb7c-111">父代</span><span class="sxs-lookup"><span data-stu-id="7bb7c-111">Parent</span></span>    | [<span data-ttu-id="7bb7c-112">頭</span><span class="sxs-lookup"><span data-stu-id="7bb7c-112">head</span></span>](head-element.md) |
| <span data-ttu-id="7bb7c-113">子系</span><span class="sxs-lookup"><span data-stu-id="7bb7c-113">Child</span></span>     | <span data-ttu-id="7bb7c-114">無</span><span class="sxs-lookup"><span data-stu-id="7bb7c-114">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="7bb7c-115">備註</span><span class="sxs-lookup"><span data-stu-id="7bb7c-115">Remarks</span></span>

<span data-ttu-id="7bb7c-116">選擇 Windows Media 播放清單的標題時 (.WPL) ，請考慮播放清單的內容可以是動態的。</span><span class="sxs-lookup"><span data-stu-id="7bb7c-116">When choosing a title for a Windows Media Playlist (WPL), consider that the content of the playlist can be dynamic.</span></span> <span data-ttu-id="7bb7c-117">一個不錯的方法是以 **引數** 元素的邏輯作為標題，因為這是定義播放清單內容的專案。</span><span class="sxs-lookup"><span data-stu-id="7bb7c-117">A good approach is to base the title on the logic in the **argument** elements because this is what defines the content of the playlist.</span></span> <span data-ttu-id="7bb7c-118">這種情況的範例包括「我最愛的1966中的石頭」或「最近未玩過的 Dance 歌曲」。</span><span class="sxs-lookup"><span data-stu-id="7bb7c-118">Examples of this are "My Favorite Rock Songs from 1966" or "Dance Songs That I Haven't Played Recently".</span></span>

## <a name="examples"></a><span data-ttu-id="7bb7c-119">範例</span><span class="sxs-lookup"><span data-stu-id="7bb7c-119">Examples</span></span>


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a><span data-ttu-id="7bb7c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bb7c-120">Requirements</span></span>



| <span data-ttu-id="7bb7c-121">需求</span><span class="sxs-lookup"><span data-stu-id="7bb7c-121">Requirement</span></span> | <span data-ttu-id="7bb7c-122">值</span><span class="sxs-lookup"><span data-stu-id="7bb7c-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="7bb7c-123">版本</span><span class="sxs-lookup"><span data-stu-id="7bb7c-123">Version</span></span><br/> | <span data-ttu-id="7bb7c-124">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="7bb7c-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7bb7c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7bb7c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb7c-126">**引數元素**</span><span class="sxs-lookup"><span data-stu-id="7bb7c-126">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="7bb7c-127">**head 元素**</span><span class="sxs-lookup"><span data-stu-id="7bb7c-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="7bb7c-128">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="7bb7c-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





