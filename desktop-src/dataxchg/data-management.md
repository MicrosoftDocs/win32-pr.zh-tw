---
title: 資料管理
description: 本主題討論記憶體物件如何將資料從某個應用程式傳遞到另一個應用程式。
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- 'Windows消費者介面，動態資料交換 (DDE) '
- 動態資料交換 (DDE) 、資料管理
- DDE (動態資料交換) 、資料管理
- '資料交換、動態資料交換 (DDE) '
- 'Windows消費者介面，動態資料交換管理程式庫 (DDEML) '
- 動態資料交換管理程式庫 (DDEML) 、資料管理
- DDEML (動態資料交換管理程式庫) ，資料管理
- '資料交換、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換 (DDE) ，物件
- DDE (動態資料交換) ，物件
- 動態資料交換管理程式庫 (DDEML) 、物件
- DDEML (動態資料交換管理程式庫) ，物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85dc9b8ccd82d184866ac9ed28f15bdeac424ec0bf9bd7767a520dea69bc4d11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953738"
---
# <a name="data-management"></a>資料管理

因為動態資料交換 (DDE) 會使用記憶體物件將資料從某個應用程式傳遞到另一個應用程式，所以動態資料交換管理程式庫 (DDEML) 會提供一組可讓 dde 應用程式用來建立和管理 dde 物件的函數。

所有涉及資料交換的交易都需要應用程式提供資料來建立包含資料的本機緩衝區，然後呼叫 [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) 函數。 此函式會配置 DDE 物件、將資料從緩衝區複製到物件，並傳回資料控制碼。 資料處理程式是一個 **DWORD** 值，DDEML 會使用此值來提供 DDE 物件中資料的存取權。 為了共用 DDE 物件中的資料，應用程式會將資料控制碼傳遞給 DDEML，而 DDEML 會將控制碼傳遞給接收資料交易之應用程式的 DDE 回呼函數。

下列範例顯示如何建立 DDE 物件，並取得物件的控制碼。 在 [**XTYP \_ ADVREQ**](xtyp-advreq.md) 交易期間，回呼函式會將目前的時間轉換為 ASCII 字串、將字串複製到本機緩衝區，然後建立包含字串的 DDE 物件。 回呼函式會將 HDDEDATA) 的控制碼傳回給 DDE 物件， (將控制碼傳遞給用戶端應用程式的 DDEML。


```
typedef struct tagTIME 
{ 
    INT     hour;   // 0 - 11 hours for analog clock 
    INT     hour12; // 12-hour format 
    INT     hour24; // 24-hour format 
    INT     minute; 
    INT     second; 
    INT     ampm;   // 0 - AM , 1 - PM 
} TIME; 
 
HDDEDATA EXPENTRY DdeCallback(uType, uFmt, hconv, hsz1, hsz2, 
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
 
    CHAR szBuf[32];
    HRESULT hResult;
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uType) 
    { 
    case XTYP_ADVREQ: 
        if ((hsz1 == hszTime && hsz2 == hszNow) && 
                (uFmt == CF_TEXT)) 
        { 
            // Copy the formatted string to a buffer. 
 
            itoa(tmTime.hour, szBuf, 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.minute < 10)
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
                if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            } 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.minute, &szBuf[*pcch], 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.second < 10) 
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.second, &szBuf[*pcch], 10);
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            } 
            szBuf[*pcch] = '\0'; 
 
            // Create a global object and return its data handle. 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            return (DdeCreateDataHandle( 
                idInst, 
                (LPBYTE) szBuf,     // instance identifier 
                *pcch + 1,          // source buffer length 
                0,                  // offset from beginning 
                hszNow,             // item name string 
                CF_TEXT,            // clipboard format 
                0));                // no creation flags 
        } else return (HDDEDATA) NULL; 
 
    // Process other transactions. 
    } 
} 
```



接收應用程式會將資料控制碼傳遞至 [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) 函式，以取得 DDE 物件的指標。 **DdeAccessData** 所傳回的指標提供唯讀存取。 應用程式應該使用指標來檢查資料，然後呼叫 [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) 函式使指標失效。 應用程式可以使用 [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) 函數，將資料複製到本機緩衝區。

下列範例會取得 *hData* 參數所識別之 DDE 物件的指標、將內容複寫到本機緩衝區，然後使指標失效。


```
HDDEDATA hdata; 
LPBYTE lpszAdviseData; 
DWORD cbDataLen; 
DWORD i; 
char szData[32]; 
 
// 
case XTYP_ADVDATA: 
    lpszAdviseData = DdeAccessData(hdata, &cbDataLen); 
    for (i = 0; i < cbDataLen; i++) 
        szData[i] = *lpszAdviseData++; 
    DdeUnaccessData(hdata); 
    return (HDDEDATA) TRUE; 
//
```



通常，當建立資料處理程式的應用程式將該控制碼傳遞給 DDEML 時，控制碼在建立的應用程式中會變成無效。 如果應用程式必須只與單一應用程式共用資料，則這種情況並不會造成問題。 但是，如果應用程式必須與多個應用程式共用相同的資料，則建立應用程式應該 \_ 在 [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)中指定 HDATA APPOWNED 旗標。 這麼做會將 DDE 物件的擁有權提供給建立的應用程式，並防止 DDEML 使資料控制碼失效。 然後，應用程式只會在呼叫 **DdeCreateDataHandle** 一次之後，將資料處理程式傳遞到任何次數。

如果應用程式 \_ 在 [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)的 *AFCMD* 參數中指定 HDATA APPOWNED 旗標，則必須呼叫 [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle)函式來釋放記憶體控制碼，而不論它是否將控制碼傳遞給 DDEML。 在結束之前，應用程式必須呼叫 **DdeFreeDataHandle** 來釋放它所建立但未傳遞至 DDEML 的任何資料處理程式。

尚未將控制碼傳遞給 DDEML 的應用程式可以將資料加入至物件，或使用 [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) 函數來覆寫物件中的資料。 一般而言，應用程式會使用 **DdeAddData** 來填滿未初始化的 DDE 物件。 當應用程式將資料控制碼傳遞給 DDEML 之後，就無法變更控制碼所識別的 DDE 物件;只能釋放。

 

 




