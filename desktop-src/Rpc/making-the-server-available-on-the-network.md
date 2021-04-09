---
title: 讓伺服器可在網路上使用
description: 在伺服器應用程式接受遠端程序呼叫之前，必須先在網路上提供。
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- 遠端程序呼叫 RPC、工作、使伺服器可供使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021656"
---
# <a name="making-the-server-available-on-the-network"></a><span data-ttu-id="c681d-104">讓伺服器可在網路上使用</span><span class="sxs-lookup"><span data-stu-id="c681d-104">Making the Server Available on the Network</span></span>

<span data-ttu-id="c681d-105">在伺服器應用程式接受遠端程序呼叫之前，必須先在網路上提供。</span><span class="sxs-lookup"><span data-stu-id="c681d-105">Before a server application can accept remote procedure calls, it must be available on the network.</span></span> <span data-ttu-id="c681d-106">若要這樣做，伺服器會向 RPC 執行時間指出它願意接受一或多個通訊協定序列的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c681d-106">To do this, the server indicates to the RPC Run time that it is willing to accept calls on one or more protocol sequences.</span></span> <span data-ttu-id="c681d-107">選擇伺服器應用程式所支援的通訊協定順序是一個重要的決策;不同的通訊協定順序具有非常不同的功能。</span><span class="sxs-lookup"><span data-stu-id="c681d-107">Choosing the protocol sequences a server application supports is an important decision; different protocol sequences have very different capabilities.</span></span> <span data-ttu-id="c681d-108">預期在本機接收呼叫的伺服器應該使用 **ncalrpc**。</span><span class="sxs-lookup"><span data-stu-id="c681d-108">Servers that expect calls to be received locally should use **ncalrpc**.</span></span> <span data-ttu-id="c681d-109">接受遠端呼叫的伺服器應該使用 **ncacn 的 \_ ip \_ tcp**。</span><span class="sxs-lookup"><span data-stu-id="c681d-109">Servers that accept remote calls should use **ncacn\_ip\_tcp**.</span></span> <span data-ttu-id="c681d-110">伺服器不應確認接收呼叫的通訊協定順序，是它們預期接收呼叫的通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="c681d-110">Servers should not verify that the protocol sequence on which they receive calls is the protocol sequence on which they expect to receive calls.</span></span> <span data-ttu-id="c681d-111">如需詳細資訊，請參閱最佳 RPC 程式設計實務中，在相同進程中執行的其他 RPC 端點的小心謹慎。</span><span class="sxs-lookup"><span data-stu-id="c681d-111">See Be Wary of Other RPC Endpoints Running in the Same Process in Best RPC Programming Practices for more information.</span></span>

<span data-ttu-id="c681d-112">下列範例會使用 **ncacn 的 \_ ip \_ tcp**。</span><span class="sxs-lookup"><span data-stu-id="c681d-112">The following example uses **ncacn\_ip\_tcp**.</span></span>

<span data-ttu-id="c681d-113">大部分的伺服器程式會使用網路上所有可用的通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="c681d-113">Most server programs use all protocol sequences available on the network.</span></span> <span data-ttu-id="c681d-114">若要這樣做，他們會叫用 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) 函式，如下列程式碼片段所示：</span><span class="sxs-lookup"><span data-stu-id="c681d-114">To do this, they invoke the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function, as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



<span data-ttu-id="c681d-115">[**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)函數的第一個參數是通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="c681d-115">The first parameter to the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function is the protocol sequence.</span></span> <span data-ttu-id="c681d-116">第二個參數相依于通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="c681d-116">The second parameter is dependent on the protocol sequence.</span></span> <span data-ttu-id="c681d-117">如程式碼片段所示，大部分的伺服器程式都會將此參數設定為 **RPC \_ C \_ PROTSEQ \_ MAX \_ 先決條件 \_ DEFAULT**。</span><span class="sxs-lookup"><span data-stu-id="c681d-117">As illustrated in the code fragment, most server programs set this parameter to **RPC\_C\_PROTSEQ\_MAX\_REQS\_DEFAULT**.</span></span> <span data-ttu-id="c681d-118">此值會將 RPC 程式庫設定為使用預設值。</span><span class="sxs-lookup"><span data-stu-id="c681d-118">This value sets the RPC library to use the default value.</span></span> <span data-ttu-id="c681d-119">第三個參數是安全描述項，不應在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="c681d-119">The third parameter is a security descriptor and should not be used in applications.</span></span> <span data-ttu-id="c681d-120">如需詳細資訊，請參閱 [**安全性**](security.md)。</span><span class="sxs-lookup"><span data-stu-id="c681d-120">For more information, see [**Security**](security.md).</span></span>

<span data-ttu-id="c681d-121">您也可以使用 [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)、 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)、 [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)或 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) 函數。</span><span class="sxs-lookup"><span data-stu-id="c681d-121">You can also use the [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep), or [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) functions.</span></span>

<span data-ttu-id="c681d-122">當伺服器應用程式至少選取一個通訊協定序列之後，使用動態端點的伺服器必須為它所使用的每個通訊協定順序建立系結資訊。</span><span class="sxs-lookup"><span data-stu-id="c681d-122">After a server application selects at least one protocol sequence, servers that use dynamic endpoints must create binding information for each protocol sequence it uses.</span></span> <span data-ttu-id="c681d-123">伺服器會在系結向量中儲存系結資訊，然後將其匯出至端點對應程式服務。</span><span class="sxs-lookup"><span data-stu-id="c681d-123">The server stores the binding information in a binding vector that it can then export to the endpoint mapper service.</span></span>

<span data-ttu-id="c681d-124">您可以使用 [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) 函數取得伺服器應用程式的系結向量，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="c681d-124">Use the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function to obtain a binding vector for the server application, as shown in the following example:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



<span data-ttu-id="c681d-125">傳遞至 [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) 函式的唯一參數是指向 RPC 系結 [**\_ \_ 向量**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) 結構指標的指標。</span><span class="sxs-lookup"><span data-stu-id="c681d-125">The only parameter passed to the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function is a pointer to a pointer to an [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) structure.</span></span> <span data-ttu-id="c681d-126">RPC 執行時間程式庫會動態配置系結向量的陣列，並將陣列的位址儲存在參數變數 (在此案例中為 **rpcBindingVector**) 。</span><span class="sxs-lookup"><span data-stu-id="c681d-126">The RPC run-time library dynamically allocates an array of binding vectors and stores the address of the array in the parameter variable (in this case, **rpcBindingVector**).</span></span> <span data-ttu-id="c681d-127">每個伺服器應用程式在使用 RpcBindingVectorFree 函式完成使用之後，會負責使用[](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)函式釋放這個系結向量 (例如，將它傳遞給適當的函式) 。</span><span class="sxs-lookup"><span data-stu-id="c681d-127">Each server application is responsible for freeing this binding vector using the [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) function once it has finished using it (for example, after it has passed it to the appropriate functions).</span></span>

 

 




