---
title: PLAYER 元素
description: PLAYER 元素
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Windows Media Player 的面板、播放機元素
- 面板、播放機元素
- PLAYER 元素
- 面板的參考、播放程式元素
- 元素，播放者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092291"
---
# <a name="player-element"></a><span data-ttu-id="a75c6-108">PLAYER 元素</span><span class="sxs-lookup"><span data-stu-id="a75c6-108">PLAYER Element</span></span>

<span data-ttu-id="a75c6-109">**Player** 元素可讓您定義事件處理常式，並在面板定義檔內的設計階段指定 **PLAYER** 物件的 **URL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a75c6-109">The **PLAYER** element lets you define event handlers and specify the **URL** property of the **Player** object at design time within a skin definition file.</span></span> <span data-ttu-id="a75c6-110">在腳本程式碼中， **player** 物件是透過 **player** global 屬性來存取，而不是透過由 **player** 元素不支援的 **識別碼** 屬性所指定的名稱來存取。</span><span class="sxs-lookup"><span data-stu-id="a75c6-110">Within script code, the **Player** object is accessed through the **player** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **PLAYER** element.</span></span>

<span data-ttu-id="a75c6-111">**PLAYER** 元素支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a75c6-111">The **PLAYER** element supports the following attribute.</span></span>



| <span data-ttu-id="a75c6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a75c6-112">Attribute</span></span>             | <span data-ttu-id="a75c6-113">描述</span><span class="sxs-lookup"><span data-stu-id="a75c6-113">Description</span></span>                                          |
|-----------------------|------------------------------------------------------|
| [<span data-ttu-id="a75c6-114">URL</span><span class="sxs-lookup"><span data-stu-id="a75c6-114">URL</span></span>](player-url.md) | <span data-ttu-id="a75c6-115">指定或抓取要播放的檔案名。</span><span class="sxs-lookup"><span data-stu-id="a75c6-115">Specifies or retrieves the name of the file to play.</span></span> |



 

<span data-ttu-id="a75c6-116">**Player** 元素可以針對從 **PLAYER** 物件引發的下列事件，執行事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="a75c6-116">The **PLAYER** element can implement event handlers for the following events fired from the **Player** object.</span></span>



