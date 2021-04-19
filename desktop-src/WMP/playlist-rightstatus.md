---
title: 播放清單。 rightStatus
description: RightStatus 屬性會指定或抓取播放清單元素右側和底部顯示的狀態文字。
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- 播放清單. rightStatus Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b382da4ae214c9a830cc64fb1aa0d0edadbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989760"
---
# <a name="playlistrightstatus"></a><span data-ttu-id="bd1eb-104">播放清單。 rightStatus</span><span class="sxs-lookup"><span data-stu-id="bd1eb-104">PLAYLIST.rightStatus</span></span>

<span data-ttu-id="bd1eb-105">**RightStatus** 屬性會指定或抓取 **播放清單** 元素右側和底部顯示的狀態文字。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-105">The **rightStatus** attribute specifies or retrieves the status text that is displayed on the right side and bottom of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a><span data-ttu-id="bd1eb-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="bd1eb-106">Possible Values</span></span>

<span data-ttu-id="bd1eb-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd1eb-108">備註</span><span class="sxs-lookup"><span data-stu-id="bd1eb-108">Remarks</span></span>

<span data-ttu-id="bd1eb-109">這個屬性可以將任何文字與特定關鍵字合併，以顯示所需的資訊，例如播放清單的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-109">This attribute can combine any text with specific keywords that will display the desired information, such as the total duration of the playlist.</span></span> <span data-ttu-id="bd1eb-110">關鍵字會以百分比符號括住 (% ) ，以保持與一般文字不同。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-110">The keywords are surrounded by percentage symbols (%) to keep them distinct from the ordinary text.</span></span>

<span data-ttu-id="bd1eb-111">您可以使用下列關鍵字。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-111">The following keywords can be used.</span></span>



| <span data-ttu-id="bd1eb-112">關鍵字</span><span class="sxs-lookup"><span data-stu-id="bd1eb-112">Keyword</span></span>               | <span data-ttu-id="bd1eb-113">描述</span><span class="sxs-lookup"><span data-stu-id="bd1eb-113">Description</span></span>                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd1eb-114">count</span><span class="sxs-lookup"><span data-stu-id="bd1eb-114">count</span></span>                 | <span data-ttu-id="bd1eb-115">播放清單中的專案數。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-115">Number of items in the playlist.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="bd1eb-116">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="bd1eb-116">size</span></span>                  | <span data-ttu-id="bd1eb-117">播放清單的總大小。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-117">Total size of the playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="bd1eb-118">duration</span><span class="sxs-lookup"><span data-stu-id="bd1eb-118">duration</span></span>              | <span data-ttu-id="bd1eb-119">播放清單的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-119">Total duration of the playlist.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="bd1eb-120">*Xxx*</span><span class="sxs-lookup"><span data-stu-id="bd1eb-120">*XXX*</span></span>                 | <span data-ttu-id="bd1eb-121">在具有 *XXX* 的播放清單上執行 **getItemInfo** ，這是要接收的專案。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-121">Does a **getItemInfo** on the playlist with *XXX* being the item to receive.</span></span>                                                                                                                                 |
| <span data-ttu-id="bd1eb-122">Suitablesize</span><span class="sxs-lookup"><span data-stu-id="bd1eb-122">SelectedSize</span></span>          | <span data-ttu-id="bd1eb-123">播放清單中所選取專案的總大小。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-123">Total size of the selected entries in the playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="bd1eb-124">Selectedcount 個</span><span class="sxs-lookup"><span data-stu-id="bd1eb-124">SelectedCount</span></span>         | <span data-ttu-id="bd1eb-125">播放清單中選取的專案總數。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-125">Total number of selected entries in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="bd1eb-126">SelectedDuration</span><span class="sxs-lookup"><span data-stu-id="bd1eb-126">SelectedDuration</span></span>      | <span data-ttu-id="bd1eb-127">播放清單中所選取專案的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-127">Total duration of the selected entries in the playlist.</span></span>                                                                                                                                                      |
| <span data-ttu-id="bd1eb-128">CheckedCount</span><span class="sxs-lookup"><span data-stu-id="bd1eb-128">CheckedCount</span></span>          | <span data-ttu-id="bd1eb-129">播放清單中的已檢查曲目總數。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-129">Total number of checked tracks in the playlist.</span></span>                                                                                                                                                              |
| <span data-ttu-id="bd1eb-130">CheckedDuration</span><span class="sxs-lookup"><span data-stu-id="bd1eb-130">CheckedDuration</span></span>       | <span data-ttu-id="bd1eb-131">播放清單中已檢查曲目的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-131">Total duration of the checked tracks in the playlist.</span></span>                                                                                                                                                        |
| <span data-ttu-id="bd1eb-132">CheckedSize</span><span class="sxs-lookup"><span data-stu-id="bd1eb-132">CheckedSize</span></span>           | <span data-ttu-id="bd1eb-133">播放清單中已檢查曲目的總大小。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-133">Total size of the checked tracks in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="bd1eb-134">DurationString</span><span class="sxs-lookup"><span data-stu-id="bd1eb-134">DurationString</span></span>        | <span data-ttu-id="bd1eb-135">根據是否知道總計值，顯示將持續時間描述為「總時間」或「估計時間」的文字。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-135">Displays text that describes the duration as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="bd1eb-136">此文字後面接著 "% duration%"。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-136">This text is followed by "%duration%".</span></span>                                       |
| <span data-ttu-id="bd1eb-137">CheckedDurationString</span><span class="sxs-lookup"><span data-stu-id="bd1eb-137">CheckedDurationString</span></span> | <span data-ttu-id="bd1eb-138">根據是否知道總計值，顯示描述播放清單中所有已核取專案之持續時間的文字（以「總時間」或「估計時間」為依據）。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-138">Displays text that describes the duration for all checked items in the playlist as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="bd1eb-139">此文字後面接著 "% duration%"。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-139">This text is followed by "%duration%".</span></span> |



 

<span data-ttu-id="bd1eb-140">若播放清單中包含七分鐘的總持續時間，則其值為 "Total Time：% duration%"，將會顯示 "Total Time： 07:00"。</span><span class="sxs-lookup"><span data-stu-id="bd1eb-140">The value "Total Time: %duration%" for a playlist that contains a total duration of seven minutes will display "Total Time: 07:00".</span></span>

## <a name="requirements"></a><span data-ttu-id="bd1eb-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd1eb-141">Requirements</span></span>



| <span data-ttu-id="bd1eb-142">需求</span><span class="sxs-lookup"><span data-stu-id="bd1eb-142">Requirement</span></span> | <span data-ttu-id="bd1eb-143">值</span><span class="sxs-lookup"><span data-stu-id="bd1eb-143">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="bd1eb-144">版本</span><span class="sxs-lookup"><span data-stu-id="bd1eb-144">Version</span></span><br/> | <span data-ttu-id="bd1eb-145">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="bd1eb-145">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd1eb-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd1eb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd1eb-147">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="bd1eb-147">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





