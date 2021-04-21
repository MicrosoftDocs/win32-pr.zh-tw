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
ms.openlocfilehash: ba12541514c8121d483236afa2163a04bd991288
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804465"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="cba9b-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml) </span><span class="sxs-lookup"><span data-stu-id="cba9b-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="cba9b-104">計算 [批次](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)正規化的反向傳播漸層。</span><span class="sxs-lookup"><span data-stu-id="cba9b-104">Computes backpropagation gradients for [batch normalization](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span></span> <span data-ttu-id="cba9b-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** 會執行多個計算，其詳細說明請見個別的輸出描述。</span><span class="sxs-lookup"><span data-stu-id="cba9b-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** performs multiple computations, which are detailed in the separate output descriptions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cba9b-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="cba9b-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="cba9b-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="cba9b-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cba9b-108">語法</span><span class="sxs-lookup"><span data-stu-id="cba9b-108">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="cba9b-109">成員</span><span class="sxs-lookup"><span data-stu-id="cba9b-109">Members</span></span>

`InputTensor`

<span data-ttu-id="cba9b-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cba9b-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cba9b-111">包含輸入資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="cba9b-111">A tensor containing the input data.</span></span> <span data-ttu-id="cba9b-112">這通常是在轉寄行程中提供作為 *InputTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="cba9b-112">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="cba9b-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cba9b-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cba9b-114">傳入的漸層 tensor。</span><span class="sxs-lookup"><span data-stu-id="cba9b-114">The incoming gradient tensor.</span></span> <span data-ttu-id="cba9b-115">這通常是從上一層的反向傳播輸出中取得。</span><span class="sxs-lookup"><span data-stu-id="cba9b-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="cba9b-116">此 tensor 的維度大小必須與 *InputTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="cba9b-116">This tensor must have the same dimension sizes as *InputTensor*.</span></span>

`MeanTensor`

<span data-ttu-id="cba9b-117">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cba9b-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cba9b-118">包含 mean 資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="cba9b-118">A tensor containing the mean data.</span></span> <span data-ttu-id="cba9b-119">這通常是在轉寄行程中提供作為 *MeanTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="cba9b-119">This is typically the same tensor that was provided as the *MeanTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="cba9b-120">任何大小與 *InputTensor* 相對應的維度大小都不相同的維度，其大小必須為1，才能進行廣播以符合輸入。</span><span class="sxs-lookup"><span data-stu-id="cba9b-120">Any dimensions that don't have the same size as the corresponding dimension of *InputTensor* must have a size of 1 so that they can be broadcast to match the input.</span></span>

<span data-ttu-id="cba9b-121">例如，以下是可接受的大小。</span><span class="sxs-lookup"><span data-stu-id="cba9b-121">For example, the following sizes are acceptable.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

<span data-ttu-id="cba9b-122">下列是錯誤，因為若要進行廣播相容，任何不相符的維度都必須是大小1。</span><span class="sxs-lookup"><span data-stu-id="cba9b-122">The following is an error since, in order to be broadcast compatible, any dimensions that don't match must be size 1.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

<span data-ttu-id="cba9b-123">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cba9b-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cba9b-124">包含變異數資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="cba9b-124">A tensor containing the variance data.</span></span> <span data-ttu-id="cba9b-125">這通常是在轉寄行程中提供作為 *VarianceTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="cba9b-125">This is typically the same tensor that was provided as the *VarianceTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="cba9b-126">此 tensor 的維度大小必須與 *MeanTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="cba9b-126">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`ScaleTensor`

<span data-ttu-id="cba9b-127">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cba9b-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cba9b-128">包含調整資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="cba9b-128">A tensor containing the scale data.</span></span> <span data-ttu-id="cba9b-129">這通常是在轉寄行程中提供作為 *ScaleTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="cba9b-129">This is typically the same tensor that was provided as the *ScaleTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="cba9b-130">此 tensor 的維度大小必須與 *MeanTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="cba9b-130">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`OutputGradientTensor`

