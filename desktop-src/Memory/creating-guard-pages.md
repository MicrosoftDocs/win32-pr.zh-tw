---
description: 防護頁面提供記憶體頁面存取的一次性警示。
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: 建立防護頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10768da75090a28ffecd5302d88dbc142ae9c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973473"
---
# <a name="creating-guard-pages"></a><span data-ttu-id="c9d9b-103">建立防護頁面</span><span class="sxs-lookup"><span data-stu-id="c9d9b-103">Creating Guard Pages</span></span>

<span data-ttu-id="c9d9b-104">防護頁面提供記憶體頁面存取的一次性警示。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-104">A guard page provides a one-shot alarm for memory page access.</span></span> <span data-ttu-id="c9d9b-105">對於需要監視大型動態資料結構成長的應用程式而言，這可能很有用。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-105">This can be useful for an application that needs to monitor the growth of large dynamic data structures.</span></span> <span data-ttu-id="c9d9b-106">例如，有作業系統使用防護頁面來執行自動堆疊檢查。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-106">For example, there are operating systems that use guard pages to implement automatic stack checking.</span></span>

<span data-ttu-id="c9d9b-107">若要建立防護頁面，請設定頁面的 **頁面 \_ 防護** 頁面保護修飾詞。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-107">To create a guard page, set the **PAGE\_GUARD** page protection modifier for the page.</span></span> <span data-ttu-id="c9d9b-108">您可以在 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)、 [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)、 [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)和 [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) 函式中指定這個值，以及其他的頁面保護修飾詞。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-108">This value can be specified, along with other page protection modifiers, in the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect), and [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) functions.</span></span> <span data-ttu-id="c9d9b-109">**Page \_ GUARD** 修飾詞可以搭配任何其他頁面保護修飾詞使用，但 **頁面 \_ NOACCESS** 除外。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-109">The **PAGE\_GUARD** modifier can be used with any other page protection modifiers, except **PAGE\_NOACCESS**.</span></span>

<span data-ttu-id="c9d9b-110">如果程式嘗試存取防護頁面中的位址，系統會 (0x80000001) 例外狀況，引發 **狀態 \_ 防護 \_ 頁面 \_ 違規** 。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-110">If a program attempts to access an address within a guard page, the system raises a **STATUS\_GUARD\_PAGE\_VIOLATION** (0x80000001) exception.</span></span> <span data-ttu-id="c9d9b-111">系統也會清除 **page \_ guard** 修飾詞，以移除記憶體頁面的 GUARD 頁面狀態。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-111">The system also clears the **PAGE\_GUARD** modifier, removing the memory page's guard page status.</span></span> <span data-ttu-id="c9d9b-112">系統將不會停止下一次嘗試存取記憶體頁面，並出現 **狀態 \_ 防護 \_ 頁面 \_ 違規例外狀況** 。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-112">The system will not stop the next attempt to access the memory page with a **STATUS\_GUARD\_PAGE\_VIOLATION** exception.</span></span>

<span data-ttu-id="c9d9b-113">如果在系統服務期間發生防護頁面例外狀況，服務會失敗，而且通常會傳回一些失敗狀態指標。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-113">If a guard page exception occurs during a system service, the service fails and typically returns some failure status indicator.</span></span> <span data-ttu-id="c9d9b-114">因為系統也會移除相關的記憶體頁面的防護頁面狀態，所以相同系統服務的下一次調用將不會因為 **狀態 \_ 防護 \_ 頁面 \_ 違規** 例外狀況而失敗 (除非您當然，有人重新建立防護頁面) 。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-114">Since the system also removes the relevant memory page's guard page status, the next invocation of the same system service won't fail due to a **STATUS\_GUARD\_PAGE\_VIOLATION** exception (unless, of course, someone reestablishes the guard page).</span></span>

<span data-ttu-id="c9d9b-115">下列簡短的程式說明防護頁面保護的行為。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-115">The following short program illustrates the behavior of guard page protection.</span></span>


```C++
/* A program to demonstrate the use of guard pages of memory. Allocate
   a page of memory as a guard page, then try to access the page. That
   will fail, but doing so releases the lock on the guard page, so the
   next access works correctly.

   The output will look like this. The actual address may vary.

   This computer has a page size of 4096.
   Committed 4096 bytes at address 0x00520000
   Cannot lock at 00520000, error = 0x80000001
   2nd Lock Achieved at 00520000

   This sample does not show how to use the guard page fault to
   "grow" a dynamic array, such as a stack. */

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <tchar.h>

int main()
{
  LPVOID lpvAddr;               // address of the test memory
  DWORD dwPageSize;             // amount of memory to allocate.
  BOOL bLocked;                 // address of the guarded memory
  SYSTEM_INFO sSysInfo;         // useful information about the system

  GetSystemInfo(&sSysInfo);     // initialize the structure

  _tprintf(TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

  dwPageSize = sSysInfo.dwPageSize;

  // Try to allocate the memory.

  lpvAddr = VirtualAlloc(NULL, dwPageSize,
                         MEM_RESERVE | MEM_COMMIT,
                         PAGE_READONLY | PAGE_GUARD);

  if(lpvAddr == NULL) {
    _tprintf(TEXT("VirtualAlloc failed. Error: %ld\n"),
             GetLastError());
    return 1;

  } else {
    _ftprintf(stderr, TEXT("Committed %lu bytes at address 0x%lp\n"),
              dwPageSize, lpvAddr);
  }

  // Try to lock the committed memory. This fails the first time 
  // because of the guard page.

  bLocked = VirtualLock(lpvAddr, dwPageSize);
  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot lock at %lp, error = 0x%lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("Lock Achieved at %lp\n"), lpvAddr);
  }

  // Try to lock the committed memory again. This succeeds the second
  // time because the guard page status was removed by the first 
  // access attempt.

  bLocked = VirtualLock(lpvAddr, dwPageSize);

  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot get 2nd lock at %lp, error = %lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("2nd Lock Achieved at %lp\n"), lpvAddr);
  }

  return 0;
}
```



<span data-ttu-id="c9d9b-116">嘗試鎖定記憶體區塊的第一次嘗試失敗，引發 **狀態 \_ 防護 \_ 頁面 \_ 違規例外狀況** 。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-116">The first attempt to lock the memory block fails, raising a **STATUS\_GUARD\_PAGE\_VIOLATION** exception.</span></span> <span data-ttu-id="c9d9b-117">第二次嘗試成功，因為第一次嘗試時已將記憶體區塊的防護頁面保護切換為關閉。</span><span class="sxs-lookup"><span data-stu-id="c9d9b-117">The second attempt succeeds, because the memory block's guard page protection has been toggled off by the first attempt.</span></span>

 

 
