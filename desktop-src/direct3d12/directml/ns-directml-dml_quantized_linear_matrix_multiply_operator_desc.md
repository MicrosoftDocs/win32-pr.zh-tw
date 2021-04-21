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
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803570"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="0da6c-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="0da6c-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="0da6c-105">在量化資料上執行矩陣乘法函數。</span><span class="sxs-lookup"><span data-stu-id="0da6c-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="0da6c-106">這個運算子在數學上相當於 dequantizing 輸入，然後執行矩陣相乘，然後量化輸出。</span><span class="sxs-lookup"><span data-stu-id="0da6c-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="0da6c-107">此運算子要求矩陣乘以輸入張量為4D，格式為 `{ BatchCount, ChannelCount, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="0da6c-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="0da6c-108">矩陣乘法運算子將會執行 BatchCount \* ChannelCount number of 獨立矩陣乘法運算。</span><span class="sxs-lookup"><span data-stu-id="0da6c-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="0da6c-109">例如，如果 *ATensor* 的 *大小* 為， `{ BatchCount, ChannelCount, M, K }` 且 *BTensor* *的大小* 為 `{ BatchCount, ChannelCount, K, N }` ，而 *OutputTensor* 的大小為， `{ BatchCount, ChannelCount, M, N }` 則矩陣乘法運算子將會執行 BatchCount \* ChannelCount 獨立矩陣乘法運算的維度 {M，K} x {K，n} = {M，n}。</span><span class="sxs-lookup"><span data-stu-id="0da6c-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="0da6c-110">Dequantize 函式</span><span class="sxs-lookup"><span data-stu-id="0da6c-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="0da6c-111">量化函式</span><span class="sxs-lookup"><span data-stu-id="0da6c-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="0da6c-112">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="0da6c-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="0da6c-113">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="0da6c-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0da6c-114">語法</span><span class="sxs-lookup"><span data-stu-id="0da6c-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="0da6c-115">成員</span><span class="sxs-lookup"><span data-stu-id="0da6c-115">Members</span></span>

`ATensor`

