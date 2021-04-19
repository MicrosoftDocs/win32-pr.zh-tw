---
description: LlMulDiv 函式會將公式 ( (a \* b) + rnd) /c，其中每個詞彙都是64位值。
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: 'llMulDiv 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e45d22eec1536517bd2b57d875dd596e4a1e28db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993320"
---
# <a name="llmuldiv-function"></a><span data-ttu-id="7a105-103">llMulDiv 函式</span><span class="sxs-lookup"><span data-stu-id="7a105-103">llMulDiv function</span></span>

<span data-ttu-id="7a105-104">`llMulDiv`函數會執行公式， `((a*b)+rnd)/c` 其中每個詞彙都是64位值。</span><span class="sxs-lookup"><span data-stu-id="7a105-104">The `llMulDiv` function implements the formula `((a*b)+rnd)/c` where each term is a 64-bit value.</span></span>

<span data-ttu-id="7a105-105">時間戳記和搜尋時間是64位的值，因此這個函式適用于在32位系統上執行轉換。</span><span class="sxs-lookup"><span data-stu-id="7a105-105">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="7a105-106">例如，每秒位元組數的公式為</span><span class="sxs-lookup"><span data-stu-id="7a105-106">For example, the formula for bytes-per-second is</span></span>


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



<span data-ttu-id="7a105-107">可以計算為 `llMulDiv(nBytes, rtTime, 10000000, 0)` 。</span><span class="sxs-lookup"><span data-stu-id="7a105-107">which can be calculated as `llMulDiv(nBytes, rtTime, 10000000, 0)`.</span></span> <span data-ttu-id="7a105-108">使用 *rnd* 參數作為舍入係數。</span><span class="sxs-lookup"><span data-stu-id="7a105-108">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a105-109">語法</span><span class="sxs-lookup"><span data-stu-id="7a105-109">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a><span data-ttu-id="7a105-110">參數</span><span class="sxs-lookup"><span data-stu-id="7a105-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a105-111">*的*</span><span class="sxs-lookup"><span data-stu-id="7a105-111">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="7a105-112">被乘數.</span><span class="sxs-lookup"><span data-stu-id="7a105-112">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="7a105-113">*b*</span><span class="sxs-lookup"><span data-stu-id="7a105-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="7a105-114">乘數。</span><span class="sxs-lookup"><span data-stu-id="7a105-114">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="7a105-115">*c*</span><span class="sxs-lookup"><span data-stu-id="7a105-115">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="7a105-116">因數。</span><span class="sxs-lookup"><span data-stu-id="7a105-116">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="7a105-117">*rnd*</span><span class="sxs-lookup"><span data-stu-id="7a105-117">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="7a105-118">進位係數。</span><span class="sxs-lookup"><span data-stu-id="7a105-118">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a105-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a105-119">Return value</span></span>

<span data-ttu-id="7a105-120">傳回 `(a * b + rnd)/c` 計算或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7a105-120">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="7a105-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7a105-121">Return code</span></span>                                                                                       | <span data-ttu-id="7a105-122">Description</span><span class="sxs-lookup"><span data-stu-id="7a105-122">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a105-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="7a105-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="7a105-124">發生溢位，因為結果太大 (正) 。</span><span class="sxs-lookup"><span data-stu-id="7a105-124">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="7a105-125"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="7a105-125"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="7a105-126">發生溢位，因為結果太大 (負) 。</span><span class="sxs-lookup"><span data-stu-id="7a105-126">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a105-127">備註</span><span class="sxs-lookup"><span data-stu-id="7a105-127">Remarks</span></span>

<span data-ttu-id="7a105-128">分割區的舍入方向為零。</span><span class="sxs-lookup"><span data-stu-id="7a105-128">Rounding on the division is toward zero.</span></span> <span data-ttu-id="7a105-129">零除會視為溢位條件。</span><span class="sxs-lookup"><span data-stu-id="7a105-129">Division by zero is counted as an overflow condition.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a105-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a105-130">Requirements</span></span>



| <span data-ttu-id="7a105-131">需求</span><span class="sxs-lookup"><span data-stu-id="7a105-131">Requirement</span></span> | <span data-ttu-id="7a105-132">值</span><span class="sxs-lookup"><span data-stu-id="7a105-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a105-133">標頭</span><span class="sxs-lookup"><span data-stu-id="7a105-133">Header</span></span><br/>  | <dl> <span data-ttu-id="7a105-134"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7a105-134"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7a105-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="7a105-135">Library</span></span><br/> | <dl> <span data-ttu-id="7a105-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7a105-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a105-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a105-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a105-138">其他 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="7a105-138">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="7a105-139">**Int64x32Div32**</span><span class="sxs-lookup"><span data-stu-id="7a105-139">**Int64x32Div32**</span></span>](int64x32div32.md)
</dt> </dl>

 

 




