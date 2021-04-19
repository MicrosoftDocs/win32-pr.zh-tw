---
description: 若要取得無效邏輯網路的通知，請使用 WSANSPIoctl 函數來註冊網路位置變更事件。
ms.assetid: 531b6269-5f35-44c1-ad0f-c5f103029893
title: 查詢 NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac7a4f57e14bb967b04d3a9fd6fe66717da3878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982361"
---
# <a name="querying-nla"></a>查詢 NLA

若要取得無效邏輯網路的通知，請使用 [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) 函數來註冊網路位置變更事件。 您可以使用兩種方法來判斷先前有效的網路位置是否失效：輪詢方法，或使用重迭 i/o 或 Windows 訊息的通知。

查詢會使用 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)、 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 和 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) 函式來形成，以列舉所有可用的邏輯網路。 本節的其餘部分會個別說明這些函式的用法，從 **WSALookupServiceBegin** 函數開始。

> [!Note]  
> NLA 需要 Mswsock .h 標頭檔，其預設不包含在 Winsock2 檔案中。

 

## <a name="step-1-initiate-the-query"></a>步驟1：起始查詢

如需快速參考， [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) 函式具有下列語法：

``` syntax
INT WSALookupServiceBegin(
  LPWSAQUERYSET lpqsRestrictions,
  DWORD dwControlFlags,
  LPHANDLE lphLookup
);
```

NLA 支援下列 *dwControlFlags* 查閱旗標：

<dl> LUP \_ 傳回 \_ 名稱  
LUP \_ 傳回 \_ 批註  
LUP \_ 傳回 \_ BLOB  
LUP \_ 傳回 \_ 全部  
LUP \_ 深度  
</dl>

這些旗標會將後續呼叫 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)時所傳回的結果集限制為包含指定類型之欄位的網路。 例如， \_ \_ 在 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)函式呼叫的 *dwControlFlags* 參數中指定 LUP RETURN BLOB，會將對 **WSALookupServiceNext** 的後續呼叫的結果集限制為包含 BLOB 資訊的網路。 使用 LUP \_ RETURN \_ ALL 旗標相當於指定 LUP 傳回 \_ \_ 名稱、LUP 傳回 \_ \_ 批註和 LUP 傳回 \_ \_ BLOB，但不是 LUP \_ 深度。

如需這些查閱旗標的說明，請參閱 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) 函數參考頁面。

*LphLookup* 參數中 nla 所傳回的查閱控制碼是 nla 私用的，而且不應該修改。 由於傳回的控制碼對 NLA 而言是私用的，因此無法使用 [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) 等函數。

在成功完成時，NLA 會傳回零，如 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) 函數參考頁面中所定義。 否則，NLA 支援下列錯誤碼。

| 錯誤                    | 意義                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | 未執行成功呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 函式來初始化 NLA。                                                   |
| WSAEINVAL                | 有一或多個參數無效，或在函式呼叫中指定的參數適用于 IP 以外的通訊協定。                                         |
| \_找不 \_ 到 WSASERVICE   | 在 *lpqsRestrictions* 參數中傳遞之 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構的 *LPSERVICECLASSID* 參數包含不正確 GUID。 |
| WSANO \_ 資料              | \_ *DwControlFlags* 參數中指定了 LUP 容器旗標。                                                                                       |
| WSAEFAULT                | 嘗試存取使用者提供的參數時發生存取違規。                                                                            |
| WSASYSNOTREADY           | NLA 服務無法處理要求。                                                                                                      |
| WSA \_ 沒有 \_ 足夠的 \_ 記憶體 | NLA 或 NLA 服務無法配置足夠的記憶體來處理此要求。                                                                        |



 

## <a name="step-2-perform-the-query"></a>步驟2：執行查詢

查詢 NLA 的下一個步驟需要使用 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 函數。 如需快速參考， **WSALookupServiceNext** 函數具有下列語法：

``` syntax
INT WSALookupServiceNext(
  HANDLE hLookup,
  DWORD dwControlFlags,
  LPDWORD lpdwBufferLength,
  LPWSAQUERYSET lpqsResults
);
```

*LLookup* 參數是從上一次呼叫 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)函數所傳回的查詢控制碼。

*DwControlFlags* 參數支援下列旗標：