<span data-ttu-id="0da6c-116">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0da6c-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0da6c-117">包含資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="0da6c-117">A tensor containing the A data.</span></span> <span data-ttu-id="0da6c-118">此 tensor 的維度應該是 `{ BatchCount, ChannelCount, M, K }` 。</span><span class="sxs-lookup"><span data-stu-id="0da6c-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="0da6c-119">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0da6c-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0da6c-120">包含 ATensor 規模資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="0da6c-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="0da6c-121">`AScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或需要個別的資料列量化，則預期的維度為 `{ 1, 1, M, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="0da6c-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="0da6c-122">這些刻度值是用來 dequantizing 值。</span><span class="sxs-lookup"><span data-stu-id="0da6c-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="0da6c-123">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0da6c-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0da6c-124">包含 *ATensor* 零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="0da6c-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="0da6c-125">`{ 1, 1, 1, 1 }`如果需要每個 tensor 量化，或需要個別的資料列量化，AZeroPointTensor 的預期維度是 `{ 1, 1, M, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="0da6c-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="0da6c-126">這些零點值是用來 dequantizing ATensor 值。</span><span class="sxs-lookup"><span data-stu-id="0da6c-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="0da6c-127">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0da6c-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0da6c-128">包含 B 資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="0da6c-128">A tensor containing the B data.</span></span> <span data-ttu-id="0da6c-129">此 tensor 的維度應該是 `{ BatchCount, ChannelCount, K, N }` 。</span><span class="sxs-lookup"><span data-stu-id="0da6c-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="0da6c-130">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0da6c-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0da6c-131">包含 *BTensor* 規模資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="0da6c-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="0da6c-132">`BScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, 1, N }` 每個資料行的量化是必要的，則預期的維度為。</span><span class="sxs-lookup"><span data-stu-id="0da6c-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="0da6c-133">這些縮放值會用來 dequantizing *BTensor* 值。</span><span class="sxs-lookup"><span data-stu-id="0da6c-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="0da6c-134">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0da6c-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0da6c-135">包含 *BTensor* 零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="0da6c-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="0da6c-136">`BZeroPointTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, 1, N }` 每個資料行的量化是必要的，則預期的維度為。</span><span class="sxs-lookup"><span data-stu-id="0da6c-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="0da6c-137">這些零點值是用來 dequantizing *BTensor* 值。</span><span class="sxs-lookup"><span data-stu-id="0da6c-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="0da6c-138">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0da6c-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0da6c-139">包含篩選調整資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="0da6c-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="0da6c-140">`OutputScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或需要個別的資料列量化，則預期的維度為 `{ 1, 1, M, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="0da6c-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="0da6c-141">此比例值是用來 dequantizing 篩選值。</span><span class="sxs-lookup"><span data-stu-id="0da6c-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="0da6c-142">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0da6c-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0da6c-143">包含篩選零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="0da6c-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="0da6c-144">`OutputZeroPointTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, M, 1 }` 每個資料列的量化是必要的，則預期的維度為。</span><span class="sxs-lookup"><span data-stu-id="0da6c-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="0da6c-145">這個零點值是用來 dequantizing 篩選值。</span><span class="sxs-lookup"><span data-stu-id="0da6c-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="0da6c-146">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0da6c-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0da6c-147">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="0da6c-147">A tensor to write the results to.</span></span> <span data-ttu-id="0da6c-148">這個 tensor 的維度是 `{ BatchCount, ChannelCount, M, N }` 。</span><span class="sxs-lookup"><span data-stu-id="0da6c-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="0da6c-149">可用性</span><span class="sxs-lookup"><span data-stu-id="0da6c-149">Availability</span></span>
<span data-ttu-id="0da6c-150">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="0da6c-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="0da6c-151">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="0da6c-151">Tensor constraints</span></span>
* <span data-ttu-id="0da6c-152">*ATensor* 和 `AZeroPointTensor` 必須具有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="0da6c-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="0da6c-153">*BTensor* 和 `BZeroPointTensor` 必須具有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="0da6c-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="0da6c-154">*OutputTensor* 和 `OutputZeroPointTensor` 必須具有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="0da6c-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="0da6c-155">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="0da6c-155">Tensor support</span></span>
| <span data-ttu-id="0da6c-156">張</span><span class="sxs-lookup"><span data-stu-id="0da6c-156">Tensor</span></span> | <span data-ttu-id="0da6c-157">類型</span><span class="sxs-lookup"><span data-stu-id="0da6c-157">Kind</span></span> | <span data-ttu-id="0da6c-158">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="0da6c-158">Supported dimension counts</span></span> | <span data-ttu-id="0da6c-159">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="0da6c-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0da6c-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="0da6c-160">ATensor</span></span> | <span data-ttu-id="0da6c-161">輸入</span><span class="sxs-lookup"><span data-stu-id="0da6c-161">Input</span></span> | <span data-ttu-id="0da6c-162">4</span><span class="sxs-lookup"><span data-stu-id="0da6c-162">4</span></span> | <span data-ttu-id="0da6c-163">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="0da6c-163">INT8, UINT8</span></span> |
| <span data-ttu-id="0da6c-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="0da6c-164">AScaleTensor</span></span> | <span data-ttu-id="0da6c-165">輸入</span><span class="sxs-lookup"><span data-stu-id="0da6c-165">Input</span></span> | <span data-ttu-id="0da6c-166">4</span><span class="sxs-lookup"><span data-stu-id="0da6c-166">4</span></span> | <span data-ttu-id="0da6c-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="0da6c-167">FLOAT32</span></span> |
| <span data-ttu-id="0da6c-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="0da6c-168">AZeroPointTensor</span></span> | <span data-ttu-id="0da6c-169">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="0da6c-169">Optional input</span></span> | <span data-ttu-id="0da6c-170">4</span><span class="sxs-lookup"><span data-stu-id="0da6c-170">4</span></span> | <span data-ttu-id="0da6c-171">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="0da6c-171">INT8, UINT8</span></span> |
| <span data-ttu-id="0da6c-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="0da6c-172">BTensor</span></span> | <span data-ttu-id="0da6c-173">輸入</span><span class="sxs-lookup"><span data-stu-id="0da6c-173">Input</span></span> | <span data-ttu-id="0da6c-174">4</span><span class="sxs-lookup"><span data-stu-id="0da6c-174">4</span></span> | <span data-ttu-id="0da6c-175">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="0da6c-175">INT8, UINT8</span></span> |
| <span data-ttu-id="0da6c-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="0da6c-176">BScaleTensor</span></span> | <span data-ttu-id="0da6c-177">輸入</span><span class="sxs-lookup"><span data-stu-id="0da6c-177">Input</span></span> | <span data-ttu-id="0da6c-178">4</span><span class="sxs-lookup"><span data-stu-id="0da6c-178">4</span></span> | <span data-ttu-id="0da6c-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="0da6c-179">FLOAT32</span></span> |
| <span data-ttu-id="0da6c-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="0da6c-180">BZeroPointTensor</span></span> | <span data-ttu-id="0da6c-181">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="0da6c-181">Optional input</span></span> | <span data-ttu-id="0da6c-182">4</span><span class="sxs-lookup"><span data-stu-id="0da6c-182">4</span></span> | <span data-ttu-id="0da6c-183">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="0da6c-183">INT8, UINT8</span></span> |
| <span data-ttu-id="0da6c-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="0da6c-184">OutputScaleTensor</span></span> | <span data-ttu-id="0da6c-185">輸入</span><span class="sxs-lookup"><span data-stu-id="0da6c-185">Input</span></span> | <span data-ttu-id="0da6c-186">4</span><span class="sxs-lookup"><span data-stu-id="0da6c-186">4</span></span> | <span data-ttu-id="0da6c-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="0da6c-187">FLOAT32</span></span> |
| <span data-ttu-id="0da6c-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="0da6c-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="0da6c-189">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="0da6c-189">Optional input</span></span> | <span data-ttu-id="0da6c-190">4</span><span class="sxs-lookup"><span data-stu-id="0da6c-190">4</span></span> | <span data-ttu-id="0da6c-191">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="0da6c-191">INT8, UINT8</span></span> |
| <span data-ttu-id="0da6c-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="0da6c-192">OutputTensor</span></span> | <span data-ttu-id="0da6c-193">輸出</span><span class="sxs-lookup"><span data-stu-id="0da6c-193">Output</span></span> | <span data-ttu-id="0da6c-194">4</span><span class="sxs-lookup"><span data-stu-id="0da6c-194">4</span></span> | <span data-ttu-id="0da6c-195">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="0da6c-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="0da6c-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="0da6c-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0da6c-197">**標頭**</span><span class="sxs-lookup"><span data-stu-id="0da6c-197">**Header**</span></span> | <span data-ttu-id="0da6c-198">directml。h</span><span class="sxs-lookup"><span data-stu-id="0da6c-198">directml.h</span></span> |