---
title: 金鑰組應
description: 金鑰組應
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應程式，金鑰組應
- 金鑰組應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932065"
---
# <a name="key-maps"></a><span data-ttu-id="89f9f-107">金鑰組應</span><span class="sxs-lookup"><span data-stu-id="89f9f-107">Key Maps</span></span>

<span data-ttu-id="89f9f-108">Patch map 轉譯表中的每個專案都可以有相關聯的索引鍵對應。</span><span class="sxs-lookup"><span data-stu-id="89f9f-108">Each entry in the patch-map translation table can have an associated key map.</span></span> <span data-ttu-id="89f9f-109">金鑰組應會影響注意事項、注意和 polyphonic 的 aftertouch 訊息。</span><span class="sxs-lookup"><span data-stu-id="89f9f-109">Key maps affect note-on, note-off, and polyphonic-key-aftertouch messages.</span></span> <span data-ttu-id="89f9f-110">索引鍵對應具有轉譯資料表，其中每個128的 MIDI 金鑰值都有一個專案。</span><span class="sxs-lookup"><span data-stu-id="89f9f-110">A key map has a translation table with an entry for each of the 128 MIDI key values.</span></span> <span data-ttu-id="89f9f-111">例如，如果索引鍵值60的專案是72，則 MIDI 對應工具會修改 MIDI 附注訊息，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="89f9f-111">For example, if the entry for key value 60 is 72, the MIDI Mapper modifies MIDI note-on messages as shown in the following illustration.</span></span>

![midi 對應程式映射](images/mmap-a06.gif)

<span data-ttu-id="89f9f-113">Key map 適用于具有金鑰型 percussion 檢測，並將特定 percussion 音效指派給每個金鑰的合成程式。</span><span class="sxs-lookup"><span data-stu-id="89f9f-113">Key maps are useful with synthesizers that have key-based percussion instruments with a particular percussion sound assigned to each key.</span></span> <span data-ttu-id="89f9f-114">金鑰組應通常會指派給 percussion 通道 (10 和 16) 修補程式中的第一個修補程式。</span><span class="sxs-lookup"><span data-stu-id="89f9f-114">Key maps are usually assigned to the first patch in the patch maps on the percussion channels (10 and 16).</span></span>

 

 




