---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: 使用 *InputTensor* 執行 *FilterTensor* 的卷積。 這個運算子會在量化資料上執行向前卷積。 這個運算子在數學上相當於 dequantizing 輸入、convolving，然後量化輸出。
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 4dd50d80dfe4ae60e3fe7e67124ef00bfbc7bf2b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803880"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="5293c-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="5293c-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="5293c-106">使用 *InputTensor* 執行 *FilterTensor* 的卷積。</span><span class="sxs-lookup"><span data-stu-id="5293c-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="5293c-107">這個運算子會在量化資料上執行向前卷積。</span><span class="sxs-lookup"><span data-stu-id="5293c-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="5293c-108">這個運算子在數學上相當於 dequantizing 輸入、convolving，然後量化輸出。</span><span class="sxs-lookup"><span data-stu-id="5293c-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="5293c-109">此運算子使用的量化線性函式是線性量化函數</span><span class="sxs-lookup"><span data-stu-id="5293c-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="5293c-110">Dequantize 函式</span><span class="sxs-lookup"><span data-stu-id="5293c-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="5293c-111">量化函式</span><span class="sxs-lookup"><span data-stu-id="5293c-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="5293c-112">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="5293c-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5293c-113">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="5293c-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5293c-114">語法</span><span class="sxs-lookup"><span data-stu-id="5293c-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a><span data-ttu-id="5293c-115">成員</span><span class="sxs-lookup"><span data-stu-id="5293c-115">Members</span></span>

`InputTensor`

