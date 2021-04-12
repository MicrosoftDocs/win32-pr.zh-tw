---
title: QuadReadLaneAt 函式
description: 從目前四內的通道識別碼所識別的通道傳回指定的來源值。
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- QuadReadLaneAt 函式 HLSL
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463925"
---
# <a name="quadreadlaneat-function"></a><span data-ttu-id="0cf1d-104">QuadReadLaneAt 函式</span><span class="sxs-lookup"><span data-stu-id="0cf1d-104">QuadReadLaneAt function</span></span>

<span data-ttu-id="0cf1d-105">從目前四內的通道識別碼所識別的通道傳回指定的來源值。</span><span class="sxs-lookup"><span data-stu-id="0cf1d-105">Returns the specified source value from the lane identified by the lane ID within the current quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf1d-106">語法</span><span class="sxs-lookup"><span data-stu-id="0cf1d-106">Syntax</span></span>


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a><span data-ttu-id="0cf1d-107">參數</span><span class="sxs-lookup"><span data-stu-id="0cf1d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cf1d-108">*sourceValue*</span><span class="sxs-lookup"><span data-stu-id="0cf1d-108">*sourceValue*</span></span> 
</dt> <dd>

<span data-ttu-id="0cf1d-109">要求的類型。</span><span class="sxs-lookup"><span data-stu-id="0cf1d-109">The requested type.</span></span>

</dd> <dt>

<span data-ttu-id="0cf1d-110">*quadLaneID*</span><span class="sxs-lookup"><span data-stu-id="0cf1d-110">*quadLaneID*</span></span> 
</dt> <dd>

<span data-ttu-id="0cf1d-111">通道識別碼;這會是從0到3的值。</span><span class="sxs-lookup"><span data-stu-id="0cf1d-111">The lane ID; this will be a value from 0 to 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cf1d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cf1d-112">Return value</span></span>

<span data-ttu-id="0cf1d-113">指定的來源值。</span><span class="sxs-lookup"><span data-stu-id="0cf1d-113">The specified source value.</span></span> <span data-ttu-id="0cf1d-114">此函式的結果在四個之間是一致的。</span><span class="sxs-lookup"><span data-stu-id="0cf1d-114">The result of this function is uniform across the quad.</span></span> <span data-ttu-id="0cf1d-115">如果來源通道為非使用中，則結果為未定義。</span><span class="sxs-lookup"><span data-stu-id="0cf1d-115">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cf1d-116">備註</span><span class="sxs-lookup"><span data-stu-id="0cf1d-116">Remarks</span></span>

<span data-ttu-id="0cf1d-117">如需四邊形的詳細資訊，請參閱 [著色器模型6的總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)。</span><span class="sxs-lookup"><span data-stu-id="0cf1d-117">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="0cf1d-118">只有在圖元和計算著色器中才支援來自著色器模型6.0 的函式。</span><span class="sxs-lookup"><span data-stu-id="0cf1d-118">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="0cf1d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cf1d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf1d-120">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="0cf1d-120">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




