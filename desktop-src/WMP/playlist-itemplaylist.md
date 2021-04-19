---
title: 播放清單。 itemPlaylist
description: ItemPlaylist 屬性會抓取播放清單元素中指定索引處所顯示媒體專案的播放清單。
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- 播放清單. itemPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999501"
---
# <a name="playlistitemplaylist"></a><span data-ttu-id="28470-104">播放清單。 itemPlaylist</span><span class="sxs-lookup"><span data-stu-id="28470-104">PLAYLIST.itemPlaylist</span></span>

<span data-ttu-id="28470-105">**ItemPlaylist** 屬性會抓取 **播放清單** 元素中指定索引處所顯示媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="28470-105">The **itemPlaylist** attribute retrieves the playlist for the media item that is displayed at the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a><span data-ttu-id="28470-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="28470-106">Possible Values</span></span>

<span data-ttu-id="28470-107">這個屬性是唯讀的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="28470-107">This attribute is a read-only **Playlist** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="28470-108">參數</span><span class="sxs-lookup"><span data-stu-id="28470-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28470-109"><span id="index"></span><span id="INDEX"></span>*指數*</span><span class="sxs-lookup"><span data-stu-id="28470-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="28470-110">包含播放清單專案索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="28470-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28470-111">備註</span><span class="sxs-lookup"><span data-stu-id="28470-111">Remarks</span></span>

<span data-ttu-id="28470-112">**ItemPlaylist** 屬性會傳回播放 **清單** 元素中展開的播放清單物件。</span><span class="sxs-lookup"><span data-stu-id="28470-112">The **itemPlaylist** property will return the playlist object that is expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="28470-113">例如，如果有兩個未在 **播放清單** 元素中展開的嵌套播放清單，且其中包含三個媒體剪輯， **itemPlaylist** (1) 將會傳回包含兩個嵌套播放清單的父播放清單。</span><span class="sxs-lookup"><span data-stu-id="28470-113">For example, if there are two nested playlists that are not expanded in the **PLAYLIST** element, and that contain three media clips each, **itemPlaylist**(1) will return the parent playlist that contains the two nested playlists.</span></span> <span data-ttu-id="28470-114">如果展開第二個播放清單， **itemPlaylist** (1) 將會傳回第二個播放清單。</span><span class="sxs-lookup"><span data-stu-id="28470-114">If the second playlist is expanded, **itemPlaylist**(1) will return the second playlist.</span></span> <span data-ttu-id="28470-115">如果這兩個播放清單都已展開， **itemPlaylist** (1) 將會傳回第一個播放清單。</span><span class="sxs-lookup"><span data-stu-id="28470-115">If both playlists are expanded, **itemPlaylist**(1) will return the first playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="28470-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="28470-116">Requirements</span></span>



| <span data-ttu-id="28470-117">需求</span><span class="sxs-lookup"><span data-stu-id="28470-117">Requirement</span></span> | <span data-ttu-id="28470-118">值</span><span class="sxs-lookup"><span data-stu-id="28470-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="28470-119">版本</span><span class="sxs-lookup"><span data-stu-id="28470-119">Version</span></span><br/> | <span data-ttu-id="28470-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="28470-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28470-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28470-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28470-122">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="28470-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="28470-123">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="28470-123">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





