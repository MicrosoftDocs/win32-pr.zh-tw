---
title: Midl_user_free 函式
description: Midl \_ 使用者 \_ free 函數必須由 RPC 開發人員提供。
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713ed05173b709780b6496f233051fa3adddff8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382685"
---
# <a name="the-midl_user_free-function"></a><span data-ttu-id="c83cb-103">Midl \_ 使用者 \_ free 函數</span><span class="sxs-lookup"><span data-stu-id="c83cb-103">The midl\_user\_free Function</span></span>

<span data-ttu-id="c83cb-104">**Midl \_ 使用者 \_ free** 函數必須由 RPC 開發人員提供。</span><span class="sxs-lookup"><span data-stu-id="c83cb-104">The **midl\_user\_free** function must be supplied by RPC developers.</span></span> <span data-ttu-id="c83cb-105">它會配置 RPC 存根和程式庫常式的記憶體。</span><span class="sxs-lookup"><span data-stu-id="c83cb-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="c83cb-106">**Midl \_ 使用者 \_ free** 函數必須符合下列原型：</span><span class="sxs-lookup"><span data-stu-id="c83cb-106">Your **midl\_user\_free** function must match the following prototype:</span></span>

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

<span data-ttu-id="c83cb-107">*PBuffer* 參數會指定要釋放之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="c83cb-107">The *pBuffer* parameter specifies a pointer to the memory that is to be freed.</span></span> <span data-ttu-id="c83cb-108">用戶端應用程式和伺服器應用程式都必須執行 **midl \_ 使用者 \_ 自由** 函式，除非您在憑證相容性 ([**/osf**](/windows/desktop/Midl/-osf)) 模式中進行編譯。</span><span class="sxs-lookup"><span data-stu-id="c83cb-108">Both client application and server application must implement the **midl\_user\_free** function unless you are compiling in OSF-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="c83cb-109">**Midl \_ 使用者 \_ free** 函數必須能夠釋出 [**midl \_ 使用者配置所 \_ 配置**](the-midl-user-allocate-function.md)的所有儲存體。</span><span class="sxs-lookup"><span data-stu-id="c83cb-109">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](the-midl-user-allocate-function.md).</span></span>

<span data-ttu-id="c83cb-110">處理已配置的物件時，應用程式和存根會呼叫 **midl \_ 使用者 \_ free** ：</span><span class="sxs-lookup"><span data-stu-id="c83cb-110">Applications and stubs call **midl\_user\_free** when dealing with allocated objects:</span></span>

-   <span data-ttu-id="c83cb-111">伺服器應用程式應該呼叫 **midl \_ 使用者 \_ free** 以釋出應用程式所配置的記憶體，例如刪除動態配置的資料節點時。</span><span class="sxs-lookup"><span data-stu-id="c83cb-111">The server application should call **midl\_user\_free** to free memory allocated by the application, such as when deleting a dynamically allocated node of data.</span></span>
-   <span data-ttu-id="c83cb-112">伺服器 stub 會在封送處理所有 out **\_ \_** \[ \] 引數、 \[ in \] 、 \[ out \] 引數和函式傳回值之後，呼叫 midl 使用者 free 釋放伺服器上的記憶體。</span><span class="sxs-lookup"><span data-stu-id="c83cb-112">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all \[out\] arguments, \[in\],\[out\] arguments, and the function return value.</span></span>

<span data-ttu-id="c83cb-113">例如，顯示 "Hello，world" 的 RPC Windows 範例程式會在 C 函式免費的情況下實行 **midl \_ 使用者 \_** ：</span><span class="sxs-lookup"><span data-stu-id="c83cb-113">For example, the RPC Windows sample program that displays "Hello, world" implements **midl\_user\_free** in terms of the C function free:</span></span>


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> <span data-ttu-id="c83cb-114">如果啟用了 RpcSs 封裝 (例如，因為使用 [ \[ [**啟用 \_ 配置**](/windows/desktop/Midl/enable-allocate)] \] 屬性) 的結果，您的伺服器程式應該使用 [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree)來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="c83cb-114">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), your server program should use [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) to free memory.</span></span> <span data-ttu-id="c83cb-115">如需詳細資訊，請參閱「 [RpcSs 記憶體管理套件](rpcss-memory-management-package.md)」。</span><span class="sxs-lookup"><span data-stu-id="c83cb-115">For more information, see [RpcSs Memory Management Package](rpcss-memory-management-package.md).</span></span>

 

 

 