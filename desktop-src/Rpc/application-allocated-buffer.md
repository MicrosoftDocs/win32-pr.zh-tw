---
title: Application-Allocated 緩衝區
description: ACF 屬性 \ 位元組 \_ 計數 \ 會將存根導向至用戶端支援常式未配置或釋放的預先配置緩衝區。
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463544"
---
# <a name="application-allocated-buffer"></a><span data-ttu-id="17069-103">Application-Allocated 緩衝區</span><span class="sxs-lookup"><span data-stu-id="17069-103">Application-Allocated Buffer</span></span>

<span data-ttu-id="17069-104">ACF 屬性 \[ [**位元組 \_ 計數**](/windows/desktop/Midl/byte-count) \] 會將存根導向至用戶端支援常式未配置或釋放的預先配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="17069-104">The ACF attribute \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] directs the stubs to use a preallocated buffer that is not allocated or freed by the client support routines.</span></span> <span data-ttu-id="17069-105">\[ **Byte \_ count** \] 屬性會套用至指向緩衝區的指標或陣列參數。</span><span class="sxs-lookup"><span data-stu-id="17069-105">The \[**byte\_count**\] attribute is applied to a pointer or array parameter that points to the buffer.</span></span> <span data-ttu-id="17069-106">它需要指定緩衝區大小的參數（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="17069-106">It requires a parameter that specifies the buffer size in bytes.</span></span>

<span data-ttu-id="17069-107">用戶端配置的記憶體區域可以包含具有多個指標的複雜資料結構。</span><span class="sxs-lookup"><span data-stu-id="17069-107">The client-allocated memory area can contain complex data structures with multiple pointers.</span></span> <span data-ttu-id="17069-108">因為記憶體區域是連續的，所以應用程式不需要進行數個呼叫來個別釋放每個指標和結構。</span><span class="sxs-lookup"><span data-stu-id="17069-108">Because the memory area is contiguous, the application does not have to make several calls to free each pointer and structure individually.</span></span> <span data-ttu-id="17069-109">當使用 [ \[ [**配置 (所有 \_ 節點)**](/windows/desktop/Midl/allocate) ] \] 屬性時，只要呼叫記憶體配置常式或免費的常式，就可以配置或釋放記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="17069-109">As when using the \[[**allocate(all\_nodes)**](/windows/desktop/Midl/allocate)\] attribute, the memory area can be allocated or freed with one call to the memory-allocation routine or the free routine.</span></span> <span data-ttu-id="17069-110">不過，與使用 [ \[ **配置 (所有 \_ 節點)** \] 屬性不同的是，緩衝區參數不是由用戶端 stub 所管理，而是由用戶端應用程式所管理。</span><span class="sxs-lookup"><span data-stu-id="17069-110">However, unlike using the \[**allocate(all\_nodes)**\] attribute, the buffer parameter is not managed by the client stub but by the client application.</span></span>

<span data-ttu-id="17069-111">緩衝區必須是 \[ [**out**](/windows/desktop/Midl/out-idl) \] 參數，而緩衝區長度（以位元組為單位）必須是僅供使用的 \[ [](/windows/desktop/Midl/in) \] 參數。</span><span class="sxs-lookup"><span data-stu-id="17069-111">The buffer must be an \[[**out**](/windows/desktop/Midl/out-idl)\]-only parameter and the buffer length in bytes must be an \[[**in**](/windows/desktop/Midl/in)\]-only parameter.</span></span> <span data-ttu-id="17069-112">\[ [**Byte \_ count**](/windows/desktop/Midl/byte-count) \] 屬性只能套用至指標類型。</span><span class="sxs-lookup"><span data-stu-id="17069-112">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute can only be applied to pointer types.</span></span> <span data-ttu-id="17069-113">\[ **Byte \_ count** \] ACF 屬性是適用于 DCE IDL 的 Microsoft 擴充功能，因此，如果您使用 MIDL [**/osf**](/windows/desktop/Midl/-osf)參數進行編譯，就無法使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="17069-113">The \[**byte\_count**\] ACF attribute is a Microsoft extension to DCE IDL and, as such, is not available if you compile using the MIDL [**/osf**](/windows/desktop/Midl/-osf) switch.</span></span>

<span data-ttu-id="17069-114">在下列範例中，參數 *pRoot* 使用 byte count：</span><span class="sxs-lookup"><span data-stu-id="17069-114">In the following example, the parameter *pRoot* uses byte count:</span></span>

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

<span data-ttu-id="17069-115">[ \[ [**位元組 \_ 計數**](/windows/desktop/Midl/byte-count)] \] 屬性會顯示在 ACF 中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="17069-115">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute appears in the ACF as:</span></span>

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

<span data-ttu-id="17069-116">從這些 IDL 和 ACF 檔產生的用戶端 stub 不會配置或釋放此緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="17069-116">The client stub generated from these IDL and ACF files does not allocate or free the memory for this buffer.</span></span> <span data-ttu-id="17069-117">伺服器 stub 會使用提供的大小參數，在單一呼叫中配置和釋出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="17069-117">The server stub allocates and frees the buffer in a single call using the provided size parameter.</span></span> <span data-ttu-id="17069-118">如果資料太大而無法使用指定的緩衝區大小，則會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="17069-118">If the data is too large for the specified buffer size, an exception is raised.</span></span>

 

 