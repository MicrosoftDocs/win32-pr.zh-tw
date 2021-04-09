---
title: 優先順序
description: 優先順序
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Windows Media 中繼檔，優先權順序
- Windows Media 中繼檔，優先順序
- 中繼檔，優先權順序
- 中繼檔，優先順序
- Windows Media，中繼檔
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021101"
---
# <a name="order-of-precedence"></a><span data-ttu-id="2bd46-108">優先順序</span><span class="sxs-lookup"><span data-stu-id="2bd46-108">Order of Precedence</span></span>

<span data-ttu-id="2bd46-109">並非所有的中繼檔元素屬性都有相等的建立。</span><span class="sxs-lookup"><span data-stu-id="2bd46-109">Not all metafile element attributes are created equal.</span></span> <span data-ttu-id="2bd46-110">某些中繼檔元素屬性會覆寫其他元素屬性。</span><span class="sxs-lookup"><span data-stu-id="2bd46-110">Some metafile element attributes override other element attributes.</span></span> <span data-ttu-id="2bd46-111">專案屬性可以根據位置和順序，依據類似的元素屬性來覆寫。</span><span class="sxs-lookup"><span data-stu-id="2bd46-111">Element attributes can be overridden by similar element attributes depending on position and order.</span></span> <span data-ttu-id="2bd46-112">中繼檔播放清單的任何屬性都會覆寫參考的 Windows Media 檔案中包含的屬性。</span><span class="sxs-lookup"><span data-stu-id="2bd46-112">Any attributes of a metafile playlist override those contained in a referenced Windows Media file.</span></span> <span data-ttu-id="2bd46-113">覆寫另一個屬性的屬性會有較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="2bd46-113">An attribute that overrides another has higher precedence.</span></span>

<span data-ttu-id="2bd46-114">下表顯示階層（最高優先順序到最低）。</span><span class="sxs-lookup"><span data-stu-id="2bd46-114">The hierarchy, highest precedence to lowest, is shown in the following table.</span></span> <span data-ttu-id="2bd46-115">永遠不會覆寫最高優先順序的專案。</span><span class="sxs-lookup"><span data-stu-id="2bd46-115">The highest precedence item is never overridden.</span></span>



| <span data-ttu-id="2bd46-116">影響範圍</span><span class="sxs-lookup"><span data-stu-id="2bd46-116">Scope</span></span>                    | <span data-ttu-id="2bd46-117">階層</span><span class="sxs-lookup"><span data-stu-id="2bd46-117">Hierarchy</span></span>                                   |
|--------------------------|---------------------------------------------|
| <span data-ttu-id="2bd46-118">「簽署的 DRM 內容」</span><span class="sxs-lookup"><span data-stu-id="2bd46-118">"Signed DRM content"</span></span>     | <span data-ttu-id="2bd46-119">永遠不會覆寫。</span><span class="sxs-lookup"><span data-stu-id="2bd46-119">Never overridden.</span></span>                           |
| <span data-ttu-id="2bd46-120">**REF** 元素範圍</span><span class="sxs-lookup"><span data-stu-id="2bd46-120">**REF** element scope</span></span>    | <span data-ttu-id="2bd46-121">僅由已簽署的 DRM 內容覆寫。</span><span class="sxs-lookup"><span data-stu-id="2bd46-121">Only overridden by signed DRM content.</span></span>      |
| <span data-ttu-id="2bd46-122">**ENTRY** 元素範圍</span><span class="sxs-lookup"><span data-stu-id="2bd46-122">**ENTRY** element scope</span></span>  | <span data-ttu-id="2bd46-123">覆寫下列類別目錄的元素。</span><span class="sxs-lookup"><span data-stu-id="2bd46-123">Overrides elements of the categories below.</span></span> |
| <span data-ttu-id="2bd46-124">**ASX** 範圍</span><span class="sxs-lookup"><span data-stu-id="2bd46-124">**ASX** scope</span></span>            | <span data-ttu-id="2bd46-125">覆寫媒體檔案元素。</span><span class="sxs-lookup"><span data-stu-id="2bd46-125">Overrides media file elements.</span></span>              |
| <span data-ttu-id="2bd46-126">Windows Media 檔案範圍</span><span class="sxs-lookup"><span data-stu-id="2bd46-126">Windows Media file scope</span></span> | <span data-ttu-id="2bd46-127">由上述所有的覆寫。</span><span class="sxs-lookup"><span data-stu-id="2bd46-127">Overridden by all of the above.</span></span>             |



 

