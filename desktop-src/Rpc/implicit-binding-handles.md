---
title: 隱含系結控制碼
description: 隱含系結控制碼可讓您的應用程式選取特定的伺服器，以執行其遠端程序呼叫。
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fda8501224d66518ad2e86f13fb769c4b2fa0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023586"
---
# <a name="implicit-binding-handles"></a><span data-ttu-id="b9cb6-103">隱含系結控制碼</span><span class="sxs-lookup"><span data-stu-id="b9cb6-103">Implicit Binding Handles</span></span>

<span data-ttu-id="b9cb6-104">隱含系結控制碼可讓您的應用程式選取特定的伺服器，以執行其遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-104">Implicit binding handles allow your application to select a specific server to execute its remote procedure calls.</span></span> <span data-ttu-id="b9cb6-105">如需詳細資訊，請參閱 [客戶](client-side-binding.md)端系結。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-105">For details, see [Client-Side Binding](client-side-binding.md).</span></span> <span data-ttu-id="b9cb6-106">它們也可讓您的用戶端/伺服器程式使用已驗證的系結。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-106">They also enable your client/server program to use authenticated bindings.</span></span> <span data-ttu-id="b9cb6-107">也就是說，用戶端可以在隱含系結控制碼中指定驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-107">That is, the client can specify authentication information in an implicit binding handle.</span></span> <span data-ttu-id="b9cb6-108">RPC 執行時間程式庫會使用驗證資訊，在用戶端與伺服器之間建立經過驗證的 RPC 會話。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-108">The RPC run-time library uses the authentication information to establish an authenticated RPC session between the client and the server.</span></span> <span data-ttu-id="b9cb6-109">如需詳細資訊，請參閱[安全性](security.md)。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-109">For more information, see [Security](security.md).</span></span>

> [!Note]  
> <span data-ttu-id="b9cb6-110">隱含系結控制碼不是安全線程。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-110">Implicit binding handles are not thread safe.</span></span> <span data-ttu-id="b9cb6-111">因此，多執行緒應用程式應該避免使用隱含的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-111">Multi-threaded applications therefore should avoid using implicit binding handles.</span></span>

 

<span data-ttu-id="b9cb6-112">當您的應用程式使用隱含系結時，用戶端必須設定系結資訊，讓它可以建立系結。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-112">When your application uses implicit bindings, the client must set the binding information so that it can create the binding.</span></span> <span data-ttu-id="b9cb6-113">用戶端建立隱含系結之後，不需要將任何系結控制碼傳遞至遠端程式。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-113">After the client creates an implicit binding, it does not need to pass any binding handles to remote procedures.</span></span> <span data-ttu-id="b9cb6-114">RPC 程式庫會處理通訊會話的其他機制。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-114">The RPC library handles the rest of the mechanics of the communication session.</span></span>

<span data-ttu-id="b9cb6-115">用戶端會將隱含控制碼的系結資訊儲存在全域變數中。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-115">The client stores the binding information for an implicit handle in a global variable.</span></span> <span data-ttu-id="b9cb6-116">當 MIDL 編譯器從 MIDL 檔案中的介面規格產生用戶端 stub 和標頭檔時，它也會產生全域系結控制碼變數的程式碼。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-116">When the MIDL compiler generates the client stub and header file from the interface specification in your MIDL file, it also generates code for a global binding handle variable.</span></span> <span data-ttu-id="b9cb6-117">您的用戶端程式會初始化控制碼，然後不會再次參考它，直到它終結系結為止。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-117">Your client program initializes the handle and then does not refer to it again until it destroys the binding.</span></span>

<span data-ttu-id="b9cb6-118">您可以 \[ 在介面的 ACF 中指定 [**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle)屬性，藉以建立隱含的控制碼，如下所示 \] ：</span><span class="sxs-lookup"><span data-stu-id="b9cb6-118">You create an implicit handle by specifying the \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] attribute in the ACF for an interface as follows:</span></span>

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

<span data-ttu-id="b9cb6-119">在上述範例中使用的 **控制碼 \_ t 型別** 是用來定義系結控制碼的 MIDL 資料型別。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-119">The **handle\_t** type, which is used in the preceding example, is a MIDL data type used for defining binding handles.</span></span>

<span data-ttu-id="b9cb6-120">建立隱含控制碼之後，應用程式必須使用它做為 RPC 執行時間程式庫函式的參數。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-120">After creating the implicit handle, the application needs to use it as a parameter to the RPC run-time library functions.</span></span> <span data-ttu-id="b9cb6-121">請勿使用隱含控制碼做為遠端程序呼叫的參數。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-121">Do not use the implicit handle as a parameter to remote procedure calls.</span></span> <span data-ttu-id="b9cb6-122">下列程式碼範例將示範隱含系結控制碼的使用。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-122">The following code sample demonstrates the use of implicit binding handles.</span></span>

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

<span data-ttu-id="b9cb6-123">在上述範例中，RPC 執行時間程式庫函式 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 和 [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) 都需要在其參數清單中傳遞隱含系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-123">In the preceding example, the RPC run-time library functions [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) and [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) both required the implicit binding handle to be passed in their parameter lists.</span></span> <span data-ttu-id="b9cb6-124">不過，遠端過程 MyRemoteProcedure 並不是 RPC 執行時間程式庫函式，因此不會發生。</span><span class="sxs-lookup"><span data-stu-id="b9cb6-124">However, the remote procedure MyRemoteProcedure did not, since it is not an RPC run-time library function.</span></span>

 

 