---
title: 調整速度、音量和縮放比例
description: 調整速度、音量和縮放比例
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- MCIWndSetSpeed 宏
- MCIWndGetSpeed 宏
- MCIWndSetVolume 宏
- MCIWndGetVolume 宏
- MCIWndSetZoom 宏
- MCIWndGetZoom 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372231"
---
# <a name="adjusting-speed-volume-and-zoom"></a><span data-ttu-id="2eae0-109">調整速度、音量和縮放比例</span><span class="sxs-lookup"><span data-stu-id="2eae0-109">Adjusting Speed, Volume, and Zoom</span></span>

<span data-ttu-id="2eae0-110">[速度]、[音量] 和 [縮放] 宏可提供 [MCIWnd] 功能表上的 **View**、 **volume** 和 **speed** 命令功能。</span><span class="sxs-lookup"><span data-stu-id="2eae0-110">The speed, volume, and zoom macros provide the functionality of the **View**, **Volume**, and **Speed** commands on the MCIWnd menu.</span></span> <span data-ttu-id="2eae0-111">本節所述的宏一般會搭配影片和其他裝置使用，這些裝置會在播放期間顯示影像。</span><span class="sxs-lookup"><span data-stu-id="2eae0-111">The macros described in this section are generally used with video and other devices that display images during playback.</span></span>

<span data-ttu-id="2eae0-112">某些裝置支援多種播放速度變更。</span><span class="sxs-lookup"><span data-stu-id="2eae0-112">Some devices support multiple playback speed changes.</span></span> <span data-ttu-id="2eae0-113">您可以使用 [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) 宏來設定這些裝置的播放速度。</span><span class="sxs-lookup"><span data-stu-id="2eae0-113">You can set the playback speed for these devices by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span> <span data-ttu-id="2eae0-114">此宏會將播放速度定義為1000。</span><span class="sxs-lookup"><span data-stu-id="2eae0-114">This macro defines the playback speed as 1000.</span></span> <span data-ttu-id="2eae0-115">較高的值表示速度更快。</span><span class="sxs-lookup"><span data-stu-id="2eae0-115">Higher values indicate faster speeds.</span></span> <span data-ttu-id="2eae0-116">較低的值表示速度較慢。</span><span class="sxs-lookup"><span data-stu-id="2eae0-116">Lower values indicate slower speeds.</span></span>

<span data-ttu-id="2eae0-117">您可以使用 [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) 宏來取得目前的播放速度。</span><span class="sxs-lookup"><span data-stu-id="2eae0-117">You can retrieve the current playback speed by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span> <span data-ttu-id="2eae0-118">這個宏使用的值和範圍與 **MCIWndSetSpeed** 所使用的相同。</span><span class="sxs-lookup"><span data-stu-id="2eae0-118">This macro uses the same values and range as those used by **MCIWndSetSpeed**.</span></span>

<span data-ttu-id="2eae0-119">某些裝置支援磁片區變更。</span><span class="sxs-lookup"><span data-stu-id="2eae0-119">Some devices support volume changes.</span></span> <span data-ttu-id="2eae0-120">您可以使用 [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) 宏來調整或設定磁片區。</span><span class="sxs-lookup"><span data-stu-id="2eae0-120">You can adjust or set the volume by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span> <span data-ttu-id="2eae0-121">此宏將一般磁片區層級定義為1000。</span><span class="sxs-lookup"><span data-stu-id="2eae0-121">This macro defines the normal volume level as 1000.</span></span> <span data-ttu-id="2eae0-122">較高的值表示較大的磁片區。</span><span class="sxs-lookup"><span data-stu-id="2eae0-122">Higher values indicate louder volumes.</span></span> <span data-ttu-id="2eae0-123">較低的值表示更安靜的磁片區。</span><span class="sxs-lookup"><span data-stu-id="2eae0-123">Lower values indicate quieter volumes.</span></span>

<span data-ttu-id="2eae0-124">您可以使用 [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) 宏來取得目前的磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="2eae0-124">You can retrieve the current volume level by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span> <span data-ttu-id="2eae0-125">這個宏使用的數值和範圍與 **MCIWndSetVolume** 所使用的數值和範圍相同。</span><span class="sxs-lookup"><span data-stu-id="2eae0-125">This macro uses the same numerical values and range as those used by **MCIWndSetVolume**.</span></span>

<span data-ttu-id="2eae0-126">針對使用播放視窗的裝置，MCIWnd 支援可設定播放映射大小的縮放功能。</span><span class="sxs-lookup"><span data-stu-id="2eae0-126">For devices that use a playback window, MCIWnd supports a zoom feature that sets the size of the playback image.</span></span> <span data-ttu-id="2eae0-127">您可以使用 [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) 宏來設定播放映射大小。</span><span class="sxs-lookup"><span data-stu-id="2eae0-127">You can set the playback image size by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span> <span data-ttu-id="2eae0-128">宏會重新定義播放影像大小，同時維持影像的固定外觀比例。</span><span class="sxs-lookup"><span data-stu-id="2eae0-128">The macro redefines the playback image size while maintaining a constant aspect ratio for the image.</span></span> <span data-ttu-id="2eae0-129">縮放值會以原始影像大小的百分比來定義。</span><span class="sxs-lookup"><span data-stu-id="2eae0-129">The zoom value is defined as a percentage of the original image size.</span></span> <span data-ttu-id="2eae0-130">因此，100代表原始影像大小，50表示顯示的影像是其原始大小的一半，而200表示顯示的影像是其原始大小的兩倍。</span><span class="sxs-lookup"><span data-stu-id="2eae0-130">Thus, 100 represents the original image size, 50 indicates the image shown is half its original size, and 200 indicates that the image shown is twice its original size.</span></span>

<span data-ttu-id="2eae0-131">您可以使用 [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) 宏來取得目前的縮放值。</span><span class="sxs-lookup"><span data-stu-id="2eae0-131">You can retrieve the current zoom value by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span> <span data-ttu-id="2eae0-132">這個宏使用的值和範圍與 **MCIWndSetZoom** 所使用的相同。</span><span class="sxs-lookup"><span data-stu-id="2eae0-132">This macro uses the same values and range as those used by **MCIWndSetZoom**.</span></span>

> [!Note]  
> <span data-ttu-id="2eae0-133">標準 MCI CD 音訊和波形音訊驅動程式不支援磁片區或速度變更。</span><span class="sxs-lookup"><span data-stu-id="2eae0-133">The standard MCI CD audio and waveform-audio drivers do not support volume or speed changes.</span></span>

 

 

 




