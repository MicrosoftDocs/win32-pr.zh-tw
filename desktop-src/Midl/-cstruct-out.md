---
title: /cstruct_out 參數
description: /Cstruct_out 參數會修改 COM 介面的 C 定義，此介面會傳回結構，以符合 c + + 實施者所提供的 ABI。
keywords:
- /cstruct_out switch MIDL
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844507"
---
# <a name="cstruct_out-switch"></a><span data-ttu-id="64bc3-104">/cstruct \_ out 參數</span><span class="sxs-lookup"><span data-stu-id="64bc3-104">/cstruct\_out switch</span></span>

<span data-ttu-id="64bc3-105">此參數會修改 COM 介面的 C 定義，這個介面會傳回結構以符合 c + + 實施者所提供的 ABI。</span><span class="sxs-lookup"><span data-stu-id="64bc3-105">This switch modifies the C definition of a COM interface which returns structures to match the ABI a C++ implementer would provide.</span></span>

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a><span data-ttu-id="64bc3-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="64bc3-106">Switch Options</span></span>

<span data-ttu-id="64bc3-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="64bc3-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="64bc3-108">備註</span><span class="sxs-lookup"><span data-stu-id="64bc3-108">Remarks</span></span>

<span data-ttu-id="64bc3-109">某些介面定義 (特別 `d3d12.idl` 是) 包含傳回 `__stdcall` 結構的方法。</span><span class="sxs-lookup"><span data-stu-id="64bc3-109">Some interface definitions (notably those in `d3d12.idl`) contain `__stdcall` methods that return structures.</span></span> <span data-ttu-id="64bc3-110">MSVC 中的 C 和 c + + Abi 會因其實作為這類函式的方式而有所不同：</span><span class="sxs-lookup"><span data-stu-id="64bc3-110">The C and C++ ABIs from MSVC differ in how they implement such functions:</span></span>

* <span data-ttu-id="64bc3-111">C 會將它們視為一般函式，將隱藏 `this` 指標作為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="64bc3-111">C treats them as plain functions that take a hidden `this` pointer as the first parameter.</span></span> <span data-ttu-id="64bc3-112">編譯器會套用小型結構優化，以允許小於8個位元組的結構 (或更大的值（如果所有值都是在暫存器中傳回的浮點數) ）。</span><span class="sxs-lookup"><span data-stu-id="64bc3-112">The complier applies a small struct optimization that allows structs smaller than 8 bytes (or larger if all values are floating point) to be returned in registers.</span></span> <span data-ttu-id="64bc3-113">只有較大的結構會升級為使用隱藏的參數和呼叫端配置的傳回值。</span><span class="sxs-lookup"><span data-stu-id="64bc3-113">Only larger structures are promoted to use a hidden parameter and caller-allocated return value.</span></span>
* <span data-ttu-id="64bc3-114">C + + 會將它們視為成員函式。</span><span class="sxs-lookup"><span data-stu-id="64bc3-114">C++ treats them as member functions.</span></span> <span data-ttu-id="64bc3-115">編譯器 *一律* 會藉由將隱藏的參數插入 (呼叫端配置的傳回值指標，) 做為指標之後的第二個參數 `this` 。</span><span class="sxs-lookup"><span data-stu-id="64bc3-115">The compiler *always* does so by inserting a hidden parameter (a pointer to a caller-allocated return value) as the second parameter, after the `this` pointer.</span></span> <span data-ttu-id="64bc3-116">它也會傳回相同的指標做為其傳回值。</span><span class="sxs-lookup"><span data-stu-id="64bc3-116">It also returns that same pointer as its return value.</span></span>

<span data-ttu-id="64bc3-117">此參數會強制產生的標頭中介面的 C 定義，假設實作者使用 c + +，而 C 程式碼則應該改為明確地使用 c + + ABI。</span><span class="sxs-lookup"><span data-stu-id="64bc3-117">This switch forces the C definition of interfaces in the resulting header to assume that the implementer was using C++, and that the C code should instead explicitly use the C++ ABI.</span></span> <span data-ttu-id="64bc3-118">這表示函式包含傳回值指標的隱藏參數，並會直接傳回該指標，而不是直接傳回結構。</span><span class="sxs-lookup"><span data-stu-id="64bc3-118">This implies that the function includes a hidden parameter for the return value pointer and returns that pointer instead of the structure directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="64bc3-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64bc3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64bc3-120">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="64bc3-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>
