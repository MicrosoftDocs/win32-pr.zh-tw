---
title: 進程記憶體使用量資訊
description: GetProcessMemoryInfo 函式會採用進程控制碼做為輸入，並將進程 \_ 記憶體 \_ 計數器結構填入進程的記憶體統計資料相關資訊。
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840491"
---
# <a name="process-memory-usage-information"></a><span data-ttu-id="bb727-103">進程記憶體使用量資訊</span><span class="sxs-lookup"><span data-stu-id="bb727-103">Process Memory Usage Information</span></span>

<span data-ttu-id="bb727-104">[**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo)函式會採用進程控制碼做為輸入，並將進程 [**\_ 記憶體 \_ 計數器**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters)結構填入進程的記憶體統計資料相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bb727-104">The [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function takes a process handle as input and fills a [**PROCESS\_MEMORY\_COUNTERS**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) structure with information about the memory statistics for the process.</span></span> <span data-ttu-id="bb727-105">**Cb** 成員接收結構的大小。</span><span class="sxs-lookup"><span data-stu-id="bb727-105">The **cb** member receives the size of the structure.</span></span> <span data-ttu-id="bb727-106">**PageFaultCount** 成員會收到分頁錯誤數。</span><span class="sxs-lookup"><span data-stu-id="bb727-106">The **PageFaultCount** member receives the number of page faults.</span></span> <span data-ttu-id="bb727-107">其餘成員會收到下列類別的目前和尖峰記憶體使用量：</span><span class="sxs-lookup"><span data-stu-id="bb727-107">The remaining members receive the current and peak memory usage in the following categories:</span></span>

-   <span data-ttu-id="bb727-108">工作集</span><span class="sxs-lookup"><span data-stu-id="bb727-108">working set</span></span>
-   <span data-ttu-id="bb727-109">分頁集區</span><span class="sxs-lookup"><span data-stu-id="bb727-109">paged pool</span></span>
-   <span data-ttu-id="bb727-110">非分頁集區</span><span class="sxs-lookup"><span data-stu-id="bb727-110">nonpaged pool</span></span>
-   <span data-ttu-id="bb727-111">分頁檔</span><span class="sxs-lookup"><span data-stu-id="bb727-111">pagefile</span></span>

<span data-ttu-id="bb727-112">*工作集* 是指在指定時間實際對應至進程內容的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="bb727-112">The *working set* is the amount of memory physically mapped to the process context at a given time.</span></span> <span data-ttu-id="bb727-113">*分頁式集* 區中的記憶體是系統記憶體，可在磁片上傳送至分頁檔 (分頁) 未使用時使用。</span><span class="sxs-lookup"><span data-stu-id="bb727-113">Memory in the *paged pool* is system memory that can be transferred to the paging file on disk (paged) when it is not being used.</span></span> <span data-ttu-id="bb727-114">*非分頁集區中* 的記憶體是系統記憶體，只要配置了對應的物件，就無法將其分頁至磁片。</span><span class="sxs-lookup"><span data-stu-id="bb727-114">Memory in the *nonpaged pool* is system memory that cannot be paged to disk as long as the corresponding objects are allocated.</span></span> <span data-ttu-id="bb727-115">*頁面* 檔案使用方式代表針對系統分頁檔案中的進程所設定的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="bb727-115">The *pagefile* usage represents how much memory is set aside for the process in the system paging file.</span></span> <span data-ttu-id="bb727-116">當記憶體使用量過高時，虛擬記憶體管理員會將選取的記憶體分頁至磁片。</span><span class="sxs-lookup"><span data-stu-id="bb727-116">When memory usage is too high, the virtual memory manager pages selected memory to disk.</span></span> <span data-ttu-id="bb727-117">當執行緒需要不在記憶體中的頁面時，記憶體管理員會從分頁檔重載該頁面。</span><span class="sxs-lookup"><span data-stu-id="bb727-117">When a thread needs a page that is not in memory, the memory manager reloads it from the paging file.</span></span>

 

 




