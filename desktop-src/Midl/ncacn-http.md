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
# <a name="ncacn_http-attribute"></a><span data-ttu-id="d8b3a-104">ncacn \_ HTTP 屬性</span><span class="sxs-lookup"><span data-stu-id="d8b3a-104">ncacn\_http attribute</span></span>

<span data-ttu-id="d8b3a-105">**Ncacn \_ HTTP** 關鍵字會識別 Microsoft Internet INFORMATION Server (IIS) 作為端點的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-105">The **ncacn\_http** keyword identifies the Microsoft Internet Information Server (IIS) as the protocol family for the endpoint.</span></span>

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a><span data-ttu-id="d8b3a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8b3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b3a-107">*rpc \_ 伺服器*</span><span class="sxs-lookup"><span data-stu-id="d8b3a-107">*rpc\_server*</span></span> 
</dt> <dd>

<span data-ttu-id="d8b3a-108">執行 RPC 伺服器進程之電腦的網際網路位址或名稱。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-108">The Internet address or name of the machine that the RPC server process is running on.</span></span>

</dd> <dt>

<span data-ttu-id="d8b3a-109">*端點*</span><span class="sxs-lookup"><span data-stu-id="d8b3a-109">*endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="d8b3a-110">RPC 伺服器進程正在接聽的知名 (靜態) TCP/IP 通訊埠。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-110">The well-known (static) TCP/IP port that the RPC server process is listening on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8b3a-111">備註</span><span class="sxs-lookup"><span data-stu-id="d8b3a-111">Remarks</span></span>

<span data-ttu-id="d8b3a-112">識別 Microsoft Internet Information Server (IIS) 作為通訊協定系列，可讓用戶端和伺服器應用程式使用 Microsoft Internet Information Server (IIS) 作為 proxy，在網際網路上進行通訊。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-112">Identifying the Microsoft Internet Information Server (IIS) as the protocol family allows client and server applications to communicate across the internet by using the Microsoft Internet Information Server (IIS) as a proxy.</span></span> <span data-ttu-id="d8b3a-113">由於呼叫是透過已建立的 HTTP 埠傳送通道，因此可以跨防火牆。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-113">Because calls are tunneled through an established HTTP port, they can cross firewalls.</span></span>

<span data-ttu-id="d8b3a-114">任何 RPC 用戶端和伺服器應用程式都可以支援 **ncacn \_ HTTP** 通訊協定，只要它們已聯網至網際網路資訊伺服器即可。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-114">Any RPC client and server applications can support the **ncacn\_http** protocol as long as they are networked to an Internet Information Server.</span></span> <span data-ttu-id="d8b3a-115">IIS 會聯繫 RPC 伺服器，並建立 TCP/IP 通訊端，以供用戶端維護。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-115">The IIS contacts the RPC server and establishes a TCP/IP socket, which it maintains for the client.</span></span> <span data-ttu-id="d8b3a-116">IIS 會與 RPC 伺服器協調 TCP/IP 連線，一旦協商完成，就會成為 RPC proxy，在用戶端 TCP/IP 通訊端與伺服器端 TCP/IP 通訊端之間轉送資料。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-116">The IIS negotiates a TCP/IP connection with the RPC server, and once the negotiation is complete, acts as an RPC proxy, forwarding data between the client-side TCP/IP socket and the server-side TCP/IP socket.</span></span> <span data-ttu-id="d8b3a-117">當 IIS RPC proxy 偵測到用戶端或伺服器端的會話關閉時，它會關閉剩餘的通訊端。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-117">When the IIS RPC proxy detects a session close on either the client or the server side, it closes the remaining socket.</span></span>

<span data-ttu-id="d8b3a-118">用戶端應用程式會隱含地使用靜態系結至 IIS，但是伺服器可以使用動態端點，以及伺服器的 RPCSS (端點對應程式) 解析 RPC 伺服器埠。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-118">The client application implicitly uses static binding to the IIS, but the server can use dynamic endpoints, with the server's RPCSS (endpoint mapper) resolving the RPC server port.</span></span> <span data-ttu-id="d8b3a-119">如果 IIS 與 RPC 伺服器位於不同的電腦上，則 IIS 會接收遠端呼叫、在 RPC 伺服器電腦上聯繫 RPCSS 以取得伺服器進程端點，然後再將呼叫轉送至適當的 RPC 伺服器。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-119">If the IIS is on a different machine than the RPC server, the IIS receives the remote call, contacts RPCSS on the RPC server machine to get the server process endpoint, and then forwards the call to the appropriate RPC server.</span></span>

<span data-ttu-id="d8b3a-120">如果 Internet Explorer 已安裝，則傳輸會檢查登錄，以查看是否有 HTTP proxy 的設定。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-120">If Internet Explorer is installed, the transport will check the registry to see if there is a configuration for an HTTP proxy.</span></span> <span data-ttu-id="d8b3a-121">如果有 proxy 存在，則傳輸會使用它。</span><span class="sxs-lookup"><span data-stu-id="d8b3a-121">If a proxy exists, the transport will use it.</span></span>

## <a name="examples"></a><span data-ttu-id="d8b3a-122">範例</span><span class="sxs-lookup"><span data-stu-id="d8b3a-122">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d8b3a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8b3a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b3a-124">**端點**</span><span class="sxs-lookup"><span data-stu-id="d8b3a-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="d8b3a-125"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="d8b3a-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d8b3a-126">**字串系結**</span><span class="sxs-lookup"><span data-stu-id="d8b3a-126">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 