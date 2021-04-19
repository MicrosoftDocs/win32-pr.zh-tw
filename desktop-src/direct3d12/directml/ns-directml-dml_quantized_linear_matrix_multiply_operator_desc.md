---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: 在量化資料上執行矩陣乘法函數。 這個運算子在數學上相當於 dequantizing 輸入，然後執行矩陣相乘，然後量化輸出。
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: d0b20a37bca6ddf6083b116b53290a6b6b2084f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106997308"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="cace5-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="cace5-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="cace5-105">在量化資料上執行矩陣乘法函數。</span><span class="sxs-lookup"><span data-stu-id="cace5-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="cace5-106">這個運算子在數學上相當於 dequantizing 輸入，然後執行矩陣相乘，然後量化輸出。</span><span class="sxs-lookup"><span data-stu-id="cace5-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="cace5-107">此運算子要求矩陣乘以輸入張量為4D，格式為 `{ BatchCount, ChannelCount, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="cace5-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="cace5-108">矩陣乘法運算子將會執行 BatchCount \* ChannelCount number of 獨立矩陣乘法運算。</span><span class="sxs-lookup"><span data-stu-id="cace5-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="cace5-109">例如，如果 *ATensor* 的 *大小* 為， `{ BatchCount, ChannelCount, M, K }` 且 *BTensor* *的大小* 為 `{ BatchCount, ChannelCount, K, N }` ，而 *OutputTensor* 的大小為， `{ BatchCount, ChannelCount, M, N }` 則矩陣乘法運算子將會執行 BatchCount \* ChannelCount 獨立矩陣乘法運算的維度 {M，K} x {K，n} = {M，n}。</span><span class="sxs-lookup"><span data-stu-id="cace5-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="cace5-110">Dequantize 函式</span><span class="sxs-lookup"><span data-stu-id="cace5-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="cace5-111">量化函式</span><span class="sxs-lookup"><span data-stu-id="cace5-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="cace5-112">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="cace5-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="cace5-113">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="cace5-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cace5-114">語法</span><span class="sxs-lookup"><span data-stu-id="cace5-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="cace5-115">成員</span><span class="sxs-lookup"><span data-stu-id="cace5-115">Members</span></span>

`ATensor`

