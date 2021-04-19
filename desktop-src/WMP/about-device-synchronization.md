---
title: 關於裝置同步處理
description: 關於裝置同步處理
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player，同步處理裝置
- Windows Media Player 物件模型，同步處理裝置
- 物件模型，同步處理裝置
- Windows Media Player ActiveX 控制項，同步處理裝置
- ActiveX 控制項，同步處理裝置
- Windows Media Player 的行動 ActiveX 控制項，同步處理裝置
- Windows Media Player 行動裝置，同步處理裝置
- 正在同步處理裝置，關於
- 裝置同步處理，關於
- 同步處理裝置，手動轉移
- 裝置同步處理，手動傳輸
- 同步處理裝置，自動同步處理
- 裝置同步處理，自動同步處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967197"
---
# <a name="about-device-synchronization"></a><span data-ttu-id="75655-116">關於裝置同步處理</span><span class="sxs-lookup"><span data-stu-id="75655-116">About Device Synchronization</span></span>

<span data-ttu-id="75655-117">Windows Media Player 10 引進了新的模型，可將數位媒體內容與可攜式裝置進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="75655-117">Windows Media Player 10 introduced a new model for synchronizing digital media content with portable devices.</span></span> <span data-ttu-id="75655-118">從使用者的觀點來看，這表示您可以指定哪些播放清單 (包括自動播放清單) 自動與裝置同步處理。</span><span class="sxs-lookup"><span data-stu-id="75655-118">From the user's perspective, this means you can specify which playlists (including auto playlists) synchronize automatically with devices.</span></span> <span data-ttu-id="75655-119">您也可以手動將數位媒體內容傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="75655-119">You can also manually transfer digital media content to devices.</span></span> <span data-ttu-id="75655-120">從開發人員的觀點來看，這表示您可以在應用程式中充分利用新功能。</span><span class="sxs-lookup"><span data-stu-id="75655-120">From the developer's perspective, this means there is new functionality exposed that you can take advantage of in your applications.</span></span> <span data-ttu-id="75655-121">若要這樣做，您必須建立 Windows Media Player 控制項的遠端實例。</span><span class="sxs-lookup"><span data-stu-id="75655-121">To do this, you must create a remoted instance of the Windows Media Player control.</span></span>

<span data-ttu-id="75655-122">使用者可以透過兩種方式將數位媒體內容複寫到裝置：</span><span class="sxs-lookup"><span data-stu-id="75655-122">There are two ways a user can copy digital media content to a device:</span></span>

-   <span data-ttu-id="75655-123">**手動轉移。**</span><span class="sxs-lookup"><span data-stu-id="75655-123">**Manual transfer.**</span></span> <span data-ttu-id="75655-124">使用者會在媒體櫃中選取數位媒體內容，然後開始將內容傳送到裝置。</span><span class="sxs-lookup"><span data-stu-id="75655-124">The user selects digital media content in the library and then initiates a transfer of the content to the device.</span></span> <span data-ttu-id="75655-125">這與舊版 Windows Media Player 所提供的功能類似。</span><span class="sxs-lookup"><span data-stu-id="75655-125">This is similar to the functionality provided by previous versions of Windows Media Player.</span></span> <span data-ttu-id="75655-126">Windows Media Player SDK 不提供將數位媒體傳送至裝置的方法。</span><span class="sxs-lookup"><span data-stu-id="75655-126">The Windows Media Player SDK does not provide methods for transferring digital media to a device.</span></span>
-   <span data-ttu-id="75655-127">**自動同步處理。**</span><span class="sxs-lookup"><span data-stu-id="75655-127">**Automatic synchronization.**</span></span> <span data-ttu-id="75655-128">使用者指定自動與裝置同步處理的播放清單。</span><span class="sxs-lookup"><span data-stu-id="75655-128">The user specifies playlists that automatically synchronize with the device.</span></span> <span data-ttu-id="75655-129">這是 Windows Media Player 10 或更新版本的功能。</span><span class="sxs-lookup"><span data-stu-id="75655-129">This is a feature of Windows Media Player 10 or later.</span></span> <span data-ttu-id="75655-130">Windows Media Player SDK 提供管理自動同步處理的功能。</span><span class="sxs-lookup"><span data-stu-id="75655-130">The Windows Media Player SDK provides functionality for managing automatic synchronization.</span></span> <span data-ttu-id="75655-131">這項功能的設計目的是讓您為應用程式建立自訂使用者介面，以指定裝置同步處理的執行方式，以及提供狀態資訊給使用者。</span><span class="sxs-lookup"><span data-stu-id="75655-131">This functionality is designed to let you build a custom user interface for your application to specify how device synchronization happens and to provide status information to users.</span></span>

<span data-ttu-id="75655-132">若要讓自動同步處理正常運作，必須在 Windows Media Player 和裝置之間建立特殊的關聯性。</span><span class="sxs-lookup"><span data-stu-id="75655-132">For automatic synchronization to work, a special relationship must be established between Windows Media Player and the device.</span></span> <span data-ttu-id="75655-133">此關聯性稱為 *合作* 關係。</span><span class="sxs-lookup"><span data-stu-id="75655-133">This relationship is called a *partnership*.</span></span>

<span data-ttu-id="75655-134">下列各節提供有關裝置同步處理的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="75655-134">The following sections provide more information about device synchronization.</span></span>

-   [<span data-ttu-id="75655-135">關於裝置</span><span class="sxs-lookup"><span data-stu-id="75655-135">About Devices</span></span>](about-devices.md)
-   [<span data-ttu-id="75655-136">關於合作關係</span><span class="sxs-lookup"><span data-stu-id="75655-136">About Partnerships</span></span>](about-partnerships.md)
-   [<span data-ttu-id="75655-137">關於同步處理引擎</span><span class="sxs-lookup"><span data-stu-id="75655-137">About the Synchronization Engine</span></span>](about-the-synchronization-engine.md)
-   [<span data-ttu-id="75655-138">關於播放清單同步處理</span><span class="sxs-lookup"><span data-stu-id="75655-138">About Playlist Synchronization</span></span>](about-playlist-synchronization.md)

## <a name="related-topics"></a><span data-ttu-id="75655-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="75655-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75655-140">**關於 Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="75655-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="75655-141">**遠端處理 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="75655-141">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="75655-142">**使用可攜式裝置**</span><span class="sxs-lookup"><span data-stu-id="75655-142">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




