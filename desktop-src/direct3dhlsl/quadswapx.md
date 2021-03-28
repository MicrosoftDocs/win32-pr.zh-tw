---
title: QuadReadAcrossX 函式
description: 傳回指定的區域值，此值會從這個四的 X 方向中的另一個通道讀取。
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- QuadReadAcrossX 函式 HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104093511"
---
# <a name="quadreadacrossx-function"></a><span data-ttu-id="8235a-104">QuadReadAcrossX 函式</span><span class="sxs-lookup"><span data-stu-id="8235a-104">QuadReadAcrossX function</span></span>

<span data-ttu-id="8235a-105">傳回指定的區域值，此值會從這個四的 X 方向中的另一個通道讀取。</span><span class="sxs-lookup"><span data-stu-id="8235a-105">Returns the specified local value read from the other lane in this quad in the X direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="8235a-106">語法</span><span class="sxs-lookup"><span data-stu-id="8235a-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="8235a-107">參數</span><span class="sxs-lookup"><span data-stu-id="8235a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8235a-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="8235a-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="8235a-109">要求的類型。</span><span class="sxs-lookup"><span data-stu-id="8235a-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8235a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8235a-110">Return value</span></span>

<span data-ttu-id="8235a-111">指定的區域值。</span><span class="sxs-lookup"><span data-stu-id="8235a-111">The specified local value.</span></span> <span data-ttu-id="8235a-112">如果來源通道為非使用中，則結果為未定義。</span><span class="sxs-lookup"><span data-stu-id="8235a-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="8235a-113">備註</span><span class="sxs-lookup"><span data-stu-id="8235a-113">Remarks</span></span>

<span data-ttu-id="8235a-114">如需四邊形的詳細資訊，請參閱 [著色器模型6的總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)。</span><span class="sxs-lookup"><span data-stu-id="8235a-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="8235a-115">只有在圖元和計算著色器中才支援來自著色器模型6.0 的函式。</span><span class="sxs-lookup"><span data-stu-id="8235a-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="8235a-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8235a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8235a-117">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="8235a-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




