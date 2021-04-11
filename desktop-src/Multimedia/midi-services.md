---
title: MIDI 服務
description: MIDI 服務
ms.assetid: 884066c2-6927-4f5b-902b-8baef9a4a0d7
keywords:
- Windows 多媒體，MIDI 服務
- 多媒體，MIDI 服務
- 多媒體音訊、MIDI 服務
- 音訊、MIDI 服務
- 音樂檢測數位介面 (MIDI) 、MIDI 服務
- MIDI (的音樂檢測數位介面) 、MIDI 服務
- MIDI 服務，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc412ddec21245e9682a2a2e79e3f8031d2a6918
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375205"
---
# <a name="midi-services"></a><span data-ttu-id="6c0eb-110">MIDI 服務</span><span class="sxs-lookup"><span data-stu-id="6c0eb-110">MIDI Services</span></span>

<span data-ttu-id="6c0eb-111">大部分的應用程式都可以使用 MCI MIDI sequencer 或串流緩衝區 (而 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) 函式) 來執行所需的所有 MIDI 功能。</span><span class="sxs-lookup"><span data-stu-id="6c0eb-111">Most applications will be able to use the MCI MIDI sequencer or stream buffers (and the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function) to implement all the MIDI functionality they need.</span></span> <span data-ttu-id="6c0eb-112">這類的 MIDI 開發人員（產生 MIDI 撰寫或排序工具）可以使用串流功能和 MIDI 服務的組合，或僅使用 MIDI 服務。</span><span class="sxs-lookup"><span data-stu-id="6c0eb-112">Serious MIDI developers — those producing MIDI authoring or sequencing tools — can use either a combination of the stream capabilities and the MIDI services or use only the MIDI services.</span></span> <span data-ttu-id="6c0eb-113">下列主題提供有關使用 MIDI 服務的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="6c0eb-113">The following topics provides general information about using the MIDI services.</span></span>

-   [<span data-ttu-id="6c0eb-114">查詢 MIDI 裝置</span><span class="sxs-lookup"><span data-stu-id="6c0eb-114">Querying MIDI Devices</span></span>](querying-midi-devices.md)
-   [<span data-ttu-id="6c0eb-115">開啟和關閉設備磁碟機</span><span class="sxs-lookup"><span data-stu-id="6c0eb-115">Opening and Closing Device Drivers</span></span>](opening-and-closing-device-drivers.md)
-   [<span data-ttu-id="6c0eb-116">配置和準備 MIDI 資料區塊</span><span class="sxs-lookup"><span data-stu-id="6c0eb-116">Allocating and Preparing MIDI Data Blocks</span></span>](allocating-and-preparing-midi-data-blocks.md)
-   [<span data-ttu-id="6c0eb-117">管理 MIDI 資料區塊</span><span class="sxs-lookup"><span data-stu-id="6c0eb-117">Managing MIDI Data Blocks</span></span>](managing-midi-data-blocks.md)
-   [<span data-ttu-id="6c0eb-118">要求時間格式</span><span class="sxs-lookup"><span data-stu-id="6c0eb-118">Requesting Time Formats</span></span>](requesting-time-formats.md)
-   [<span data-ttu-id="6c0eb-119">處理 MIDI 功能的錯誤</span><span class="sxs-lookup"><span data-stu-id="6c0eb-119">Handling Errors with MIDI Functions</span></span>](handling-errors-with-midi-functions.md)

 

 