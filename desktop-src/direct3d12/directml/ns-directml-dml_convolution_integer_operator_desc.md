---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: 使用 *InputTensor* 執行 *FilterTensor* 的卷積。 這個運算子會在整數資料上執行向前卷積。
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: c16690ea1e3049ffeba398bbbaca2003f965a832
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106985799"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="fca1c-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="fca1c-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="fca1c-105">使用 *InputTensor* 執行 *FilterTensor* 的卷積。</span><span class="sxs-lookup"><span data-stu-id="fca1c-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="fca1c-106">這個運算子會在整數資料上執行向前卷積。</span><span class="sxs-lookup"><span data-stu-id="fca1c-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="fca1c-107">選擇性的零點張量也可以用來從輸入和篩選 tensor 減去零點值。</span><span class="sxs-lookup"><span data-stu-id="fca1c-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fca1c-108">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="fca1c-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="fca1c-109">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="fca1c-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fca1c-110">語法</span><span class="sxs-lookup"><span data-stu-id="fca1c-110">Syntax</span></span>
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```

## <a name="members"></a><span data-ttu-id="fca1c-111">成員</span><span class="sxs-lookup"><span data-stu-id="fca1c-111">Members</span></span>

`InputTensor`

<span data-ttu-id="fca1c-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fca1c-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fca1c-113">包含輸入資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="fca1c-113">A tensor containing the input data.</span></span> <span data-ttu-id="fca1c-114">*InputTensor* 的預期維度是 `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="fca1c-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="fca1c-115">類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fca1c-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fca1c-116">包含輸入零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="fca1c-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="fca1c-117">*InputZeroPointTensor* 的預期維度是 `{ 1, 1, 1, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="fca1c-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="fca1c-118">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fca1c-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fca1c-119">包含篩選資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="fca1c-119">A tensor containing the filter data.</span></span> <span data-ttu-id="fca1c-120">*FilterTensor* 的預期維度是 `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="fca1c-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="fca1c-121">類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fca1c-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fca1c-122">包含篩選零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="fca1c-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="fca1c-123"> `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, OutputChannelCount, 1, 1 }` 需要每個通道的量化，FilterZeroPointTensor 的預期維度是。</span><span class="sxs-lookup"><span data-stu-id="fca1c-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="fca1c-124">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fca1c-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fca1c-125">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="fca1c-125">The tensor to write the results to.</span></span> <span data-ttu-id="fca1c-126">*OutputTensor* 的預期維度是 `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="fca1c-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="fca1c-127">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fca1c-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="fca1c-128">卷積運算的空間維度數目。</span><span class="sxs-lookup"><span data-stu-id="fca1c-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="fca1c-129">空間維度是卷積 *FilterTensor* 的較低維度。</span><span class="sxs-lookup"><span data-stu-id="fca1c-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="fca1c-130">此值也會決定進展、 *Dilations*、 *StartPadding* 和 *EndPadding* *陣列的大小*。</span><span class="sxs-lookup"><span data-stu-id="fca1c-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="fca1c-131">唯一支援的值為2。</span><span class="sxs-lookup"><span data-stu-id="fca1c-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="fca1c-132">類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="fca1c-132">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="fca1c-133">陣列，包含卷積運算的進展。</span><span class="sxs-lookup"><span data-stu-id="fca1c-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="fca1c-134">這些進展適用于卷積篩選。</span><span class="sxs-lookup"><span data-stu-id="fca1c-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="fca1c-135">它們與 [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)中包含的 tensor 進步不同。</span><span class="sxs-lookup"><span data-stu-id="fca1c-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="fca1c-136">類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="fca1c-136">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="fca1c-137">陣列，包含卷積運算的 dilations。</span><span class="sxs-lookup"><span data-stu-id="fca1c-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="fca1c-138">Dilations 是套用至篩選核心元素的進展。</span><span class="sxs-lookup"><span data-stu-id="fca1c-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="fca1c-139">這有藉由以零填補內部篩選核心元素來模擬較大的篩選核心效果。</span><span class="sxs-lookup"><span data-stu-id="fca1c-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="fca1c-140">類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="fca1c-140">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="fca1c-141">陣列，包含要套用至卷積作業之篩選和輸入 tensor 的每個空間維度開頭的填補值。</span><span class="sxs-lookup"><span data-stu-id="fca1c-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="fca1c-142">類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="fca1c-142">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="fca1c-143">陣列，包含要套用至卷積作業之篩選和輸入 tensor 的每個空間維度結尾的填補值。</span><span class="sxs-lookup"><span data-stu-id="fca1c-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="fca1c-144">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fca1c-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="fca1c-145">要將卷積作業劃分成的群組數目。</span><span class="sxs-lookup"><span data-stu-id="fca1c-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="fca1c-146">*GroupCount* 可以用來設定等於輸入通道計數的 *GroupCount* ，以達成深度的卷積。</span><span class="sxs-lookup"><span data-stu-id="fca1c-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="fca1c-147">這會將每個輸入通道的卷積分割為不同的卷積。</span><span class="sxs-lookup"><span data-stu-id="fca1c-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="fca1c-148">可用性</span><span class="sxs-lookup"><span data-stu-id="fca1c-148">Availability</span></span>
<span data-ttu-id="fca1c-149">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="fca1c-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="fca1c-150">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="fca1c-150">Tensor constraints</span></span>
* <span data-ttu-id="fca1c-151">*FilterTensor* 和 *FilterZeroPointTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="fca1c-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="fca1c-152">*InputTensor* 和 *InputZeroPointTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="fca1c-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fca1c-153">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="fca1c-153">Tensor support</span></span>
| <span data-ttu-id="fca1c-154">張</span><span class="sxs-lookup"><span data-stu-id="fca1c-154">Tensor</span></span> | <span data-ttu-id="fca1c-155">類型</span><span class="sxs-lookup"><span data-stu-id="fca1c-155">Kind</span></span> | <span data-ttu-id="fca1c-156">維度</span><span class="sxs-lookup"><span data-stu-id="fca1c-156">Dimensions</span></span> | <span data-ttu-id="fca1c-157">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="fca1c-157">Supported dimension counts</span></span> | <span data-ttu-id="fca1c-158">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="fca1c-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="fca1c-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="fca1c-159">InputTensor</span></span> | <span data-ttu-id="fca1c-160">輸入</span><span class="sxs-lookup"><span data-stu-id="fca1c-160">Input</span></span> | <span data-ttu-id="fca1c-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="fca1c-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="fca1c-162">4</span><span class="sxs-lookup"><span data-stu-id="fca1c-162">4</span></span> | <span data-ttu-id="fca1c-163">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="fca1c-163">INT8, UINT8</span></span> |
| <span data-ttu-id="fca1c-164">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="fca1c-164">InputZeroPointTensor</span></span> | <span data-ttu-id="fca1c-165">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="fca1c-165">Optional input</span></span> | <span data-ttu-id="fca1c-166">{1，1，1，1}</span><span class="sxs-lookup"><span data-stu-id="fca1c-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="fca1c-167">4</span><span class="sxs-lookup"><span data-stu-id="fca1c-167">4</span></span> | <span data-ttu-id="fca1c-168">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="fca1c-168">INT8, UINT8</span></span> |
| <span data-ttu-id="fca1c-169">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="fca1c-169">FilterTensor</span></span> | <span data-ttu-id="fca1c-170">輸入</span><span class="sxs-lookup"><span data-stu-id="fca1c-170">Input</span></span> | <span data-ttu-id="fca1c-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span><span class="sxs-lookup"><span data-stu-id="fca1c-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="fca1c-172">4</span><span class="sxs-lookup"><span data-stu-id="fca1c-172">4</span></span> | <span data-ttu-id="fca1c-173">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="fca1c-173">INT8, UINT8</span></span> |
| <span data-ttu-id="fca1c-174">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="fca1c-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="fca1c-175">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="fca1c-175">Optional input</span></span> | <span data-ttu-id="fca1c-176">{1，FilterZeroPointChannelCount，1，1}</span><span class="sxs-lookup"><span data-stu-id="fca1c-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="fca1c-177">4</span><span class="sxs-lookup"><span data-stu-id="fca1c-177">4</span></span> | <span data-ttu-id="fca1c-178">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="fca1c-178">INT8, UINT8</span></span> |
| <span data-ttu-id="fca1c-179">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="fca1c-179">OutputTensor</span></span> | <span data-ttu-id="fca1c-180">輸出</span><span class="sxs-lookup"><span data-stu-id="fca1c-180">Output</span></span> | <span data-ttu-id="fca1c-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="fca1c-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="fca1c-182">4</span><span class="sxs-lookup"><span data-stu-id="fca1c-182">4</span></span> | <span data-ttu-id="fca1c-183">INT32</span><span class="sxs-lookup"><span data-stu-id="fca1c-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="fca1c-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="fca1c-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fca1c-185">**標頭**</span><span class="sxs-lookup"><span data-stu-id="fca1c-185">**Header**</span></span> | <span data-ttu-id="fca1c-186">directml。h</span><span class="sxs-lookup"><span data-stu-id="fca1c-186">directml.h</span></span> |