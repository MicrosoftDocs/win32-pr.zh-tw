---
title: 'firstbit (sm5-asm) '
description: 從 LSB 或 MSB 尋找數位中設定的第一個位。
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313748"
---
# <a name="firstbit-sm5---asm"></a><span data-ttu-id="4ab57-103">firstbit (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="4ab57-103">firstbit (sm5 - asm)</span></span>

<span data-ttu-id="4ab57-104">從 LSB 或 MSB 尋找數位中設定的第一個位。</span><span class="sxs-lookup"><span data-stu-id="4ab57-104">Finds the first bit set in a number, either from LSB or MSB.</span></span>



| <span data-ttu-id="4ab57-105">firstbit { \_ 嗨</span><span class="sxs-lookup"><span data-stu-id="4ab57-105">firstbit{\_hi\</span></span>|<span data-ttu-id="4ab57-106">\_高低</span><span class="sxs-lookup"><span data-stu-id="4ab57-106">\_lo\</span></span>|<span data-ttu-id="4ab57-107">\_shi} dest \[ \] 、src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4ab57-107">\_shi} dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="4ab57-108">項目</span><span class="sxs-lookup"><span data-stu-id="4ab57-108">Item</span></span>                                                            | <span data-ttu-id="4ab57-109">描述</span><span class="sxs-lookup"><span data-stu-id="4ab57-109">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab57-110"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="4ab57-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4ab57-111">\[在 \] *src0* 中第一個位集合的整數位置，從 LSB for FIRSTBIT \_ lo 或 MSB for firstbit hi 開始 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4ab57-111">\[in\] The integer position of the first bit set in *src0* starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span><br/> |
| <span data-ttu-id="4ab57-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4ab57-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4ab57-113">\[在 \] 輸入整數中。</span><span class="sxs-lookup"><span data-stu-id="4ab57-113">\[in\] The input integer.</span></span><br/>                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="4ab57-114">備註</span><span class="sxs-lookup"><span data-stu-id="4ab57-114">Remarks</span></span>

<span data-ttu-id="4ab57-115">這項作業會傳回32位輸入中第一位設定的整數位置，從 LSB for firstbit \_ lo 或 MSB for firstbit hi 開始 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4ab57-115">This operation returns the integer position of the first bit set in the 32-bit input starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span> <span data-ttu-id="4ab57-116">例如， \_ 在0x00000001 上的 firstbit lo 會傳回0。</span><span class="sxs-lookup"><span data-stu-id="4ab57-116">For example firstbit\_lo on 0x00000001 returns 0.</span></span> <span data-ttu-id="4ab57-117">\_0x10000000 上的 firstbit hi 會傳回3。</span><span class="sxs-lookup"><span data-stu-id="4ab57-117">firstbit\_hi on 0x10000000 returns 3.</span></span>

<span data-ttu-id="4ab57-118">\_如果數位為負數，則 firstbit 已簽署) 的 shi (s 會傳回 MSB 中的第一個 0; 否則會傳回 MSB 中的前1個。</span><span class="sxs-lookup"><span data-stu-id="4ab57-118">firstbit\_shi (s for signed) returns the first 0 from the MSB if the number is negative; otherwise it returns the first 1 from the MSB.</span></span>

<span data-ttu-id="4ab57-119">如果找不到相符項，則指令的所有變體會在32位暫存器中傳回 ~ 0 (0xffffffff) 。</span><span class="sxs-lookup"><span data-stu-id="4ab57-119">All variants of the instruction return ~0 (0xffffffff in 32-bit register) if no match is found.</span></span>

<span data-ttu-id="4ab57-120">您可以使用此指令快速列舉位中的設定位，或找出數位中最大的2乘冪。</span><span class="sxs-lookup"><span data-stu-id="4ab57-120">Use this instruction to quickly enumerate set bits in a bitfield, or find the largest power of 2 in a number.</span></span>

<span data-ttu-id="4ab57-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="4ab57-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4ab57-122">頂點</span><span class="sxs-lookup"><span data-stu-id="4ab57-122">Vertex</span></span> | <span data-ttu-id="4ab57-123">船體</span><span class="sxs-lookup"><span data-stu-id="4ab57-123">Hull</span></span> | <span data-ttu-id="4ab57-124">網域</span><span class="sxs-lookup"><span data-stu-id="4ab57-124">Domain</span></span> | <span data-ttu-id="4ab57-125">幾何</span><span class="sxs-lookup"><span data-stu-id="4ab57-125">Geometry</span></span> | <span data-ttu-id="4ab57-126">像素</span><span class="sxs-lookup"><span data-stu-id="4ab57-126">Pixel</span></span> | <span data-ttu-id="4ab57-127">計算</span><span class="sxs-lookup"><span data-stu-id="4ab57-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4ab57-128">X</span><span class="sxs-lookup"><span data-stu-id="4ab57-128">X</span></span>      | <span data-ttu-id="4ab57-129">X</span><span class="sxs-lookup"><span data-stu-id="4ab57-129">X</span></span>    | <span data-ttu-id="4ab57-130">X</span><span class="sxs-lookup"><span data-stu-id="4ab57-130">X</span></span>      | <span data-ttu-id="4ab57-131">X</span><span class="sxs-lookup"><span data-stu-id="4ab57-131">X</span></span>        | <span data-ttu-id="4ab57-132">X</span><span class="sxs-lookup"><span data-stu-id="4ab57-132">X</span></span>     | <span data-ttu-id="4ab57-133">X</span><span class="sxs-lookup"><span data-stu-id="4ab57-133">X</span></span>       |



 

## <a name="mimimum-shader-model"></a><span data-ttu-id="4ab57-134">最低著色器模型</span><span class="sxs-lookup"><span data-stu-id="4ab57-134">Mimimum Shader Model</span></span>

<span data-ttu-id="4ab57-135">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="4ab57-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4ab57-136">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4ab57-136">Shader Model</span></span>                                              | <span data-ttu-id="4ab57-137">支援</span><span class="sxs-lookup"><span data-stu-id="4ab57-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4ab57-138">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4ab57-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4ab57-139">是</span><span class="sxs-lookup"><span data-stu-id="4ab57-139">yes</span></span>       |
| [<span data-ttu-id="4ab57-140">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="4ab57-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4ab57-141">不可以</span><span class="sxs-lookup"><span data-stu-id="4ab57-141">no</span></span>        |
| [<span data-ttu-id="4ab57-142">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="4ab57-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4ab57-143">不可以</span><span class="sxs-lookup"><span data-stu-id="4ab57-143">no</span></span>        |
| [<span data-ttu-id="4ab57-144">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4ab57-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4ab57-145">不可以</span><span class="sxs-lookup"><span data-stu-id="4ab57-145">no</span></span>        |
| [<span data-ttu-id="4ab57-146">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4ab57-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4ab57-147">不可以</span><span class="sxs-lookup"><span data-stu-id="4ab57-147">no</span></span>        |
| [<span data-ttu-id="4ab57-148">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4ab57-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4ab57-149">不可以</span><span class="sxs-lookup"><span data-stu-id="4ab57-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4ab57-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ab57-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ab57-151">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4ab57-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





