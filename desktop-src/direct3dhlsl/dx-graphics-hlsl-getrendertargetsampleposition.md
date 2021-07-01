---
title: GetRenderTargetSamplePosition
description: 取得給定範例索引的取樣位置 (x，y) 。
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- GetRenderTargetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c31bc829f8990517ddbea8be7c25eead413ab666
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120573"
---
# <a name="getrendertargetsampleposition"></a><span data-ttu-id="9d049-104">GetRenderTargetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="9d049-104">GetRenderTargetSamplePosition</span></span>

<span data-ttu-id="9d049-105">取得給定範例索引的取樣位置 (x，y) 。</span><span class="sxs-lookup"><span data-stu-id="9d049-105">Gets the sampling position (x,y) for a given sample index.</span></span>

<span data-ttu-id="9d049-106">float<2> GetRenderTargetSamplePosition ( in int<1> Index</span><span class="sxs-lookup"><span data-stu-id="9d049-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span></span><br/><span data-ttu-id="9d049-107">);</span><span class="sxs-lookup"><span data-stu-id="9d049-107">);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="9d049-108">參數</span><span class="sxs-lookup"><span data-stu-id="9d049-108">Parameters</span></span>



| <span data-ttu-id="9d049-109">項目</span><span class="sxs-lookup"><span data-stu-id="9d049-109">Item</span></span>                                                                                       | <span data-ttu-id="9d049-110">描述</span><span class="sxs-lookup"><span data-stu-id="9d049-110">Description</span></span>                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="9d049-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*指數*</span><span class="sxs-lookup"><span data-stu-id="9d049-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*</span></span><br/> | <span data-ttu-id="9d049-112">\[以 \] 零為基底的範例索引。</span><span class="sxs-lookup"><span data-stu-id="9d049-112">\[in\] A zero-based sample index.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9d049-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d049-113">Return Value</span></span>

<span data-ttu-id="9d049-114">給定範例的 (x，y) 位置。</span><span class="sxs-lookup"><span data-stu-id="9d049-114">The (x,y) position of the given sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d049-115">備註</span><span class="sxs-lookup"><span data-stu-id="9d049-115">Remarks</span></span>

<span data-ttu-id="9d049-116">您可以使用此函數和 [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) ，找出轉譯目標的取樣位置數目和位置。</span><span class="sxs-lookup"><span data-stu-id="9d049-116">Use this function and [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="9d049-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9d049-117">Minimum Shader Model</span></span>

<span data-ttu-id="9d049-118">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9d049-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9d049-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9d049-119">Shader Model</span></span>                                                        | <span data-ttu-id="9d049-120">支援</span><span class="sxs-lookup"><span data-stu-id="9d049-120">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="9d049-121">[著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="9d049-121">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="9d049-122">是</span><span class="sxs-lookup"><span data-stu-id="9d049-122">yes</span></span>       |
| [<span data-ttu-id="9d049-123">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9d049-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="9d049-124">否</span><span class="sxs-lookup"><span data-stu-id="9d049-124">no</span></span>        |
| [<span data-ttu-id="9d049-125">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9d049-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="9d049-126">否</span><span class="sxs-lookup"><span data-stu-id="9d049-126">no</span></span>        |
| [<span data-ttu-id="9d049-127">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9d049-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="9d049-128">否</span><span class="sxs-lookup"><span data-stu-id="9d049-128">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="9d049-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d049-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d049-130">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="9d049-130">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





