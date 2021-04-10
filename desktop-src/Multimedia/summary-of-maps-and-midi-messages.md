---
title: 地圖和 MIDI 訊息的摘要
description: 地圖和 MIDI 訊息的摘要
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應工具，通道對應
- MIDI 對應程式，修補程式對應
- MIDI 對應程式，金鑰組應
- 通道對應
- 修補程式對應
- 金鑰組應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675068"
---
# <a name="summary-of-maps-and-midi-messages"></a><span data-ttu-id="f90ba-111">地圖和 MIDI 訊息的摘要</span><span class="sxs-lookup"><span data-stu-id="f90ba-111">Summary of Maps and MIDI Messages</span></span>

<span data-ttu-id="f90ba-112">以下是 MIDI 訊息的狀態位元組和影響每個訊息的對應類型。</span><span class="sxs-lookup"><span data-stu-id="f90ba-112">Following are the status bytes for MIDI messages and the map types that affect each message.</span></span>



| <span data-ttu-id="f90ba-113">MIDI 狀態</span><span class="sxs-lookup"><span data-stu-id="f90ba-113">MIDI status</span></span> | <span data-ttu-id="f90ba-114">Description</span><span class="sxs-lookup"><span data-stu-id="f90ba-114">Description</span></span>               | <span data-ttu-id="f90ba-115">對應類型</span><span class="sxs-lookup"><span data-stu-id="f90ba-115">Map types</span></span>                |
|-------------|---------------------------|--------------------------|
| <span data-ttu-id="f90ba-116">0x80-0x8F</span><span class="sxs-lookup"><span data-stu-id="f90ba-116">0x80-0x8F</span></span>   | <span data-ttu-id="f90ba-117">請注意</span><span class="sxs-lookup"><span data-stu-id="f90ba-117">Note off</span></span>                  | <span data-ttu-id="f90ba-118">通道對應，金鑰組應</span><span class="sxs-lookup"><span data-stu-id="f90ba-118">Channel maps, key maps</span></span>   |
| <span data-ttu-id="f90ba-119">0x90-0x9F</span><span class="sxs-lookup"><span data-stu-id="f90ba-119">0x90-0x9F</span></span>   | <span data-ttu-id="f90ba-120">注意 </span><span class="sxs-lookup"><span data-stu-id="f90ba-120">Note on</span></span>                   | <span data-ttu-id="f90ba-121">通道對應，金鑰組應</span><span class="sxs-lookup"><span data-stu-id="f90ba-121">Channel maps, key maps</span></span>   |
| <span data-ttu-id="f90ba-122">0xA0-0xAF</span><span class="sxs-lookup"><span data-stu-id="f90ba-122">0xA0-0xAF</span></span>   | <span data-ttu-id="f90ba-123">Polyphonic-key aftertouch</span><span class="sxs-lookup"><span data-stu-id="f90ba-123">Polyphonic-key aftertouch</span></span> | <span data-ttu-id="f90ba-124">通道對應，金鑰組應</span><span class="sxs-lookup"><span data-stu-id="f90ba-124">Channel maps, key maps</span></span>   |
| <span data-ttu-id="f90ba-125">0xB0-0xBF</span><span class="sxs-lookup"><span data-stu-id="f90ba-125">0xB0-0xBF</span></span>   | <span data-ttu-id="f90ba-126">控制項變更</span><span class="sxs-lookup"><span data-stu-id="f90ba-126">Control change</span></span>            | <span data-ttu-id="f90ba-127">Channel maps、patch map</span><span class="sxs-lookup"><span data-stu-id="f90ba-127">Channel maps, patch maps</span></span> |
| <span data-ttu-id="f90ba-128">0xC0-0xCF</span><span class="sxs-lookup"><span data-stu-id="f90ba-128">0xC0-0xCF</span></span>   | <span data-ttu-id="f90ba-129">程式變更</span><span class="sxs-lookup"><span data-stu-id="f90ba-129">Program change</span></span>            | <span data-ttu-id="f90ba-130">Channel maps、patch map</span><span class="sxs-lookup"><span data-stu-id="f90ba-130">Channel maps, patch maps</span></span> |
| <span data-ttu-id="f90ba-131">0xD0-0xDF</span><span class="sxs-lookup"><span data-stu-id="f90ba-131">0xD0-0xDF</span></span>   | <span data-ttu-id="f90ba-132">通道 aftertouch</span><span class="sxs-lookup"><span data-stu-id="f90ba-132">Channel aftertouch</span></span>        | <span data-ttu-id="f90ba-133">通道對應</span><span class="sxs-lookup"><span data-stu-id="f90ba-133">Channel maps</span></span>             |
| <span data-ttu-id="f90ba-134">0xE0-0xEF</span><span class="sxs-lookup"><span data-stu-id="f90ba-134">0xE0-0xEF</span></span>   | <span data-ttu-id="f90ba-135">音調-折彎變更</span><span class="sxs-lookup"><span data-stu-id="f90ba-135">Pitch-bend change</span></span>         | <span data-ttu-id="f90ba-136">通道對應</span><span class="sxs-lookup"><span data-stu-id="f90ba-136">Channel maps</span></span>             |
| <span data-ttu-id="f90ba-137">0xF0-0xFF</span><span class="sxs-lookup"><span data-stu-id="f90ba-137">0xF0-0xFF</span></span>   | <span data-ttu-id="f90ba-138">系統</span><span class="sxs-lookup"><span data-stu-id="f90ba-138">System</span></span>                    | <span data-ttu-id="f90ba-139">未對應</span><span class="sxs-lookup"><span data-stu-id="f90ba-139">Not mapped</span></span>               |



 

-   <span data-ttu-id="f90ba-140">高序位四個位代表狀態值。</span><span class="sxs-lookup"><span data-stu-id="f90ba-140">The high-order four bits represent the status value.</span></span> <span data-ttu-id="f90ba-141">低序位四個位代表通道資訊。</span><span class="sxs-lookup"><span data-stu-id="f90ba-141">The low-order four bits represent the channel information.</span></span>
-   <span data-ttu-id="f90ba-142">修補程式對應只會影響主要磁碟區) 的控制器 7 (。</span><span class="sxs-lookup"><span data-stu-id="f90ba-142">Patch maps affect only controller 7 (main volume).</span></span>
-   <span data-ttu-id="f90ba-143">系統訊息會傳送至通道對應中列出的所有裝置。</span><span class="sxs-lookup"><span data-stu-id="f90ba-143">System messages are sent to all devices listed in a channel map.</span></span>

 

 




