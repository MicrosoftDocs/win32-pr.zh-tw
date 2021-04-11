---
description: 當 CreateProcess 函數建立新的進程時，會傳回新進程的控制碼及其主要執行緒。
ms.assetid: cf6b80de-de02-4222-a414-e940ffaed8fe
title: 進程控制碼和識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a1ec0acb6535f8f64b9f4bd0815392d61fccbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319155"
---
# <a name="process-handles-and-identifiers"></a><span data-ttu-id="59c8b-103">進程控制碼和識別碼</span><span class="sxs-lookup"><span data-stu-id="59c8b-103">Process Handles and Identifiers</span></span>

<span data-ttu-id="59c8b-104">當 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數建立新的進程時，會傳回新進程的控制碼及其主要執行緒。</span><span class="sxs-lookup"><span data-stu-id="59c8b-104">When a new process is created by the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, handles of the new process and its primary thread are returned.</span></span> <span data-ttu-id="59c8b-105">這些控制碼是使用完整存取權限所建立，且受限於安全性存取檢查，可用於任何接受執行緒或進程控制碼的函式。</span><span class="sxs-lookup"><span data-stu-id="59c8b-105">These handles are created with full access rights, and — subject to security access checking — can be used in any of the functions that accept thread or process handles.</span></span> <span data-ttu-id="59c8b-106">這些控制碼可由子進程繼承，視建立時指定的繼承旗標而定。</span><span class="sxs-lookup"><span data-stu-id="59c8b-106">These handles can be inherited by child processes, depending on the inheritance flag specified when they are created.</span></span> <span data-ttu-id="59c8b-107">控制碼在關閉之前都是有效的，即使它們所代表的進程或執行緒已經終止也是一樣。</span><span class="sxs-lookup"><span data-stu-id="59c8b-107">The handles are valid until closed, even after the process or thread they represent has been terminated.</span></span>

<span data-ttu-id="59c8b-108">[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函式也會傳回可在整個系統中唯一識別進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="59c8b-108">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function also returns an identifier that uniquely identifies the process throughout the system.</span></span> <span data-ttu-id="59c8b-109">進程可以使用 [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) 函式來取得自己的處理序識別碼 (也稱為處理序識別碼或 PID) 。</span><span class="sxs-lookup"><span data-stu-id="59c8b-109">A process can use the [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) function to get its own process identifier (also known as the process ID or PID).</span></span> <span data-ttu-id="59c8b-110">從建立程式到進程終止之前，識別碼是有效的。</span><span class="sxs-lookup"><span data-stu-id="59c8b-110">The identifier is valid from the time the process is created until the process has been terminated.</span></span> <span data-ttu-id="59c8b-111">進程可以使用 [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) 函式來取得其父進程的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="59c8b-111">A process can use the [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) function to obtain the process identifier of its parent process.</span></span>

<span data-ttu-id="59c8b-112">如果您有進程識別碼，您可以藉由呼叫 [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) 函式來取得處理控制碼。</span><span class="sxs-lookup"><span data-stu-id="59c8b-112">If you have a process identifier, you can get the process handle by calling the [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) function.</span></span> <span data-ttu-id="59c8b-113">**OpenProcess** 可讓您指定控制碼的存取權限，以及是否可以繼承。</span><span class="sxs-lookup"><span data-stu-id="59c8b-113">**OpenProcess** enables you to specify the handle's access rights and whether it can be inherited.</span></span>

<span data-ttu-id="59c8b-114">處理常式可以使用 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) 函式，將虛擬控制碼取出至它自己的處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="59c8b-114">A process can use the [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) function to retrieve a pseudo handle to its own process object.</span></span> <span data-ttu-id="59c8b-115">這個虛擬控制碼只對呼叫進程有效;它無法被繼承或複製以供其他進程使用。</span><span class="sxs-lookup"><span data-stu-id="59c8b-115">This pseudo handle is valid only for the calling process; it cannot be inherited or duplicated for use by other processes.</span></span> <span data-ttu-id="59c8b-116">若要取得進程的實際控制碼，請呼叫 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 函數。</span><span class="sxs-lookup"><span data-stu-id="59c8b-116">To get the real handle to the process, call the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function.</span></span>

 

 
