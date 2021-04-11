---
description: 執行緒考量
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: 執行緒考量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acde9a06802a867cb6a93e7c52be8066ad483c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026010"
---
# <a name="threading-considerations"></a><span data-ttu-id="f4170-103">執行緒考量</span><span class="sxs-lookup"><span data-stu-id="f4170-103">Threading Considerations</span></span>

<span data-ttu-id="f4170-104">COM + 佇列元件錄製器能夠在進程的多執行緒單元 (MTA) 或單一執行緒的單元 (STA) 中執行。</span><span class="sxs-lookup"><span data-stu-id="f4170-104">The COM+ queued components recorder is capable of running in the process's multithreaded apartment (MTA) or in a single-threaded apartment (STA).</span></span> <span data-ttu-id="f4170-105">當記錄器在 STA 中執行時，COM + 會要求每個包含物件的單元都必須有「 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 」佇列，以處理來自相同進程中其他進程和單元的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f4170-105">When the recorder is run in the STA, COM+ requires that each apartment containing objects must have a [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) queue to handle calls from other processes and apartments within the same process.</span></span> <span data-ttu-id="f4170-106">這表示執行緒的工作函式必須有訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="f4170-106">This means that the thread's work function must have a message loop.</span></span> <span data-ttu-id="f4170-107">當已排入佇列的元件具現化時，傳回的介面指標一律為 proxy 介面指標，而不是直接介面指標。</span><span class="sxs-lookup"><span data-stu-id="f4170-107">When a queued component is instantiated, the interface pointer returned is always a proxy interface pointer rather than a direct interface pointer.</span></span> <span data-ttu-id="f4170-108">指標實際上是對記錄器實例的參考。</span><span class="sxs-lookup"><span data-stu-id="f4170-108">The pointer is actually a reference to an instance of the recorder.</span></span> <span data-ttu-id="f4170-109">如果將此錄製器介面參考傳遞至另一個執行緒，原始執行緒仍必須執行 Windows 訊息迴圈，才能讓接收端執行緒 unmarshal 介面。</span><span class="sxs-lookup"><span data-stu-id="f4170-109">If this recorder interface reference is passed to another thread, the original thread must still be running the Windows message loop so that the receiving thread can unmarshal the interface.</span></span> <span data-ttu-id="f4170-110">如果不是這種情況，接收端執行緒會在呼叫 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)時停止回應。</span><span class="sxs-lookup"><span data-stu-id="f4170-110">If this is not the case, the receiving thread hangs in a call to [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span>

<span data-ttu-id="f4170-111">如果您使用基本專案來同步處理執行緒，請考慮使用 [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) ，而不是其他同步處理函數。</span><span class="sxs-lookup"><span data-stu-id="f4170-111">If you are using primitives to synchronize the threads, consider using [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) instead of other synchronization functions.</span></span> <span data-ttu-id="f4170-112">這會檢查佇列中的訊息，以及同步處理物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="f4170-112">This checks for messages in the queue as well as the state of the synchronization object.</span></span>

 

 
