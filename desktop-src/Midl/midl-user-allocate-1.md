---
title: midl_user_allocate 屬性
description: Midl \_ 使用者配置函式 \_ 是用戶端和伺服器應用程式提供來配置記憶體的函式。
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate 屬性 MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315061"
---
# <a name="midl_user_allocate-attribute"></a><span data-ttu-id="91ce2-104">midl \_ 使用者 \_ 配置屬性</span><span class="sxs-lookup"><span data-stu-id="91ce2-104">midl\_user\_allocate attribute</span></span>

<span data-ttu-id="91ce2-105">**Midl \_ 使用者 \_ 配置** 函式是用戶端和伺服器應用程式提供來配置記憶體的函式。</span><span class="sxs-lookup"><span data-stu-id="91ce2-105">The **midl\_user\_allocate** function is a function that client and server applications provide to allocate memory.</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a><span data-ttu-id="91ce2-106">參數</span><span class="sxs-lookup"><span data-stu-id="91ce2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ce2-107">*cBytes*</span><span class="sxs-lookup"><span data-stu-id="91ce2-107">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="91ce2-108">指定要配置的位元組計數。</span><span class="sxs-lookup"><span data-stu-id="91ce2-108">Specifies the count of bytes to allocate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91ce2-109">備註</span><span class="sxs-lookup"><span data-stu-id="91ce2-109">Remarks</span></span>

<span data-ttu-id="91ce2-110">用戶端應用程式和伺服器應用程式都必須執行 **midl \_ 使用者 \_ 配置** 函式，除非您在憑證相容性 ([**/osf**](-osf.md)) 模式中進行編譯。</span><span class="sxs-lookup"><span data-stu-id="91ce2-110">Both client applications and server applications must implement the **midl\_user\_allocate** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="91ce2-111">應用程式和產生的存根在處理指標所參考的物件時，會呼叫 **midl \_ 使用者 \_ 配置** ：</span><span class="sxs-lookup"><span data-stu-id="91ce2-111">Applications and generated stubs call **midl\_user\_allocate** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="91ce2-112">伺服器應用程式應該呼叫 **midl \_ 使用者 \_ 配置** 來配置 applicationâ的記憶體，例如，建立新節點時。</span><span class="sxs-lookup"><span data-stu-id="91ce2-112">The server application should call **midl\_user\_allocate** to allocate memory for the applicationâ€”for example, when creating a new node.</span></span>
-   <span data-ttu-id="91ce2-113">當將指向的資料封送處理至伺服器位址空間時，伺服器 stub 會呼叫 **midl \_ 使用者 \_ 配置** 。</span><span class="sxs-lookup"><span data-stu-id="91ce2-113">The server stub calls **midl\_user\_allocate** when unmarshaling pointed-at data into the server address space.</span></span>
-   <span data-ttu-id="91ce2-114">從 [**out**](out-idl.md)指標所參考的伺服器封送資料時，用戶端 stub 會呼叫 **midl \_ 使用者 \_ 配置**。</span><span class="sxs-lookup"><span data-stu-id="91ce2-114">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an [**out**](out-idl.md) pointer.</span></span> <span data-ttu-id="91ce2-115">請注意，對於 **\[** [**in**](in.md) **\]** 、 **\[ out \]** 和 **\[** [**unique**](unique.md) **\]** 指標而言，只有在輸入上的 **\[ 唯一 \]** 指標值為 **Null** ，且在呼叫期間變更為非 **Null** 值時，用戶端 stub 才會呼叫 **midl \_ 使用者 \_ 配置**。</span><span class="sxs-lookup"><span data-stu-id="91ce2-115">Note that for **\[**[**in**](in.md)**\]**, **\[out\]**, and **\[**[**unique**](unique.md)**\]** pointers, the client stub calls **midl\_user\_allocate** only if the **\[unique\]** pointer value was **NULL** on input and changes to a non-**NULL** value during the call.</span></span> <span data-ttu-id="91ce2-116">如果輸入上的 **\[ \] unique** 指標不是 **Null** ，則用戶端 stub 會將相關聯的資料寫入現有的記憶體。</span><span class="sxs-lookup"><span data-stu-id="91ce2-116">If the **\[unique\]** pointer was non-**NULL** on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="91ce2-117">如果 **midl \_ 使用者 \_ 配置** 無法配置記憶體，則必須傳回 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="91ce2-117">If **midl\_user\_allocate** fails to allocate memory, it must return a **NULL** pointer.</span></span>

<span data-ttu-id="91ce2-118">建議 **midl \_ 使用者 \_ 配置** 傳回8個位元組對齊的指標。</span><span class="sxs-lookup"><span data-stu-id="91ce2-118">It is recommended that **midl\_user\_allocate** return a pointer that is 8 bytes aligned.</span></span>

## <a name="examples"></a><span data-ttu-id="91ce2-119">範例</span><span class="sxs-lookup"><span data-stu-id="91ce2-119">Examples</span></span>


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a><span data-ttu-id="91ce2-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91ce2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ce2-121">**分配**</span><span class="sxs-lookup"><span data-stu-id="91ce2-121">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="91ce2-122">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="91ce2-122">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="91ce2-123">陣列和指標</span><span class="sxs-lookup"><span data-stu-id="91ce2-123">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="91ce2-124">陣列和 Sized-Pointer 屬性</span><span class="sxs-lookup"><span data-stu-id="91ce2-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="91ce2-125">**在**</span><span class="sxs-lookup"><span data-stu-id="91ce2-125">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="91ce2-126">**midl \_ 使用者 \_ 免費**</span><span class="sxs-lookup"><span data-stu-id="91ce2-126">**midl\_user\_free**</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="91ce2-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="91ce2-127">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="91ce2-128">**擴展**</span><span class="sxs-lookup"><span data-stu-id="91ce2-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="91ce2-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="91ce2-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="91ce2-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="91ce2-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="91ce2-131">**獨特**</span><span class="sxs-lookup"><span data-stu-id="91ce2-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 