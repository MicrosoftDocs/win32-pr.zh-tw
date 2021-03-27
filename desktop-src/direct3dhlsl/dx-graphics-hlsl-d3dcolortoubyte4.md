---
title: D3DCOLORtoUBYTE4
description: 將 D3DCOLOR 所設定的浮點數、4D 向量轉換成 UBYTE4。
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- D3DCOLORtoUBYTE4 HLSL
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508104"
---
# <a name="d3dcolortoubyte4"></a><span data-ttu-id="5f45b-104">D3DCOLORtoUBYTE4</span><span class="sxs-lookup"><span data-stu-id="5f45b-104">D3DCOLORtoUBYTE4</span></span>

<span data-ttu-id="5f45b-105">將 D3DCOLOR 所設定的浮點數、4D 向量轉換成 UBYTE4。</span><span class="sxs-lookup"><span data-stu-id="5f45b-105">Converts a floating-point, 4D vector set by a D3DCOLOR to a UBYTE4.</span></span>



| <span data-ttu-id="5f45b-106">*ret* D3DCOLORtoUBYTE4 (*x*) </span><span class="sxs-lookup"><span data-stu-id="5f45b-106">*ret* D3DCOLORtoUBYTE4(*x*)</span></span> |
|-----------------------------|



 

<span data-ttu-id="5f45b-107">此函式會 swizzles 和調整 *x* 參數的元件。</span><span class="sxs-lookup"><span data-stu-id="5f45b-107">This function swizzles and scales components of the *x* parameter.</span></span> <span data-ttu-id="5f45b-108">您可以使用此函式來彌補一些硬體中是否缺少 UBYTE4 支援。</span><span class="sxs-lookup"><span data-stu-id="5f45b-108">Use this function to compensate for the lack of UBYTE4 support in some hardware.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f45b-109">參數</span><span class="sxs-lookup"><span data-stu-id="5f45b-109">Parameters</span></span>



| <span data-ttu-id="5f45b-110">項目</span><span class="sxs-lookup"><span data-stu-id="5f45b-110">Item</span></span>                                                   | <span data-ttu-id="5f45b-111">描述</span><span class="sxs-lookup"><span data-stu-id="5f45b-111">Description</span></span>                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="5f45b-112"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="5f45b-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="5f45b-113">\[\]要轉換的浮點數 vector4。</span><span class="sxs-lookup"><span data-stu-id="5f45b-113">\[in\] The floating-point vector4 to convert.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5f45b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f45b-114">Return Value</span></span>

<span data-ttu-id="5f45b-115">*X* 參數的 UBYTE4 標記法。</span><span class="sxs-lookup"><span data-stu-id="5f45b-115">The UBYTE4 representation of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="5f45b-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="5f45b-116">Type Description</span></span>



| <span data-ttu-id="5f45b-117">Name</span><span class="sxs-lookup"><span data-stu-id="5f45b-117">Name</span></span>  | [<span data-ttu-id="5f45b-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="5f45b-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="5f45b-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="5f45b-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5f45b-120">大小</span><span class="sxs-lookup"><span data-stu-id="5f45b-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="5f45b-121">*x*</span><span class="sxs-lookup"><span data-stu-id="5f45b-121">*x*</span></span>   | [<span data-ttu-id="5f45b-122">**向量**</span><span class="sxs-lookup"><span data-stu-id="5f45b-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5f45b-123">**浮動**</span><span class="sxs-lookup"><span data-stu-id="5f45b-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5f45b-124">4</span><span class="sxs-lookup"><span data-stu-id="5f45b-124">4</span></span>    |
| <span data-ttu-id="5f45b-125">*Ret*</span><span class="sxs-lookup"><span data-stu-id="5f45b-125">*ret*</span></span> | [<span data-ttu-id="5f45b-126">**向量**</span><span class="sxs-lookup"><span data-stu-id="5f45b-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5f45b-127">**整數**</span><span class="sxs-lookup"><span data-stu-id="5f45b-127">**integer**</span></span>](/windows/desktop/WinProg/windows-data-types)                      | <span data-ttu-id="5f45b-128">4</span><span class="sxs-lookup"><span data-stu-id="5f45b-128">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5f45b-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="5f45b-129">Minimum Shader Model</span></span>

<span data-ttu-id="5f45b-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="5f45b-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5f45b-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="5f45b-131">Shader Model</span></span>                                                                       | <span data-ttu-id="5f45b-132">支援</span><span class="sxs-lookup"><span data-stu-id="5f45b-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5f45b-133">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="5f45b-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="5f45b-134">是</span><span class="sxs-lookup"><span data-stu-id="5f45b-134">yes</span></span>       |
| [<span data-ttu-id="5f45b-135">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5f45b-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="5f45b-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5f45b-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="5f45b-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f45b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f45b-138">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="5f45b-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

