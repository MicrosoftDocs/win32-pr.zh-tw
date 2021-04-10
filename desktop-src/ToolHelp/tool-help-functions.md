---
title: 工具說明函數
description: 列出工具說明程式庫函數。
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021953"
---
# <a name="tool-help-functions"></a><span data-ttu-id="221d2-103">工具說明函數</span><span class="sxs-lookup"><span data-stu-id="221d2-103">Tool Help Functions</span></span>

<span data-ttu-id="221d2-104">下列功能是工具 help library 的一部分。</span><span class="sxs-lookup"><span data-stu-id="221d2-104">The following functions are part of the tool help library.</span></span>



| <span data-ttu-id="221d2-105">函式</span><span class="sxs-lookup"><span data-stu-id="221d2-105">Function</span></span>                                                           | <span data-ttu-id="221d2-106">描述</span><span class="sxs-lookup"><span data-stu-id="221d2-106">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="221d2-107">**CreateToolhelp32Snapshot**</span><span class="sxs-lookup"><span data-stu-id="221d2-107">**CreateToolhelp32Snapshot**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | <span data-ttu-id="221d2-108">取得指定進程的快照集，以及這些進程所使用的堆積、模組和執行緒。</span><span class="sxs-lookup"><span data-stu-id="221d2-108">Takes a snapshot of the specified processes, as well as the heaps, modules, and threads used by these processes.</span></span> |
| [<span data-ttu-id="221d2-109">**Heap32First**</span><span class="sxs-lookup"><span data-stu-id="221d2-109">**Heap32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | <span data-ttu-id="221d2-110">抓取進程已配置之堆積第一個區塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="221d2-110">Retrieves information about the first block of a heap that has been allocated by a process.</span></span>                      |
| [<span data-ttu-id="221d2-111">**Heap32ListFirst**</span><span class="sxs-lookup"><span data-stu-id="221d2-111">**Heap32ListFirst**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | <span data-ttu-id="221d2-112">抓取指定進程已配置之第一個堆積的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="221d2-112">Retrieves information about the first heap that has been allocated by a specified process.</span></span>                       |
| [<span data-ttu-id="221d2-113">**Heap32ListNext**</span><span class="sxs-lookup"><span data-stu-id="221d2-113">**Heap32ListNext**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | <span data-ttu-id="221d2-114">抓取進程已配置之下一個堆積的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="221d2-114">Retrieves information about the next heap that has been allocated by a process.</span></span>                                  |
| [<span data-ttu-id="221d2-115">**Heap32Next**</span><span class="sxs-lookup"><span data-stu-id="221d2-115">**Heap32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | <span data-ttu-id="221d2-116">抓取進程已配置之堆積的下一個區塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="221d2-116">Retrieves information about the next block of a heap that has been allocated by a process.</span></span>                       |
| [<span data-ttu-id="221d2-117">**Module32First**</span><span class="sxs-lookup"><span data-stu-id="221d2-117">**Module32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | <span data-ttu-id="221d2-118">抓取與進程相關聯之第一個模組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="221d2-118">Retrieves information about the first module associated with a process.</span></span>                                          |
| [<span data-ttu-id="221d2-119">**Module32Next**</span><span class="sxs-lookup"><span data-stu-id="221d2-119">**Module32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | <span data-ttu-id="221d2-120">抓取與進程或執行緒相關聯之下一個模組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="221d2-120">Retrieves information about the next module associated with a process or thread.</span></span>                                 |
| [<span data-ttu-id="221d2-121">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="221d2-121">**Process32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | <span data-ttu-id="221d2-122">抓取系統快照中所發生第一個進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="221d2-122">Retrieves information about the first process encountered in a system snapshot.</span></span>                                  |
| [<span data-ttu-id="221d2-123">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="221d2-123">**Process32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | <span data-ttu-id="221d2-124">抓取系統快照中所記錄之下一個進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="221d2-124">Retrieves information about the next process recorded in a system snapshot.</span></span>                                      |
| [<span data-ttu-id="221d2-125">**Thread32First**</span><span class="sxs-lookup"><span data-stu-id="221d2-125">**Thread32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | <span data-ttu-id="221d2-126">抓取系統快照中所發生之任何進程的第一個執行緒的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="221d2-126">Retrieves information about the first thread of any process encountered in a system snapshot.</span></span>                    |
| [<span data-ttu-id="221d2-127">**Thread32Next**</span><span class="sxs-lookup"><span data-stu-id="221d2-127">**Thread32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | <span data-ttu-id="221d2-128">抓取系統記憶體快照中所發生之任何進程的下一個執行緒的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="221d2-128">Retrieves information about the next thread of any process encountered in the system memory snapshot.</span></span>            |
| [<span data-ttu-id="221d2-129">**Toolhelp32ReadProcessMemory**</span><span class="sxs-lookup"><span data-stu-id="221d2-129">**Toolhelp32ReadProcessMemory**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | <span data-ttu-id="221d2-130">將配置給另一個進程的記憶體複製到應用程式提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="221d2-130">Copies memory allocated to another process into an application-supplied buffer.</span></span>                                  |



 

 

 




