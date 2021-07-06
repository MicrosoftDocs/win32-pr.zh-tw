---
title: WaveReadLaneAt 函式
description: 傳回指定 wave 內給定通道索引的運算式值。
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- WaveReadLaneAt 函式 HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 573730053a93a110381637ef8e62dc08a4aa1535
ms.sourcegitcommit: 1897c2a39b4ac4ca4b1e4aec394cef2ce2619c03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/06/2021
ms.locfileid: "113316480"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="6195b-104">WaveReadLaneAt 函式</span><span class="sxs-lookup"><span data-stu-id="6195b-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="6195b-105">傳回指定 wave 內給定通道索引的運算式值。</span><span class="sxs-lookup"><span data-stu-id="6195b-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="6195b-106">語法</span><span class="sxs-lookup"><span data-stu-id="6195b-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="6195b-107">參數</span><span class="sxs-lookup"><span data-stu-id="6195b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6195b-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="6195b-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="6195b-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="6195b-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="6195b-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="6195b-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="6195b-111">將傳回其 *expr* 結果之通道的索引。</span><span class="sxs-lookup"><span data-stu-id="6195b-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6195b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6195b-112">Return value</span></span>

<span data-ttu-id="6195b-113">產生的值是 *expr* 的結果。</span><span class="sxs-lookup"><span data-stu-id="6195b-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="6195b-114">如果 *laneIndex* 是統一的，則會是統一的。</span><span class="sxs-lookup"><span data-stu-id="6195b-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="6195b-115">備註</span><span class="sxs-lookup"><span data-stu-id="6195b-115">Remarks</span></span>

<span data-ttu-id="6195b-116">此函式實際上是 *laneIndex* 的第一個通道中的值廣播。</span><span class="sxs-lookup"><span data-stu-id="6195b-116">This function is effectively a broadcast of the value in the *laneIndex*'th lane.</span></span>

<span data-ttu-id="6195b-117">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="6195b-117">This function is supported from shader model 6.0 in all shader stages.</span></span>

## <a name="see-also"></a><span data-ttu-id="6195b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6195b-118">See also</span></span>

* [<span data-ttu-id="6195b-119">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="6195b-119">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [<span data-ttu-id="6195b-120">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="6195b-120">Shader Model 6</span></span>](shader-model-6-0.md)
