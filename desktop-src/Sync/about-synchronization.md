---
description: 若要同步存取資源，請使用其中一個 wait 函數中的其中一個同步處理物件。
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: 關於同步處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983791"
---
# <a name="about-synchronization"></a><span data-ttu-id="df4f9-103">關於同步處理</span><span class="sxs-lookup"><span data-stu-id="df4f9-103">About Synchronization</span></span>

<span data-ttu-id="df4f9-104">若要同步存取資源，請使用其中一個[wait 函數](wait-functions.md)中的其中一個[同步處理物件](synchronization-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="df4f9-104">To synchronize access to a resource, use one of the [synchronization objects](synchronization-objects.md) in one of the [wait functions](wait-functions.md).</span></span> <span data-ttu-id="df4f9-105">同步處理物件的狀態為「已 *發出信號* 」或「 *未收到信號*」。</span><span class="sxs-lookup"><span data-stu-id="df4f9-105">The state of a synchronization object is either *signaled* or *nonsignaled*.</span></span> <span data-ttu-id="df4f9-106">等候函式可讓執行緒封鎖本身的執行，直到指定的未收到信號物件設定為已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="df4f9-106">The wait functions allow a thread to block its own execution until a specified nonsignaled object is set to the signaled state.</span></span> <span data-ttu-id="df4f9-107">如需詳細資訊，請參閱 [進程間同步](interprocess-synchronization.md)處理。</span><span class="sxs-lookup"><span data-stu-id="df4f9-107">For more information, see [Interprocess Synchronization](interprocess-synchronization.md).</span></span>

<span data-ttu-id="df4f9-108">以下是其他同步處理機制：</span><span class="sxs-lookup"><span data-stu-id="df4f9-108">The following are other synchronization mechanisms:</span></span>

-   [<span data-ttu-id="df4f9-109">重迭的輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="df4f9-109">overlapped input and output</span></span>](synchronization-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="df4f9-110">非同步程序呼叫</span><span class="sxs-lookup"><span data-stu-id="df4f9-110">asynchronous procedure calls</span></span>](asynchronous-procedure-calls.md)
-   [<span data-ttu-id="df4f9-111">重要區段物件</span><span class="sxs-lookup"><span data-stu-id="df4f9-111">critical section objects</span></span>](critical-section-objects.md)
-   [<span data-ttu-id="df4f9-112">條件變數</span><span class="sxs-lookup"><span data-stu-id="df4f9-112">condition variables</span></span>](condition-variables.md)
-   [<span data-ttu-id="df4f9-113">超薄讀取器/寫入器鎖定</span><span class="sxs-lookup"><span data-stu-id="df4f9-113">slim reader/writer locks</span></span>](slim-reader-writer--srw--locks.md)
-   [<span data-ttu-id="df4f9-114">單次初始化</span><span class="sxs-lookup"><span data-stu-id="df4f9-114">one-time initialization</span></span>](one-time-initialization.md)
-   [<span data-ttu-id="df4f9-115">連鎖變數存取</span><span class="sxs-lookup"><span data-stu-id="df4f9-115">interlocked variable access</span></span>](interlocked-variable-access.md)
-   [<span data-ttu-id="df4f9-116">連鎖單向連結清單</span><span class="sxs-lookup"><span data-stu-id="df4f9-116">interlocked singly linked lists</span></span>](interlocked-singly-linked-lists.md)
-   [<span data-ttu-id="df4f9-117">計時器佇列</span><span class="sxs-lookup"><span data-stu-id="df4f9-117">timer queues</span></span>](timer-queues.md)
-   <span data-ttu-id="df4f9-118">[**system.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)宏</span><span class="sxs-lookup"><span data-stu-id="df4f9-118">the [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) macro</span></span>

<span data-ttu-id="df4f9-119">如需同步處理的詳細資訊，請參閱 [同步處理和多處理器問題](synchronization-and-multiprocessor-issues.md)。</span><span class="sxs-lookup"><span data-stu-id="df4f9-119">For additional information on synchronization, see [Synchronization and Multiprocessor Issues](synchronization-and-multiprocessor-issues.md).</span></span>

 

 
