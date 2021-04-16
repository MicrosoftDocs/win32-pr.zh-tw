---
description: Microsoft Windows HTTP Services (WinHTTP) 使用控制碼來追蹤使用 HTTP 通訊協定時所需的設定和資訊。
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: WinHTTP 中的 HINTERNET 控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf374675ad6f2114dd48e0a3ff1db50cd0dd7f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558197"
---
# <a name="hinternet-handles-in-winhttp"></a>WinHTTP 中的 HINTERNET 控制碼

Microsoft Windows HTTP Services (WinHTTP) 使用控制碼來追蹤使用 HTTP 通訊協定時所需的設定和資訊。 每個控制碼都會維護與 HTTP 會話相關的資訊、與 HTTP 伺服器的連線，或特定的資源。 本主題將描述各種類型的控制碼、這些控制碼的命名慣例，以及其階層式結構。

-   [關於 HINTERNET 控制碼](#about-hinternet-handles)
-   [命名控制碼](#naming-handles)
-   [控制碼階層](#handle-hierarchy)
-   [控制碼階層的說明](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>關於 HINTERNET 控制碼

WinHTTP 所建立和使用的控制碼稱為 **HINTERNET** 控制碼。 WinHTTP 函式會傳回無法與其他控制碼互換的 **HINTERNET** 控制碼，因此不能與 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 或 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)等函數一起使用。 同樣地，其他控制碼也不能與 WinHTTP 函數一起使用。 例如， [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 所傳回的控制碼無法傳遞至 [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)。 當使用控制碼的 API 呼叫正在進行中時，無法關閉這些 **HINTERNET** 控制碼。 為了避免競爭情形，只要 API 呼叫正在進行中，應用程式就應該保護控制碼，並防止它關閉。

Microsoft Win32 Internet (WinInet) 函數也會使用 **HINTERNET** 控制碼。 但是，WinInet 函式中使用的控制碼無法與 WinHTTP 函數中使用的控制碼交換。 如需 WinInet 的詳細資訊，請參閱 [關於 wininet](/windows/desktop/WinInet/about-wininet)。

[**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)函式會關閉 WinHTTP **HINTERNET** 控制碼。

## <a name="naming-handles"></a>命名控制碼

在整個 WinHTTP 檔中，應用程式開發介面中的函式描述 (API) 和範例程式碼示範如何建立和使用各種類型的 **HINTERNET** 控制碼。 為了追蹤可用的不同類型的控制碼，這些控制碼的命名是一致的。 下表顯示檔中慣例所使用的識別碼。



| 控制碼類型       | 函數建立控制碼                                                                                                          | 識別碼 |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| 泛型控制碼    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)、 [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)或 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | hInternet  |
| 會話控制碼    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hSession   |
| 連接控制碼 | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hConnect   |
| 要求控制碼    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hRequest   |



 

## <a name="handle-hierarchy"></a>控制碼階層

**HINTERNET** 控制碼是在階層中進行維護。 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)傳回的控制碼是會話 **HINTERNET** 控制碼。 呼叫 **WinHttpOpen** 會初始化 WinHTTP 函式，並在會話控制碼的整個存留期間開始維護使用者資訊和設定的會話內容。 [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) 指定目標 HTTP 或 HTTPS 伺服器，並建立連接 **HINTERNET** 控制碼。 根據預設，連接控制碼會繼承會話控制碼的設定。 使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 呼叫所指定的每個資源都會被指派一個要求 **HINTERNET** 控制碼。

下圖說明 **HINTERNET** 控制碼的階層架構。 圖中的每個方塊都代表一個會傳回 **HINTERNET** 控制碼的 WinHTTP 函數。

![建立控制碼的函式](images/art-winhttp2.png)

關閉控制碼之後，應用程式必須準備好接收控制碼上的回呼通知，直到最終的 **WINHTTP \_ 回呼 \_ 狀態 \_ 控制碼 \_ 關閉** 值傳回，以指出控制碼已完全關閉。

會話控制碼稱為它用來建立的任何連接處理常式的父系;同樣地，連接控制碼和其父會話控制碼也稱為連接控制碼用來建立之任何要求控制碼的父系。

當父控制碼關閉時，它所擁有的任何子系都會間接失效，即使未關閉本身也一樣，後續使用這些控制碼的要求也會失敗，並出現錯誤訊息 **\_ \_ 控制碼無效**。 無法依賴暫止的非同步要求來正確完成。

下圖顯示使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)所建立之 **HINTERNET** 控制碼的函式。 陰影方塊代表可建立控制碼的 WinHTTP 函式，而一般方塊則會顯示使用這些 **HINTERNET** 控制碼的函式。 此圖表也會進行組織，以顯示一般呼叫 WinHTTP 函數的順序。

![建立控制碼的函式](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>控制碼階層的說明

首先，使用 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)建立會話控制碼。 [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) 需要會話控制碼做為第一個參數，並傳回指定伺服器的連接控制碼。 要求控制碼是由 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)所建立，它會使用 [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)所建立的連接控制碼。 如果應用程式選擇將額外的標頭新增至要求，或應用程式必須設定認證以進行驗證，則可以使用此要求控制碼來呼叫 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) 和 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) 。 要求是由 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)傳送，此要求會使用要求控制碼。 傳送要求之後，您可以使用 [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)將其他資料傳送至伺服器，或應用程式可以直接跳到 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) ，以指定不會將任何資訊傳送至伺服器。 此時，根據應用程式的用途，您可以使用要求控制碼來呼叫 [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)、 [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)，或使用 [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) 和 [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)來取得資源。

 

 