| <span data-ttu-id="a75c6-117">事件</span><span class="sxs-lookup"><span data-stu-id="a75c6-117">Event</span></span>                                                                                            | <span data-ttu-id="a75c6-118">描述</span><span class="sxs-lookup"><span data-stu-id="a75c6-118">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="a75c6-119">AudioLanguageChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-119">AudioLanguageChange</span></span>](player-player-audiolanguagechange.md)                                     | <span data-ttu-id="a75c6-120">發生于目前的音訊語言變更時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-120">Occurs when the current audio language changes.</span></span>                                  |
| [<span data-ttu-id="a75c6-121">緩衝處理</span><span class="sxs-lookup"><span data-stu-id="a75c6-121">Buffering</span></span>](player-player-buffering.md)                                                         | <span data-ttu-id="a75c6-122">當 Windows Media Player 開始或結束緩衝時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-122">Occurs when Windows Media Player begins or ends buffering.</span></span>                       |
| [<span data-ttu-id="a75c6-123">CdromMediaChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-123">CdromMediaChange</span></span>](player-player-cdrommediachange.md)                                           | <span data-ttu-id="a75c6-124">當 CD 媒體變更時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-124">Occurs when the CD media changes.</span></span>                                                |
| [<span data-ttu-id="a75c6-125">CurrentItemChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-125">CurrentItemChange</span></span>](player-player-currentitemchange.md)                                         | <span data-ttu-id="a75c6-126">發生于目前專案變更時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-126">Occurs when the current item changes.</span></span>                                            |
| [<span data-ttu-id="a75c6-127">CurrentMediaItemAvailable</span><span class="sxs-lookup"><span data-stu-id="a75c6-127">CurrentMediaItemAvailable</span></span>](player-player-currentmediaitemavailable.md)                         | <span data-ttu-id="a75c6-128">發生于目前的媒體專案變成可用時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-128">Occurs when the current media item becomes available.</span></span>                            |
| [<span data-ttu-id="a75c6-129">CurrentPlaylistChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-129">CurrentPlaylistChange</span></span>](player-player-currentplaylistchange.md)                                 | <span data-ttu-id="a75c6-130">發生于目前的播放清單變更時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-130">Occurs when the current playlist changes.</span></span>                                        |
| [<span data-ttu-id="a75c6-131">CurrentPlaylistItemAvailable</span><span class="sxs-lookup"><span data-stu-id="a75c6-131">CurrentPlaylistItemAvailable</span></span>](player-player-currentplaylistitemavailable.md)                   | <span data-ttu-id="a75c6-132">發生于目前的播放清單專案變成可用時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-132">Occurs when the current playlist item becomes available.</span></span>                         |
| [<span data-ttu-id="a75c6-133">DomainChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-133">DomainChange</span></span>](player-player-domainchange.md)                                                   | <span data-ttu-id="a75c6-134">發生于 DVD 網域變更時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-134">Occurs when the DVD domain changes.</span></span>                                              |
| [<span data-ttu-id="a75c6-135">錯誤</span><span class="sxs-lookup"><span data-stu-id="a75c6-135">Error</span></span>](player-player-error.md)                                                                 | <span data-ttu-id="a75c6-136">當 Windows Media Player 控制項有錯誤條件時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-136">Occurs when the Windows Media Player control has an error condition.</span></span>             |
| [<span data-ttu-id="a75c6-137">MarkerHit</span><span class="sxs-lookup"><span data-stu-id="a75c6-137">MarkerHit</span></span>](player-player-markerhit.md)                                                         | <span data-ttu-id="a75c6-138">當 Windows Media Player 在剪輯中遇到標記時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-138">Occurs when Windows Media Player encounters a marker in the clip.</span></span>                |
| [<span data-ttu-id="a75c6-139">MediaChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-139">MediaChange</span></span>](player-player-mediachange.md)                                                     | <span data-ttu-id="a75c6-140">發生于媒體專案變更時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-140">Occurs when a media item changes.</span></span>                                                |
| [<span data-ttu-id="a75c6-141">MediaCollectionAttributeStringAdded</span><span class="sxs-lookup"><span data-stu-id="a75c6-141">MediaCollectionAttributeStringAdded</span></span>](player-player-mediacollectionattributestringadded.md)     | <span data-ttu-id="a75c6-142">當屬性值新增至程式庫時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-142">Occurs when an attribute value is added to the library.</span></span>                          |
| [<span data-ttu-id="a75c6-143">MediaCollectionAttributeStringChanged</span><span class="sxs-lookup"><span data-stu-id="a75c6-143">MediaCollectionAttributeStringChanged</span></span>](player-player-mediacollectionattributestringchanged.md) | <span data-ttu-id="a75c6-144">發生于程式庫中的屬性值變更時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-144">Occurs when an attribute value in the library is changed.</span></span>                        |
| [<span data-ttu-id="a75c6-145">MediaCollectionAttributeStringRemoved</span><span class="sxs-lookup"><span data-stu-id="a75c6-145">MediaCollectionAttributeStringRemoved</span></span>](player-player-mediacollectionattributestringremoved.md) | <span data-ttu-id="a75c6-146">從程式庫移除屬性值時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-146">Occurs when an attribute value is removed from the library.</span></span>                      |
| [<span data-ttu-id="a75c6-147">MediaCollectionChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-147">MediaCollectionChange</span></span>](player-player-mediacollectionchange.md)                                 | <span data-ttu-id="a75c6-148">當 **MediaCollection** 物件變更時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-148">Occurs when the **MediaCollection** object changes.</span></span>                              |
| [<span data-ttu-id="a75c6-149">MediaError</span><span class="sxs-lookup"><span data-stu-id="a75c6-149">MediaError</span></span>](player-player-mediaerror.md)                                                       | <span data-ttu-id="a75c6-150">發生于 **媒體** 物件有錯誤狀況時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-150">Occurs when the **Media** object has an error condition.</span></span>                         |
| [<span data-ttu-id="a75c6-151">ModeChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-151">ModeChange</span></span>](player-player-modechange.md)                                                       | <span data-ttu-id="a75c6-152">在隨機和一般模式之間切換時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-152">Occurs when switching between shuffle and normal mode.</span></span>                           |
| [<span data-ttu-id="a75c6-153">OpenPlaylistSwitch</span><span class="sxs-lookup"><span data-stu-id="a75c6-153">OpenPlaylistSwitch</span></span>](player-player-openplaylistswitch.md)                                       | <span data-ttu-id="a75c6-154">發生于 DVD 上的標題開始播放時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-154">Occurs when a title on a DVD begins playing.</span></span>                                     |
| [<span data-ttu-id="a75c6-155">OpenStateChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-155">OpenStateChange</span></span>](player-player-openstatechange.md)                                             | <span data-ttu-id="a75c6-156">發生于 *播放玩家*。**openState** 變更。</span><span class="sxs-lookup"><span data-stu-id="a75c6-156">Occurs when *player*.**openState** changes.</span></span>                                      |
| [<span data-ttu-id="a75c6-157">PlaylistChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-157">PlaylistChange</span></span>](player-player-playlistchange.md)                                               | <span data-ttu-id="a75c6-158">當播放清單變更時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-158">Occurs when a playlist changes.</span></span>                                                  |
| [<span data-ttu-id="a75c6-159">PlaylistCollectionChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-159">PlaylistCollectionChange</span></span>](player-player-playlistcollectionchange.md)                           | <span data-ttu-id="a75c6-160">發生于播放清單集合中的某些變更時。</span><span class="sxs-lookup"><span data-stu-id="a75c6-160">Occurs when something changes in the playlist collection.</span></span>                        |
| [<span data-ttu-id="a75c6-161">PlaylistCollectionPlaylistAdded</span><span class="sxs-lookup"><span data-stu-id="a75c6-161">PlaylistCollectionPlaylistAdded</span></span>](player-player-playlistcollectionplaylistadded.md)             | <span data-ttu-id="a75c6-162">當播放清單新增至播放清單集合時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-162">Occurs when a playlist is added to the playlist collection.</span></span>                      |
| [<span data-ttu-id="a75c6-163">PlaylistCollectionPlaylistRemoved</span><span class="sxs-lookup"><span data-stu-id="a75c6-163">PlaylistCollectionPlaylistRemoved</span></span>](player-player-playlistcollectionplaylistremoved.md)         | <span data-ttu-id="a75c6-164">從播放清單集合移除播放清單時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-164">Occurs when a playlist is removed from the playlist collection.</span></span>                  |
| [<span data-ttu-id="a75c6-165">PlayStateChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-165">PlayStateChange</span></span>](player-player-playstatechange.md)                                             | <span data-ttu-id="a75c6-166">發生于 *播放玩家*。**playState** 變更。</span><span class="sxs-lookup"><span data-stu-id="a75c6-166">Occurs when *player*.**playState** changes.</span></span>                                      |
| [<span data-ttu-id="a75c6-167">PositionChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-167">PositionChange</span></span>](player-player-positionchange.md)                                               | <span data-ttu-id="a75c6-168">發生于 *播放玩家*。*控制項*。**currentPosition** 變更。</span><span class="sxs-lookup"><span data-stu-id="a75c6-168">Occurs when *player*.*controls*.**currentPosition** changes.</span></span>                     |
| [<span data-ttu-id="a75c6-169">ScriptCommand</span><span class="sxs-lookup"><span data-stu-id="a75c6-169">ScriptCommand</span></span>](player-player-scriptcommand.md)                                                 | <span data-ttu-id="a75c6-170">當 Windows Media Player 遇到內嵌于檔案中的指令碼命令時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-170">Occurs when Windows Media Player encounters a script command embedded in a file.</span></span> |
| [<span data-ttu-id="a75c6-171">StatusChange</span><span class="sxs-lookup"><span data-stu-id="a75c6-171">StatusChange</span></span>](player-player-statuschange.md)                                                   | <span data-ttu-id="a75c6-172">當 **status** 屬性變更值時發生。</span><span class="sxs-lookup"><span data-stu-id="a75c6-172">Occurs when the **status** property changes value.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="a75c6-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="a75c6-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a75c6-174">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="a75c6-174">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="a75c6-175">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="a75c6-175">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