-   <span data-ttu-id="2bd46-128">「簽署的 DRM 內容」-數位簽章物件。</span><span class="sxs-lookup"><span data-stu-id="2bd46-128">"Signed DRM content" - Digital signature object.</span></span>

    <span data-ttu-id="2bd46-129">已簽署 DRM 內容的屬性將會覆寫所有其他屬性。</span><span class="sxs-lookup"><span data-stu-id="2bd46-129">Attributes of Signed DRM content will override all others.</span></span> <span data-ttu-id="2bd46-130">例如，將不會覆寫「簽署的 DRM 內容」的著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="2bd46-130">For example, the Copyright information of "Signed DRM content" will not be overridden.</span></span> <span data-ttu-id="2bd46-131">它一律會進行資料流程處理和呈現。</span><span class="sxs-lookup"><span data-stu-id="2bd46-131">It will always be streamed and presented.</span></span>

-   <span data-ttu-id="2bd46-132">**REF** 元素範圍</span><span class="sxs-lookup"><span data-stu-id="2bd46-132">**REF** element scope</span></span>

    <span data-ttu-id="2bd46-133">**REF** 元素的屬性將會覆寫其他元素屬性，但不會覆寫已簽署的 DRM 內容。</span><span class="sxs-lookup"><span data-stu-id="2bd46-133">Attributes of the **REF** element will override other element attributes, but not signed DRM content.</span></span>

-   <span data-ttu-id="2bd46-134">**專案** 範圍</span><span class="sxs-lookup"><span data-stu-id="2bd46-134">**ENTRY** scope</span></span>

    <span data-ttu-id="2bd46-135">**專案專案** 的屬性將會由 **REF** 元素屬性覆寫，但會覆寫其他元素屬性。</span><span class="sxs-lookup"><span data-stu-id="2bd46-135">Attributes of the **ENTRY** element will be overridden by the **REF** element attribute but will override other element attributes.</span></span> <span data-ttu-id="2bd46-136">**輸入專案專案** 的 **標題** 中繼資料會顯示，而不是來自媒體檔案的標題資訊。</span><span class="sxs-lookup"><span data-stu-id="2bd46-136">**TITLE** metadata from the **ENTRY** element is displayed instead of the title information from the media file.</span></span>

-   <span data-ttu-id="2bd46-137">**ASX** 範圍</span><span class="sxs-lookup"><span data-stu-id="2bd46-137">**ASX** scope</span></span>

    <span data-ttu-id="2bd46-138">在中繼檔中輸入的任何屬性都會覆寫 Windows Media 檔案中包含的屬性。</span><span class="sxs-lookup"><span data-stu-id="2bd46-138">Any properties that are entered in the metafile override those contained in the Windows Media file.</span></span> <span data-ttu-id="2bd46-139">**專案專案** 的屬性會覆寫 **ASX** 元素屬性。</span><span class="sxs-lookup"><span data-stu-id="2bd46-139">Attributes of the **ENTRY** element override **ASX** element attributes.</span></span> <span data-ttu-id="2bd46-140">在播放 **專案專案** 的參考 media 剪輯時，會顯示來自 **輸入** 元素的 **標題** 中繼資料，而不是來自 **ASX** 元素的標題資訊。</span><span class="sxs-lookup"><span data-stu-id="2bd46-140">While the **ENTRY** element's referenced media clip is playing, **TITLE** metadata from the **ENTRY** element is displayed instead of title information from the **ASX** element.</span></span>

-   <span data-ttu-id="2bd46-141">Windows Media 檔案範圍</span><span class="sxs-lookup"><span data-stu-id="2bd46-141">Windows Media file scope</span></span>

    <span data-ttu-id="2bd46-142">Windows Media 檔案的屬性會由任何元檔案屬性覆寫。</span><span class="sxs-lookup"><span data-stu-id="2bd46-142">Attributes of the Windows Media file are overridden by any metafile attributes.</span></span> <span data-ttu-id="2bd46-143">只有在中繼檔中沒有針對該元素定義的中繼資料時，才會顯示媒體檔案中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2bd46-143">Media file metadata is displayed only if there is no metadata defined for that element in the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bd46-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="2bd46-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bd46-145">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="2bd46-145">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="2bd46-146">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="2bd46-146">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="2bd46-147">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="2bd46-147">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="2bd46-148">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="2bd46-148">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




