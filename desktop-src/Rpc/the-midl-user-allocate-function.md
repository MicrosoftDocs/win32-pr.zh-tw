---
title: Midl_user_allocate 函式
description: Midl \_ 使用者 \_ 配置函數是必須由 RPC 應用程式開發人員提供的程式。
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092964"
---
# <a name="the-midl_user_allocate-function"></a><span data-ttu-id="104b3-103">Midl \_ 使用者 \_ 配置函數</span><span class="sxs-lookup"><span data-stu-id="104b3-103">The midl\_user\_allocate Function</span></span>

<span data-ttu-id="104b3-104">**Midl \_ 使用者 \_ 配置** 函數是必須由 RPC 應用程式開發人員提供的程式。</span><span class="sxs-lookup"><span data-stu-id="104b3-104">The **midl\_user\_allocate** function is a procedure that must be supplied by developers of RPC applications.</span></span> <span data-ttu-id="104b3-105">它會配置 RPC 存根和程式庫常式的記憶體。</span><span class="sxs-lookup"><span data-stu-id="104b3-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="104b3-106">**Midl \_ 使用者 \_ 配置** 函數必須符合下列原型：</span><span class="sxs-lookup"><span data-stu-id="104b3-106">Your **midl\_user\_allocate** function must match the following prototype:</span></span>

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

<span data-ttu-id="104b3-107">*CBytes* 參數會指定要配置的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="104b3-107">The *cBytes* parameter specifies the number of bytes to allocate.</span></span> <span data-ttu-id="104b3-108">用戶端應用程式和伺服器應用程式都必須執行 **midl \_ 使用者 \_ 配置** 函式，除非您在憑證相容性 (/osf) 模式中進行編譯。</span><span class="sxs-lookup"><span data-stu-id="104b3-108">Both client applications and server applications must implement the **midl\_user\_allocate** function unless you are compiling in OSF-compatibility (/osf) mode.</span></span> <span data-ttu-id="104b3-109">應用程式和產生的存根呼叫 midl 使用者直接或間接配置來管理 **\_ \_ 配置** 的物件。</span><span class="sxs-lookup"><span data-stu-id="104b3-109">Applications and generated stubs call **midl\_user\_allocate** directly or indirectly to manage allocated objects.</span></span> <span data-ttu-id="104b3-110">例如：</span><span class="sxs-lookup"><span data-stu-id="104b3-110">For example:</span></span>

-   <span data-ttu-id="104b3-111">用戶端和伺服器應用程式會呼叫 **midl \_ 使用者 \_ 配置** 來配置應用程式的記憶體，例如在樹狀結構或連結清單中建立新節點時。</span><span class="sxs-lookup"><span data-stu-id="104b3-111">The client and server applications call **midl\_user\_allocate** to allocate memory for the application, such as when creating a new node in a tree or linked list.</span></span>
-   <span data-ttu-id="104b3-112">當將資料封送處理至伺服器位址空間時，伺服器 stub 會呼叫 **midl \_ 使用者 \_ 配置** 。</span><span class="sxs-lookup"><span data-stu-id="104b3-112">The server stub calls **midl\_user\_allocate** when unmarshaling data into the server address space.</span></span>
-   <span data-ttu-id="104b3-113">從 out 指標所參考的伺服器封送資料時，用戶端 stub 會呼叫 **midl \_ 使用者 \_ 配置** \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="104b3-113">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an \[out\] pointer.</span></span> <span data-ttu-id="104b3-114">請注意，對於 \[ in \] 、 \[ out \] 和 \[ unique \] 指標而言，只有在輸入上的唯一指標值為 null，且在呼叫期間變更為非 null 值時，用戶端 stub 才會呼叫 **midl \_ 使用者 \_ 配置** \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="104b3-114">Note that for \[in\], \[out\], and \[unique\] pointers, the client stub calls **midl\_user\_allocate** only if the \[unique\] pointer value was null on input and changes to a non-null value during the call.</span></span> <span data-ttu-id="104b3-115">如果 \[ \] 輸入上的 unique 指標不是 null，則用戶端 stub 會將相關聯的資料寫入現有的記憶體。</span><span class="sxs-lookup"><span data-stu-id="104b3-115">If the \[unique\] pointer was non-null on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="104b3-116">如果 **midl \_ 使用者 \_ 配置** 無法配置記憶體，則應該傳回 null 指標。</span><span class="sxs-lookup"><span data-stu-id="104b3-116">If **midl\_user\_allocate** fails to allocate memory, it should return a null pointer.</span></span>

<span data-ttu-id="104b3-117">**Midl \_ 使用者 \_ 配置** 函式應傳回8位元組對齊的指標。</span><span class="sxs-lookup"><span data-stu-id="104b3-117">The **midl\_user\_allocate** function should return an 8-byte aligned pointer.</span></span>

<span data-ttu-id="104b3-118">例如，平臺軟體發展工具組所提供的範例程式 (SDK) 根據 C 函數 [**malloc**](pointers-and-memory-allocation.md)來實行 **midl \_ 使用者 \_ 配置**：</span><span class="sxs-lookup"><span data-stu-id="104b3-118">For example, the sample programs provided with the Platform Software Development Kit (SDK) implement **midl\_user\_allocate** in terms of the C function [**malloc**](pointers-and-memory-allocation.md):</span></span>


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> <span data-ttu-id="104b3-119">如果已啟用 RpcSs 封裝 (例如，當使用 [ \[ [**啟用 \_ 配置**](/windows/desktop/Midl/enable-allocate)] 屬性) 的結果時 \] ，請使用 [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate)在伺服器端配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="104b3-119">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) to allocate memory on the server side.</span></span> <span data-ttu-id="104b3-120">如需 \[ **啟用 \_ 配置** 的詳細資訊 \] ，請參閱 [MIDL 參考](/windows/desktop/Midl/midl-language-reference)。</span><span class="sxs-lookup"><span data-stu-id="104b3-120">For additional information on \[**enable\_allocate**\], see [MIDL Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 

 