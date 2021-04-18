---
title: force_allocate 屬性
description: ACF 屬性 \ force \_ 配置 \ 強制使用 midl 使用者配置來配置指標參數， \_ \_ 而不是將配置優化。
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate 屬性 MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463008"
---
# <a name="force_allocate-attribute"></a><span data-ttu-id="fcd8d-104">強制 \_ 配置屬性</span><span class="sxs-lookup"><span data-stu-id="fcd8d-104">force\_allocate attribute</span></span>

<span data-ttu-id="fcd8d-105">ACF 屬性 \[ **強制 \_ 配置** \] 會強制使用 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md)來配置指標參數，而不是將配置優化。</span><span class="sxs-lookup"><span data-stu-id="fcd8d-105">The ACF attribute \[**force\_allocate**\] forces a pointer parameter to be allocated using [**midl\_user\_allocate**](midl-user-allocate-1.md) instead of optimizing away the allocation.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a><span data-ttu-id="fcd8d-106">參數</span><span class="sxs-lookup"><span data-stu-id="fcd8d-106">Parameters</span></span>

<span data-ttu-id="fcd8d-107">這個屬性沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fcd8d-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd8d-108">備註</span><span class="sxs-lookup"><span data-stu-id="fcd8d-108">Remarks</span></span>

<span data-ttu-id="fcd8d-109">RPC 會藉由提供內部記憶體緩衝區的指標，嘗試將伺服器上的記憶體配置降至最低。</span><span class="sxs-lookup"><span data-stu-id="fcd8d-109">RPC attempts to minimize memory allocations on the server by supplying pointers to internal memory buffers.</span></span> <span data-ttu-id="fcd8d-110">這種方法可能會導致應用程式發生問題，而這些應用程式嘗試在 RPC 提供的指標上直接呼叫 [**midl \_ 使用者 \_**](midl-user-free-1.md) ，因為已優化的指標無法釋放。</span><span class="sxs-lookup"><span data-stu-id="fcd8d-110">This approach can cause problems for applications that attempt to directly call [**midl\_user\_free**](midl-user-free-1.md) on RPC-supplied pointers, because a pointer that has been optimized cannot be freed.</span></span> <span data-ttu-id="fcd8d-111">使用 **\[ 強制 \_ 配置 \]** 來標記參數，將會使所有衍生它的指標都無法進行優化。</span><span class="sxs-lookup"><span data-stu-id="fcd8d-111">Marking a parameter with **\[force\_allocate\]** will prevent this optimization for all pointers deriving it.</span></span>

<span data-ttu-id="fcd8d-112">**\[ 強制 \_ 配置 \]** 的另一種常見用法，是在應用程式需要大於所指向記憶體的對齊情況時，保證所指向的記憶體對齊。</span><span class="sxs-lookup"><span data-stu-id="fcd8d-112">Another common use for **\[force\_allocate\]** is to guarantee the alignment of the memory being pointed to if an application requires an alignment greater than that of the memory pointed to.</span></span> <span data-ttu-id="fcd8d-113">例如，應用程式通常會以位元組的泛型陣列來傳遞資料，而不是使用實際的型別，但是位元組只保證會對齊1，這可能會對採用較大對齊的應用程式造成問題。</span><span class="sxs-lookup"><span data-stu-id="fcd8d-113">For example, applications often pass data in a generic array of bytes rather than using the actual type, but a byte is only guaranteed to be aligned at 1, which may cause problems for applications that assume a larger alignment.</span></span> <span data-ttu-id="fcd8d-114">藉由使用 **\[ 強制 \_ 配置 \]** 來標記參數，應用程式可以保證所指向的所有記憶體都具有等於 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md)所保證的對齊。</span><span class="sxs-lookup"><span data-stu-id="fcd8d-114">By marking the parameter with **\[force\_allocate\]**, the application can guarantee all memory pointed to will have an alignment equal to that guaranteed by [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fcd8d-115">範例</span><span class="sxs-lookup"><span data-stu-id="fcd8d-115">Examples</span></span>

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a><span data-ttu-id="fcd8d-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcd8d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd8d-117">避免資訊隱藏</span><span class="sxs-lookup"><span data-stu-id="fcd8d-117">Avoiding Information Hiding</span></span>](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[<span data-ttu-id="fcd8d-118">設計64位相容介面</span><span class="sxs-lookup"><span data-stu-id="fcd8d-118">Designing 64-bit-Compatible Interfaces</span></span>](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[<span data-ttu-id="fcd8d-119">**midl \_ 使用者 \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-119">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="fcd8d-120">**midl \_ 使用者 \_ 免費**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-120">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="fcd8d-121">**分配**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-121">**allocate**</span></span>](allocate.md)
</dt> </dl>

 

 