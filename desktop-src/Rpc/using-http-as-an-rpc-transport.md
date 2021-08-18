---
title: 使用 HTTP 做為 RPC 傳輸
description: RPC over HTTP 可讓用戶端程式使用網際網路，在遠端網路上執行伺服器程式所提供的程式。
ms.assetid: b5062d70-7625-4a9f-a8c1-025ef8342fcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8775aab1771dcc6da9cade97d36c7141d6d66d8bc8172a20c8263ef64b8ed7ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010779"
---
# <a name="using-http-as-an-rpc-transport"></a>使用 HTTP 做為 RPC 傳輸

RPC over HTTP 可讓用戶端程式使用網際網路，在遠端網路上執行伺服器程式所提供的程式。 RPC over HTTP 會透過已建立的 HTTP 埠對其呼叫進行通道處理。 因此，其呼叫可以跨用戶端和伺服器網路上的網路防火牆。

RPC over HTTP 會將其呼叫路由傳送至位於 RPC 伺服器網路上的 RPC proxy。 RPC Proxy 會建立和維護與 RPC 伺服器的連線。 它可做為 proxy、將遠端程序呼叫發送至 RPC 伺服器，並將伺服器的回復傳送回用戶端應用程式。 下圖說明此程式。

![rpc 伺服器與適用于 rpc HTTP 的網際網路資訊伺服器之間的互動](images/httprpc1.png)

此圖表顯示用戶端應用程式網路上的防火牆。 RPC over HTTP 不需要這麼做就能運作。 但是，如果用戶端網路有防火牆，則也需要 proxy 伺服器程式，例如 Microsoft Proxy 伺服器。

當用戶端程式發出使用 HTTP 做為傳輸的遠端程序呼叫時，用戶端上的 RPC 執行時間程式庫會聯繫 RPC proxy。 根據 RPC 用戶端是否要求使用 HTTP 或 HTTPS (使用 SSL 的 HTTP) 埠80或埠443。 RPC proxy 會聯繫 RPC 伺服器程式，並建立 TCP/IP 連接。 用戶端和 RPC proxy 會維護其在網際網路上的 HTTP 或 HTTPS 連線。 用戶端對 RPC proxy 的 HTTP 或 HTTPS 連線可以通過防火牆 (受限於適當存取權限) 如果有的話）。 然後伺服器可以執行遠端程序呼叫，並透過 RPC proxy 使用連接來回複用戶端。 RPC proxy 是在 IIS 內容中執行的 ISAPI 延伸模組。

如果用戶端或伺服器因為任何原因而中斷連線，RPC proxy 將會偵測到它並結束 RPC 會話。 只要會話繼續，RPC proxy 就會維持與用戶端和伺服器的連接。 它會將遠端程序呼叫從用戶端轉送到伺服器，並將回復從伺服器傳送到用戶端。

RPC 用戶端程式可以建立表單的字串系結，藉以透過網際網路將 RPC 呼叫通道：

``` syntax
[object_uuid@]ncacn_http:rpc_server[endpoint,HttpProxy=proxy_server:http_port,RpcProxy=rpc_proxy:rpc_port,HttpConnectionOption=UseHttpProxy]
```

其中：

-   *物件 \_ UUID* 指定 RPC 物件 uuid。 如需詳細資訊，請參閱 [產生介面 uuid](generating-interface-uuids.md) 和 [字串 UUID](string-uuid.md)。
-   **ncacn \_ HTTP** 會選取 RPC over HTTP 的通訊協定順序規格。 如需詳細資訊，請參閱 [通訊協定順序常數](protocol-sequence-constants.md) 和 [字串](string-binding.md)系結。
-   *rpc \_ 伺服器* 是執行 rpc 伺服器進程之電腦的網路位址。 伺服器位址必須以可由 RPC proxy 電腦看見且可理解的形式指定，而不是由用戶端來指定。 由於用戶端不會直接連線到伺服器，因此不需要能夠解析伺服器的名稱，也不需要建立與伺服器的連接。 RPC proxy 會代表用戶端建立連線，因此 *rpc \_ 伺服器* 必須是 rpc proxy 可辨識的名稱。
-   *端點* 會指定 RPC 伺服器進程接聽遠端程序呼叫的 tcp/ip 通訊埠。 如需詳細資訊，請參閱 [尋找端點](finding-endpoints.md)。
-   **HttpProxy** 選擇性地指定 RPC 用戶端網路上的 HTTP proxy 伺服器，例如 Microsoft proxy 伺服器。 如果選取 proxy 伺服器，則不會指定埠號碼，如果未要求 SSL，RPC 存根預設會使用埠80，而如果指定了 SSL，則會使用埠443。
-   **RpcProxy** 指定作為 RPC 伺服器之 PROXY 的 IIS 電腦的位址和埠號碼。 如果 RPC 伺服器進程位於與 RPC proxy 不同的電腦上，您只需要指定此程式。 如果未指定埠號碼，則如果未指定 SSL，RPC 用戶端存根預設會使用埠80，如果指定 SSL (HTTPS) ，則會使用埠443。
-   **HttpConnectionOption** 可選擇性地讓您在進行 HTTP 連線時，指示 RPC 的行為。 **UseHttpProxy** 值會指示 RPC 隨時透過 Http proxy 路由傳送流量，包括當用戶端的網際網路選項設定在 Internet Explorer 為「針對本機位址略過 proxy 伺服器」的時候。

    Windows 7、Windows Server 2008 R2、Windows 8.1 和已安裝 KB2916915 的 Windows Server 2012 R2 都支援此選項。 Windows 8 和 Windows Server 2012 不支援這個選項。 應用程式可以藉由檢查位於下列登錄機碼底下的 **ConnectionOptionsFlag** 登錄值，來判斷 RPC 執行時間是否支援此選項：

    **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Rpc**

    如果設定此登錄值的位 0 (LSB) ，則支援此特定選項。否則，系統中的 RPC 執行時間不支援此選項。

