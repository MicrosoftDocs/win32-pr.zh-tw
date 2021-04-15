---
title: partial_ignore 屬性
description: ACF 屬性 \ partial \_ ignore \ 會定義特殊版本的 \ unique \ 指標，以提供選擇性的 out 語義。
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore 屬性 MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373277"
---
# <a name="partial_ignore-attribute"></a><span data-ttu-id="8f999-104">部分 \_ 忽略屬性</span><span class="sxs-lookup"><span data-stu-id="8f999-104">partial\_ignore attribute</span></span>

<span data-ttu-id="8f999-105">ACF 屬性 **\[ 部分 \_ 忽略 \]** 會定義提供選擇性 out 語義之 **\[ 唯一 \]** 指標的特殊版本。</span><span class="sxs-lookup"><span data-stu-id="8f999-105">The ACF attribute **\[partial\_ignore\]** defines a specialized version of **\[unique\]** pointers that provides optional-out semantics.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a><span data-ttu-id="8f999-106">備註</span><span class="sxs-lookup"><span data-stu-id="8f999-106">Remarks</span></span>

<span data-ttu-id="8f999-107">建立函式時，通常會允許使用者指定非 **Null** 指標給選擇性的傳回資料，通常稱為選擇性的輸出指標。</span><span class="sxs-lookup"><span data-stu-id="8f999-107">When creating a function, it is common to allow users to specify a non-**NULL** pointer to optional return data, often referred to as an optional-out pointer.</span></span> <span data-ttu-id="8f999-108">使用者所指向的記憶體通常不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="8f999-108">The memory pointed to by the user is not typically required to be initialized.</span></span> <span data-ttu-id="8f999-109">這項技術代表透過 RPC 使用函式時的問題。</span><span class="sxs-lookup"><span data-stu-id="8f999-109">This technique represents a problem when the function is used over RPC.</span></span>

<span data-ttu-id="8f999-110">如果選擇性-out 指標有效，但指向未初始化的資料，RPC 會嘗試封送處理該資料並將其傳送至伺服器，這可能會導致封送處理失敗並中止呼叫。</span><span class="sxs-lookup"><span data-stu-id="8f999-110">If the optional-out pointer is valid, but points to uninitialized data, RPC attempts to marshal that data and send it to the server, which can cause the marshaling to fail and abort the call.</span></span> <span data-ttu-id="8f999-111">即使封送處理成功，可能會有大量無用的資料傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="8f999-111">Even if the marshaling succeeds, a potentially large amount of useless data is sent to the server.</span></span>

<span data-ttu-id="8f999-112">這些問題的解決方式是將指標標示為 **\[ in、out、unique、 \_ partial \] ignore**。</span><span class="sxs-lookup"><span data-stu-id="8f999-112">These problems are solved by marking the pointer as **\[in, out, unique, partial\_ignore\]**.</span></span> <span data-ttu-id="8f999-113">所有四個屬性都必須存在。</span><span class="sxs-lookup"><span data-stu-id="8f999-113">All four attributes must be present.</span></span> <span data-ttu-id="8f999-114">當用戶端上的 **\[ 部分 \_ 忽略 \]** 指標封送處理時，傳送至伺服器的唯一資料就是顯示指標是否為 **Null** 的指示器。</span><span class="sxs-lookup"><span data-stu-id="8f999-114">When a **\[partial\_ignore\]** pointer is marshaled on the client side, the only data sent to the server is an indicator showing whether the pointer is **NULL**.</span></span> <span data-ttu-id="8f999-115">如果指標為非 **Null**，則伺服器端常式會接收以零初始化之記憶體區塊的有效指標。</span><span class="sxs-lookup"><span data-stu-id="8f999-115">If the pointer is non-**NULL**, the server-side routine receives a valid pointer to a block of memory that has been initialized with zeros.</span></span> <span data-ttu-id="8f999-116">如果指標為 **null**，則伺服器端常式會收到 **null** 指標。</span><span class="sxs-lookup"><span data-stu-id="8f999-116">If the pointer is **NULL**, the server-side routine receives a **NULL** pointer.</span></span>

<span data-ttu-id="8f999-117">在這種情況下，指標的大小上限必須在編譯時期或根據輸入參數妥善定義，因為伺服器需要配置空間給所指向的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="8f999-117">In this situation, the maximum size of the pointer must be well defined either at compile time or based on input parameters, because the server needs to allocate space for the memory location being pointed to.</span></span> <span data-ttu-id="8f999-118">例如，簡單 **\[ 字串 \]** 指標沒有定義完善的大小，因為字串是以 Null 字元隱含地結束。</span><span class="sxs-lookup"><span data-stu-id="8f999-118">For example, a simple **\[string\]** pointer does not have a well defined size because the string is implicitly terminated by a NULL character.</span></span> <span data-ttu-id="8f999-119">在此情況下，藉由新增 **\[ 大小 \_ 為 \]** 屬性來指定字串大小上限，會達到定義完善的大小需求。</span><span class="sxs-lookup"><span data-stu-id="8f999-119">In this case, specifying the maximum size of the string by adding a **\[size\_is\]** attribute would achieve the well defined size requirement.</span></span>

## <a name="examples"></a><span data-ttu-id="8f999-120">範例</span><span class="sxs-lookup"><span data-stu-id="8f999-120">Examples</span></span>

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a><span data-ttu-id="8f999-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f999-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f999-122">**獨特**</span><span class="sxs-lookup"><span data-stu-id="8f999-122">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