<span data-ttu-id="5293c-116">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5293c-117">包含輸入資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="5293c-117">A tensor containing the input data.</span></span> <span data-ttu-id="5293c-118">*InputTensor* 的預期維度是 `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="5293c-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="5293c-119">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5293c-120">包含輸入小數位數資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="5293c-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="5293c-121">的預期維度 `InputScaleTensor` 是 `{ 1, 1, 1, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="5293c-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="5293c-122">此比例值是用來 dequantizing 輸入值。</span><span class="sxs-lookup"><span data-stu-id="5293c-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="5293c-123">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5293c-124">包含輸入零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="5293c-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="5293c-125">*InputZeroPointTensor* 的預期維度是 `{ 1, 1, 1, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="5293c-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="5293c-126">這個零點值是用來 dequantizing 輸入值。</span><span class="sxs-lookup"><span data-stu-id="5293c-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="5293c-127">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5293c-128">包含篩選資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="5293c-128">A tensor containing the filter data.</span></span> <span data-ttu-id="5293c-129">*FilterTensor* 的預期維度是 `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="5293c-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="5293c-130">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5293c-131">包含篩選調整資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="5293c-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="5293c-132">`FilterScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, OutputChannelCount, 1, 1 }` 需要每個通道量化，則預期的維度為。</span><span class="sxs-lookup"><span data-stu-id="5293c-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="5293c-133">此比例值是用來 dequantizing 篩選值。</span><span class="sxs-lookup"><span data-stu-id="5293c-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="5293c-134">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5293c-135">包含篩選零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="5293c-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="5293c-136"> `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, OutputChannelCount, 1, 1 }` 需要每個通道量化，FilterZeroPointTensor 的預期維度是。</span><span class="sxs-lookup"><span data-stu-id="5293c-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="5293c-137">這個零點值是用來 dequantizing 篩選值。</span><span class="sxs-lookup"><span data-stu-id="5293c-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="5293c-138">類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5293c-139">包含偏差資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="5293c-139">A tensor containing the bias data.</span></span> <span data-ttu-id="5293c-140">偏差 tensor 是一種 tensor，其中包含的資料會在已新增至結果的卷積結尾的輸出 tensor 之間進行廣播。</span><span class="sxs-lookup"><span data-stu-id="5293c-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="5293c-141">BiasTensor 的預期維度是 `{ 1, OutputChannelCount, 1, 1 }` 為4d。</span><span class="sxs-lookup"><span data-stu-id="5293c-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="5293c-142">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5293c-143">包含輸出小數位數資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="5293c-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="5293c-144">OutputScaleTensor 的預期維度是 `{ 1, 1, 1, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="5293c-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="5293c-145">此輸入小數位數值可用來量化卷積輸出值。</span><span class="sxs-lookup"><span data-stu-id="5293c-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="5293c-146">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5293c-147">包含篩選零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="5293c-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="5293c-148">OutputZeroPointTensor 的預期維度是 `{ 1, 1, 1, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="5293c-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="5293c-149">這個輸入的零點值是用來量化輸出值的卷積。</span><span class="sxs-lookup"><span data-stu-id="5293c-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="5293c-150">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5293c-151">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="5293c-151">A tensor to write the results to.</span></span> <span data-ttu-id="5293c-152">OutputTensor 的預期維度是 `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="5293c-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="5293c-153">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5293c-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5293c-154">卷積運算的空間維度數目。</span><span class="sxs-lookup"><span data-stu-id="5293c-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="5293c-155">空間維度是卷積篩選 tensor *FilterTensor* 的較低維度。</span><span class="sxs-lookup"><span data-stu-id="5293c-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="5293c-156">此值也會決定進展、 *Dilations*、 *StartPadding* 和 *EndPadding* *陣列的大小*。</span><span class="sxs-lookup"><span data-stu-id="5293c-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="5293c-157">唯一支援的值為2。</span><span class="sxs-lookup"><span data-stu-id="5293c-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="5293c-158">類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-158">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="5293c-159">積運算的進展。</span><span class="sxs-lookup"><span data-stu-id="5293c-159">The strides of the convolution operation.</span></span> <span data-ttu-id="5293c-160">這些進展適用于卷積篩選。</span><span class="sxs-lookup"><span data-stu-id="5293c-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="5293c-161">它們與 [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)中包含的 tensor 進步不同。</span><span class="sxs-lookup"><span data-stu-id="5293c-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="5293c-162">類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-162">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="5293c-163">卷積運算的 Dilations。</span><span class="sxs-lookup"><span data-stu-id="5293c-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="5293c-164">Dilations 是套用至篩選核心元素的進展。</span><span class="sxs-lookup"><span data-stu-id="5293c-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="5293c-165">這有藉由以零填補內部篩選核心元素來模擬較大的篩選核心效果。</span><span class="sxs-lookup"><span data-stu-id="5293c-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="5293c-166">類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-166">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="5293c-167">要套用至卷積運算之篩選和輸入 tensor 的每個空間維度開頭的填補值。</span><span class="sxs-lookup"><span data-stu-id="5293c-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="5293c-168">類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5293c-168">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="5293c-169">要套用至卷積運算之篩選和輸入 tensor 的每個空間維度結尾的填補值。</span><span class="sxs-lookup"><span data-stu-id="5293c-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="5293c-170">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5293c-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5293c-171">要將卷積作業分割成的群組數目。</span><span class="sxs-lookup"><span data-stu-id="5293c-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="5293c-172">*GroupCount* 可以用來設定等於輸入通道計數的 *GroupCount* ，以達成深度的卷積。</span><span class="sxs-lookup"><span data-stu-id="5293c-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="5293c-173">這會將每個輸入通道的卷積分割為不同的卷積。</span><span class="sxs-lookup"><span data-stu-id="5293c-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="5293c-174">可用性</span><span class="sxs-lookup"><span data-stu-id="5293c-174">Availability</span></span>
<span data-ttu-id="5293c-175">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="5293c-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5293c-176">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="5293c-176">Tensor constraints</span></span>
* <span data-ttu-id="5293c-177">*FilterTensor* 和 *FilterZeroPointTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="5293c-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="5293c-178">*InputTensor* 和 *InputZeroPointTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="5293c-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="5293c-179">*OutputTensor* 和 `OutputZeroPointTensor` 必須具有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="5293c-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5293c-180">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="5293c-180">Tensor support</span></span>
| <span data-ttu-id="5293c-181">張</span><span class="sxs-lookup"><span data-stu-id="5293c-181">Tensor</span></span> | <span data-ttu-id="5293c-182">類型</span><span class="sxs-lookup"><span data-stu-id="5293c-182">Kind</span></span> | <span data-ttu-id="5293c-183">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="5293c-183">Supported dimension counts</span></span> | <span data-ttu-id="5293c-184">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="5293c-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5293c-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5293c-185">InputTensor</span></span> | <span data-ttu-id="5293c-186">輸入</span><span class="sxs-lookup"><span data-stu-id="5293c-186">Input</span></span> | <span data-ttu-id="5293c-187">4</span><span class="sxs-lookup"><span data-stu-id="5293c-187">4</span></span> | <span data-ttu-id="5293c-188">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="5293c-188">INT8, UINT8</span></span> |
| <span data-ttu-id="5293c-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="5293c-189">InputScaleTensor</span></span> | <span data-ttu-id="5293c-190">輸入</span><span class="sxs-lookup"><span data-stu-id="5293c-190">Input</span></span> | <span data-ttu-id="5293c-191">4</span><span class="sxs-lookup"><span data-stu-id="5293c-191">4</span></span> | <span data-ttu-id="5293c-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="5293c-192">FLOAT32</span></span> |
| <span data-ttu-id="5293c-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="5293c-193">InputZeroPointTensor</span></span> | <span data-ttu-id="5293c-194">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="5293c-194">Optional input</span></span> | <span data-ttu-id="5293c-195">4</span><span class="sxs-lookup"><span data-stu-id="5293c-195">4</span></span> | <span data-ttu-id="5293c-196">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="5293c-196">INT8, UINT8</span></span> |
| <span data-ttu-id="5293c-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="5293c-197">FilterTensor</span></span> | <span data-ttu-id="5293c-198">輸入</span><span class="sxs-lookup"><span data-stu-id="5293c-198">Input</span></span> | <span data-ttu-id="5293c-199">4</span><span class="sxs-lookup"><span data-stu-id="5293c-199">4</span></span> | <span data-ttu-id="5293c-200">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="5293c-200">INT8, UINT8</span></span> |
| <span data-ttu-id="5293c-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="5293c-201">FilterScaleTensor</span></span> | <span data-ttu-id="5293c-202">輸入</span><span class="sxs-lookup"><span data-stu-id="5293c-202">Input</span></span> | <span data-ttu-id="5293c-203">4</span><span class="sxs-lookup"><span data-stu-id="5293c-203">4</span></span> | <span data-ttu-id="5293c-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="5293c-204">FLOAT32</span></span> |
| <span data-ttu-id="5293c-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="5293c-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="5293c-206">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="5293c-206">Optional input</span></span> | <span data-ttu-id="5293c-207">4</span><span class="sxs-lookup"><span data-stu-id="5293c-207">4</span></span> | <span data-ttu-id="5293c-208">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="5293c-208">INT8, UINT8</span></span> |
| <span data-ttu-id="5293c-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="5293c-209">BiasTensor</span></span> | <span data-ttu-id="5293c-210">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="5293c-210">Optional input</span></span> | <span data-ttu-id="5293c-211">4</span><span class="sxs-lookup"><span data-stu-id="5293c-211">4</span></span> | <span data-ttu-id="5293c-212">INT32</span><span class="sxs-lookup"><span data-stu-id="5293c-212">INT32</span></span> |
| <span data-ttu-id="5293c-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="5293c-213">OutputScaleTensor</span></span> | <span data-ttu-id="5293c-214">輸入</span><span class="sxs-lookup"><span data-stu-id="5293c-214">Input</span></span> | <span data-ttu-id="5293c-215">4</span><span class="sxs-lookup"><span data-stu-id="5293c-215">4</span></span> | <span data-ttu-id="5293c-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="5293c-216">FLOAT32</span></span> |
| <span data-ttu-id="5293c-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="5293c-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="5293c-218">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="5293c-218">Optional input</span></span> | <span data-ttu-id="5293c-219">4</span><span class="sxs-lookup"><span data-stu-id="5293c-219">4</span></span> | <span data-ttu-id="5293c-220">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="5293c-220">INT8, UINT8</span></span> |
| <span data-ttu-id="5293c-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5293c-221">OutputTensor</span></span> | <span data-ttu-id="5293c-222">輸出</span><span class="sxs-lookup"><span data-stu-id="5293c-222">Output</span></span> | <span data-ttu-id="5293c-223">4</span><span class="sxs-lookup"><span data-stu-id="5293c-223">4</span></span> | <span data-ttu-id="5293c-224">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="5293c-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="5293c-225">規格需求</span><span class="sxs-lookup"><span data-stu-id="5293c-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5293c-226">**標頭**</span><span class="sxs-lookup"><span data-stu-id="5293c-226">**Header**</span></span> | <span data-ttu-id="5293c-227">directml。h</span><span class="sxs-lookup"><span data-stu-id="5293c-227">directml.h</span></span> |