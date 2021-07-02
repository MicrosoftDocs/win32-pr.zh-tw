---
description: 本主題將識別 WinHTTP 提供的函式。
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: WinHTTP 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e45289230c1cc22a7f8799dfbbe1dafddccf38
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174976"
---
# <a name="winhttp-functions"></a>WinHTTP 函數

WinHTTP 提供下列功能：

<dl> <dt>

[**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

將一或多個 HTTP 要求標頭新增至 HTTP 要求控制碼。

</dd> <dt>

[**WinHttpAddRequestHeadersEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheadersex)
</dt> <dd>

將一或多個 HTTP 要求標頭新增至 HTTP 要求控制碼，讓您可以使用不同的名稱/值字串。

</dd> <dt>

[**WinHttpCheckPlatform**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

判斷 WinHTTP 是否支援目前的平臺。

</dd> <dt>

[**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

關閉單一 [HINTERNET](hinternet-handles-in-winhttp.md) 控制碼。

</dd> <dt>

[**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

指定 HTTP 要求的初始目標伺服器。

</dd> <dt>

[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

將 URL 分隔成其元件部分，例如，主機名稱和路徑。

</dd> <dt>

[**WinHttpCreateProxyResolver**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

建立 [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)所使用的控制碼。

</dd> <dt>

[**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

從元件部分建立 URL，例如主機名稱和路徑。

</dd> <dt>

[**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

尋找 Proxy 自動設定 (PAC) 檔的 URL。 此函數會報告 PAC 檔案的 URL，但不會下載檔案。

</dd> <dt>

[**WinHttpFreeProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

釋出從先前的 [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)呼叫取出的資料。

</dd> <dt>

[**WinHttpFreeQueryConnectionGroupResult**](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

釋放先前呼叫 [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)所配置的記憶體。

</dd> <dt>

[**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

從登錄抓取預設的 WinHTTP proxy 設定。

</dd> <dt>

[**WinHTTPGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

取得目前使用者的 Internet Explorer (IE) proxy 設定。

</dd> <dt>

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

抓取指定之 URL 的 proxy 資訊。

</dd> <dt>

[**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

抓取指定之 URL 的 proxy 資訊。

</dd> <dt>

[**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

抓取 [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)呼叫的結果。

</dd> <dt>

[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

初始化應用程式對 WinHTTP 函式的使用。

</dd> <dt>

[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

建立 HTTP 要求控制碼。

</dd> <dt>

[**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

傳回伺服器支援的授權配置。

</dd> <dt>

[**WinHttpQueryConnectionGroup**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

抓取 WinHttp 連接的目前狀態原因。

</dd> <dt>

[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

傳回可立即使用 [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)讀取的資料位元組數目。

</dd> <dt>

[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

抓取與 HTTP 要求相關聯的標頭資訊。

</dd> <dt>

[**WinHttpQueryHeadersEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheadersex)
</dt> <dd>

抓取與 HTTP 要求相關聯的標頭資訊;提供一種方式來取出剖析的標頭名稱和值字串。

</dd> <dt>

[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

在指定的控制碼上查詢網際網路選項。

</dd> <dt>

[**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

從 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 函數所開啟的控制碼讀取資料。

</dd> <dt>

[**WinHttpReadDataEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddataex)
</dt> <dd>

從 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 函數所開啟的控制碼讀取資料。

</dd> <dt>

[**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

結束由 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)起始的 HTTP 要求。

</dd> <dt>

[**WinHttpResetAutoProxy**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

重設自動 proxy。

</dd> <dt>

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

將指定的要求傳送至 HTTP 伺服器。

</dd> <dt>

[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

將必要的授權認證傳遞給伺服器。

</dd> <dt>

[**WinHttpSetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

在登錄中設定預設的 WinHTTP proxy 設定。

</dd> <dt>

[**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

設定網際網路選項。

</dd> <dt>

[**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

設定 WinHTTP 可以在作業期間進行的呼叫回呼函數。

</dd> <dt>

[**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

設定與 HTTP 交易相關的各種超時時間。

</dd> <dt>

[**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

根據 HTTP 版本1.0 規格來格式化日期和時間。

</dd> <dt>

[**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

取得 HTTP 時間/日期字串，並將它轉換成 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構。

</dd> <dt>

[**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

將要求資料寫入至 HTTP 伺服器。

</dd> <dt>

[**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

關閉 WebSocket 連接。

</dd> <dt>

[**WinHttpWebSocketCompleteUpgrade**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

完成 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)啟動的 WebSocket 交握。

</dd> <dt>

[**WinHttpWebSocketQueryCloseStatus**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

取得伺服器所傳送的關閉狀態。

</dd> <dt>

[**WinHttpWebSocketReceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

接收來自 WebSocket 連接的資料。

</dd> <dt>

[**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

透過 WebSocket 連接傳送資料。

</dd> <dt>

[**WinHttpWebSocketShutdown**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

將關閉框架傳送至 WebSocket 連接。

</dd> </dl>


