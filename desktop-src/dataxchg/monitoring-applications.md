---
title: 監視應用程式
description: 本主題討論如何使用動態資料交換管理程式庫的元素，建立可監視系統中動態資料交換活動的應用程式。
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- 'Windows 消費者介面，動態資料交換 (DDE) '
- 動態資料交換 (的 DDE) 監視應用程式
- DDE (動態資料交換) ，監視應用程式
- '資料交換、動態資料交換 (DDE) '
- 'Windows 消費者介面、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換管理程式庫 (DDEML) 監視應用程式
- DDEML (動態資料交換管理程式庫) ，監視應用程式
- '資料交換、動態資料交換管理程式庫 (DDEML) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f75685d4caa15e519485b2d8b37983faa35366
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021191"
---
# <a name="monitoring-applications"></a>監視應用程式

動態資料交換管理程式庫 (DDEML) 的 API 元素可用來建立應用程式，以監視系統中的動態資料交換 () 活動。 如同任何 DDEML 應用程式，DDE 監視應用程式也會包含一個 DDE 回呼函數。 DDEML 會在每次發生 DDE 事件時通知監視應用程式的 DDE 回呼函式，將事件的相關資訊傳遞給回呼函數。 應用程式通常會在視窗中顯示資訊，或將其寫入檔案。

若要從 DDEML 接收通知，應用程式必須 \_ 在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 函式的呼叫中指定 APPCLASS 監視器旗標，以註冊為 DDE 監視器。 在這個相同的呼叫中，應用程式可以指定一或多個監視旗標，以指出 DDEML 用來通知應用程式回呼函數的事件種類。 應用程式可以指定下列監視旗標：



| 旗標          | 描述                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MF \_ 回呼 | 只要將交易傳送至系統中的任何 DDE 回呼函式，就會通知回呼函數。                                                                                                                                           |
| MF \_ 約定      | 每當建立或終止交談時，就會通知回呼函式。                                                                                                                                                                |
| MF \_ 錯誤    | 每次發生 DDEML 錯誤時，通知回呼函式。                                                                                                                                                                                       |
| MF \_ HSZ \_ 資訊 | 每次 DDEML 應用程式建立、釋放或遞增字串控制碼的使用計數，或每當字串控制碼因為呼叫 [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) 函式而釋出時，就會通知回呼函數。 |
| MF \_ 連結     | 每當有建議迴圈開始或結束時，通知回呼函數。                                                                                                                                                                         |
| MF \_ POSTMSGS  | 每當系統或應用程式張貼 DDE 訊息時，就會通知回呼函式。                                                                                                                                                           |
| MF \_ SENDMSGS  | 每當系統或應用程式傳送 DDE 訊息時，就會通知回呼函數。                                                                                                                                                           |



 

下列範例示範如何註冊 DDE 監視應用程式，讓其 DDE 回呼函數接收所有 DDE 事件的通知。


```
DWORD idInst; 
PFNCALLBACK lpDdeProc; 
hInst = hInstance; 
 
if (DdeInitialize( 
        (LPDWORD) &idInst,  // instance identifier 
        DDECallback,        // pointer to callback function 
        APPCLASS_MONITOR |  // this is a monitoring application 
        MF_CALLBACKS     |  // monitor callback functions 
        MF_CONV          |  // monitor conversation data 
        MF_ERRORS        |  // monitor DDEML errors 
        MF_HSZ_INFO      |  // monitor data handle activity 
        MF_LINKS         |  // monitor advise loops 
        MF_POSTMSGS      |  // monitor posted DDE messages 
        MF_SENDMSGS,        // monitor sent DDE messages 
        0))                 // reserved 
{
    return FALSE; 
}
```



DDEML 會將 [**XTYP \_ 監視器**](xtyp-monitor.md) 交易傳送至應用程式的 dde 回呼函式，以通知監視 DDE 事件的應用程式。 在此交易期間，DDEML 會傳遞監視器旗標，以指定所發生之 DDE 事件的類型，以及包含事件詳細資訊的 DDE 物件控制碼。 DDEML 會提供一組結構，讓應用程式用來從 DDE 物件解壓縮資訊。 每種類型的 DDE 事件都有對應的結構。



| 結構                                  | Description                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | 包含交易的相關資訊。                         |
| [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | 包含對話的相關資訊。                        |
| [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | 包含最新 DDE 錯誤的相關資訊。                  |
| [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | 包含建議迴圈的相關資訊。                        |
| [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | 包含字串控制碼的相關資訊。                       |
| [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | 包含已傳送或張貼之 DDE 訊息的相關資訊。 |



 

下列範例顯示 DDE 監視應用程式的 DDE 回呼函式，它會格式化每個字串控制碼事件的相關資訊，然後在視窗中顯示資訊。 函數會使用 [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) 結構，從 DDE 物件中解壓縮資訊。


```
HDDEDATA CALLBACK DDECallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
    LPVOID lpData; 
    CHAR *szAction; 
    CHAR szBuf[256]; 
    DWORD cb;
    HRESULT hResult; 
 
    switch (uType) 
    { 
        case XTYP_MONITOR: 
            // Obtain a pointer to the global memory object. 
 
            if (lpData = DdeAccessData(hdata, &cb)) 
            { 
                // Examine the monitor flag. 
 
                switch (dwData2) 
                { 
                    case MF_HSZ_INFO: 
 
#define PHSZS ((MONHSZSTRUCT *)lpData) 
 
                        // The global memory object contains 
                        // string handle data. Use the MONHSZSTRUCT 
                        // structure to access the data. 
 
                        switch (PHSZS->fsAction) 
                        { 
                            // Examine the action flags to determine
                            // the action performed on the handle.
 
                            case MH_CREATE: 
                                szAction = "Created"; 
                                break; 
 
                            case MH_KEEP: 
                                szAction = "Incremented"; 
                                break; 
 
                            case MH_DELETE: 
                                szAction = "Deleted"; 
                                break; 
 
                            case MH_CLEANUP: 
                                szAction = "Cleaned up"; 
                                break; 
 
                            default: 
                                DdeUnaccessData(hdata); 
                                return (HDDEDATA) 0; 
                        } 
 
                        // Write formatted output to a buffer. 
                        hResult = StringCchPrintf(szBuf, 256/sizeof(TCHAR),
                            "Handle %s, Task: %x, Hsz: %lx(%s)", 
                            (LPSTR) szAction, PHSZS->hTask, 
                            PHSZS->hsz, (LPSTR) PHSZS->str);
                        if (FAILED(hResult))
                        {
                        // TO DO: Write error handler.
                            return;
                        } 
                        // Display text or write to a file. 
 
                        break; 
 
#undef PHSZS 
 
                    // Process other MF_* flags. 
 
                    default: 
                        break; 
                } 
            } 
 
            // Free the global memory object. 
 
            DdeUnaccessData(hdata); 
            break; 
 
        default: 
            break; 
    } 
    return (HDDEDATA) 0; 
} 
```



 

 




