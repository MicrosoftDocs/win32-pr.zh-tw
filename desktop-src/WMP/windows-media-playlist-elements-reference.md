---
title: Windows Media 播放清單元素參考
description: Windows Media 播放清單元素參考
ms.assetid: 3f88d46a-59d3-4200-bf99-a3dddae1b0ac
keywords:
- 'Windows Media 播放清單 (.WPL) '
- '.WPL (Windows Media 播放清單) '
- 'Windows Media、Windows Media 播放清單 (.WPL) '
- '播放清單、Windows Media 播放清單 (.WPL) '
- Windows Media 播放清單的參考
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aad06ba85da09835349bdee5fc604e18379a1eff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932229"
---
# <a name="windows-media-playlist-elements-reference"></a><span data-ttu-id="2ebd6-108">Windows Media 播放清單元素參考</span><span class="sxs-lookup"><span data-stu-id="2ebd6-108">Windows Media Playlist Elements Reference</span></span>

<span data-ttu-id="2ebd6-109">本節包含所有 Windows Media 播放清單元素的參考檔。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-109">This section contains reference documentation for all Windows Media Playlist elements.</span></span> <span data-ttu-id="2ebd6-110">參考專案包含元素的定義、其屬性和值，以及與每個專案相關的特殊條件。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-110">Reference entries include definitions of the elements, their attributes and values, and special conditions related to each element.</span></span>

<span data-ttu-id="2ebd6-111">支援下列播放清單元素。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-111">The following playlist elements are supported.</span></span>



| <span data-ttu-id="2ebd6-112">元素</span><span class="sxs-lookup"><span data-stu-id="2ebd6-112">Element</span></span>                                    | <span data-ttu-id="2ebd6-113">描述</span><span class="sxs-lookup"><span data-stu-id="2ebd6-113">Description</span></span>                                                                                                                                                                                          |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ebd6-114">引數</span><span class="sxs-lookup"><span data-stu-id="2ebd6-114">argument</span></span>](argument-element.md)           | <span data-ttu-id="2ebd6-115">包含條件字串的其中一個部分。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-115">Contains one portion of a condition string.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="2ebd6-116">body</span><span class="sxs-lookup"><span data-stu-id="2ebd6-116">body</span></span>](body-element.md)                   | <span data-ttu-id="2ebd6-117">包含定義播放清單內容的元素。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-117">Contains the elements that define the contents of a playlist.</span></span>                                                                                                                                        |
| [<span data-ttu-id="2ebd6-118">filter</span><span class="sxs-lookup"><span data-stu-id="2ebd6-118">filter</span></span>](filter-element.md)               | <span data-ttu-id="2ebd6-119">包含的元素會限制播放清單的大小、播放清單的持續時間，或播放清單中的媒體專案數目。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-119">Contains elements that limit the size of a playlist, duration of a playlist, or number of media items in a playlist.</span></span>                                                                                 |
| [<span data-ttu-id="2ebd6-120">片段</span><span class="sxs-lookup"><span data-stu-id="2ebd6-120">fragment</span></span>](fragment-element.md)           | <span data-ttu-id="2ebd6-121">指定從程式庫中選取專案之查詢的其中一個條件。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-121">Specifies one condition of the query that selects items from the library.</span></span>                                                                                                                            |
| [<span data-ttu-id="2ebd6-122">頭</span><span class="sxs-lookup"><span data-stu-id="2ebd6-122">head</span></span>](head-element.md)                   | <span data-ttu-id="2ebd6-123">包含適用于整個播放清單的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-123">Contains metadata that applies to the entire playlist.</span></span>                                                                                                                                               |
| [<span data-ttu-id="2ebd6-124">media</span><span class="sxs-lookup"><span data-stu-id="2ebd6-124">media</span></span>](media-element.md)                 | <span data-ttu-id="2ebd6-125">指定播放清單中的其中一個媒體專案。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-125">Specifies one of the media items in a playlist.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="2ebd6-126">元</span><span class="sxs-lookup"><span data-stu-id="2ebd6-126">meta</span></span>](meta-element.md)                   | <span data-ttu-id="2ebd6-127">指定套用至整個播放清單的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-127">Specifies metadata that applies to the entire playlist.</span></span>                                                                                                                                              |
| [<span data-ttu-id="2ebd6-128">querySet</span><span class="sxs-lookup"><span data-stu-id="2ebd6-128">querySet</span></span>](queryset-element.md)           | <span data-ttu-id="2ebd6-129">包含元素，這些元素會定義要從程式庫中選取哪些媒體專案。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-129">Contains elements that define which media items will be selected from the library.</span></span>                                                                                                                   |
| [<span data-ttu-id="2ebd6-130">序列</span><span class="sxs-lookup"><span data-stu-id="2ebd6-130">seq</span></span>](seq-element.md)                     | <span data-ttu-id="2ebd6-131">包含定義靜態播放清單的元素，或定義智慧播放清單的元素。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-131">Contains elements that define a static playlist or elements that define a smart playlist.</span></span>                                                                                                            |
| [<span data-ttu-id="2ebd6-132">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="2ebd6-132">smartPlaylist</span></span>](smartplaylist-element.md) | <span data-ttu-id="2ebd6-133">包含動態定義的播放清單部分。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-133">Contains the dynamically defined portion of a playlist.</span></span>                                                                                                                                              |
| [<span data-ttu-id="2ebd6-134">Smil</span><span class="sxs-lookup"><span data-stu-id="2ebd6-134">smil</span></span>](smil-element.md)                   | <span data-ttu-id="2ebd6-135">**Smil** 元素一律是 Windows Media 播放清單中的最上層元素， (.wpl) 檔。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-135">The **smil** element is always the top-level element in a Windows Media Playlist (WPL) file.</span></span> <span data-ttu-id="2ebd6-136">它會指定檔案使用 SMIL (同步處理的多媒體整合語言) 語法和文法。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-136">It specifies that the file uses SMIL (Synchronized Multimedia Integration Language) syntax and grammar.</span></span> |
| [<span data-ttu-id="2ebd6-137">sourceFilter</span><span class="sxs-lookup"><span data-stu-id="2ebd6-137">sourceFilter</span></span>](sourcefilter-element.md)   | <span data-ttu-id="2ebd6-138">包含從程式庫中選取專案的元素。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-138">Contains elements that select items from a library.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="2ebd6-139">title</span><span class="sxs-lookup"><span data-stu-id="2ebd6-139">title</span></span>](title-element--wpl.md)            | <span data-ttu-id="2ebd6-140">指定播放清單的標題。</span><span class="sxs-lookup"><span data-stu-id="2ebd6-140">Specifies a title for the playlist.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="2ebd6-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ebd6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ebd6-142">**Windows Media 播放清單**</span><span class="sxs-lookup"><span data-stu-id="2ebd6-142">**Windows Media Playlists**</span></span>](windows-media-playlists.md)
</dt> </dl>

 

 




