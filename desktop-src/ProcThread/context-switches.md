---
description: 排程器會為每個優先權層級維護可執行執行緒的佇列。
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: 環境切換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192763"
---
# <a name="context-switches"></a><span data-ttu-id="6a4a2-103">環境切換</span><span class="sxs-lookup"><span data-stu-id="6a4a2-103">Context Switches</span></span>

<span data-ttu-id="6a4a2-104">排程器會為每個優先權層級維護可執行執行緒的佇列。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-104">The scheduler maintains a queue of executable threads for each priority level.</span></span> <span data-ttu-id="6a4a2-105">這些稱為就緒的 *執行緒*。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-105">These are known as *ready threads*.</span></span> <span data-ttu-id="6a4a2-106">當處理器變成可用時，系統會執行 *內容切換*。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-106">When a processor becomes available, the system performs a *context switch*.</span></span> <span data-ttu-id="6a4a2-107">內容切換中的步驟如下：</span><span class="sxs-lookup"><span data-stu-id="6a4a2-107">The steps in a context switch are:</span></span>

1.  <span data-ttu-id="6a4a2-108">儲存剛剛完成執行之執行緒的內容。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-108">Save the context of the thread that just finished executing.</span></span>
2.  <span data-ttu-id="6a4a2-109">將剛剛完成執行的執行緒放在佇列的結尾，以瞭解其優先順序。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-109">Place the thread that just finished executing at the end of the queue for its priority.</span></span>
3.  <span data-ttu-id="6a4a2-110">尋找包含就緒執行緒的最高優先順序佇列。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-110">Find the highest priority queue that contains ready threads.</span></span>
4.  <span data-ttu-id="6a4a2-111">移除佇列開頭的執行緒、載入其內容，然後執行它。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-111">Remove the thread at the head of the queue, load its context, and execute it.</span></span>

<span data-ttu-id="6a4a2-112">下列執行緒類別並非就緒的執行緒。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-112">The following classes of threads are not ready threads.</span></span>

-   <span data-ttu-id="6a4a2-113">使用 CREATE 擱置旗標建立的執行緒 \_</span><span class="sxs-lookup"><span data-stu-id="6a4a2-113">Threads created with the CREATE\_SUSPENDED flag</span></span>
-   <span data-ttu-id="6a4a2-114">使用 [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) 或 [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) 函式執行期間停止的執行緒</span><span class="sxs-lookup"><span data-stu-id="6a4a2-114">Threads halted during execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function</span></span>
-   <span data-ttu-id="6a4a2-115">等候同步處理物件或輸入的執行緒。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-115">Threads waiting for a synchronization object or input.</span></span>

<span data-ttu-id="6a4a2-116">在暫停或封鎖的執行緒準備好執行之前，排程器不會將任何處理器時間配置給它們，無論其優先順序為何。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-116">Until threads that are suspended or blocked become ready to run, the scheduler does not allocate any processor time to them, regardless of their priority.</span></span>

<span data-ttu-id="6a4a2-117">內容切換的最常見原因如下：</span><span class="sxs-lookup"><span data-stu-id="6a4a2-117">The most common reasons for a context switch are:</span></span>

-   <span data-ttu-id="6a4a2-118">時間配量已過。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-118">The time slice has elapsed.</span></span>
-   <span data-ttu-id="6a4a2-119">具有較高優先順序的執行緒已準備好執行。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-119">A thread with a higher priority has become ready to run.</span></span>
-   <span data-ttu-id="6a4a2-120">執行中的執行緒需要等候。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-120">A running thread needs to wait.</span></span>

<span data-ttu-id="6a4a2-121">當執行中的執行緒需要等候時，它會會讓出其時間配量的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="6a4a2-121">When a running thread needs to wait, it relinquishes the remainder of its time slice.</span></span>

 

 
