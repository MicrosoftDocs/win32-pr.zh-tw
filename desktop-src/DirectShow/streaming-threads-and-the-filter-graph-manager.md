---
description: 串流執行緒和篩選圖形管理員
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: 串流執行緒和篩選圖形管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978241"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a><span data-ttu-id="72cdf-103">串流執行緒和篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="72cdf-103">Streaming Threads and the Filter Graph Manager</span></span>

<span data-ttu-id="72cdf-104">當篩選圖形管理員停止圖形時，會等候所有串流執行緒關閉。</span><span class="sxs-lookup"><span data-stu-id="72cdf-104">When the Filter Graph Manager stops the graph, it waits for all streaming threads to shut down.</span></span> <span data-ttu-id="72cdf-105">這對篩選準則具有下列含意：</span><span class="sxs-lookup"><span data-stu-id="72cdf-105">This has the following implications for filters:</span></span>

-   <span data-ttu-id="72cdf-106">篩選絕不能從資料流程執行緒呼叫篩選圖形管理員上的方法。</span><span class="sxs-lookup"><span data-stu-id="72cdf-106">A filter must never call methods on the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="72cdf-107">篩選圖形管理員會使用重要區段來同步處理自己的作業。</span><span class="sxs-lookup"><span data-stu-id="72cdf-107">The Filter Graph Manager uses a critical section to synchronize its own operations.</span></span> <span data-ttu-id="72cdf-108">如果串流執行緒嘗試保存此重要區段，它可能會造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="72cdf-108">If a streaming thread tries to hold this critical section, it can cause a deadlock.</span></span> <span data-ttu-id="72cdf-109">例如：假設另一個執行緒停止圖形。</span><span class="sxs-lookup"><span data-stu-id="72cdf-109">For example: Suppose that another thread stops the graph.</span></span> <span data-ttu-id="72cdf-110">該執行緒會採用篩選圖形鎖定，並等候篩選停止傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="72cdf-110">That thread takes the filter graph lock and waits for your filter to stop delivering data.</span></span> <span data-ttu-id="72cdf-111">如果您的篩選器正在等候鎖定，則永遠不會停止，因而造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="72cdf-111">If your filter is waiting for the lock, it will never stop, causing a deadlock.</span></span>

-   <span data-ttu-id="72cdf-112">篩選絕不能從串流執行緒 **AddRef** 或 **QueryInterface** 篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="72cdf-112">A filter must never **AddRef** or **QueryInterface** the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="72cdf-113">如果篩選 (透過 **AddRef** 或 **QueryInterface**) 在篩選圖形管理員上保存參考計數，它可能會成為保存參考計數的最後一個物件。</span><span class="sxs-lookup"><span data-stu-id="72cdf-113">If the filter holds a reference count on the Filter Graph Manager (through **AddRef** or **QueryInterface**), it might become the last object to hold a reference count.</span></span> <span data-ttu-id="72cdf-114">當篩選呼叫 **釋放** 時，篩選圖形管理員會終結本身。</span><span class="sxs-lookup"><span data-stu-id="72cdf-114">When the filter calls **Release**, the Filter Graph Manager destroys itself.</span></span> <span data-ttu-id="72cdf-115">在其清除常式內，篩選圖形管理員會嘗試停止圖形，使其等候串流執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="72cdf-115">Inside its cleanup routine, the Filter Graph Manager attempts to stop the graph, causing it to wait for the streaming thread to exit.</span></span> <span data-ttu-id="72cdf-116">但是，它正在串流執行緒內等候，所以串流執行緒無法結束。</span><span class="sxs-lookup"><span data-stu-id="72cdf-116">However, it is waiting inside the streaming thread, so the streaming thread cannot exit.</span></span> <span data-ttu-id="72cdf-117">結果是鎖死。</span><span class="sxs-lookup"><span data-stu-id="72cdf-117">The result is a deadlock.</span></span>

 

 



