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
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2020
ms.locfileid: "104374896"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="dafd2-104">WaveReadLaneAt 函式</span><span class="sxs-lookup"><span data-stu-id="dafd2-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="dafd2-105">傳回指定 wave 內給定通道索引的運算式值。</span><span class="sxs-lookup"><span data-stu-id="dafd2-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="dafd2-106">語法</span><span class="sxs-lookup"><span data-stu-id="dafd2-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="dafd2-107">參數</span><span class="sxs-lookup"><span data-stu-id="dafd2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dafd2-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="dafd2-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="dafd2-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="dafd2-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="dafd2-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="dafd2-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="dafd2-111">將傳回其 *expr* 結果之通道的索引。</span><span class="sxs-lookup"><span data-stu-id="dafd2-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dafd2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dafd2-112">Return value</span></span>

<span data-ttu-id="dafd2-113">產生的值是 *expr* 的結果。</span><span class="sxs-lookup"><span data-stu-id="dafd2-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="dafd2-114">如果 *laneIndex* 是統一的，則會是統一的。</span><span class="sxs-lookup"><span data-stu-id="dafd2-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="dafd2-115">備註</span><span class="sxs-lookup"><span data-stu-id="dafd2-115">Remarks</span></span>

<span data-ttu-id="dafd2-116">此函數實際上是 laneIndex'th 通道中的值廣播。</span><span class="sxs-lookup"><span data-stu-id="dafd2-116">This function is effectively a broadcast of the value in the laneIndex’th lane.</span></span>

<span data-ttu-id="dafd2-117">著色器模型6.0 支援下列著色器類型中的函數：</span><span class="sxs-lookup"><span data-stu-id="dafd2-117">This function is supported from shader model 6.0, in the following types of shaders:</span></span>



| <span data-ttu-id="dafd2-118">頂點</span><span class="sxs-lookup"><span data-stu-id="dafd2-118">Vertex</span></span> | <span data-ttu-id="dafd2-119">船體</span><span class="sxs-lookup"><span data-stu-id="dafd2-119">Hull</span></span> | <span data-ttu-id="dafd2-120">網域</span><span class="sxs-lookup"><span data-stu-id="dafd2-120">Domain</span></span> | <span data-ttu-id="dafd2-121">幾何</span><span class="sxs-lookup"><span data-stu-id="dafd2-121">Geometry</span></span> | <span data-ttu-id="dafd2-122">像素</span><span class="sxs-lookup"><span data-stu-id="dafd2-122">Pixel</span></span> | <span data-ttu-id="dafd2-123">計算</span><span class="sxs-lookup"><span data-stu-id="dafd2-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="dafd2-124">x</span><span class="sxs-lookup"><span data-stu-id="dafd2-124">x</span></span>     | <span data-ttu-id="dafd2-125">x</span><span class="sxs-lookup"><span data-stu-id="dafd2-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dafd2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dafd2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dafd2-127">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="dafd2-127">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="dafd2-128">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="dafd2-128">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




