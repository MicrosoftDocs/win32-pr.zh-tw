---
description: 作業的 VMR 模式
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: 作業的 VMR 模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980730"
---
# <a name="vmr-modes-of-operation"></a><span data-ttu-id="ad4a7-103">作業的 VMR 模式</span><span class="sxs-lookup"><span data-stu-id="ad4a7-103">VMR Modes of Operation</span></span>

<span data-ttu-id="ad4a7-104">VMR 的元件架構可讓應用程式以各種方式進行設定，視轉譯的執行方式而定。</span><span class="sxs-lookup"><span data-stu-id="ad4a7-104">The component architecture of the VMR enables applications to configure it in various ways, depending on how rendering is to be performed.</span></span> <span data-ttu-id="ad4a7-105">下表顯示三種呈現模式以及兩種混合模式，以及每個設定都存在的元件。</span><span class="sxs-lookup"><span data-stu-id="ad4a7-105">The following table shows the three presentation modes and the two mixing modes, and the components that are present for each configuration.</span></span>



| <span data-ttu-id="ad4a7-106">模式</span><span class="sxs-lookup"><span data-stu-id="ad4a7-106">Mode</span></span>       | <span data-ttu-id="ad4a7-107">單一資料流程</span><span class="sxs-lookup"><span data-stu-id="ad4a7-107">Single Stream</span></span>                                                                     | <span data-ttu-id="ad4a7-108">多個資料流程 (混合模式) </span><span class="sxs-lookup"><span data-stu-id="ad4a7-108">Multiple Streams (Mixing Mode)</span></span>                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad4a7-109">視窗</span><span class="sxs-lookup"><span data-stu-id="ad4a7-109">Windowed</span></span>   | <span data-ttu-id="ad4a7-110">配置器-presenterCore 同步處理單位</span><span class="sxs-lookup"><span data-stu-id="ad4a7-110">Allocator-presenterCore Synchronization Unit</span></span><br/> <span data-ttu-id="ad4a7-111">視窗管理員</span><span class="sxs-lookup"><span data-stu-id="ad4a7-111">Window Manager</span></span><br/> | <span data-ttu-id="ad4a7-112">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="ad4a7-112">MixerCompositor\*</span></span><br/> <span data-ttu-id="ad4a7-113">配置器-展示者</span><span class="sxs-lookup"><span data-stu-id="ad4a7-113">Allocator-presenter</span></span><br/> <span data-ttu-id="ad4a7-114">核心同步處理單位</span><span class="sxs-lookup"><span data-stu-id="ad4a7-114">Core Synchronization Unit</span></span><br/> <span data-ttu-id="ad4a7-115">視窗管理員</span><span class="sxs-lookup"><span data-stu-id="ad4a7-115">Window Manager</span></span><br/> |
| <span data-ttu-id="ad4a7-116">窗戶</span><span class="sxs-lookup"><span data-stu-id="ad4a7-116">Windowless</span></span> | <span data-ttu-id="ad4a7-117">配置器-presenterCore 同步處理單位</span><span class="sxs-lookup"><span data-stu-id="ad4a7-117">Allocator-presenterCore Synchronization Unit</span></span><br/>                           | <span data-ttu-id="ad4a7-118">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="ad4a7-118">MixerCompositor\*</span></span><br/> <span data-ttu-id="ad4a7-119">配置器-展示者</span><span class="sxs-lookup"><span data-stu-id="ad4a7-119">Allocator-presenter</span></span><br/> <span data-ttu-id="ad4a7-120">核心同步處理單位</span><span class="sxs-lookup"><span data-stu-id="ad4a7-120">Core Synchronization Unit</span></span><br/>                           |
| <span data-ttu-id="ad4a7-121">Renderless</span><span class="sxs-lookup"><span data-stu-id="ad4a7-121">Renderless</span></span> | <span data-ttu-id="ad4a7-122">配置器-) 核心同步處理單位提供的應用程式提供者 (</span><span class="sxs-lookup"><span data-stu-id="ad4a7-122">Allocator-presenter (provided by application)Core Synchronization Unit</span></span><br/> | <span data-ttu-id="ad4a7-123">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="ad4a7-123">MixerCompositor\*</span></span><br/> <span data-ttu-id="ad4a7-124">配置器-由應用程式) 提供的簡報者 (</span><span class="sxs-lookup"><span data-stu-id="ad4a7-124">Allocator-presenter (provided by application)</span></span><br/> <span data-ttu-id="ad4a7-125">核心同步處理單位</span><span class="sxs-lookup"><span data-stu-id="ad4a7-125">Core Synchronization Unit</span></span><br/> |



 

<span data-ttu-id="ad4a7-126">\* 指出應用程式有提供自訂群組件或使用預設元件的選項。</span><span class="sxs-lookup"><span data-stu-id="ad4a7-126">\* Indicates that the application has the option to provide a custom component or use the default component.</span></span>

<span data-ttu-id="ad4a7-127">在 [所有設定] 中，當您使用 VMR 建立篩選圖形時要記住的重點是，您必須先設定 VMR，然後再進行連接。</span><span class="sxs-lookup"><span data-stu-id="ad4a7-127">In all configurations, the main point to remember when you create filter graphs with the VMR is that you must configure the VMR before you connect it.</span></span>

<span data-ttu-id="ad4a7-128">對於所有設定，VMR 連接到上游篩選器之後，就無法動態新增或移除 pin，但可以連線並中斷連線。</span><span class="sxs-lookup"><span data-stu-id="ad4a7-128">For all configurations, pins cannot be dynamically added or removed after the VMR is connected to the upstream filter, but they can be connected and disconnected.</span></span> <span data-ttu-id="ad4a7-129">如果應用程式不確定需要多少 pin，則應該將 VMR 設定為可能需要的最大數目。</span><span class="sxs-lookup"><span data-stu-id="ad4a7-129">If the application is unsure how many pins will be needed, it should configure the VMR for the maximum number that might be needed.</span></span> <span data-ttu-id="ad4a7-130">篩選器上是否有未使用的輸入 pin 不會降低轉譯效能。</span><span class="sxs-lookup"><span data-stu-id="ad4a7-130">The presence of unused input pins on the filter does not degrade rendering performance.</span></span> <span data-ttu-id="ad4a7-131">不同于舊的重迭混音器，VMR 沒有輸出的 pin，因為它不需要個別的視窗管理篩選。</span><span class="sxs-lookup"><span data-stu-id="ad4a7-131">Unlike the old Overlay Mixer, the VMR has no output pin because it does not require a separate filter for window management.</span></span>

<span data-ttu-id="ad4a7-132">下列各節說明如何設定指定模式的 VMR：</span><span class="sxs-lookup"><span data-stu-id="ad4a7-132">The following sections describe how to configure the VMR for a given mode:</span></span>

-   [<span data-ttu-id="ad4a7-133">VMR 視窗 (相容性) 模式</span><span class="sxs-lookup"><span data-stu-id="ad4a7-133">VMR Windowed (Compatibility) Mode</span></span>](vmr-windowed--compatibility--mode.md)
-   [<span data-ttu-id="ad4a7-134">VMR 無視窗模式</span><span class="sxs-lookup"><span data-stu-id="ad4a7-134">VMR Windowless Mode</span></span>](vmr-windowless-mode.md)
-   [<span data-ttu-id="ad4a7-135">具有多個資料流程 (混合模式的 VMR) </span><span class="sxs-lookup"><span data-stu-id="ad4a7-135">VMR with Multiple Streams (Mixing Mode)</span></span>](vmr-with-multiple-streams--mixing-mode.md)
-   [<span data-ttu-id="ad4a7-136">YUV 混合模式</span><span class="sxs-lookup"><span data-stu-id="ad4a7-136">YUV Mixing Mode</span></span>](yuv-mixing-mode.md)
-   [<span data-ttu-id="ad4a7-137">在組合空間中定位和移動影片矩形</span><span class="sxs-lookup"><span data-stu-id="ad4a7-137">Positioning and Moving Video Rectangles in Composition Space</span></span>](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [<span data-ttu-id="ad4a7-138">VMR Renderless 播放模式 (自訂配置器-展示者) </span><span class="sxs-lookup"><span data-stu-id="ad4a7-138">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [<span data-ttu-id="ad4a7-139">DirectDraw 獨佔模式</span><span class="sxs-lookup"><span data-stu-id="ad4a7-139">DirectDraw Exclusive Mode</span></span>](directdraw-exclusive-mode.md)

 

 




