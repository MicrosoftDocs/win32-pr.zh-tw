---
description: Int64x32Div32 函式會將公式 ( (a \* b) + rnd) /c，其中 a 是64位值，b、c 和 rnd 則是32位值。
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: 'Int64x32Div32 函式 (Wxutil) '
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
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993230"
---
# <a name="int64x32div32-function"></a><span data-ttu-id="4b6d3-103">Int64x32Div32 函式</span><span class="sxs-lookup"><span data-stu-id="4b6d3-103">Int64x32Div32 function</span></span>

<span data-ttu-id="4b6d3-104">`Int64x32Div32`函數會實作為 `((a*b)+rnd)/c` 64 位值的公式，而 *b*、 *c* 和 *rnd* 是32位值。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-104">The `Int64x32Div32` function implements the formula `((a*b)+rnd)/c` where *a* is a 64-bit value and *b*, *c*, and *rnd* are 32-bit values.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b6d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="4b6d3-105">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
);
```



## <a name="parameters"></a><span data-ttu-id="4b6d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="4b6d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b6d3-107">*的*</span><span class="sxs-lookup"><span data-stu-id="4b6d3-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="4b6d3-108">被乘數.</span><span class="sxs-lookup"><span data-stu-id="4b6d3-108">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="4b6d3-109">*b*</span><span class="sxs-lookup"><span data-stu-id="4b6d3-109">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="4b6d3-110">乘數。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-110">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="4b6d3-111">*c*</span><span class="sxs-lookup"><span data-stu-id="4b6d3-111">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="4b6d3-112">因數。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="4b6d3-113">*rnd*</span><span class="sxs-lookup"><span data-stu-id="4b6d3-113">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4b6d3-114">進位係數。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-114">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b6d3-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b6d3-115">Return value</span></span>

<span data-ttu-id="4b6d3-116">傳回 `(a * b + rnd)/c` 計算或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-116">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="4b6d3-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4b6d3-117">Return code</span></span>                                                                                       | <span data-ttu-id="4b6d3-118">Description</span><span class="sxs-lookup"><span data-stu-id="4b6d3-118">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b6d3-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="4b6d3-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="4b6d3-120">發生溢位，因為結果太大 (正) 。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-120">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="4b6d3-121"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="4b6d3-121"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="4b6d3-122">發生溢位，因為結果太大 (負) 。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-122">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b6d3-123">備註</span><span class="sxs-lookup"><span data-stu-id="4b6d3-123">Remarks</span></span>

<span data-ttu-id="4b6d3-124">分割區的舍入方向為零。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-124">Rounding on the division is toward zero.</span></span> <span data-ttu-id="4b6d3-125">零除會視為溢位條件。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-125">Division by zero is counted as an overflow condition.</span></span>

<span data-ttu-id="4b6d3-126">時間戳記和搜尋時間是64位的值，因此這個函式適用于在32位系統上執行轉換。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-126">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="4b6d3-127">例如，在 MPEG 1 中，系統時鐘參考是 90-kHz，或每秒90000刻度。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-127">For example, in MPEG-1 the system clock reference is 90-kHz, or 90,000 ticks per second.</span></span> <span data-ttu-id="4b6d3-128">將此轉換為參考時間的公式 (100-毫微秒單位) 為</span><span class="sxs-lookup"><span data-stu-id="4b6d3-128">The formula to convert this to reference time (100-nanosecond units) is</span></span>


```C++
(timestamp * 1000) / 9
```



<span data-ttu-id="4b6d3-129">可以計算為 `Int64x32Div32(timestamp, 1000, 9, 0)` 。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-129">which can be calculated as `Int64x32Div32(timestamp, 1000, 9, 0)`.</span></span> <span data-ttu-id="4b6d3-130">使用 *rnd* 參數作為舍入係數。</span><span class="sxs-lookup"><span data-stu-id="4b6d3-130">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b6d3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b6d3-131">Requirements</span></span>



| <span data-ttu-id="4b6d3-132">需求</span><span class="sxs-lookup"><span data-stu-id="4b6d3-132">Requirement</span></span> | <span data-ttu-id="4b6d3-133">值</span><span class="sxs-lookup"><span data-stu-id="4b6d3-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b6d3-134">標頭</span><span class="sxs-lookup"><span data-stu-id="4b6d3-134">Header</span></span><br/>  | <dl> <span data-ttu-id="4b6d3-135"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4b6d3-135"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4b6d3-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="4b6d3-136">Library</span></span><br/> | <dl> <span data-ttu-id="4b6d3-137"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4b6d3-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b6d3-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b6d3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b6d3-139">其他 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="4b6d3-139">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="4b6d3-140">**llMulDiv**</span><span class="sxs-lookup"><span data-stu-id="4b6d3-140">**llMulDiv**</span></span>](llmuldiv.md)
</dt> </dl>

 

 




