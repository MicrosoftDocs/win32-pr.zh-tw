---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: 計算 [批次](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)正規化的反向傳播漸層。
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550433"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="240ea-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml) </span><span class="sxs-lookup"><span data-stu-id="240ea-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="240ea-104">計算 [批次](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)正規化的反向傳播漸層。</span><span class="sxs-lookup"><span data-stu-id="240ea-104">Computes backpropagation gradients for [batch normalization](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span></span> <span data-ttu-id="240ea-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** 會執行多個計算，其詳細說明請見個別的輸出描述。</span><span class="sxs-lookup"><span data-stu-id="240ea-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** performs multiple computations, which are detailed in the separate output descriptions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="240ea-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="240ea-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="240ea-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="240ea-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="240ea-108">語法</span><span class="sxs-lookup"><span data-stu-id="240ea-108">Syntax</span></span>
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="240ea-109">成員</span><span class="sxs-lookup"><span data-stu-id="240ea-109">Members</span></span>

`InputTensor`

<span data-ttu-id="240ea-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="240ea-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="240ea-111">包含輸入資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="240ea-111">A tensor containing the input data.</span></span> <span data-ttu-id="240ea-112">這通常是在轉寄行程中提供作為 *InputTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="240ea-112">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="240ea-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="240ea-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="240ea-114">傳入的漸層 tensor。</span><span class="sxs-lookup"><span data-stu-id="240ea-114">The incoming gradient tensor.</span></span> <span data-ttu-id="240ea-115">這通常是從上一層的反向傳播輸出中取得。</span><span class="sxs-lookup"><span data-stu-id="240ea-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="240ea-116">此 tensor 的維度大小必須與 *InputTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="240ea-116">This tensor must have the same dimension sizes as *InputTensor*.</span></span>

`MeanTensor`

<span data-ttu-id="240ea-117">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="240ea-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="240ea-118">包含 mean 資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="240ea-118">A tensor containing the mean data.</span></span> <span data-ttu-id="240ea-119">這通常是在轉寄行程中提供作為 *MeanTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="240ea-119">This is typically the same tensor that was provided as the *MeanTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="240ea-120">任何大小與 *InputTensor* 相對應的維度大小都不相同的維度，其大小必須為1，才能進行廣播以符合輸入。</span><span class="sxs-lookup"><span data-stu-id="240ea-120">Any dimensions that don't have the same size as the corresponding dimension of *InputTensor* must have a size of 1 so that they can be broadcast to match the input.</span></span>

<span data-ttu-id="240ea-121">例如，以下是可接受的大小。</span><span class="sxs-lookup"><span data-stu-id="240ea-121">For example, the following sizes are acceptable.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

<span data-ttu-id="240ea-122">下列是錯誤，因為若要進行廣播相容，任何不相符的維度都必須是大小1。</span><span class="sxs-lookup"><span data-stu-id="240ea-122">The following is an error since, in order to be broadcast compatible, any dimensions that don't match must be size 1.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

<span data-ttu-id="240ea-123">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="240ea-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="240ea-124">包含變異數資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="240ea-124">A tensor containing the variance data.</span></span> <span data-ttu-id="240ea-125">這通常是在轉寄行程中提供作為 *VarianceTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="240ea-125">This is typically the same tensor that was provided as the *VarianceTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="240ea-126">此 tensor 的維度大小必須與 *MeanTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="240ea-126">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`ScaleTensor`

<span data-ttu-id="240ea-127">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="240ea-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="240ea-128">包含調整資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="240ea-128">A tensor containing the scale data.</span></span> <span data-ttu-id="240ea-129">這通常是在轉寄行程中提供作為 *ScaleTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="240ea-129">This is typically the same tensor that was provided as the *ScaleTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="240ea-130">此 tensor 的維度大小必須與 *MeanTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="240ea-130">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`OutputGradientTensor`

