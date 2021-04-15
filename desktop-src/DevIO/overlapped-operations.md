---
description: 重迭作業可讓執行緒在背景執行耗時的 i/o 作業，讓執行緒可以自由執行其他工作。
ms.assetid: 8c0eb20d-685a-4750-8253-a87089b68509
title: 重迭的作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d8dc9e39386e25129d3e7d7a5281a8299d54ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468221"
---
# <a name="overlapped-operations"></a><span data-ttu-id="69726-103">重迭的作業</span><span class="sxs-lookup"><span data-stu-id="69726-103">Overlapped Operations</span></span>

<span data-ttu-id="69726-104">重迭作業可讓執行緒在背景執行耗時的 i/o 作業，讓執行緒可以自由執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="69726-104">Overlapped operations enable a thread to perform a time-consuming I/O operation in the background, leaving the thread free to perform other tasks.</span></span> <span data-ttu-id="69726-105">若要在通訊資源上啟用重迭的 i/o 作業，執行緒必須在控制碼開啟時，于 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函式中指定檔案 **\_ 旗 \_** 標重迭旗標。</span><span class="sxs-lookup"><span data-stu-id="69726-105">To enable overlapped I/O operations on a communications resource, the thread must specify the **FILE\_FLAG\_OVERLAPPED** flag in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function when the handle is opened.</span></span> <span data-ttu-id="69726-106">若要執行 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 或 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 函數做為重迭的作業，呼叫的執行緒必須指定重迭 [**結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="69726-106">To run the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) or [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function as an overlapped operation, the calling thread must specify a pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="69726-107">重迭 **的結構必須** 包含手動重設的控制碼 (而非自動重設) 事件物件。</span><span class="sxs-lookup"><span data-stu-id="69726-107">The **OVERLAPPED** structure must contain a handle to a manual-reset (not an auto-reset) event object.</span></span> <span data-ttu-id="69726-108">在作業完成之前，系統會將事件物件的狀態設定為不會發出信號。」</span><span class="sxs-lookup"><span data-stu-id="69726-108">The system sets the state of the event object to not-signaled when a call to the I/O function returns before the operation has been completed.</span></span> <span data-ttu-id="69726-109">當作業完成時，系統會將事件物件的狀態設定為收到信號。</span><span class="sxs-lookup"><span data-stu-id="69726-109">The system sets the state of the event object to signaled when the operation has been completed.</span></span> <span data-ttu-id="69726-110">執行緒會使用等候函式來檢查事件物件的目前狀態，或等候其狀態收到信號。</span><span class="sxs-lookup"><span data-stu-id="69726-110">The thread uses a wait function to check the current state of the event object or to wait for its state to be signaled.</span></span>

<span data-ttu-id="69726-111">[**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)和 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)函數只能做為重迭的作業執行。</span><span class="sxs-lookup"><span data-stu-id="69726-111">The [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) functions can be performed only as overlapped operations.</span></span> <span data-ttu-id="69726-112">呼叫執行緒會指定 [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) 函式的指標，該函式會在重迭的作業完成時執行。</span><span class="sxs-lookup"><span data-stu-id="69726-112">The calling thread specifies a pointer to the [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) function, which is performed when the overlapped operation is completed.</span></span> <span data-ttu-id="69726-113">只有當呼叫的執行緒執行可提供警示作業時，才會執行完成常式。</span><span class="sxs-lookup"><span data-stu-id="69726-113">The completion routine is executed only if the calling thread performs an alertable operation.</span></span>

<span data-ttu-id="69726-114">如需事件物件、等候函式、可提供警示等候和完成常式的詳細資訊，請參閱 [關於同步](/windows/desktop/Sync/about-synchronization)處理。</span><span class="sxs-lookup"><span data-stu-id="69726-114">For more information about event objects, wait functions, alertable waits, and completion routines, see [About Synchronization](/windows/desktop/Sync/about-synchronization).</span></span>

 

 
