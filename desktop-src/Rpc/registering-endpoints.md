---
title: 註冊端點
description: 在伺服器主機電腦的端點對應中註冊伺服器程式，可讓用戶端程式判斷哪個端點 (通常是 TCP/IP 通訊埠，或是伺服器程式正在接聽的具名管道) 。
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- 遠端程序呼叫 RPC、工作、註冊端點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23e02aaae18a9d28b989d16850693a8a8f0678e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671084"
---
# <a name="registering-endpoints"></a><span data-ttu-id="b1617-104">註冊端點</span><span class="sxs-lookup"><span data-stu-id="b1617-104">Registering Endpoints</span></span>

<span data-ttu-id="b1617-105">在伺服器主機電腦的端點對應中註冊伺服器程式，可讓用戶端程式判斷哪個端點 (通常是 TCP/IP 通訊埠，或是伺服器程式正在接聽的具名管道) 。</span><span class="sxs-lookup"><span data-stu-id="b1617-105">Registering the server program in the endpoint map of the server host computer enables client programs to determine which endpoint (usually a TCP/IP port or a named pipe) the server program is listening to.</span></span> <span data-ttu-id="b1617-106">伺服器程式會呼叫 [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) 函式，如下列程式碼片段所示，在伺服器主機系統的端點對應中註冊自己：</span><span class="sxs-lookup"><span data-stu-id="b1617-106">To register itself in the server host system's endpoint map, a server program calls the [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) function as shown in the following code fragment:</span></span>


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



<span data-ttu-id="b1617-107">[**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)的第一個參數是表示介面的結構。</span><span class="sxs-lookup"><span data-stu-id="b1617-107">The first parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is the structure that represents the interface.</span></span> <span data-ttu-id="b1617-108">您可以在 MIDL 編譯器從 MIDL 檔案為此分散式應用程式產生的標頭檔中找到它。</span><span class="sxs-lookup"><span data-stu-id="b1617-108">You can find it in the header file that the MIDL compiler generated from your MIDL file for this distributed application.</span></span> <span data-ttu-id="b1617-109">請參閱 [開發介面](developing-the-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="b1617-109">See [Developing the Interface](developing-the-interface.md).</span></span> <span data-ttu-id="b1617-110">接下來， **RpcEpRegister** 需要您的應用程式傳遞一組儲存在系結向量中的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="b1617-110">Next, **RpcEpRegister** needs your application to pass a set of binding handles that are stored in a binding vector.</span></span>

<span data-ttu-id="b1617-111">除了註冊介面名稱之外，您的伺服器應用程式也可以在端點對應中註冊物件 Uuid。</span><span class="sxs-lookup"><span data-stu-id="b1617-111">In addition to registering interface names, your server application can also register object UUIDs in the endpoint map.</span></span> <span data-ttu-id="b1617-112">在此範例中，沒有任何物件 Uuid 可註冊，因此 [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) 的第三個參數會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b1617-112">In this example, there are no object UUIDs to register, so the third parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is set to **NULL**.</span></span>

<span data-ttu-id="b1617-113">最後一個參數是批註字串。</span><span class="sxs-lookup"><span data-stu-id="b1617-113">The last parameter is a comment string.</span></span> <span data-ttu-id="b1617-114">雖然 RPC 執行時間程式庫不會使用此字串，但建議您設定字串，因為它可改善系統的管理性。</span><span class="sxs-lookup"><span data-stu-id="b1617-114">Although the RPC run-time library does not use this string, setting the string is recommended, as it improves manageability of the system.</span></span> <span data-ttu-id="b1617-115">系統管理員可以使用此字串來偵測哪些應用程式所使用的埠，然後這些應用程式可以用來判斷防火牆要管理哪些埠。</span><span class="sxs-lookup"><span data-stu-id="b1617-115">A system administrator can use the string to detect which ports are used by which applications, which can then be used to determine which ports to be managed by firewalls.</span></span>

 

 




