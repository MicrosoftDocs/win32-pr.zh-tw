---
title: QuadReadAcrossY 函式
description: 傳回從這個四個 Y 方向的其他通道讀取的指定來源值。
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- QuadReadAcrossY 函式 HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104971812"
---
# <a name="quadreadacrossy-function"></a><span data-ttu-id="a1744-104">QuadReadAcrossY 函式</span><span class="sxs-lookup"><span data-stu-id="a1744-104">QuadReadAcrossY function</span></span>

<span data-ttu-id="a1744-105">傳回從這個四個 Y 方向的其他通道讀取的指定來源值。</span><span class="sxs-lookup"><span data-stu-id="a1744-105">Returns the specified source value read from the other lane in this quad in the Y direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1744-106">語法</span><span class="sxs-lookup"><span data-stu-id="a1744-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossY(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="a1744-107">參數</span><span class="sxs-lookup"><span data-stu-id="a1744-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1744-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="a1744-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="a1744-109">要求的類型。</span><span class="sxs-lookup"><span data-stu-id="a1744-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1744-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1744-110">Return value</span></span>

<span data-ttu-id="a1744-111">指定的來源值。</span><span class="sxs-lookup"><span data-stu-id="a1744-111">The specified source value.</span></span> <span data-ttu-id="a1744-112">如果來源通道為非使用中，則結果為未定義。</span><span class="sxs-lookup"><span data-stu-id="a1744-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1744-113">備註</span><span class="sxs-lookup"><span data-stu-id="a1744-113">Remarks</span></span>

<span data-ttu-id="a1744-114">如需四邊形的詳細資訊，請參閱 [著色器模型6的總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)。</span><span class="sxs-lookup"><span data-stu-id="a1744-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="a1744-115">只有在圖元和計算著色器中才支援來自著色器模型6.0 的函式。</span><span class="sxs-lookup"><span data-stu-id="a1744-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="a1744-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1744-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1744-117">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="a1744-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




