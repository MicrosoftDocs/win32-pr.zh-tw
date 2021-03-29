---
title: 'continuec (sm4-asm) '
description: 在目前迴圈的開頭有條件地繼續執行。
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d480d8828f8f68af1f6a2ff4f52224041d5241df
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971556"
---
# <a name="continuec-sm4---asm"></a><span data-ttu-id="23d25-103">continuec (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="23d25-103">continuec (sm4 - asm)</span></span>

<span data-ttu-id="23d25-104">在目前迴圈的開頭有條件地繼續執行。</span><span class="sxs-lookup"><span data-stu-id="23d25-104">Conditionally continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="23d25-105">continuec { \_ z </span><span class="sxs-lookup"><span data-stu-id="23d25-105">continuec{\_z</span></span>\|<span data-ttu-id="23d25-106">\_nz} src0. 選取 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="23d25-106">\_nz} src0.select\_component</span></span> |
|---------------------------------------------|



 



| <span data-ttu-id="23d25-107">詞彙</span><span class="sxs-lookup"><span data-stu-id="23d25-107">Term</span></span>                                                            | <span data-ttu-id="23d25-108">描述</span><span class="sxs-lookup"><span data-stu-id="23d25-108">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="23d25-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="23d25-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="23d25-110">\[用 \] 來測試條件的元件。</span><span class="sxs-lookup"><span data-stu-id="23d25-110">\[in\] The component against which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23d25-111">備註</span><span class="sxs-lookup"><span data-stu-id="23d25-111">Remarks</span></span>

<span data-ttu-id="23d25-112">**continuec** 只能在 [迴圈](loop--sm4---asm-.md) 或 [endloop](endloop--sm4---asm-.md)內使用。</span><span class="sxs-lookup"><span data-stu-id="23d25-112">**continuec** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="23d25-113">下列範例顯示如何使用 **continuec** 指令。</span><span class="sxs-lookup"><span data-stu-id="23d25-113">The following example shows how to use the **continuec** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



<span data-ttu-id="23d25-114">Token 格式包含著色器中對應迴圈指令的位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="23d25-114">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="23d25-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="23d25-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="23d25-116">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="23d25-116">Vertex Shader</span></span> | <span data-ttu-id="23d25-117">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="23d25-117">Geometry Shader</span></span> | <span data-ttu-id="23d25-118">像素著色器</span><span class="sxs-lookup"><span data-stu-id="23d25-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="23d25-119">x</span><span class="sxs-lookup"><span data-stu-id="23d25-119">x</span></span>             | <span data-ttu-id="23d25-120">x</span><span class="sxs-lookup"><span data-stu-id="23d25-120">x</span></span>               | <span data-ttu-id="23d25-121">x</span><span class="sxs-lookup"><span data-stu-id="23d25-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="23d25-122">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="23d25-122">Minimum Shader Model</span></span>

<span data-ttu-id="23d25-123">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="23d25-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="23d25-124">著色器模型</span><span class="sxs-lookup"><span data-stu-id="23d25-124">Shader Model</span></span>                                              | <span data-ttu-id="23d25-125">支援</span><span class="sxs-lookup"><span data-stu-id="23d25-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="23d25-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="23d25-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="23d25-127">是</span><span class="sxs-lookup"><span data-stu-id="23d25-127">yes</span></span>       |
| [<span data-ttu-id="23d25-128">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="23d25-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="23d25-129">是</span><span class="sxs-lookup"><span data-stu-id="23d25-129">yes</span></span>       |
| [<span data-ttu-id="23d25-130">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="23d25-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="23d25-131">是</span><span class="sxs-lookup"><span data-stu-id="23d25-131">yes</span></span>       |
| [<span data-ttu-id="23d25-132">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="23d25-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="23d25-133">不可以</span><span class="sxs-lookup"><span data-stu-id="23d25-133">no</span></span>        |
| [<span data-ttu-id="23d25-134">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="23d25-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="23d25-135">不可以</span><span class="sxs-lookup"><span data-stu-id="23d25-135">no</span></span>        |
| [<span data-ttu-id="23d25-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="23d25-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="23d25-137">不可以</span><span class="sxs-lookup"><span data-stu-id="23d25-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="23d25-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="23d25-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23d25-139">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="23d25-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





