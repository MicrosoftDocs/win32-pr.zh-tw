---
description: 下列函式可用於調試。
ms.assetid: 95a838a2-f138-4682-b733-3f363b6c4a4b
title: 調試函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bf5f81b08e3a7b324f276fc1a7b5d256d40819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973757"
---
# <a name="debugging-functions"></a>調試函數

下列函式可用於調試。



| 函式                                                           | 描述                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)   | 判斷指定的進程是否正在進行調試。                         |
| [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent)                   | 讓偵錯工具繼續先前回報的偵錯工具事件的執行緒。 |
| [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)                   | 讓偵錯工具附加至使用中的進程，並將它進行 debug。                     |
| [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)           | 停止偵錯工具，使其無法偵測指定的進程。                            |
| [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)                                   | 導致在目前的進程中發生中斷點例外狀況。                      |
| [**DebugBreakProcess**](/windows/desktop/api/WinBase/nf-winbase-debugbreakprocess)                     | 導致在指定的進程中發生中斷點例外狀況。                    |
| [**DebugSetProcessKillOnExit**](/windows/desktop/api/WinBase/nf-winbase-debugsetprocesskillonexit)     | 設定要在呼叫執行緒結束時執行的動作。                      |
| [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)                                     | 將執行控制傳送至偵錯工具。                                        |
| [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache)             | 清空指定進程的指令快取。                            |
| [**GetThreadCoNtext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)                       | 抓取指定之執行緒的內容。                                      |
| [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry)           | 抓取指定之選取器和執行緒的描述項資料表專案。           |
| [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)                     | 判斷呼叫進程是否正在由使用者模式偵錯工具進行處理。   |
| [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)                     | 將字串傳送至要顯示的偵錯工具。                                         |
| [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)                     | 從指定進程中的記憶體區域讀取資料。                           |
| [**SetThreadCoNtext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)                       | 設定指定之執行緒的內容。                                          |
| [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent)                     | 等候偵錯工具在正在進行調試的進程中發生。                   |
| [**Wow64GetThreadCoNtext**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadcontext)             | 捕獲指定之 WOW64 執行緒的內容。                                |
| [**Wow64GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadselectorentry) | 抓取指定之選取器和 WOW64 執行緒的描述項資料表專案。     |
| [**Wow64SetThreadCoNtext**](/windows/desktop/api/WinBase/nf-winbase-wow64setthreadcontext)             | 設定指定之 WOW64 執行緒的內容。                                     |
| [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)                   | 將資料寫入指定進程中的記憶體區域。                            |



 

 

 
