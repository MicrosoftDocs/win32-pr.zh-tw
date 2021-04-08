---
title: MCIWnd 視窗消費者介面
description: MCIWnd 視窗消費者介面
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021064"
---
# <a name="mciwnd-window-user-interface"></a><span data-ttu-id="b0fb8-103">MCIWnd 視窗消費者介面</span><span class="sxs-lookup"><span data-stu-id="b0fb8-103">MCIWnd Window User Interface</span></span>

<span data-ttu-id="b0fb8-104">MCIWnd 提供額外的功能來調整 MCIWnd 視窗的外觀、自訂應用程式的行為，以及調整播放效能。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-104">MCIWnd provides additional features to adjust the look of the MCIWnd window, customize the behavior of your application, and tune playback performance.</span></span> <span data-ttu-id="b0fb8-105">MCIWnd 視窗包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="b0fb8-105">The following features are included in the MCIWnd window:</span></span>

-   <span data-ttu-id="b0fb8-106">具有 **播放**、 **停止**、 **錄製** 和 **功能表** 按鈕的工具列</span><span class="sxs-lookup"><span data-stu-id="b0fb8-106">A toolbar with **Play**, **Stop**, **Record** and **Menu** buttons</span></span>
-   <span data-ttu-id="b0fb8-107">控制播放內容中之位置的播放程式</span><span class="sxs-lookup"><span data-stu-id="b0fb8-107">A trackbar that controls positioning within the playback content</span></span>
-   <span data-ttu-id="b0fb8-108">包含常用命令的快顯功能表</span><span class="sxs-lookup"><span data-stu-id="b0fb8-108">A pop-up menu containing common commands</span></span>
-   <span data-ttu-id="b0fb8-109">顯示影像的影片和其他裝置的播放區域</span><span class="sxs-lookup"><span data-stu-id="b0fb8-109">A playback area for video and other devices that display images</span></span>

<span data-ttu-id="b0fb8-110">下圖顯示使用者控制的影片播放初始狀態。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-110">The following illustration shows the initial state of user-controlled video playback.</span></span> <span data-ttu-id="b0fb8-111">使用的範例檔案是 CLOCK.AVI。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-111">The sample file used is CLOCK.AVI.</span></span>

![clock.avi 映射](images/mciwnd1.gif)

<span data-ttu-id="b0fb8-113">MCIWnd 視窗包含影片的播放區域，以及播放期間顯示影像的其他裝置。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-113">The MCIWnd window includes a playback area for video and other devices that display images during playback.</span></span> <span data-ttu-id="b0fb8-114">MCIWnd 會略過波形-音訊裝置、MIDI sequencers，以及未寫入顯示器的其他裝置的播放區域。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-114">MCIWnd omits the playback area from waveform-audio devices, MIDI sequencers, and other devices that do not write to the display.</span></span> <span data-ttu-id="b0fb8-115">下圖顯示波形音訊播放區域。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-115">The following illustration shows the waveform-audio playback area.</span></span>

![mciwnd 視窗影像](images/mciwnd4.gif)

<span data-ttu-id="b0fb8-117">[ **播放** ] 按鈕位於 [MCIWnd] 視窗的左下角。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-117">The **Play** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="b0fb8-118">它會在內容停止時顯示。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-118">It appears when the content is stopped.</span></span> <span data-ttu-id="b0fb8-119">使用者可以透過下列方式播放內容：</span><span class="sxs-lookup"><span data-stu-id="b0fb8-119">The user can play the content in the following ways:</span></span>

-   <span data-ttu-id="b0fb8-120">若要從目前的播放位置播放內容，請選取 [ **播放** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-120">To play the content from the current playback position, select the **Play** button.</span></span>
-   <span data-ttu-id="b0fb8-121">若要從目前的播放位置播放全螢幕的內容，請在按住 CTRL 鍵時選取 [ **播放** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-121">To play the content full-screen from the current playback position, select the **Play** button while holding down the CTRL key.</span></span>
-   <span data-ttu-id="b0fb8-122">若要從目前的播放位置反向播放內容，請在按住 SHIFT 鍵時選取 [ **播放** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-122">To play the content backward from the current playback position, select the **Play** button while holding down the SHIFT key.</span></span>

<span data-ttu-id="b0fb8-123">**功能表** 按鈕（位於 [**播放**] 按鈕旁邊）會啟動功能表，讓使用者能夠開啟和關閉音訊- (AVI) 檔案，以及調整影像大小、播放速度和音量。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-123">The **Menu** button, located next to the **Play** button, activates a menu that allows the user to open and close audio-video interleaved (AVI) files, and to adjust the image size, playback speed, and volume.</span></span> <span data-ttu-id="b0fb8-124"> (當游標位於視窗的工作區時，使用者也可以按一下滑鼠右鍵來啟用功能表。 ) 功能表也包含變更目前裝置設定的命令、將播放內容複寫到剪貼簿，以及發行 MCI 命令。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-124">(The user can also activate the menu by clicking the right mouse button whenever the cursor is in the client area of the window.) The menu also includes commands to change the configuration of the current device, to copy the playback content to the clipboard, and to issue MCI commands.</span></span>

<span data-ttu-id="b0fb8-125">[ **功能表** ] 按鈕右邊的 [內容] 表示播放 (的持續時間，或記錄) 內容。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-125">The trackbar to the right of the **Menu** button represents the duration of the playback (or recorded) content.</span></span> <span data-ttu-id="b0fb8-126">[顯示] 上的滑杆表示內容中目前的播放位置。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-126">The slider on the trackbar represents the current playback position within the content.</span></span> <span data-ttu-id="b0fb8-127">當滑杆位於頂端的頂端時，目前的播放位置是內容的開頭。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-127">When the slider is positioned at the left end of the trackbar, the current playback position is the beginning of the content.</span></span> <span data-ttu-id="b0fb8-128">使用者可以透過在 [並排] 拖曳滑杆，移至內容中的不同位置。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-128">The user can move to different locations in the content by dragging the slider along the trackbar.</span></span> <span data-ttu-id="b0fb8-129">[ **停止** ] 按鈕位於 [MCIWnd] 視窗的左下角。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-129">The **Stop** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="b0fb8-130">它會在播放內容時顯示。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-130">It appears when the content is played.</span></span> <span data-ttu-id="b0fb8-131">下圖顯示現正播放的影片。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-131">The following illustration shows video playback in progress.</span></span>

![影片播放影像](images/mciwnd2.gif)

<span data-ttu-id="b0fb8-133">MCIWnd 控制項也可以包含可錄製之裝置的 [ **記錄** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-133">The MCIWnd controls can also include a **Record** button for devices that can record.</span></span> <span data-ttu-id="b0fb8-134">[ **錄製** ] 按鈕以紅色圓圈標示，而且只有在裝置能夠錄製時才會出現。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-134">The **Record** button is marked with a red circle and appears only when the device is capable of recording.</span></span>

> [!Note]  
> <span data-ttu-id="b0fb8-135">播放視窗必須對齊四個圖元的界限，以獲得最佳的影片播放效能。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-135">The playback window must be aligned on a four-pixel boundary for the best video playback performance.</span></span> <span data-ttu-id="b0fb8-136">一般而言，Windows 會在建立時自動對齊視窗。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-136">Typically, Windows aligns the window automatically when it is created.</span></span> <span data-ttu-id="b0fb8-137">如果使用者從其初始位置移動或伸展視窗，影片播放速度可能會減少一半。</span><span class="sxs-lookup"><span data-stu-id="b0fb8-137">If a user moves or stretches the window from its initial position, video playback speed might be reduced by half.</span></span>

 

 

 