<dl> LUP \_ 傳回 \_ 名稱  
LUP \_ 傳回 \_ 批註  
LUP \_ 傳回 \_ BLOB  
LUP \_ 傳回 \_ 全部  
LUP \_ FLUSHPREVIOUS  
</dl>

這些旗標獨立于 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) 函式呼叫中支援的旗標。 請注意，先前呼叫 **WSALookupServiceBegin** 函式所指定的任何條件約束都會限制查閱;使用 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 函式新增旗標，以嘗試將查詢擴大至 **WSALookupServiceBegin** 呼叫中指定的條件約束以外的範圍，會以無訊息方式略過。 不過，您可以指定一組比 **WSALookupServiceBegin** 呼叫中所指定更嚴格的旗標。

如果 *lpqsResults* 中詳細說明的網路是使用中的網路，則會附加一系列的 **NLA \_ BLOB** 結構，如同 *lpqsResults* 中所傳回之 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構的 **lpBlob** 成員所指定。 這些 **NLA \_ blob** 結構可能是連結的，而且可以藉由在 \_ nextOffset 為非零值的情況下，透過遍歷清單來列舉。 若要取得所有網路位置資訊的結果，請繼續呼叫 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)，直到 \_ 不傳回 WSA E \_ NO \_ 其他錯誤為止（如 **WSALookupServiceNext** 參考頁面中所述）。

[**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)函式也會與 [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)函數搭配使用，以接收網路變更的通知。 如需詳細資訊，請參閱 [來自 NLA 的通知](notification-from-nla-2.md) 。

在成功完成時，NLA 會傳回零。 NLA 的用戶端應該繼續呼叫 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)，函式直到 \_ 未傳回 WSA E 為止 \_ \_ ，表示已傳回可用網路的所有相關資訊。

否則，呼叫 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)，適用于 NLA 的函式支援下列錯誤碼。

| 錯誤                    | 意義                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | 未執行初始化 NLA 的 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 函式的成功呼叫。                                                                                                                                                                                                                                                                                                |
| WSA \_ 不正確 \_ 控制碼     | *HLookup* 參數中提供的查閱控制碼不是有效的 NLA SP 控制碼。 用戶端必須先呼叫 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) 函式，並接收有效的 NLA SP 控制碼，以取得查詢結果。                                                                                                                                                               |
| WSAESYSNOTREADY          | NLA 服務無法處理此要求。                                                                                                                                                                                                                                                                                                                                                     |
| WSAEFAULT                | *LpdwBufferLength* 參數中指定的緩衝區大小不足以保存 *lpqsResults* 所指向的結果。 必要的緩衝區是在 *lpdwBufferLength* 中指定;如果用戶端無法提供夠大的緩衝區，用戶端可以呼叫 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 函數，並將 *DWCONTROLFLAGS* 設定為 LUP \_ FLUSHPREVIOUS，以略過該專案。 |
| WSA \_ 沒有 \_ 足夠的 \_ 記憶體 | 因為呼叫進程中的記憶體不足，所以 NLA 無法從 NLA 系統服務取得網路資訊。                                                                                                                                                                                                                                                                                  |
| WSA \_ E \_ 否 \_ 其他         | 沒有其他網路可列舉查詢。                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="step-3-terminate-the-query"></a>步驟3：終止查詢

當所有對 NLA 的查詢都已完成，而且應用程式不再需要使用 NLA 時，應該呼叫 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) 函數。 如果應用程式會根據提交的查詢接收變更通知，請勿呼叫 **WSALookupServiceEnd** 。 如需接收通知的詳細資訊，請參閱 [來自 NLA 的通知](notification-from-nla-2.md) 。 如同大部分的 Windows 通訊端服務提供者，NLA 會維護其用戶端的參考計數。 當對 NLA 的查詢完成時呼叫 **WSALookupServiceEnd** 函式，可讓 NLA 不再需要的系統資源被釋放。

NLA 支援下列 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) 函式呼叫的錯誤碼。

| 錯誤                | 意義                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED    | 未執行成功呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 函式來初始化 NLA。 |
| WSA \_ 不正確 \_ 控制碼 | *HLookup* 參數中提供的控制碼不是有效的 NLA SP 控制碼。                             |



 

 

 



