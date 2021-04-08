---
title: Controls 物件
description: Controls 物件提供使用下列屬性和方法來操作媒體播放的方式。
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- 控制項物件 Windows Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "103678832"
---
# <a name="controls-object"></a><span data-ttu-id="750ac-104">Controls 物件</span><span class="sxs-lookup"><span data-stu-id="750ac-104">Controls Object</span></span>

<span data-ttu-id="750ac-105">**Controls** 物件提供使用下列屬性和方法來操作媒體播放的方式。</span><span class="sxs-lookup"><span data-stu-id="750ac-105">The **Controls** object provides a way to manipulate the playback of media using the following properties and methods.</span></span>

<span data-ttu-id="750ac-106">**Controls** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="750ac-106">The **Controls** object supports the following properties.</span></span>



| <span data-ttu-id="750ac-107">屬性</span><span class="sxs-lookup"><span data-stu-id="750ac-107">Property</span></span>                                                            | <span data-ttu-id="750ac-108">描述</span><span class="sxs-lookup"><span data-stu-id="750ac-108">Description</span></span>                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="750ac-109">audioLanguageCount</span><span class="sxs-lookup"><span data-stu-id="750ac-109">audioLanguageCount</span></span>](controls-audiolanguagecount.md)               | <span data-ttu-id="750ac-110">抓取支援的音訊語言數目。</span><span class="sxs-lookup"><span data-stu-id="750ac-110">Retrieves the number of supported audio languages.</span></span>                                                                                                |
| [<span data-ttu-id="750ac-111">currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="750ac-111">currentAudioLanguage</span></span>](controls-currentaudiolanguage.md)           | <span data-ttu-id="750ac-112">指定或抓取用來播放音訊語言 (LCID) 的地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="750ac-112">Specifies or retrieves the locale identifier (LCID) of the audio language for playback</span></span>                                                            |
| [<span data-ttu-id="750ac-113">currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="750ac-113">currentAudioLanguageIndex</span></span>](controls-currentaudiolanguageindex.md) | <span data-ttu-id="750ac-114">指定或抓取對應于播放音訊語言的單一索引。</span><span class="sxs-lookup"><span data-stu-id="750ac-114">Specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>                                                   |
| [<span data-ttu-id="750ac-115">currentItem</span><span class="sxs-lookup"><span data-stu-id="750ac-115">currentItem</span></span>](controls-currentitem.md)                             | <span data-ttu-id="750ac-116">指定或抓取目前的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="750ac-116">Specifies or retrieves the current media item.</span></span>                                                                                                    |
| [<span data-ttu-id="750ac-117">currentMarker</span><span class="sxs-lookup"><span data-stu-id="750ac-117">currentMarker</span></span>](controls-currentmarker.md)                         | <span data-ttu-id="750ac-118">指定或抓取目前的標記編號。</span><span class="sxs-lookup"><span data-stu-id="750ac-118">Specifies or retrieves the current marker number.</span></span>                                                                                                 |
| [<span data-ttu-id="750ac-119">currentPosition</span><span class="sxs-lookup"><span data-stu-id="750ac-119">currentPosition</span></span>](controls-currentposition.md)                     | <span data-ttu-id="750ac-120">以秒為單位，指定或抓取媒體專案中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="750ac-120">Specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>                                                      |
| [<span data-ttu-id="750ac-121">currentPositionString</span><span class="sxs-lookup"><span data-stu-id="750ac-121">currentPositionString</span></span>](controls-currentpositionstring.md)         | <span data-ttu-id="750ac-122">以 **字串** 形式捕獲媒體專案中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="750ac-122">Retrieves the current position in the media item as a **String**.</span></span>                                                                                 |
| [<span data-ttu-id="750ac-123">currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="750ac-123">currentPositionTimecode</span></span>](controls-currentpositiontimecode.md)     | <span data-ttu-id="750ac-124">使用時間代碼格式，指定或抓取目前媒體專案中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="750ac-124">Specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="750ac-125">這個屬性目前支援 SMPTE 時間代碼。</span><span class="sxs-lookup"><span data-stu-id="750ac-125">This property currently supports SMPTE time code.</span></span> |
| [<span data-ttu-id="750ac-126">isAvailable</span><span class="sxs-lookup"><span data-stu-id="750ac-126">isAvailable</span></span>](controls-isavailable.md)                             | <span data-ttu-id="750ac-127">抓取指定的資訊類型是否可用，或是否可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="750ac-127">Retrieves whether a specified type of information is available or a given action can be performed.</span></span>                                                |



 

<span data-ttu-id="750ac-128">**Controls** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="750ac-128">The **Controls** object supports the following methods.</span></span>