<span data-ttu-id="cba9b-131">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cba9b-131">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cba9b-132">輸入中的每個對應值 `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` 。</span><span class="sxs-lookup"><span data-stu-id="cba9b-132">For every corresponding value in the inputs, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))`.</span></span>

<span data-ttu-id="cba9b-133">此 tensor 的維度大小必須與 *InputTensor* / *InputGradientTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="cba9b-133">This tensor must have the same dimension sizes as *InputTensor*/*InputGradientTensor*.</span></span>

`OutputScaleGradientTensor`

<span data-ttu-id="cba9b-134">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cba9b-134">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cba9b-135">此 tensor 的維度大小必須與 *MeanTensor* / *VarianceTensor* / *ScaleTensor '* 相同。</span><span class="sxs-lookup"><span data-stu-id="cba9b-135">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="cba9b-136">下列計算會完成，或輸入中的每個對應值。</span><span class="sxs-lookup"><span data-stu-id="cba9b-136">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

<span data-ttu-id="cba9b-137">`sum`會跨任何需要廣播的維度進行計算。</span><span class="sxs-lookup"><span data-stu-id="cba9b-137">The `sum` is computed across any dimensions that need to be broadcast.</span></span> <span data-ttu-id="cba9b-138">如果不需要廣播，則不需要加總。</span><span class="sxs-lookup"><span data-stu-id="cba9b-138">If there is no broadcast needed, then no sum is needed.</span></span>

<span data-ttu-id="cba9b-139">以下為範例。</span><span class="sxs-lookup"><span data-stu-id="cba9b-139">Here's an example.</span></span>

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

<span data-ttu-id="cba9b-140">元素 [0， **0**，0，0] `OutputScaleGradientTensor` 是 `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` 所有 90 (3 \* 5 \* 6) 元素 [[0，2]， **0**，[0，4]，[0，5]] 的總和。</span><span class="sxs-lookup"><span data-stu-id="cba9b-140">Element [0, **0**, 0, 0] of `OutputScaleGradientTensor` is the sum of `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` for all 90 (3\*5\*6) elements [[0,2], **0**, [0,4], [0,5]].</span></span>

`OutputBiasGradientTensor`

<span data-ttu-id="cba9b-141">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cba9b-141">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cba9b-142">此 tensor 的維度大小必須與 *MeanTensor* / *VarianceTensor* / *ScaleTensor '* 相同。</span><span class="sxs-lookup"><span data-stu-id="cba9b-142">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="cba9b-143">下列計算會完成，或輸入中的每個對應值。</span><span class="sxs-lookup"><span data-stu-id="cba9b-143">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputBiasGradient = sum(InputGradient)`  

<span data-ttu-id="cba9b-144">`sum`會跨任何需要廣播的維度來計算 (請參閱 *OutputScaleGradientTensor*) 的範例。</span><span class="sxs-lookup"><span data-stu-id="cba9b-144">The `sum` is computed across any dimensions that need to be broadcast (see the example for *OutputScaleGradientTensor*).</span></span> <span data-ttu-id="cba9b-145">如果不需要廣播，則不需要加總。</span><span class="sxs-lookup"><span data-stu-id="cba9b-145">If there is no broadcast needed, then no sum is needed.</span></span>

`Epsilon`

<span data-ttu-id="cba9b-146">類型： **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cba9b-146">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="cba9b-147">加入至變異數的小值，以避免零。</span><span class="sxs-lookup"><span data-stu-id="cba9b-147">A small value added to the variance to avoid zero.</span></span>

