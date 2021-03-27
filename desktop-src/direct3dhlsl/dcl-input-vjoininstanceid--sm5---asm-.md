---
title: 'dcl_input vJoinInstanceID (sm5-asm) '
description: 在輪廓著色器聯結階段中宣告實例識別碼。
ms.assetid: 2EABB24A-7ED7-460D-A2AD-D2C40DCCB2DC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bae9351fc7183aa37cd660c265aab803f4661e9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932830"
---
# <a name="dcl_input-vjoininstanceid-sm5---asm"></a><span data-ttu-id="f8733-103">dcl \_ 輸入 vJoinInstanceID (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="f8733-103">dcl\_input vJoinInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="f8733-104">在輪廓著色器聯結階段中宣告實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8733-104">Declare the instance ID in a hull shader join phase.</span></span>



| <span data-ttu-id="f8733-105">dcl \_ 輸入 vJoinInstanceID</span><span class="sxs-lookup"><span data-stu-id="f8733-105">dcl\_input vJoinInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="f8733-106">項目</span><span class="sxs-lookup"><span data-stu-id="f8733-106">Item</span></span>                                                                                                                               | <span data-ttu-id="f8733-107">描述</span><span class="sxs-lookup"><span data-stu-id="f8733-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="f8733-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vJoinInstanceID*</span><span class="sxs-lookup"><span data-stu-id="f8733-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vJoinInstanceID*</span></span><br/> | <span data-ttu-id="f8733-109">\[在 \] 實例識別碼中。</span><span class="sxs-lookup"><span data-stu-id="f8733-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f8733-110">備註</span><span class="sxs-lookup"><span data-stu-id="f8733-110">Remarks</span></span>

<span data-ttu-id="f8733-111">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="f8733-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f8733-112">頂點</span><span class="sxs-lookup"><span data-stu-id="f8733-112">Vertex</span></span> | <span data-ttu-id="f8733-113">船體</span><span class="sxs-lookup"><span data-stu-id="f8733-113">Hull</span></span> | <span data-ttu-id="f8733-114">網域</span><span class="sxs-lookup"><span data-stu-id="f8733-114">Domain</span></span> | <span data-ttu-id="f8733-115">幾何</span><span class="sxs-lookup"><span data-stu-id="f8733-115">Geometry</span></span> | <span data-ttu-id="f8733-116">像素</span><span class="sxs-lookup"><span data-stu-id="f8733-116">Pixel</span></span> | <span data-ttu-id="f8733-117">計算</span><span class="sxs-lookup"><span data-stu-id="f8733-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="f8733-118">X</span><span class="sxs-lookup"><span data-stu-id="f8733-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f8733-119">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f8733-119">Minimum Shader Model</span></span>

<span data-ttu-id="f8733-120">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="f8733-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f8733-121">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f8733-121">Shader Model</span></span>                                              | <span data-ttu-id="f8733-122">支援</span><span class="sxs-lookup"><span data-stu-id="f8733-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f8733-123">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f8733-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f8733-124">是</span><span class="sxs-lookup"><span data-stu-id="f8733-124">yes</span></span>       |
| [<span data-ttu-id="f8733-125">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="f8733-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f8733-126">不可以</span><span class="sxs-lookup"><span data-stu-id="f8733-126">no</span></span>        |
| [<span data-ttu-id="f8733-127">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="f8733-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f8733-128">不可以</span><span class="sxs-lookup"><span data-stu-id="f8733-128">no</span></span>        |
| [<span data-ttu-id="f8733-129">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f8733-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f8733-130">不可以</span><span class="sxs-lookup"><span data-stu-id="f8733-130">no</span></span>        |
| [<span data-ttu-id="f8733-131">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f8733-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f8733-132">不可以</span><span class="sxs-lookup"><span data-stu-id="f8733-132">no</span></span>        |
| [<span data-ttu-id="f8733-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f8733-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f8733-134">不可以</span><span class="sxs-lookup"><span data-stu-id="f8733-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f8733-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8733-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8733-136">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f8733-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