<span data-ttu-id="240ea-131">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="240ea-131">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="240ea-132">輸入中的每個對應值 `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` 。</span><span class="sxs-lookup"><span data-stu-id="240ea-132">For every corresponding value in the inputs, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))`.</span></span>

<span data-ttu-id="240ea-133">此 tensor 的維度大小必須與 *InputTensor* / *InputGradientTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="240ea-133">This tensor must have the same dimension sizes as *InputTensor*/*InputGradientTensor*.</span></span>

`OutputScaleGradientTensor`

<span data-ttu-id="240ea-134">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="240ea-134">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="240ea-135">此 tensor 的維度大小必須與 *MeanTensor* / *VarianceTensor* / *ScaleTensor '* 相同。</span><span class="sxs-lookup"><span data-stu-id="240ea-135">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="240ea-136">下列計算會完成，或輸入中的每個對應值。</span><span class="sxs-lookup"><span data-stu-id="240ea-136">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

<span data-ttu-id="240ea-137">`sum`會跨任何需要廣播的維度進行計算。</span><span class="sxs-lookup"><span data-stu-id="240ea-137">The `sum` is computed across any dimensions that need to be broadcast.</span></span> <span data-ttu-id="240ea-138">如果不需要廣播，則不需要加總。</span><span class="sxs-lookup"><span data-stu-id="240ea-138">If there is no broadcast needed, then no sum is needed.</span></span>

<span data-ttu-id="240ea-139">以下為範例。</span><span class="sxs-lookup"><span data-stu-id="240ea-139">Here's an example.</span></span>

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

<span data-ttu-id="240ea-140">元素 [0， **0**，0，0] `OutputScaleGradientTensor` 是 `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` 所有 90 (3 \* 5 \* 6) 元素 [[0，2]， **0**，[0，4]，[0，5]] 的總和。</span><span class="sxs-lookup"><span data-stu-id="240ea-140">Element [0, **0**, 0, 0] of `OutputScaleGradientTensor` is the sum of `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` for all 90 (3\*5\*6) elements [[0,2], **0**, [0,4], [0,5]].</span></span>

`OutputBiasGradientTensor`

<span data-ttu-id="240ea-141">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="240ea-141">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="240ea-142">此 tensor 的維度大小必須與 *MeanTensor* / *VarianceTensor* / *ScaleTensor '* 相同。</span><span class="sxs-lookup"><span data-stu-id="240ea-142">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="240ea-143">下列計算會完成，或輸入中的每個對應值。</span><span class="sxs-lookup"><span data-stu-id="240ea-143">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputBiasGradient = sum(InputGradient)`  

<span data-ttu-id="240ea-144">`sum`會跨任何需要廣播的維度來計算 (請參閱 *OutputScaleGradientTensor*) 的範例。</span><span class="sxs-lookup"><span data-stu-id="240ea-144">The `sum` is computed across any dimensions that need to be broadcast (see the example for *OutputScaleGradientTensor*).</span></span> <span data-ttu-id="240ea-145">如果不需要廣播，則不需要加總。</span><span class="sxs-lookup"><span data-stu-id="240ea-145">If there is no broadcast needed, then no sum is needed.</span></span>

`Epsilon`

