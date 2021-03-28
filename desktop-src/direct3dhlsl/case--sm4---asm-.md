---
title: '案例 (sm4-asm) '
description: Switch 指令中的標籤。
ms.assetid: 456BB918-327E-4E15-8D38-F53850CAF666
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0278b8492575b1ef54fd64fc24b031fdec6cfb21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971557"
---
# <a name="case-sm4---asm"></a><span data-ttu-id="66e56-103">案例 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="66e56-103">case (sm4 - asm)</span></span>

<span data-ttu-id="66e56-104">Switch 指令中的標籤。</span><span class="sxs-lookup"><span data-stu-id="66e56-104">A label in a switch instruction.</span></span>



| <span data-ttu-id="66e56-105">案例 \[ 32-位立即\]</span><span class="sxs-lookup"><span data-stu-id="66e56-105">case \[32-bit immediate\]</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="66e56-106">備註</span><span class="sxs-lookup"><span data-stu-id="66e56-106">Remarks</span></span>

<span data-ttu-id="66e56-107">因為只有在未加入程式碼的 **情況下** ，才會發生這種情況，所以多個 **案例** (包括 [預設](default--sm4---asm-.md)) 可以共用相同的程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="66e56-107">Because falling through **cases** is valid only if there is no code added, multiple **cases** (including [default](default--sm4---asm-.md)) can share the same code block.</span></span>

<span data-ttu-id="66e56-108">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="66e56-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="66e56-109">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="66e56-109">Vertex Shader</span></span> | <span data-ttu-id="66e56-110">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="66e56-110">Geometry Shader</span></span> | <span data-ttu-id="66e56-111">像素著色器</span><span class="sxs-lookup"><span data-stu-id="66e56-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="66e56-112">x</span><span class="sxs-lookup"><span data-stu-id="66e56-112">x</span></span>             | <span data-ttu-id="66e56-113">x</span><span class="sxs-lookup"><span data-stu-id="66e56-113">x</span></span>               | <span data-ttu-id="66e56-114">x</span><span class="sxs-lookup"><span data-stu-id="66e56-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="66e56-115">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="66e56-115">Minimum Shader Model</span></span>

<span data-ttu-id="66e56-116">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="66e56-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="66e56-117">著色器模型</span><span class="sxs-lookup"><span data-stu-id="66e56-117">Shader Model</span></span>                                              | <span data-ttu-id="66e56-118">支援</span><span class="sxs-lookup"><span data-stu-id="66e56-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="66e56-119">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="66e56-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="66e56-120">是</span><span class="sxs-lookup"><span data-stu-id="66e56-120">yes</span></span>       |
| [<span data-ttu-id="66e56-121">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="66e56-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="66e56-122">是</span><span class="sxs-lookup"><span data-stu-id="66e56-122">yes</span></span>       |
| [<span data-ttu-id="66e56-123">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="66e56-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="66e56-124">是</span><span class="sxs-lookup"><span data-stu-id="66e56-124">yes</span></span>       |
| [<span data-ttu-id="66e56-125">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="66e56-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="66e56-126">不可以</span><span class="sxs-lookup"><span data-stu-id="66e56-126">no</span></span>        |
| [<span data-ttu-id="66e56-127">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="66e56-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="66e56-128">不可以</span><span class="sxs-lookup"><span data-stu-id="66e56-128">no</span></span>        |
| [<span data-ttu-id="66e56-129">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="66e56-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="66e56-130">不可以</span><span class="sxs-lookup"><span data-stu-id="66e56-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="66e56-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="66e56-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66e56-132">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="66e56-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




