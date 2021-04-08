---
title: ncacn_HTTP 屬性
description: Ncacn \_ HTTP 關鍵字會識別 Microsoft Internet Information Server (IIS) 作為端點的通訊協定系列。
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_HTTP 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7043aaa3a011b37a4b593a03b2d74658caab6fde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682117"
---
# <a name="ncacn_http-attribute"></a>ncacn \_ HTTP 屬性

**Ncacn \_ HTTP** 關鍵字會識別 Microsoft Internet INFORMATION Server (IIS) 作為端點的通訊協定系列。

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a>參數

<dl> <dt>

*rpc \_ 伺服器* 
</dt> <dd>

執行 RPC 伺服器進程之電腦的網際網路位址或名稱。

</dd> <dt>

*端點* 
</dt> <dd>

RPC 伺服器進程正在接聽的知名 (靜態) TCP/IP 通訊埠。

</dd> </dl>

## <a name="remarks"></a>備註

識別 Microsoft Internet Information Server (IIS) 作為通訊協定系列，可讓用戶端和伺服器應用程式使用 Microsoft Internet Information Server (IIS) 作為 proxy，在網際網路上進行通訊。 由於呼叫是透過已建立的 HTTP 埠傳送通道，因此可以跨防火牆。

任何 RPC 用戶端和伺服器應用程式都可以支援 **ncacn \_ HTTP** 通訊協定，只要它們已聯網至網際網路資訊伺服器即可。 IIS 會聯繫 RPC 伺服器，並建立 TCP/IP 通訊端，以供用戶端維護。 IIS 會與 RPC 伺服器協調 TCP/IP 連線，一旦協商完成，就會成為 RPC proxy，在用戶端 TCP/IP 通訊端與伺服器端 TCP/IP 通訊端之間轉送資料。 當 IIS RPC proxy 偵測到用戶端或伺服器端的會話關閉時，它會關閉剩餘的通訊端。

用戶端應用程式會隱含地使用靜態系結至 IIS，但是伺服器可以使用動態端點，以及伺服器的 RPCSS (端點對應程式) 解析 RPC 伺服器埠。 如果 IIS 與 RPC 伺服器位於不同的電腦上，則 IIS 會接收遠端呼叫、在 RPC 伺服器電腦上聯繫 RPCSS 以取得伺服器進程端點，然後再將呼叫轉送至適當的 RPC 伺服器。

如果 Internet Explorer 已安裝，則傳輸會檢查登錄，以查看是否有 HTTP proxy 的設定。 如果有 proxy 存在，則傳輸會使用它。

## <a name="examples"></a>範例

``` syntax
//RPC client accesses an RPC server application, which is listening on //endpoint 2225 of an IIS Web Server named major7.microsoft.com 
[   
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.0), 
    endpoint("ncacn_http:major7.microsoft.com[2225]") 
] 
interface iface
{
    // Interface definition statements.
}

//string binding format. 
//IIS Web server (websvr1)is on a different machine than the RPC
//server, and endpoints are dynamic
"obj_uuid@ncacn_http:major7.microsoft.com
    [,]"

//tells the transport to use proxysvr, port 80, as the outgoing http 
//server:
"obj_uuid@ncacn_http:major7.microsoft.com[,]"
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**端點**](endpoint.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**字串系結**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 