<span data-ttu-id="cace5-116">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cace5-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cace5-117">包含資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="cace5-117">A tensor containing the A data.</span></span> <span data-ttu-id="cace5-118">此 tensor 的維度應該是 `{ BatchCount, ChannelCount, M, K }` 。</span><span class="sxs-lookup"><span data-stu-id="cace5-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="cace5-119">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cace5-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cace5-120">包含 ATensor 規模資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="cace5-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="cace5-121">`AScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或需要個別的資料列量化，則預期的維度為 `{ 1, 1, M, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="cace5-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="cace5-122">這些刻度值是用來 dequantizing 值。</span><span class="sxs-lookup"><span data-stu-id="cace5-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="cace5-123">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cace5-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cace5-124">包含 *ATensor* 零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="cace5-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="cace5-125">`{ 1, 1, 1, 1 }`如果需要每個 tensor 量化，或需要個別的資料列量化，AZeroPointTensor 的預期維度是 `{ 1, 1, M, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="cace5-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="cace5-126">這些零點值是用來 dequantizing ATensor 值。</span><span class="sxs-lookup"><span data-stu-id="cace5-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="cace5-127">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cace5-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cace5-128">包含 B 資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="cace5-128">A tensor containing the B data.</span></span> <span data-ttu-id="cace5-129">此 tensor 的維度應該是 `{ BatchCount, ChannelCount, K, N }` 。</span><span class="sxs-lookup"><span data-stu-id="cace5-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="cace5-130">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cace5-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cace5-131">包含 *BTensor* 規模資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="cace5-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="cace5-132">`BScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, 1, N }` 每個資料行的量化是必要的，則預期的維度為。</span><span class="sxs-lookup"><span data-stu-id="cace5-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="cace5-133">這些縮放值會用來 dequantizing *BTensor* 值。</span><span class="sxs-lookup"><span data-stu-id="cace5-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="cace5-134">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cace5-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cace5-135">包含 *BTensor* 零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="cace5-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="cace5-136">`BZeroPointTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, 1, N }` 每個資料行的量化是必要的，則預期的維度為。</span><span class="sxs-lookup"><span data-stu-id="cace5-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="cace5-137">這些零點值是用來 dequantizing *BTensor* 值。</span><span class="sxs-lookup"><span data-stu-id="cace5-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="cace5-138">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cace5-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cace5-139">包含篩選調整資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="cace5-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="cace5-140">`OutputScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或需要個別的資料列量化，則預期的維度為 `{ 1, 1, M, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="cace5-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="cace5-141">此比例值是用來 dequantizing 篩選值。</span><span class="sxs-lookup"><span data-stu-id="cace5-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="cace5-142">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cace5-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cace5-143">包含篩選零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="cace5-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="cace5-144">`OutputZeroPointTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, M, 1 }` 每個資料列的量化是必要的，則預期的維度為。</span><span class="sxs-lookup"><span data-stu-id="cace5-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="cace5-145">這個零點值是用來 dequantizing 篩選值。</span><span class="sxs-lookup"><span data-stu-id="cace5-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="cace5-146">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cace5-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cace5-147">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="cace5-147">A tensor to write the results to.</span></span> <span data-ttu-id="cace5-148">這個 tensor 的維度是 `{ BatchCount, ChannelCount, M, N }` 。</span><span class="sxs-lookup"><span data-stu-id="cace5-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="cace5-149">可用性</span><span class="sxs-lookup"><span data-stu-id="cace5-149">Availability</span></span>
<span data-ttu-id="cace5-150">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="cace5-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cace5-151">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="cace5-151">Tensor constraints</span></span>
* <span data-ttu-id="cace5-152">*ATensor* 和 `AZeroPointTensor` 必須具有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="cace5-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="cace5-153">*BTensor* 和 `BZeroPointTensor` 必須具有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="cace5-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="cace5-154">*OutputTensor* 和 `OutputZeroPointTensor` 必須具有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="cace5-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cace5-155">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="cace5-155">Tensor support</span></span>
| <span data-ttu-id="cace5-156">張</span><span class="sxs-lookup"><span data-stu-id="cace5-156">Tensor</span></span> | <span data-ttu-id="cace5-157">類型</span><span class="sxs-lookup"><span data-stu-id="cace5-157">Kind</span></span> | <span data-ttu-id="cace5-158">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="cace5-158">Supported dimension counts</span></span> | <span data-ttu-id="cace5-159">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="cace5-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cace5-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="cace5-160">ATensor</span></span> | <span data-ttu-id="cace5-161">輸入</span><span class="sxs-lookup"><span data-stu-id="cace5-161">Input</span></span> | <span data-ttu-id="cace5-162">4</span><span class="sxs-lookup"><span data-stu-id="cace5-162">4</span></span> | <span data-ttu-id="cace5-163">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="cace5-163">INT8, UINT8</span></span> |
| <span data-ttu-id="cace5-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cace5-164">AScaleTensor</span></span> | <span data-ttu-id="cace5-165">輸入</span><span class="sxs-lookup"><span data-stu-id="cace5-165">Input</span></span> | <span data-ttu-id="cace5-166">4</span><span class="sxs-lookup"><span data-stu-id="cace5-166">4</span></span> | <span data-ttu-id="cace5-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cace5-167">FLOAT32</span></span> |
| <span data-ttu-id="cace5-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cace5-168">AZeroPointTensor</span></span> | <span data-ttu-id="cace5-169">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="cace5-169">Optional input</span></span> | <span data-ttu-id="cace5-170">4</span><span class="sxs-lookup"><span data-stu-id="cace5-170">4</span></span> | <span data-ttu-id="cace5-171">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="cace5-171">INT8, UINT8</span></span> |
| <span data-ttu-id="cace5-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="cace5-172">BTensor</span></span> | <span data-ttu-id="cace5-173">輸入</span><span class="sxs-lookup"><span data-stu-id="cace5-173">Input</span></span> | <span data-ttu-id="cace5-174">4</span><span class="sxs-lookup"><span data-stu-id="cace5-174">4</span></span> | <span data-ttu-id="cace5-175">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="cace5-175">INT8, UINT8</span></span> |
| <span data-ttu-id="cace5-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cace5-176">BScaleTensor</span></span> | <span data-ttu-id="cace5-177">輸入</span><span class="sxs-lookup"><span data-stu-id="cace5-177">Input</span></span> | <span data-ttu-id="cace5-178">4</span><span class="sxs-lookup"><span data-stu-id="cace5-178">4</span></span> | <span data-ttu-id="cace5-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cace5-179">FLOAT32</span></span> |
| <span data-ttu-id="cace5-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cace5-180">BZeroPointTensor</span></span> | <span data-ttu-id="cace5-181">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="cace5-181">Optional input</span></span> | <span data-ttu-id="cace5-182">4</span><span class="sxs-lookup"><span data-stu-id="cace5-182">4</span></span> | <span data-ttu-id="cace5-183">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="cace5-183">INT8, UINT8</span></span> |
| <span data-ttu-id="cace5-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cace5-184">OutputScaleTensor</span></span> | <span data-ttu-id="cace5-185">輸入</span><span class="sxs-lookup"><span data-stu-id="cace5-185">Input</span></span> | <span data-ttu-id="cace5-186">4</span><span class="sxs-lookup"><span data-stu-id="cace5-186">4</span></span> | <span data-ttu-id="cace5-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cace5-187">FLOAT32</span></span> |
| <span data-ttu-id="cace5-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cace5-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="cace5-189">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="cace5-189">Optional input</span></span> | <span data-ttu-id="cace5-190">4</span><span class="sxs-lookup"><span data-stu-id="cace5-190">4</span></span> | <span data-ttu-id="cace5-191">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="cace5-191">INT8, UINT8</span></span> |
| <span data-ttu-id="cace5-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cace5-192">OutputTensor</span></span> | <span data-ttu-id="cace5-193">輸出</span><span class="sxs-lookup"><span data-stu-id="cace5-193">Output</span></span> | <span data-ttu-id="cace5-194">4</span><span class="sxs-lookup"><span data-stu-id="cace5-194">4</span></span> | <span data-ttu-id="cace5-195">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="cace5-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="cace5-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="cace5-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cace5-197">**標頭**</span><span class="sxs-lookup"><span data-stu-id="cace5-197">**Header**</span></span> | <span data-ttu-id="cace5-198">directml。h</span><span class="sxs-lookup"><span data-stu-id="cace5-198">directml.h</span></span> |