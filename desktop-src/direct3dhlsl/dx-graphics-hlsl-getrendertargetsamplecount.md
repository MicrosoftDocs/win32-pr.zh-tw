---
title: GetRenderTargetSampleCount
description: 取得呈現目標的樣本數。
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- GetRenderTargetSampleCount HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96c159a2ed63684b4bad2cbc6fa789c2dbd76edf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462585"
---
# <a name="getrendertargetsamplecount"></a><span data-ttu-id="2aaf8-104">GetRenderTargetSampleCount</span><span class="sxs-lookup"><span data-stu-id="2aaf8-104">GetRenderTargetSampleCount</span></span>

<span data-ttu-id="2aaf8-105">取得呈現目標的樣本數。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-105">Gets the number of samples for a render target.</span></span>



| <span data-ttu-id="2aaf8-106">*UINT* GetRenderTargetSampleCount () </span><span class="sxs-lookup"><span data-stu-id="2aaf8-106">*UINT* GetRenderTargetSampleCount()</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="2aaf8-107">參數</span><span class="sxs-lookup"><span data-stu-id="2aaf8-107">Parameters</span></span>



| <span data-ttu-id="2aaf8-108">項目</span><span class="sxs-lookup"><span data-stu-id="2aaf8-108">Item</span></span>                                                                                 | <span data-ttu-id="2aaf8-109">描述</span><span class="sxs-lookup"><span data-stu-id="2aaf8-109">Description</span></span> |
|--------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="2aaf8-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>沒有</span><span class="sxs-lookup"><span data-stu-id="2aaf8-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="2aaf8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2aaf8-111">Return Value</span></span>

<span data-ttu-id="2aaf8-112">樣本數。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-112">The number of samples.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aaf8-113">備註</span><span class="sxs-lookup"><span data-stu-id="2aaf8-113">Remarks</span></span>

<span data-ttu-id="2aaf8-114">您可以使用此函數和 [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) ，找出轉譯目標的取樣位置數目和位置。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-114">Use this function and [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="2aaf8-115">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2aaf8-115">Minimum Shader Model</span></span>

<span data-ttu-id="2aaf8-116">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2aaf8-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2aaf8-117">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2aaf8-117">Shader Model</span></span>                                                        | <span data-ttu-id="2aaf8-118">支援</span><span class="sxs-lookup"><span data-stu-id="2aaf8-118">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="2aaf8-119">[著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="2aaf8-119">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="2aaf8-120">是</span><span class="sxs-lookup"><span data-stu-id="2aaf8-120">yes</span></span>       |
| [<span data-ttu-id="2aaf8-121">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2aaf8-121">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="2aaf8-122">不可以</span><span class="sxs-lookup"><span data-stu-id="2aaf8-122">no</span></span>        |
| [<span data-ttu-id="2aaf8-123">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2aaf8-123">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="2aaf8-124">不可以</span><span class="sxs-lookup"><span data-stu-id="2aaf8-124">no</span></span>        |
| [<span data-ttu-id="2aaf8-125">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2aaf8-125">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="2aaf8-126">不可以</span><span class="sxs-lookup"><span data-stu-id="2aaf8-126">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="2aaf8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2aaf8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aaf8-128">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="2aaf8-128">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





