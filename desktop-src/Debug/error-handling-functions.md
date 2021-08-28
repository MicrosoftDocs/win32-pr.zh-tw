---
description: 下列函式可用於錯誤處理。
ms.assetid: ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5
title: 錯誤處理函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60fdc25327bed4966336571c20580b0bfdc22b38858d3edad560359eaf0710e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912758"
---
# <a name="error-handling-functions"></a>錯誤處理函數

下列函式可用於錯誤處理。



| 函式                                                 | 描述                                                                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**嗶**](/windows/win32/api/utilapiset/nf-utilapiset-beep)                                     | 在喇叭上產生簡單的聲音。                                                                                        |
| [**CaptureStackbackTrace**](/previous-versions/windows/desktop/legacy/bb204633(v=vs.85))   | 藉由向上查看堆疊並記錄每個畫面格的資訊，來捕獲堆疊回溯追蹤。                             |
| [**FatalAppExit**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-fatalappexita)                     | 顯示訊息方塊，並在訊息方塊關閉時終止應用程式。                                         |
| [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow)                       | 將指定的視窗閃爍一次。                                                                                        |
| [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex)                   | 閃爍指定的視窗。                                                                                                 |
| [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)                   | 格式化訊息字串。                                                                                                     |
| [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode)                     | 抓取目前進程的錯誤模式。                                                                             |
| [**3]。Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)                     | 抓取呼叫執行緒的最後錯誤碼值。                                                                         |
| [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)         | 捕獲呼叫執行緒的錯誤模式。                                                                              |
| [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep)                       | 播放波形音效。                                                                                                       |
| [**RtlLookupFunctionEntry**](/windows/desktop/api/WinNT/nf-winnt-rtllookupfunctionentry) | 搜尋作用中函式資料表中是否有對應到指定電腦值的專案。                                  |
| [**RtlNtStatusToDosError**](/windows/desktop/api/Winternl/nf-winternl-rtlntstatustodoserror)   | 抓取對應于指定 NT 錯誤碼的系統錯誤碼。                                              |
| [**RtlPcToFileHeader**](/windows/desktop/api/WinNT/nf-winnt-rtlpctofileheader)           | 抓取包含指定的電腦值之影像的基底位址。                                                 |
| [**RtlUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind)                           | 起始程序呼叫框架的回溯。                                                                                 |
| [**RtlUnwind2**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind2)                         | 起始程序呼叫框架的回溯。                                                                                 |
| [**RtlUnwindEx**](/windows/desktop/api/WinNT/nf-winnt-rtlunwindex)                       | 起始程序呼叫框架的回溯。                                                                                 |
| [**RtlVirtualUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlvirtualunwind)             | 抓取函式在指定的函式內容前面的調用內容。                                |
| [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)                     | 控制系統是否會處理指定的嚴重錯誤類型，或處理常式是否會處理這些錯誤。       |
| [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)                     | 設定呼叫執行緒的最後錯誤碼。                                                                              |
| [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex)                 | 設定呼叫執行緒的最後錯誤碼。                                                                              |
| [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)         | 控制系統是否會處理指定的嚴重錯誤類型，或呼叫執行緒是否會處理它們。 |



 

 

 