## <a name="availability"></a><span data-ttu-id="cba9b-148">可用性</span><span class="sxs-lookup"><span data-stu-id="cba9b-148">Availability</span></span>
<span data-ttu-id="cba9b-149">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。</span><span class="sxs-lookup"><span data-stu-id="cba9b-149">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cba9b-150">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="cba9b-150">Tensor constraints</span></span>
<span data-ttu-id="cba9b-151">*InputGradientTensor*、 *InputTensor*、 *MeanTensor*、 *OutputBiasGradientTensor*、 *OutputGradientTensor*、 *OutputScaleGradientTensor*、 *ScaleTensor* 和 *VarianceTensor* 必須有相同的 *資料類型* 和 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="cba9b-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cba9b-152">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="cba9b-152">Tensor support</span></span>
| <span data-ttu-id="cba9b-153">張</span><span class="sxs-lookup"><span data-stu-id="cba9b-153">Tensor</span></span> | <span data-ttu-id="cba9b-154">類型</span><span class="sxs-lookup"><span data-stu-id="cba9b-154">Kind</span></span> | <span data-ttu-id="cba9b-155">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="cba9b-155">Supported dimension counts</span></span> | <span data-ttu-id="cba9b-156">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="cba9b-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cba9b-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cba9b-157">InputTensor</span></span> | <span data-ttu-id="cba9b-158">輸入</span><span class="sxs-lookup"><span data-stu-id="cba9b-158">Input</span></span> | <span data-ttu-id="cba9b-159">1至8</span><span class="sxs-lookup"><span data-stu-id="cba9b-159">1 to 8</span></span> | <span data-ttu-id="cba9b-160">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cba9b-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cba9b-161">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="cba9b-161">InputGradientTensor</span></span> | <span data-ttu-id="cba9b-162">輸入</span><span class="sxs-lookup"><span data-stu-id="cba9b-162">Input</span></span> | <span data-ttu-id="cba9b-163">1至8</span><span class="sxs-lookup"><span data-stu-id="cba9b-163">1 to 8</span></span> | <span data-ttu-id="cba9b-164">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cba9b-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cba9b-165">MeanTensor</span><span class="sxs-lookup"><span data-stu-id="cba9b-165">MeanTensor</span></span> | <span data-ttu-id="cba9b-166">輸入</span><span class="sxs-lookup"><span data-stu-id="cba9b-166">Input</span></span> | <span data-ttu-id="cba9b-167">1至8</span><span class="sxs-lookup"><span data-stu-id="cba9b-167">1 to 8</span></span> | <span data-ttu-id="cba9b-168">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cba9b-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cba9b-169">VarianceTensor</span><span class="sxs-lookup"><span data-stu-id="cba9b-169">VarianceTensor</span></span> | <span data-ttu-id="cba9b-170">輸入</span><span class="sxs-lookup"><span data-stu-id="cba9b-170">Input</span></span> | <span data-ttu-id="cba9b-171">1至8</span><span class="sxs-lookup"><span data-stu-id="cba9b-171">1 to 8</span></span> | <span data-ttu-id="cba9b-172">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cba9b-172">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cba9b-173">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cba9b-173">ScaleTensor</span></span> | <span data-ttu-id="cba9b-174">輸入</span><span class="sxs-lookup"><span data-stu-id="cba9b-174">Input</span></span> | <span data-ttu-id="cba9b-175">1至8</span><span class="sxs-lookup"><span data-stu-id="cba9b-175">1 to 8</span></span> | <span data-ttu-id="cba9b-176">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cba9b-176">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cba9b-177">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="cba9b-177">OutputGradientTensor</span></span> | <span data-ttu-id="cba9b-178">輸出</span><span class="sxs-lookup"><span data-stu-id="cba9b-178">Output</span></span> | <span data-ttu-id="cba9b-179">1至8</span><span class="sxs-lookup"><span data-stu-id="cba9b-179">1 to 8</span></span> | <span data-ttu-id="cba9b-180">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cba9b-180">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cba9b-181">OutputScaleGradientTensor</span><span class="sxs-lookup"><span data-stu-id="cba9b-181">OutputScaleGradientTensor</span></span> | <span data-ttu-id="cba9b-182">輸出</span><span class="sxs-lookup"><span data-stu-id="cba9b-182">Output</span></span> | <span data-ttu-id="cba9b-183">1至8</span><span class="sxs-lookup"><span data-stu-id="cba9b-183">1 to 8</span></span> | <span data-ttu-id="cba9b-184">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cba9b-184">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cba9b-185">OutputBiasGradientTensor</span><span class="sxs-lookup"><span data-stu-id="cba9b-185">OutputBiasGradientTensor</span></span> | <span data-ttu-id="cba9b-186">輸出</span><span class="sxs-lookup"><span data-stu-id="cba9b-186">Output</span></span> | <span data-ttu-id="cba9b-187">1至8</span><span class="sxs-lookup"><span data-stu-id="cba9b-187">1 to 8</span></span> | <span data-ttu-id="cba9b-188">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cba9b-188">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="cba9b-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="cba9b-189">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cba9b-190">**標頭**</span><span class="sxs-lookup"><span data-stu-id="cba9b-190">**Header**</span></span> | <span data-ttu-id="cba9b-191">directml。h</span><span class="sxs-lookup"><span data-stu-id="cba9b-191">directml.h</span></span> |