| <span data-ttu-id="750ac-129">方法</span><span class="sxs-lookup"><span data-stu-id="750ac-129">Method</span></span>                                                                  | <span data-ttu-id="750ac-130">描述</span><span class="sxs-lookup"><span data-stu-id="750ac-130">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="750ac-131">fastForward</span><span class="sxs-lookup"><span data-stu-id="750ac-131">fastForward</span></span>](controls-fastforward.md)                                 | <span data-ttu-id="750ac-132">以正向方向啟動媒體專案的快速播放。</span><span class="sxs-lookup"><span data-stu-id="750ac-132">Starts fast play of the media item in the forward direction.</span></span>                                     |
| [<span data-ttu-id="750ac-133">fastReverse</span><span class="sxs-lookup"><span data-stu-id="750ac-133">fastReverse</span></span>](controls-fastreverse.md)                                 | <span data-ttu-id="750ac-134">以相反方向啟動媒體專案的快速播放。</span><span class="sxs-lookup"><span data-stu-id="750ac-134">Starts fast play of the media item in the reverse direction.</span></span>                                     |
| [<span data-ttu-id="750ac-135">getAudioLanguageDescription</span><span class="sxs-lookup"><span data-stu-id="750ac-135">getAudioLanguageDescription</span></span>](controls-getaudiolanguagedescription.md) | <span data-ttu-id="750ac-136">抓取對應于指定之以一為基礎之索引的音訊語言描述。</span><span class="sxs-lookup"><span data-stu-id="750ac-136">Retrieves the description for the audio language corresponding to the specified one-based index.</span></span> |
| [<span data-ttu-id="750ac-137">getAudioLanguageID</span><span class="sxs-lookup"><span data-stu-id="750ac-137">getAudioLanguageID</span></span>](controls-getaudiolanguageid.md)                   | <span data-ttu-id="750ac-138">抓取指定音訊語言索引的 LCID。</span><span class="sxs-lookup"><span data-stu-id="750ac-138">Retrieves the LCID for a specified audio language index.</span></span>                                         |
| [<span data-ttu-id="750ac-139">getLanguageName</span><span class="sxs-lookup"><span data-stu-id="750ac-139">getLanguageName</span></span>](controls-getlanguagename.md)                         | <span data-ttu-id="750ac-140">使用指定的 LCID 抓取音訊語言的名稱。</span><span class="sxs-lookup"><span data-stu-id="750ac-140">Retrieves the name of the audio language with the specified LCID.</span></span>                                |
| [<span data-ttu-id="750ac-141">下一步</span><span class="sxs-lookup"><span data-stu-id="750ac-141">next</span></span>](controls-next.md)                                               | <span data-ttu-id="750ac-142">將目前的專案設定為播放清單中的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="750ac-142">Sets the current item to the next item in the playlist.</span></span>                                          |
| [<span data-ttu-id="750ac-143">pause</span><span class="sxs-lookup"><span data-stu-id="750ac-143">pause</span></span>](controls-pause.md)                                             | <span data-ttu-id="750ac-144">暫停媒體專案的播放。</span><span class="sxs-lookup"><span data-stu-id="750ac-144">Pauses the playing of the media item.</span></span>                                                            |
| [<span data-ttu-id="750ac-145">玩</span><span class="sxs-lookup"><span data-stu-id="750ac-145">play</span></span>](controls-play.md)                                               | <span data-ttu-id="750ac-146">造成媒體專案開始播放。</span><span class="sxs-lookup"><span data-stu-id="750ac-146">Causes the media item to start playing.</span></span>                                                          |
| [<span data-ttu-id="750ac-147">playItem</span><span class="sxs-lookup"><span data-stu-id="750ac-147">playItem</span></span>](controls-playitem.md)                                       | <span data-ttu-id="750ac-148">導致目前的媒體專案開始播放，或繼續播放暫停的專案。</span><span class="sxs-lookup"><span data-stu-id="750ac-148">Causes the current media item to start playing, or resumes play of a paused item.</span></span>                |
| [<span data-ttu-id="750ac-149">previous</span><span class="sxs-lookup"><span data-stu-id="750ac-149">previous</span></span>](controls-previous.md)                                       | <span data-ttu-id="750ac-150">將目前的專案設定為播放清單中的上一個專案。</span><span class="sxs-lookup"><span data-stu-id="750ac-150">Sets the current item to the previous item in the playlist.</span></span>                                      |
| [<span data-ttu-id="750ac-151">步</span><span class="sxs-lookup"><span data-stu-id="750ac-151">step</span></span>](controls-step.md)                                               | <span data-ttu-id="750ac-152">導致目前的影片媒體專案凍結下一個畫面格的播放。</span><span class="sxs-lookup"><span data-stu-id="750ac-152">Causes the current video media item to freeze playback on the next frame.</span></span>                        |
| [<span data-ttu-id="750ac-153">停止</span><span class="sxs-lookup"><span data-stu-id="750ac-153">stop</span></span>](controls-stop.md)                                               | <span data-ttu-id="750ac-154">停止播放媒體專案。</span><span class="sxs-lookup"><span data-stu-id="750ac-154">Stops the playing of the media item.</span></span>                                                             |



 

<span data-ttu-id="750ac-155">您可以透過下列屬性來存取 **Controls** 物件。</span><span class="sxs-lookup"><span data-stu-id="750ac-155">The **Controls** object is accessed through the following property.</span></span>



| <span data-ttu-id="750ac-156">Object</span><span class="sxs-lookup"><span data-stu-id="750ac-156">Object</span></span>                      | <span data-ttu-id="750ac-157">屬性</span><span class="sxs-lookup"><span data-stu-id="750ac-157">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="750ac-158">球員</span><span class="sxs-lookup"><span data-stu-id="750ac-158">Player</span></span>](player-object.md) | [<span data-ttu-id="750ac-159">控制</span><span class="sxs-lookup"><span data-stu-id="750ac-159">controls</span></span>](player-controls.md) |



 

## <a name="see-also"></a><span data-ttu-id="750ac-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="750ac-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="750ac-161">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="750ac-161">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