<span data-ttu-id="240ea-146">類型： **[FLOAT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="240ea-146">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="240ea-147">加入至變異數的小值，以避免零。</span><span class="sxs-lookup"><span data-stu-id="240ea-147">A small value added to the variance to avoid zero.</span></span>

## <a name="availability"></a><span data-ttu-id="240ea-148">可用性</span><span class="sxs-lookup"><span data-stu-id="240ea-148">Availability</span></span>
<span data-ttu-id="240ea-149">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。</span><span class="sxs-lookup"><span data-stu-id="240ea-149">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="240ea-150">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="240ea-150">Tensor constraints</span></span>
<span data-ttu-id="240ea-151">*InputGradientTensor*、 *InputTensor*、 *MeanTensor*、 *OutputBiasGradientTensor*、 *OutputGradientTensor*、 *OutputScaleGradientTensor*、 *ScaleTensor* 和 *VarianceTensor* 必須有相同的 *資料類型* 和 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="240ea-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="240ea-152">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="240ea-152">Tensor support</span></span>
| <span data-ttu-id="240ea-153">張</span><span class="sxs-lookup"><span data-stu-id="240ea-153">Tensor</span></span> | <span data-ttu-id="240ea-154">種類</span><span class="sxs-lookup"><span data-stu-id="240ea-154">Kind</span></span> | <span data-ttu-id="240ea-155">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="240ea-155">Supported dimension counts</span></span> | <span data-ttu-id="240ea-156">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="240ea-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="240ea-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="240ea-157">InputTensor</span></span> | <span data-ttu-id="240ea-158">輸入</span><span class="sxs-lookup"><span data-stu-id="240ea-158">Input</span></span> | <span data-ttu-id="240ea-159">1至8</span><span class="sxs-lookup"><span data-stu-id="240ea-159">1 to 8</span></span> | <span data-ttu-id="240ea-160">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="240ea-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="240ea-161">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="240ea-161">InputGradientTensor</span></span> | <span data-ttu-id="240ea-162">輸入</span><span class="sxs-lookup"><span data-stu-id="240ea-162">Input</span></span> | <span data-ttu-id="240ea-163">1至8</span><span class="sxs-lookup"><span data-stu-id="240ea-163">1 to 8</span></span> | <span data-ttu-id="240ea-164">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="240ea-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="240ea-165">MeanTensor</span><span class="sxs-lookup"><span data-stu-id="240ea-165">MeanTensor</span></span> | <span data-ttu-id="240ea-166">輸入</span><span class="sxs-lookup"><span data-stu-id="240ea-166">Input</span></span> | <span data-ttu-id="240ea-167">1至8</span><span class="sxs-lookup"><span data-stu-id="240ea-167">1 to 8</span></span> | <span data-ttu-id="240ea-168">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="240ea-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="240ea-169">VarianceTensor</span><span class="sxs-lookup"><span data-stu-id="240ea-169">VarianceTensor</span></span> | <span data-ttu-id="240ea-170">輸入</span><span class="sxs-lookup"><span data-stu-id="240ea-170">Input</span></span> | <span data-ttu-id="240ea-171">1至8</span><span class="sxs-lookup"><span data-stu-id="240ea-171">1 to 8</span></span> | <span data-ttu-id="240ea-172">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="240ea-172">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="240ea-173">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="240ea-173">ScaleTensor</span></span> | <span data-ttu-id="240ea-174">輸入</span><span class="sxs-lookup"><span data-stu-id="240ea-174">Input</span></span> | <span data-ttu-id="240ea-175">1至8</span><span class="sxs-lookup"><span data-stu-id="240ea-175">1 to 8</span></span> | <span data-ttu-id="240ea-176">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="240ea-176">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="240ea-177">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="240ea-177">OutputGradientTensor</span></span> | <span data-ttu-id="240ea-178">輸出</span><span class="sxs-lookup"><span data-stu-id="240ea-178">Output</span></span> | <span data-ttu-id="240ea-179">1至8</span><span class="sxs-lookup"><span data-stu-id="240ea-179">1 to 8</span></span> | <span data-ttu-id="240ea-180">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="240ea-180">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="240ea-181">OutputScaleGradientTensor</span><span class="sxs-lookup"><span data-stu-id="240ea-181">OutputScaleGradientTensor</span></span> | <span data-ttu-id="240ea-182">輸出</span><span class="sxs-lookup"><span data-stu-id="240ea-182">Output</span></span> | <span data-ttu-id="240ea-183">1至8</span><span class="sxs-lookup"><span data-stu-id="240ea-183">1 to 8</span></span> | <span data-ttu-id="240ea-184">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="240ea-184">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="240ea-185">OutputBiasGradientTensor</span><span class="sxs-lookup"><span data-stu-id="240ea-185">OutputBiasGradientTensor</span></span> | <span data-ttu-id="240ea-186">輸出</span><span class="sxs-lookup"><span data-stu-id="240ea-186">Output</span></span> | <span data-ttu-id="240ea-187">1至8</span><span class="sxs-lookup"><span data-stu-id="240ea-187">1 to 8</span></span> | <span data-ttu-id="240ea-188">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="240ea-188">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="240ea-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="240ea-189">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="240ea-190">**標頭**</span><span class="sxs-lookup"><span data-stu-id="240ea-190">**Header**</span></span> | <span data-ttu-id="240ea-191">directml。h</span><span class="sxs-lookup"><span data-stu-id="240ea-191">directml.h</span></span> |