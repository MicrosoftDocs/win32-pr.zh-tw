---
title: MIDI 對應程式架構
description: MIDI 對應程式架構
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應工具，架構
- MIDI 對應程式，安裝程式對應
- MIDI 安裝對應
- MIDI 對應工具，通道對應
- MIDI 對應程式，修補程式對應
- MIDI 對應程式，金鑰組應
- 通道對應
- 修補程式對應
- 金鑰組應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301663"
---
# <a name="the-midi-mapper-architecture"></a><span data-ttu-id="780c6-114">MIDI 對應程式架構</span><span class="sxs-lookup"><span data-stu-id="780c6-114">The MIDI Mapper Architecture</span></span>

<span data-ttu-id="780c6-115">MIDI 對應工具會使用 MIDI 安裝對應來判斷如何轉譯和重新導向接收的訊息。</span><span class="sxs-lookup"><span data-stu-id="780c6-115">The MIDI Mapper uses a MIDI setup map to determine how to translate and redirect the messages it receives.</span></span> <span data-ttu-id="780c6-116">MIDI 安裝對應包含下列類型的對應。</span><span class="sxs-lookup"><span data-stu-id="780c6-116">A MIDI setup map consists of the following types of maps.</span></span>

-   [<span data-ttu-id="780c6-117">通道對應</span><span class="sxs-lookup"><span data-stu-id="780c6-117">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="780c6-118">修補程式對應</span><span class="sxs-lookup"><span data-stu-id="780c6-118">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="780c6-119">金鑰組應</span><span class="sxs-lookup"><span data-stu-id="780c6-119">Key Maps</span></span>](key-maps.md)

<span data-ttu-id="780c6-120">下圖顯示 MIDI 安裝對應中通道、修補程式和金鑰組應的角色。</span><span class="sxs-lookup"><span data-stu-id="780c6-120">The following illustration shows the roles of channel, patch, and key maps in a MIDI setup map.</span></span>

![midi 安裝對應映射中通道、修補和金鑰組應的角色](images/mmap-a02.gif)

 

 




