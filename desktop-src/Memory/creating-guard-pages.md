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
# <a name="creating-guard-pages"></a>建立防護頁面

防護頁面提供記憶體頁面存取的一次性警示。 對於需要監視大型動態資料結構成長的應用程式而言，這可能很有用。 例如，有作業系統使用防護頁面來執行自動堆疊檢查。

若要建立防護頁面，請設定頁面的 **頁面 \_ 防護** 頁面保護修飾詞。 您可以在 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)、 [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)、 [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)和 [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) 函式中指定這個值，以及其他的頁面保護修飾詞。 **Page \_ GUARD** 修飾詞可以搭配任何其他頁面保護修飾詞使用，但 **頁面 \_ NOACCESS** 除外。

如果程式嘗試存取防護頁面中的位址，系統會 (0x80000001) 例外狀況，引發 **狀態 \_ 防護 \_ 頁面 \_ 違規** 。 系統也會清除 **page \_ guard** 修飾詞，以移除記憶體頁面的 GUARD 頁面狀態。 系統將不會停止下一次嘗試存取記憶體頁面，並出現 **狀態 \_ 防護 \_ 頁面 \_ 違規例外狀況** 。

如果在系統服務期間發生防護頁面例外狀況，服務會失敗，而且通常會傳回一些失敗狀態指標。 因為系統也會移除相關的記憶體頁面的防護頁面狀態，所以相同系統服務的下一次調用將不會因為 **狀態 \_ 防護 \_ 頁面 \_ 違規** 例外狀況而失敗 (除非您當然，有人重新建立防護頁面) 。

下列簡短的程式說明防護頁面保護的行為。


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



嘗試鎖定記憶體區塊的第一次嘗試失敗，引發 **狀態 \_ 防護 \_ 頁面 \_ 違規例外狀況** 。 第二次嘗試成功，因為第一次嘗試時已將記憶體區塊的防護頁面保護切換為關閉。

 

 
