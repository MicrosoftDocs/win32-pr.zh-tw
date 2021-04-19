---
title: 執行緒走
description: 包含執行緒清單的快照集包含每個目前正在執行之進程的每個執行緒的相關資訊。
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- 列舉
- 列舉，執行緒
- 執行緒
- 執行緒，列舉執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967683"
---
# <a name="thread-walking"></a><span data-ttu-id="bf5b8-107">執行緒走</span><span class="sxs-lookup"><span data-stu-id="bf5b8-107">Thread Walking</span></span>

<span data-ttu-id="bf5b8-108">包含執行緒清單的快照集包含每個目前正在執行之進程的每個執行緒的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf5b8-108">A snapshot that includes the thread list contains information about each thread of each currently executing process.</span></span> <span data-ttu-id="bf5b8-109">您可以使用 [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) 函式，來取得清單中第一個執行緒的資訊。</span><span class="sxs-lookup"><span data-stu-id="bf5b8-109">You can retrieve information for the first thread in the list by using the [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) function.</span></span> <span data-ttu-id="bf5b8-110">在取得清單中的第一個執行緒之後，您可以使用 [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) 函式來抓取後續執行緒的資訊。</span><span class="sxs-lookup"><span data-stu-id="bf5b8-110">After retrieving the first thread in the list, you can retrieve information for subsequent threads by using the [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) function.</span></span> <span data-ttu-id="bf5b8-111">**Thread32First** 和 **Thread32Next** 會以快照集中個別執行緒的相關資訊來填滿 [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) 結構。</span><span class="sxs-lookup"><span data-stu-id="bf5b8-111">**Thread32First** and **Thread32Next** fill a [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) structure with information about individual threads in the snapshot.</span></span>

<span data-ttu-id="bf5b8-112">您可以取得包含執行緒的快照集，然後藉由追蹤執行緒清單來列舉特定進程的執行緒，並保留與指定進程具有相同處理序識別碼之執行緒的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf5b8-112">You can enumerate the threads of a specific process by taking a snapshot that includes the threads and then by traversing the thread list, keeping information about the threads that have the same process identifier as the specified process.</span></span>

<span data-ttu-id="bf5b8-113">您可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式來取得 [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)和 [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)的擴充錯誤狀態碼。</span><span class="sxs-lookup"><span data-stu-id="bf5b8-113">You can retrieve an extended error status code for [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) and [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="bf5b8-114">[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)的 **th32ThreadID** 成員內容是執行緒識別碼，可供任何需要執行緒識別碼的函式使用。</span><span class="sxs-lookup"><span data-stu-id="bf5b8-114">The contents of the **th32ThreadID** member of [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) is a thread identifier and can be used by any functions that require a thread identifier.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bf5b8-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf5b8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf5b8-116">遍歷執行緒清單</span><span class="sxs-lookup"><span data-stu-id="bf5b8-116">Traversing the Thread List</span></span>](traversing-the-thread-list.md)
</dt> </dl>

 

 