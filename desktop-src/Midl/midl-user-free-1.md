---
title: midl_user_free 屬性
description: Midl \_ 使用者 free 函式 \_ 是由用戶端和伺服器應用程式提供，以解除配置動態配置的記憶體。
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free 屬性 MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314902"
---
# <a name="midl_user_free-attribute"></a><span data-ttu-id="f9aab-104">midl \_ 使用者 \_ 可用屬性</span><span class="sxs-lookup"><span data-stu-id="f9aab-104">midl\_user\_free attribute</span></span>

<span data-ttu-id="f9aab-105">**Midl \_ 使用者 \_ free** 函式是由用戶端和伺服器應用程式提供，以解除配置動態配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f9aab-105">The **midl\_user\_free** function is provided by client and server applications to deallocate dynamically allocated memory.</span></span>

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a><span data-ttu-id="f9aab-106">參數</span><span class="sxs-lookup"><span data-stu-id="f9aab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9aab-107">*P*</span><span class="sxs-lookup"><span data-stu-id="f9aab-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="f9aab-108">要釋放之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="f9aab-108">A pointer to the memory block to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9aab-109">備註</span><span class="sxs-lookup"><span data-stu-id="f9aab-109">Remarks</span></span>

<span data-ttu-id="f9aab-110">用戶端應用程式和伺服器應用程式都必須執行 **midl \_ 使用者 \_ free** 函式，除非您在憑證相容性 ([**/osf**](-osf.md)) 模式中進行編譯。</span><span class="sxs-lookup"><span data-stu-id="f9aab-110">Both client application and server application must implement the **midl\_user\_free** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="f9aab-111">**Midl \_ 使用者 \_ free** 函數必須能夠釋出 [**midl \_ 使用者配置所 \_ 配置**](/windows/desktop/Rpc/the-midl-user-allocate-function)的所有儲存體。</span><span class="sxs-lookup"><span data-stu-id="f9aab-111">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span>

<span data-ttu-id="f9aab-112">處理指標所參考的物件時，應用程式和存根會呼叫 **midl \_ 使用者 \_ free** ：</span><span class="sxs-lookup"><span data-stu-id="f9aab-112">Applications and stubs call **midl\_user\_free** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="f9aab-113">伺服器應用程式應該呼叫 **midl \_ 使用者 \_ free** 來釋出 applicationâ所配置的記憶體，例如，刪除指定的節點時。</span><span class="sxs-lookup"><span data-stu-id="f9aab-113">The server application should call **midl\_user\_free** to free memory allocated by the applicationâ€”for example, when deleting a specified node.</span></span>
-   <span data-ttu-id="f9aab-114">伺服器 stub 會在封送處理所有 **\_ \_** **\[** [**out**](out-idl.md) **\]** 引數、 **\[** [**in**](in.md)、 **out \]** 引數和傳回值之後，呼叫 midl 使用者 free 釋放伺服器上的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f9aab-114">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all **\[**[**out**](out-idl.md)**\]** arguments, **\[**[**in**](in.md), **out\]** arguments, and the return value.</span></span>

## <a name="examples"></a><span data-ttu-id="f9aab-115">範例</span><span class="sxs-lookup"><span data-stu-id="f9aab-115">Examples</span></span>


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a><span data-ttu-id="f9aab-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9aab-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9aab-117">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="f9aab-117">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="f9aab-118">陣列和指標</span><span class="sxs-lookup"><span data-stu-id="f9aab-118">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="f9aab-119">陣列和 Sized-Pointer 屬性</span><span class="sxs-lookup"><span data-stu-id="f9aab-119">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="f9aab-120">**在**</span><span class="sxs-lookup"><span data-stu-id="f9aab-120">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="f9aab-121">**midl \_ 使用者 \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="f9aab-121">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="f9aab-122">**/osf**</span><span class="sxs-lookup"><span data-stu-id="f9aab-122">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="f9aab-123">**擴展**</span><span class="sxs-lookup"><span data-stu-id="f9aab-123">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="f9aab-124">**獨特**</span><span class="sxs-lookup"><span data-stu-id="f9aab-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 