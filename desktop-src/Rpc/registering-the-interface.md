---
title: 註冊介面
description: 註冊伺服器程式支援的介面，可讓用戶端程式從遠端程序呼叫分派至適當的伺服器常式。
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- 遠端程序呼叫 RPC、工作、註冊介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182980"
---
# <a name="registering-the-interface"></a><span data-ttu-id="ef8a9-104">註冊介面</span><span class="sxs-lookup"><span data-stu-id="ef8a9-104">Registering the Interface</span></span>

<span data-ttu-id="ef8a9-105">註冊伺服器程式支援的介面，可讓用戶端程式從遠端程序呼叫分派至適當的伺服器常式。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-105">Registering the interface that a server program supports enables remote procedure calls from client programs to be dispatched to the proper server routine.</span></span> <span data-ttu-id="ef8a9-106">伺服器程式會呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) 來註冊其介面。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-106">Server programs call [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to register their interfaces.</span></span> <span data-ttu-id="ef8a9-107">下列程式碼片段會示範其用途：</span><span class="sxs-lookup"><span data-stu-id="ef8a9-107">The following code fragment demonstrates its use:</span></span>


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



<span data-ttu-id="ef8a9-108">[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)函式的第一個參數是 MIDL 編譯器從 IDL 檔案產生的結構，該檔案會定義伺服器) 的介面 (或介面。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-108">The first parameter to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is a structure the MIDL compiler generates from the IDL file that defines the interface (or interfaces) for the server.</span></span> <span data-ttu-id="ef8a9-109">第二個和第三個參數分別是 UUID 和進入點向量。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-109">The second and third parameters are a UUID and an entry-point vector, respectively.</span></span> <span data-ttu-id="ef8a9-110">在此範例中，這些值會設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-110">They are set to **NULL** in this example.</span></span> <span data-ttu-id="ef8a9-111">在許多情況下，您的伺服器程式會將這些參數值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-111">In many instances, your server program will set these parameter values to **NULL**.</span></span> <span data-ttu-id="ef8a9-112">當伺服器程式在介面中提供相同程式的多個程式時，會使用第二個和第三個參數。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-112">Server programs use the second and third parameters when they provide multiple implementations of the same procedures in an interface.</span></span> <span data-ttu-id="ef8a9-113">如需詳細資訊，請參閱 [進入點向量](registering-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-113">For more information, see [Entry-Point Vectors](registering-interfaces.md).</span></span>

<span data-ttu-id="ef8a9-114">伺服器程式也可以使用 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) 來註冊介面。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-114">Server programs can also use [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) to register an interface.</span></span> <span data-ttu-id="ef8a9-115">使用此函式的其中一個優點是，它會提供您的應用程式設定安全性回呼函式的能力。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-115">One advantage of using this function is that it provides your application with the ability to set a security-callback function.</span></span> <span data-ttu-id="ef8a9-116">使用安全性回呼函數是保護介面安全的建議方法。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-116">Using security-callback functions is the recommended approach to securing an interface.</span></span>

> [!Note]  
> <span data-ttu-id="ef8a9-117">MIDL 會產生兩個非常類似的結構，一個用於用戶端，另一個用於伺服器。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-117">MIDL produces two very similar structures, one for the client and one for the server.</span></span> <span data-ttu-id="ef8a9-118">傳遞至 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) 函數的結構是 MIDL 產生之結構的伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-118">The structure passed to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is the server version of the MIDL-produced structure.</span></span>

 

 

 




