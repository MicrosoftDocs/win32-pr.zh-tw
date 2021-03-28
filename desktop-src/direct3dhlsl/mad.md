---
title: mad 函式
description: 針對三個值執行算術乘法/add 運算。
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- mad 函數 HLSL
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462589"
---
# <a name="mad-function"></a><span data-ttu-id="da922-104">mad 函式</span><span class="sxs-lookup"><span data-stu-id="da922-104">mad function</span></span>

<span data-ttu-id="da922-105">針對三個值執行算術乘法/add 運算。</span><span class="sxs-lookup"><span data-stu-id="da922-105">Performs an arithmetic multiply/add operation on three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="da922-106">語法</span><span class="sxs-lookup"><span data-stu-id="da922-106">Syntax</span></span>

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a><span data-ttu-id="da922-107">參數</span><span class="sxs-lookup"><span data-stu-id="da922-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da922-108">*mvalue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da922-108">*mvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da922-109">類型： **數值**</span><span class="sxs-lookup"><span data-stu-id="da922-109">Type: **numeric**</span></span>

<span data-ttu-id="da922-110">乘法值。</span><span class="sxs-lookup"><span data-stu-id="da922-110">The multiplication value.</span></span>

</dd> <dt>

<span data-ttu-id="da922-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da922-111">*avalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da922-112">類型： **數值**</span><span class="sxs-lookup"><span data-stu-id="da922-112">Type: **numeric**</span></span>

<span data-ttu-id="da922-113">第一個加法值。</span><span class="sxs-lookup"><span data-stu-id="da922-113">The first addition value.</span></span>

</dd> <dt>

<span data-ttu-id="da922-114">*其中 bvalue system.boolean.true* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da922-114">*bvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da922-115">類型： **數值**</span><span class="sxs-lookup"><span data-stu-id="da922-115">Type: **numeric**</span></span>

<span data-ttu-id="da922-116">第二個加法值。</span><span class="sxs-lookup"><span data-stu-id="da922-116">The second addition value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da922-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="da922-117">Return value</span></span>

<span data-ttu-id="da922-118">類型： **數值**</span><span class="sxs-lookup"><span data-stu-id="da922-118">Type: **numeric**</span></span>

<span data-ttu-id="da922-119">*Mvalue* \* *值*  +  *其中 bvalue system.boolean.true* 的結果。</span><span class="sxs-lookup"><span data-stu-id="da922-119">The result of *mvalue* \* *avalue* + *bvalue*.</span></span>

## <a name="remarks"></a><span data-ttu-id="da922-120">備註</span><span class="sxs-lookup"><span data-stu-id="da922-120">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="da922-121">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="da922-121">Minimum Shader Model</span></span>

<span data-ttu-id="da922-122">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="da922-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="da922-123">著色器模型</span><span class="sxs-lookup"><span data-stu-id="da922-123">Shader Model</span></span>                                                                | <span data-ttu-id="da922-124">支援</span><span class="sxs-lookup"><span data-stu-id="da922-124">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="da922-125">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="da922-125">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="da922-126">是</span><span class="sxs-lookup"><span data-stu-id="da922-126">yes</span></span>       |



 

<span data-ttu-id="da922-127">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="da922-127">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="da922-128">頂點</span><span class="sxs-lookup"><span data-stu-id="da922-128">Vertex</span></span> | <span data-ttu-id="da922-129">船體</span><span class="sxs-lookup"><span data-stu-id="da922-129">Hull</span></span> | <span data-ttu-id="da922-130">網域</span><span class="sxs-lookup"><span data-stu-id="da922-130">Domain</span></span> | <span data-ttu-id="da922-131">幾何</span><span class="sxs-lookup"><span data-stu-id="da922-131">Geometry</span></span> | <span data-ttu-id="da922-132">像素</span><span class="sxs-lookup"><span data-stu-id="da922-132">Pixel</span></span> | <span data-ttu-id="da922-133">計算</span><span class="sxs-lookup"><span data-stu-id="da922-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="da922-134">x</span><span class="sxs-lookup"><span data-stu-id="da922-134">x</span></span>      | <span data-ttu-id="da922-135">x</span><span class="sxs-lookup"><span data-stu-id="da922-135">x</span></span>    | <span data-ttu-id="da922-136">x</span><span class="sxs-lookup"><span data-stu-id="da922-136">x</span></span>      | <span data-ttu-id="da922-137">x</span><span class="sxs-lookup"><span data-stu-id="da922-137">x</span></span>        | <span data-ttu-id="da922-138">x</span><span class="sxs-lookup"><span data-stu-id="da922-138">x</span></span>     | <span data-ttu-id="da922-139">x</span><span class="sxs-lookup"><span data-stu-id="da922-139">x</span></span>       |



 

<span data-ttu-id="da922-140">著色器作者可以使用 **mad** 內部，在編譯的著色器輸出中明確地以 **mad** 硬體指令作為目標，這在使用 [精確](dx-graphics-hlsl-appendix-keywords.md) 關鍵字標記結果的著色器中特別有用。</span><span class="sxs-lookup"><span data-stu-id="da922-140">Shader authors can use the **mad** instrinsic to explicitly target the **mad** hardware instruction in the compiled shader output, which is particularly useful with shaders that mark results with the [precise](dx-graphics-hlsl-appendix-keywords.md) keyword.</span></span> <span data-ttu-id="da922-141">您可以在硬體中將 **mad** 指令實作為「融合的」，這可提供比起執行 **mul** 指令的精確度更高的精確度，並在後面加上「**新增** 指令」或 **mul**  +  **加入**。</span><span class="sxs-lookup"><span data-stu-id="da922-141">The **mad** instruction can be implemented in hardware as either "fused," which offers higher precision than implementing a **mul** instruction followed by an **add** instruction, or as a **mul** + **add**.</span></span>

<span data-ttu-id="da922-142">如果著色器作者使用 **mad** 內部來計算著色器標示為精確的結果，則會指出硬體使用任何有效的 **mad** 指令實行 (融合或不) ，只要該 **mad** 內建在該硬體上任何著色器中的所有用法都一致。</span><span class="sxs-lookup"><span data-stu-id="da922-142">If shader authors use the **mad** instrinsic to calculate a result that the shader marked as precise, they indicate to the hardware to use any valid implementation of the **mad** instruction (fused or not) as long as the implementation is consistent for all uses of that **mad** intrinsic in any shader on that hardware.</span></span> <span data-ttu-id="da922-143">著色器可以利用原生的 **mad** 指令 (與 **mul**  +  在某些硬體上 **新增**) ，來利用潛在的效能改進。</span><span class="sxs-lookup"><span data-stu-id="da922-143">Shaders can then take advantage of potential performance improvements by using a native **mad** instruction (versus **mul** + **add**) on some hardware.</span></span> <span data-ttu-id="da922-144">執行原生 **mad** 硬體指令的結果可能不會與執行 **mul** 後再執行 **add** 的結果不同。</span><span class="sxs-lookup"><span data-stu-id="da922-144">The result of performing a native **mad** hardware instruction might or might not be different than performing a **mul** followed by an **add**.</span></span> <span data-ttu-id="da922-145">但是，無論結果為何，結果都必須一致，才能讓相同的作業發生在多個著色器或著色器的不同部分中。</span><span class="sxs-lookup"><span data-stu-id="da922-145">However, whatever the result is, the result must be consistent for the same operation to occur in multiple shaders or different parts of a shader.</span></span>

## <a name="see-also"></a><span data-ttu-id="da922-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da922-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da922-147">內建函式</span><span class="sxs-lookup"><span data-stu-id="da922-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="da922-148">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="da922-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




