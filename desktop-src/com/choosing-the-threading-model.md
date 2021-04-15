---
title: 選擇執行緒模型
description: 選擇執行緒模型
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372589"
---
# <a name="choosing-the-threading-model"></a><span data-ttu-id="554f0-103">選擇執行緒模型</span><span class="sxs-lookup"><span data-stu-id="554f0-103">Choosing the Threading Model</span></span>

<span data-ttu-id="554f0-104">選擇物件的執行緒模型取決於物件的函數。</span><span class="sxs-lookup"><span data-stu-id="554f0-104">Choosing the threading model for an object depends on the object's function.</span></span> <span data-ttu-id="554f0-105">執行大量 i/o 的物件可能支援無限制執行緒，藉由在 i/o 延遲期間允許介面呼叫，提供最大的回應給用戶端。</span><span class="sxs-lookup"><span data-stu-id="554f0-105">An object that does extensive I/O might support free-threading to provide maximum response to clients by allowing interface calls during I/O latency.</span></span> <span data-ttu-id="554f0-106">另一方面，與使用者互動的物件可能會支援單元執行緒傳入的 COM 呼叫與其視窗作業。</span><span class="sxs-lookup"><span data-stu-id="554f0-106">On the other hand, an object that interacts with the user might support apartment threading to synchronize incoming COM calls with its window operations.</span></span>

<span data-ttu-id="554f0-107">在單一執行緒的單元中支援單元執行緒比較容易，因為 COM 會針對個別呼叫提供同步處理。</span><span class="sxs-lookup"><span data-stu-id="554f0-107">It is easier to support apartment threading in single-threaded apartments because COM provides synchronization on a per-call basis.</span></span> <span data-ttu-id="554f0-108">支援自由執行緒較難，因為物件必須執行同步處理;不過，對用戶端的回應可能更好，因為可以針對較小的程式碼區段來執行同步處理。</span><span class="sxs-lookup"><span data-stu-id="554f0-108">Supporting free-threading is more difficult because the object must implement synchronization; however, response to clients may be better because synchronization can be implemented for smaller sections of code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="554f0-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="554f0-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="554f0-110">跨單元存取介面</span><span class="sxs-lookup"><span data-stu-id="554f0-110">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="554f0-111">多執行緒單元</span><span class="sxs-lookup"><span data-stu-id="554f0-111">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="554f0-112">同進程伺服器執行緒問題</span><span class="sxs-lookup"><span data-stu-id="554f0-112">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="554f0-113">進程、執行緒和單元</span><span class="sxs-lookup"><span data-stu-id="554f0-113">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="554f0-114">單一執行緒和多執行緒通訊</span><span class="sxs-lookup"><span data-stu-id="554f0-114">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="554f0-115">單一執行緒單元</span><span class="sxs-lookup"><span data-stu-id="554f0-115">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