如需有關建立字串系結的詳細資訊，請參閱系結 [和控制碼](binding-and-handles.md)。

RPC 伺服器程式可以接聽 ncacn \_ HTTP 通訊協定順序，接受通道的 rpc 呼叫。

Microsoft 有兩個主要的 RPC over HTTP 執行：第1版和第2版。

第1版 (透過 Windows XP 來支援呼叫 RPC over HTTP v1) 。 Windows 2000 支援 RPC proxy 的第1版。

第2版 (稱為 RPC over HTTP v2) 是目前的版本。

這兩個版本具有不同的功能和有限的互通性。 此處提供差異摘要。 如需互通性考慮，請參閱 [RPC OVER HTTP 的系統需求和互通性](system-requirements-and-interoperability-for-rpc-over-http.md)。

-   RPC over HTTP v1 需要在 RPC over HTTP 用戶端與 RPC proxy 之間的所有 HTTP proxy/防火牆上啟用 SSL 通道。 RPC over HTTP v1 會嘗試透過埠80建立 SSL Tunnel，即使它所傳送的資料實際上不是 SSL 加密也一樣。 Proxy 和防火牆通常會拒絕這類要求，除非明確設定為允許這些要求。 RPC over HTTP v2 沒有這類需求。
-   RPC over HTTP v1 無法與 RPC proxy 建立 SSL 會話。 RPC over HTTP v2 可以在 SSL 會話內傳送所有 RPC over HTTP 流量;依預設，v2 需要在 SSL 會話內傳送資料。
-   RPC over HTTP v1 無法向 RPC proxy 驗證。 RPC over HTTP v2 可以進行驗證;依預設，v2 需要驗證 RPC proxy。
-   當安裝的 IIS 電腦是 web 伺服陣列的一部分時，RPC proxy v1 無法正常運作。 當安裝的 IIS 電腦是 web 伺服陣列的一部分時，RPC proxy v2 會正常運作。

> [!Note]  
> 如果用戶端程式的電腦上已安裝 Microsoft Internet Explorer，而您的用戶端未在其字串系結中指定 **HttpProxy** ，則 RPC 用戶端 stub 會在用戶端電腦上搜尋登錄中的 **HttpProxy** 專案。 如果找到一個，就會使用登錄專案中指定的 proxy。

 

比方說，假設您的用戶端程式需要在電腦之間連線到名為 Server7.microsoft.com 的電腦上的 RPC 伺服器。 此外，假設 RPC proxy 是在 Major7.microsoft.com 上執行。 RPC 伺服器程式會接聽埠2225。 您的用戶端會使用字串系結：

``` syntax
ncacn_http:Server7.microsoft.com[2225, RpcProxy=Major7.microsoft.com]
```

如果 RPC proxy 可以將伺服器名稱解析為 Server7，而不需要完整的功能變數名稱，您也可以指定：

``` syntax
ncacn_http:Server7 [2225, RpcProxy=Major7.microsoft.com]
```

如果用戶端網路使用名為 myproxy 的防火牆和網際網路 proxy 伺服器，而且用戶端上的 Internet Explorer 未設定為使用該 proxy，您就必須修改用戶端的字串系結至：

``` syntax
ncacn_http:Server7.microsoft.com[,HttpProxy=myproxy:80,RpcProxy=Major7.microsoft.com:80]
```

這會指示用戶端連接到 Server7.microsoft.com 上的 RPC 伺服器程式。 若要這樣做，用戶端會先使用埠 80 (或埠443（如果使用 SSL) 連接到 myproxy）。 這會讓用戶端程式存取網際網路。 使用網際網路時，用戶端程式會接著連接到 Major7.microsoft.com 上的 RPC proxy。 RPC proxy 將會建立與在 Server7.microsoft.com 上執行之 RPC 伺服器程式的連接。

如果用戶端網路使用防火牆，而且如果無法直接連線到 RPC proxy，則可以將用戶端字串系結修改為：

``` syntax
ncacn_http:Server7.microsoft.com[RpcProxy=Major7.microsoft.com:80,HttpConnectionOption=UseHttpProxy]
```

**HttpConnectionOption** 可讓您在進行 HTTP 連線時，指示 RPC 的行為。 **UseHttpProxy** 值會指示 RPC 隨時透過 Http proxy 路由傳送流量，包括當用戶端的網際網路選項設定在 Internet Explorer 為「針對本機位址略過 proxy 伺服器」的時候。 這會指示用戶端透過 Http proxy 強制連接至 RPC proxy。 這可加速建立連接的時間，因為它會略過在使用 HTTP proxy 之前，直接搜尋 RPC 伺服器的任何延遲。

如果使用 **HttpConnectionOption** 選項，且用戶端上的 Internet Explorer 未設定為使用該 Http proxy，則連線可能會失敗，並出現 **RPC \_ S \_ 不正確 \_ 網路 \_ 選項**。

現今大部分的電腦都是針對網頁瀏覽進行設定。 因此，大部分的用戶端不需要指定 **HttpProxy**，因為它會從網際網路連線設定中取出。

 

 




