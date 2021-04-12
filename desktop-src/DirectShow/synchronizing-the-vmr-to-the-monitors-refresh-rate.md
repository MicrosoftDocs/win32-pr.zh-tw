---
description: 將 VMR 同步處理至監視器的更新速率
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: 將 VMR 同步處理至監視器的更新速率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194954"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a><span data-ttu-id="dd18b-103">將 VMR 同步處理至監視器的更新速率</span><span class="sxs-lookup"><span data-stu-id="dd18b-103">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>

<span data-ttu-id="dd18b-104">在罕見的情況下，您可能會想要以監視器的重新整理頻率來精確同步處理影片轉譯，如此一來，每次監視器重新整理時，就只會顯示一個新的畫面格。</span><span class="sxs-lookup"><span data-stu-id="dd18b-104">In rare scenarios, you may wish to precisely synchronize video rendering with the monitor's refresh rate, so that exactly one new frame is presented each time the monitor refreshes.</span></span> <span data-ttu-id="dd18b-105">執行這項作業的最可靠方式是建立自訂配置器提供者，以使用翻轉作業（而非 array.blit 作業）將影片位寫入主要介面。</span><span class="sxs-lookup"><span data-stu-id="dd18b-105">The most reliable way to do this is to create a custom allocator-presenter that uses a flip operation instead of a blit operation to write the video bits into the primary surface.</span></span> <span data-ttu-id="dd18b-106">每次監視器重新整理時，都會呼叫 "Flip"，因此，如果您的影片資料流程未包含時間戳記，則 VMR 會盡可能快速轉譯為主要介面，但介面會封鎖串流，直到翻轉作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="dd18b-106">"Flip" is called each time the monitor refreshes, so if your video stream contains no time stamps, the VMR will render as fast as possible to the primary surface, but the surface will block the stream until the Flip operation completes.</span></span> <span data-ttu-id="dd18b-107">這表示，只要 CPU 沒有超載，下一個畫面會在每次監視器重新整理時，一律在主要介面上等候。</span><span class="sxs-lookup"><span data-stu-id="dd18b-107">This means that, as long as the CPU is not overburdened, the next frame will always be waiting in the primary surface each time the monitor refreshes.</span></span> <span data-ttu-id="dd18b-108">但是，如果有其他需要大量 CPU 的進程正在執行，它可能會使您的 DirectShow 串流執行緒，讓它無法將影片畫面的速度夠快到主要表面。</span><span class="sxs-lookup"><span data-stu-id="dd18b-108">However, if some other CPU-intensive process is running, it could possibly starve your DirectShow streaming thread so that it cannot deliver video frames fast enough to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd18b-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd18b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd18b-110">VMR Renderless 播放模式 (自訂配置器-展示者) </span><span class="sxs-lookup"><span data-stu-id="dd18b-110">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



