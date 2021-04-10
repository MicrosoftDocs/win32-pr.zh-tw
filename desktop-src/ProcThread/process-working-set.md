---
description: 程式的工作集是其虛擬位址空間中最近參考的頁面集合。
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: 處理工作集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900b5d8a19c756a9087a9b2c006259857691dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192755"
---
# <a name="process-working-set"></a><span data-ttu-id="0fdbe-103">處理工作集</span><span class="sxs-lookup"><span data-stu-id="0fdbe-103">Process Working Set</span></span>

<span data-ttu-id="0fdbe-104">程式的 *工作集* 是其虛擬位址空間中最近參考的頁面集合。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-104">The *working set* of a program is a collection of those pages in its virtual address space that have been recently referenced.</span></span> <span data-ttu-id="0fdbe-105">它包含共用和私用資料。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-105">It includes both shared and private data.</span></span> <span data-ttu-id="0fdbe-106">共用資料包含包含應用程式執行之所有指令的頁面，包括您的 Dll 和系統 Dll 中的所有指示。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-106">The shared data includes pages that contain all instructions your application executes, including those in your DLLs and the system DLLs.</span></span> <span data-ttu-id="0fdbe-107">當工作集大小增加時，記憶體需求也會增加。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-107">As the working set size increases, memory demand increases.</span></span>

<span data-ttu-id="0fdbe-108">進程有相關聯的工作集大小下限和工作集大小上限。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-108">A process has an associated minimum working set size and maximum working set size.</span></span> <span data-ttu-id="0fdbe-109">每次呼叫 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)時，它會保留進程的工作集大小下限。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-109">Each time you call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), it reserves the minimum working set size for the process.</span></span> <span data-ttu-id="0fdbe-110">當程式為使用中狀態時，虛擬記憶體管理員會嘗試保留足夠的記憶體供最小的工作集常駐，但不會超過大小上限。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-110">The virtual memory manager attempts to keep enough memory for the minimum working set resident when the process is active, but keeps no more than the maximum size.</span></span>

<span data-ttu-id="0fdbe-111">若要取得應用程式的工作集所要求的最小和最大大小，請呼叫 [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) 函數。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-111">To get the requested minimum and maximum sizes of the working set for your application, call the [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) function.</span></span>

<span data-ttu-id="0fdbe-112">系統會設定預設的工作集大小。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-112">The system sets the default working set sizes.</span></span> <span data-ttu-id="0fdbe-113">您也可以使用 [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) 函數來修改工作集大小。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-113">You can also modify the working set sizes using the [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) function.</span></span> <span data-ttu-id="0fdbe-114">設定這些值並不保證會保留或駐留記憶體。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-114">Setting these values is not a guarantee that the memory will be reserved or resident.</span></span> <span data-ttu-id="0fdbe-115">請小心要求太大或最大的工作集大小，因為這樣做可能會降低系統效能。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-115">Be careful about requesting too large a minimum or maximum working set size, because doing so can degrade system performance.</span></span>

<span data-ttu-id="0fdbe-116">若要取得處理常式之工作集目前或最大的大小，請使用 [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="0fdbe-116">To obtain the current or peak size of the working set for your process, use the [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fdbe-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="0fdbe-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0fdbe-118">[記憶體效能資訊](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0fdbe-118">[Memory Performance Information](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0fdbe-119">工作集</span><span class="sxs-lookup"><span data-stu-id="0fdbe-119">Working Set</span></span>](../memory/working-set.md)
</dt> </dl>

 

 
