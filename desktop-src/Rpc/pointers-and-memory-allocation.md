---
title: 指標和記憶體配置
description: 透過指標來變更記憶體的能力通常需要伺服器和用戶端為數組中的元素配置足夠的記憶體。
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdd4c51207de093dfe2d32ec0c275aa7a05a317
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093080"
---
# <a name="pointers-and-memory-allocation"></a><span data-ttu-id="72b52-103">指標和記憶體配置</span><span class="sxs-lookup"><span data-stu-id="72b52-103">Pointers and Memory Allocation</span></span>

<span data-ttu-id="72b52-104">透過指標來變更記憶體的能力通常需要伺服器和用戶端為數組中的元素配置足夠的記憶體。</span><span class="sxs-lookup"><span data-stu-id="72b52-104">The ability to change memory through pointers often requires that the server and the client allocate enough memory for the elements in the array.</span></span>

<span data-ttu-id="72b52-105">當存根必須配置或釋放記憶體時，它會呼叫執行時間程式庫函式，進而呼叫 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Midl/midl-user-allocate-1) 和 [**midl \_ 使用者 \_ 免費**](/windows/desktop/Midl/midl-user-free-1)的函式。</span><span class="sxs-lookup"><span data-stu-id="72b52-105">When a stub must allocate or free memory, it calls run-time library functions that in turn call the functions [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1).</span></span> <span data-ttu-id="72b52-106">這些函數未包含在執行時間程式庫中。</span><span class="sxs-lookup"><span data-stu-id="72b52-106">These functions are not included as part of the run-time library.</span></span> <span data-ttu-id="72b52-107">您必須撰寫這些函式的版本，並將它們與您的應用程式連結。</span><span class="sxs-lookup"><span data-stu-id="72b52-107">You need to write your own versions of these functions and link them with your application.</span></span> <span data-ttu-id="72b52-108">如此一來，您就可以決定如何管理記憶體。</span><span class="sxs-lookup"><span data-stu-id="72b52-108">In this way, you can decide how to manage memory.</span></span> <span data-ttu-id="72b52-109">在憑證相容性 (**/osf**) 模式中編譯 IDL 檔案時，您不需要執行這些函數。</span><span class="sxs-lookup"><span data-stu-id="72b52-109">When compiling your IDL file in OSF-compatibility (**/osf**) mode, you do not need to implement these functions.</span></span> <span data-ttu-id="72b52-110">您必須將這些函式寫入下列原型：</span><span class="sxs-lookup"><span data-stu-id="72b52-110">You must write these functions to the following prototypes:</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

<span data-ttu-id="72b52-111">例如，應用程式的這些函式版本可以直接呼叫標準程式庫函式：</span><span class="sxs-lookup"><span data-stu-id="72b52-111">For example, the versions of these functions for an application can simply call standard library functions:</span></span>


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 