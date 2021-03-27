---
title: '預設 (sm4-asm) '
description: Switch 語句中的選擇性標籤。
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92364212e4d20a6e9229c057ba424f43f8f8556
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971541"
---
# <a name="default-sm4---asm"></a><span data-ttu-id="2217b-103">預設 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="2217b-103">default (sm4 - asm)</span></span>

<span data-ttu-id="2217b-104">[Switch](switch--sm4---asm-.md)語句中的選擇性標籤。</span><span class="sxs-lookup"><span data-stu-id="2217b-104">An optional label in a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="2217b-105">預設</span><span class="sxs-lookup"><span data-stu-id="2217b-105">default</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="2217b-106">備註</span><span class="sxs-lookup"><span data-stu-id="2217b-106">Remarks</span></span>

<span data-ttu-id="2217b-107">此指令的運作方式就像 C 中的 **預設值** 。只有在未加入程式碼時才會生效，因此多個案例 (包括 **預設**) 可以共用相同的程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="2217b-107">This instruction operates just like **default** in C. Falling through is valid only if there is no code added, so multiple cases (including **default**) can share the same code block.</span></span>

<span data-ttu-id="2217b-108">**Switch** 結構中只允許一個 **default** 語句。</span><span class="sxs-lookup"><span data-stu-id="2217b-108">Only one **default** statement is permitted in a **switch** construct.</span></span>

<span data-ttu-id="2217b-109">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="2217b-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2217b-110">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="2217b-110">Vertex Shader</span></span> | <span data-ttu-id="2217b-111">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="2217b-111">Geometry Shader</span></span> | <span data-ttu-id="2217b-112">像素著色器</span><span class="sxs-lookup"><span data-stu-id="2217b-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2217b-113">x</span><span class="sxs-lookup"><span data-stu-id="2217b-113">x</span></span>             | <span data-ttu-id="2217b-114">x</span><span class="sxs-lookup"><span data-stu-id="2217b-114">x</span></span>               | <span data-ttu-id="2217b-115">x</span><span class="sxs-lookup"><span data-stu-id="2217b-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2217b-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2217b-116">Minimum Shader Model</span></span>

<span data-ttu-id="2217b-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2217b-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2217b-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2217b-118">Shader Model</span></span>                                              | <span data-ttu-id="2217b-119">支援</span><span class="sxs-lookup"><span data-stu-id="2217b-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2217b-120">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2217b-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2217b-121">是</span><span class="sxs-lookup"><span data-stu-id="2217b-121">yes</span></span>       |
| [<span data-ttu-id="2217b-122">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="2217b-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2217b-123">是</span><span class="sxs-lookup"><span data-stu-id="2217b-123">yes</span></span>       |
| [<span data-ttu-id="2217b-124">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="2217b-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2217b-125">是</span><span class="sxs-lookup"><span data-stu-id="2217b-125">yes</span></span>       |
| [<span data-ttu-id="2217b-126">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2217b-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2217b-127">不可以</span><span class="sxs-lookup"><span data-stu-id="2217b-127">no</span></span>        |
| [<span data-ttu-id="2217b-128">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2217b-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2217b-129">不可以</span><span class="sxs-lookup"><span data-stu-id="2217b-129">no</span></span>        |
| [<span data-ttu-id="2217b-130">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2217b-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2217b-131">不可以</span><span class="sxs-lookup"><span data-stu-id="2217b-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2217b-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="2217b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2217b-133">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2217b-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




