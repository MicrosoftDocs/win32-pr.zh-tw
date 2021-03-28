---
title: 'dcl_input vPrim (sm4-asm) '
description: 'dcl \_ 輸入 vPrim (sm4-asm) '
ms.assetid: 75287673-21d6-4eb7-829f-7f2f340aec54
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9742c6066d66d7aa4121c1d1d1df98a37cb0147e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373919"
---
# <a name="dcl_input-vprim-sm4---asm"></a><span data-ttu-id="65efd-103">dcl \_ 輸入 vPrim (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="65efd-103">dcl\_input vPrim (sm4 - asm)</span></span>

<span data-ttu-id="65efd-104">宣告幾何著色器使用其純量輸入（register vPrim）。</span><span class="sxs-lookup"><span data-stu-id="65efd-104">Declares that a geometry shader uses its scalar input-register vPrim.</span></span>



| <span data-ttu-id="65efd-105">dcl \_ 輸入 *vPrim*</span><span class="sxs-lookup"><span data-stu-id="65efd-105">dcl\_input *vPrim*</span></span> |
|--------------------|



 



| <span data-ttu-id="65efd-106">項目</span><span class="sxs-lookup"><span data-stu-id="65efd-106">Item</span></span>                                                                                       | <span data-ttu-id="65efd-107">描述</span><span class="sxs-lookup"><span data-stu-id="65efd-107">Description</span></span>                                                                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65efd-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span><span class="sxs-lookup"><span data-stu-id="65efd-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span></span><br/> | <span data-ttu-id="65efd-109">\[在 \] 32 位純量中，它可以套用至幾何著色器中的每個內部基本類型。</span><span class="sxs-lookup"><span data-stu-id="65efd-109">\[in\] A 32-bit scalar, which can be applied to each interior primitive in a geometry shader.</span></span><br/> |



 

<span data-ttu-id="65efd-110">純量無法套用至任何連續的基本物件。</span><span class="sxs-lookup"><span data-stu-id="65efd-110">The scalar cannot be applied to any adjacent primitives.</span></span>

<span data-ttu-id="65efd-111">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="65efd-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="65efd-112">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="65efd-112">Vertex Shader</span></span> | <span data-ttu-id="65efd-113">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="65efd-113">Geometry Shader</span></span> | <span data-ttu-id="65efd-114">像素著色器</span><span class="sxs-lookup"><span data-stu-id="65efd-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="65efd-115">x</span><span class="sxs-lookup"><span data-stu-id="65efd-115">x</span></span>               |              |



 

<span data-ttu-id="65efd-116">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="65efd-116">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="65efd-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="65efd-117">Minimum Shader Model</span></span>

<span data-ttu-id="65efd-118">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="65efd-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="65efd-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="65efd-119">Shader Model</span></span>                                              | <span data-ttu-id="65efd-120">支援</span><span class="sxs-lookup"><span data-stu-id="65efd-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="65efd-121">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="65efd-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="65efd-122">是</span><span class="sxs-lookup"><span data-stu-id="65efd-122">yes</span></span>       |
| [<span data-ttu-id="65efd-123">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="65efd-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="65efd-124">是</span><span class="sxs-lookup"><span data-stu-id="65efd-124">yes</span></span>       |
| [<span data-ttu-id="65efd-125">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="65efd-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="65efd-126">是</span><span class="sxs-lookup"><span data-stu-id="65efd-126">yes</span></span>       |
| [<span data-ttu-id="65efd-127">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="65efd-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="65efd-128">不可以</span><span class="sxs-lookup"><span data-stu-id="65efd-128">no</span></span>        |
| [<span data-ttu-id="65efd-129">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="65efd-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="65efd-130">不可以</span><span class="sxs-lookup"><span data-stu-id="65efd-130">no</span></span>        |
| [<span data-ttu-id="65efd-131">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="65efd-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="65efd-132">不可以</span><span class="sxs-lookup"><span data-stu-id="65efd-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="65efd-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="65efd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65efd-134">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="65efd-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





