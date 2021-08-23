---
description: PNRP 使用 WSANSPIoctl 函式來接收有關下列變更的通知。
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP 和 WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cc07415fb483e75af8d836274d45a2c53f205e3aae15f893f909d2363c0d15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553308"
---
# <a name="pnrp-and-wsanspioctl"></a>PNRP 和 WSANSPIoctl

PNRP 使用 [**WSANSPIoctl**](winsock-nsp-reference-links.md) 函式來接收有關下列變更的通知：

-   網路雲端清單
-   名稱解析要求的結果可用性

第一次呼叫 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) 時，會定義用戶端收到通知的資訊類型。 您可以使用 Windows 訊息、完成常式、WSAEVENT 物件的控制碼，或埠來通知用戶端。 如需選項和設定 *lpCompletion* 參數的詳細資訊，請參閱 **WSANSPIoctl**。

若要在呼叫 [**WSALookupServiceNext**](winsock-nsp-reference-links.md)之後繼續接收通知，應用程式必須再次呼叫 **WSANSPIoctl** 。

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)函式會封鎖，即使呼叫 **WSANSPIoctl** 也是一樣。 在呼叫 **WSALookupServiceNext** 之前，應用程式必須等到收到通知（如果封鎖發生問題）。

呼叫此函式時，參數必須具有下列值：

<dl> <dt>

<span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*
</dt> <dd>

指定 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) 傳回的控制碼。

</dd> <dt>

<span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*
</dt> <dd>

必須是 **SIO 的 \_ NSP \_ 通知 \_ 變更**。

</dd> <dt>

<span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*
</dt> <dd>

必須是 **Null**。

</dd> <dt>

<span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*
</dt> <dd>

必須為零 (0) 。

</dd> <dt>

<span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*
</dt> <dd>

必須是 **Null**。

</dd> <dt>

<span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*
</dt> <dd>

必須為零 (0) 。

</dd> <dt>

<span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*
</dt> <dd>

必須是 **Null**。

</dd> <dt>

<span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*
</dt> <dd>

指定 **Null** 或 [**WSACOMPLETION**](winsock-nsp-reference-links.md) 結構的指標。

</dd> </dl>

收到通知之後，請呼叫 [**WSALookupServiceNext**](winsock-nsp-reference-links.md) 一次以取得結果。

若要結束搜尋，請呼叫 [**WSALookupServiceEnd**](winsock-nsp-reference-links.md)。

## <a name="resolution-notifications"></a>解決方案通知

每當新增名稱解析專案時，就可以通知用戶端。 然後，用戶端會呼叫 [**WSALookupServiceNext**](winsock-nsp-reference-links.md) 來取得解析資料。

如果用戶端未使用這項技術，就可以封鎖對 [**WSALookupServiceNext**](winsock-nsp-reference-links.md) 的呼叫，直到指定的超時時間發生為止。

## <a name="cloud-list-notifications"></a>雲端清單通知

當一組雲端發生變更時，就可以通知用戶端。

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)函式會將 **WSA \_ E \_ NO \_ 其他** 傳回為 set 分隔符號。 用戶端應用程式必須列舉現有的雲端，才會傳回此訊息，然後使用通知配置來取出後續變更。 用戶端應用程式也可以呼叫 **WSALookupServiceNext**，但呼叫會被封鎖，直到發生變更為止。

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)函數會傳回 **WSAQUERYSET** 結構中的雲端。 **DwOutputFlags** 成員中會傳回下列其中一個旗標。



| 值               | 描述                                             |
|---------------------|---------------------------------------------------------|
| \_已 \_ 新增結果   | 已新增傳回的雲端。                    |
| 結果 \_ 已 \_ 變更 | 傳回的雲端已變更。                  |
| 結果 \_ 已 \_ 刪除 | 傳回的雲端已刪除且無效。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PNRP 和 WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP 和 WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP 和 WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[PNRP NSP 錯誤碼](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSANSPIoctl**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSALookupServiceBegin**
</dt> <dt>

**WSALookupServiceEnd**
</dt> <dt>

**WSAQUERYSET**
</dt> </dl>

 

 



