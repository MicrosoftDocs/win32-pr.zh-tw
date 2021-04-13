---
title: " (RPC) 的字串"
description: " (RPC) 的三種字串類型和遠端程序呼叫。"
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316060"
---
# <a name="strings-rpc"></a><span data-ttu-id="c25c1-103"> (RPC) 的字串</span><span class="sxs-lookup"><span data-stu-id="c25c1-103">Strings (RPC)</span></span>

<span data-ttu-id="c25c1-104">有三個字串類型以格式字元中的下列結束子字串表示。</span><span class="sxs-lookup"><span data-stu-id="c25c1-104">There are three strings types denoted by the following ending sub-strings in the format character.</span></span>



| <span data-ttu-id="c25c1-105">類型</span><span class="sxs-lookup"><span data-stu-id="c25c1-105">Type</span></span>                  | <span data-ttu-id="c25c1-106">Substring</span><span class="sxs-lookup"><span data-stu-id="c25c1-106">Substring</span></span> |
|-----------------------|-----------|
| <span data-ttu-id="c25c1-107">字元字串</span><span class="sxs-lookup"><span data-stu-id="c25c1-107">Character string</span></span>      | <span data-ttu-id="c25c1-108">CSTRING</span><span class="sxs-lookup"><span data-stu-id="c25c1-108">CSTRING</span></span>   |
| <span data-ttu-id="c25c1-109">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="c25c1-109">Wide character string</span></span> | <span data-ttu-id="c25c1-110">WSTRING</span><span class="sxs-lookup"><span data-stu-id="c25c1-110">WSTRING</span></span>   |
| <span data-ttu-id="c25c1-111">可字串結構</span><span class="sxs-lookup"><span data-stu-id="c25c1-111">String-able structure</span></span> | <span data-ttu-id="c25c1-112">SSTRING</span><span class="sxs-lookup"><span data-stu-id="c25c1-112">SSTRING</span></span>   |



 

### <a name="nonconformant-strings"></a><span data-ttu-id="c25c1-113">Nonconformant 字串</span><span class="sxs-lookup"><span data-stu-id="c25c1-113">Nonconformant Strings</span></span>

<span data-ttu-id="c25c1-114">Nonconformant 字串的範例是固定大小陣列上的 **\[ 字串 \]** 。</span><span class="sxs-lookup"><span data-stu-id="c25c1-114">An example of nonconformant string is a **\[string\]** on a fixed-size array.</span></span>

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a><span data-ttu-id="c25c1-115">符合標準的字串</span><span class="sxs-lookup"><span data-stu-id="c25c1-115">Conformant Strings</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

<span data-ttu-id="c25c1-116">–或–</span><span class="sxs-lookup"><span data-stu-id="c25c1-116">–or–</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

<span data-ttu-id="c25c1-117">第一個格式描述一般字串，例如 **\[ 字串 \]** char \* 引數。</span><span class="sxs-lookup"><span data-stu-id="c25c1-117">The first format describes common strings, like a **\[string\]** char \* argument.</span></span> <span data-ttu-id="c25c1-118">大小一致的字串具有後者的描述。</span><span class="sxs-lookup"><span data-stu-id="c25c1-118">A sized conformant string has the latter description.</span></span>

<span data-ttu-id="c25c1-119">一致性 \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。</span><span class="sxs-lookup"><span data-stu-id="c25c1-119">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

### <a name="structure-strings"></a><span data-ttu-id="c25c1-120">結構字串</span><span class="sxs-lookup"><span data-stu-id="c25c1-120">Structure Strings</span></span>

<span data-ttu-id="c25c1-121">以下是可 nonconformant 字串的結構：</span><span class="sxs-lookup"><span data-stu-id="c25c1-121">The following is a nonconformant string-able structure:</span></span>

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

<span data-ttu-id="c25c1-122">符合字串能力的結構：</span><span class="sxs-lookup"><span data-stu-id="c25c1-122">Conformant string-able structure:</span></span>

``` syntax
FC_C_SSTRING 
element_size<1>
```

<span data-ttu-id="c25c1-123">等於</span><span class="sxs-lookup"><span data-stu-id="c25c1-123">–or –</span></span>

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

<span data-ttu-id="c25c1-124">第二個描述適用于大小可進行字串的結構。</span><span class="sxs-lookup"><span data-stu-id="c25c1-124">The latter description is for a sized string-able structure.</span></span>

 

 