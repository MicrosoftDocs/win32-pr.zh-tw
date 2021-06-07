---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: 計算最大共用 (的反向傳播漸層查看 [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)) 。
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 3b0b10fa8ee17c9d06e779c3c990f134bc4ae669
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417243"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="8a3fc-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="8a3fc-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8a3fc-104">計算最大共用 (的反向傳播漸層查看 [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)) 。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-104">Computes backpropagation gradients for max pooling (see [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span></span>

<span data-ttu-id="8a3fc-105">請考慮不含填補或 dilations 的 2x2 **DML_MAX_POOLING2_OPERATOR_DESC** 以及1的跨距，以執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-105">Consider a 2x2 **DML_MAX_POOLING2_OPERATOR_DESC** without padding nor dilations and a stride of 1, which performs the following.</span></span>

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

<span data-ttu-id="8a3fc-106">輸入 tensor 中每個2x2 視窗的最大元素都會產生輸出的一個元素。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-106">The largest element of each 2x2 window in the input tensor produces one element of the output.</span></span> <span data-ttu-id="8a3fc-107">以下是指定類似參數的 **DML_MAX_POOLING_GRAD_OPERATOR_DESC** 輸出範例。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-107">Below is an example of the output of **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, given similar parameters.</span></span>

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

<span data-ttu-id="8a3fc-108">實際上，這個運算子會使用 *InputTensor* 來判斷每個視窗中最大專案的索引，並根據這些索引將 *InputGradientTensor* 的值分配至 *OutputGradientTensor* 。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-108">In effect, this operator uses the *InputTensor* to determine the index of the largest element from each window, and distributes the values of *InputGradientTensor* into the *OutputGradientTensor* based on these indices.</span></span> <span data-ttu-id="8a3fc-109">當索引重迭時，值會加總。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-109">Where indices overlap, the values are summed.</span></span> <span data-ttu-id="8a3fc-110">任何未參考的輸出元素都會清空。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-110">Any unreferenced output elements are zeroed.</span></span>

<span data-ttu-id="8a3fc-111">如果系結 (，視窗中有一個以上的元素有相同的最大值) ，則會選擇具有最低邏輯元素索引的專案。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-111">In the case of a tie (where more than one element in a window has the same maximum value), the element with the lowest logical element index is chosen.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a3fc-112">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="8a3fc-113">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a3fc-114">語法</span><span class="sxs-lookup"><span data-stu-id="8a3fc-114">Syntax</span></span>

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a><span data-ttu-id="8a3fc-115">成員</span><span class="sxs-lookup"><span data-stu-id="8a3fc-115">Members</span></span>

`InputTensor`

<span data-ttu-id="8a3fc-116">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8a3fc-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8a3fc-117">輸入功能 tensor。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-117">The input feature tensor.</span></span> <span data-ttu-id="8a3fc-118">這通常是在轉寄行程中提供作為 *InputTensor* [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-118">This is typically the same tensor that was provided as the *InputTensor* to [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="8a3fc-119">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8a3fc-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8a3fc-120">傳入的漸層 tensor。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-120">The incoming gradient tensor.</span></span> <span data-ttu-id="8a3fc-121">這通常是從上一層的反向傳播輸出中取得。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-121">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="8a3fc-122">一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)的 *輸出* 相同。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-122">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="8a3fc-123">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8a3fc-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8a3fc-124">包含 backpropagated 漸層的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-124">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="8a3fc-125">一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)的 *輸入* 相同。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-125">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="8a3fc-126">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8a3fc-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8a3fc-127">*進步*、 *WindowSize*、 *StartPadding*、 *EndPadding* 和 *Dilations* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-127">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, *EndPadding*, and *Dilations* arrays.</span></span> <span data-ttu-id="8a3fc-128">此值必須等於空間維度計數， (InputTensor 的 DimensionCount-2) 。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-128">This value must equal the spatial dimension count (InputTensor's DimensionCount - 2).</span></span> <span data-ttu-id="8a3fc-129">因為這個運算子只支援4D 張量，所以此參數唯一有效的值為2。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-129">As this operator only supports 4D tensors, the only valid value for this parameter is 2.</span></span>

`Strides`

<span data-ttu-id="8a3fc-130">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8a3fc-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8a3fc-131">請參閱 [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)中的 *進步*。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-131">See *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`WindowSize`

<span data-ttu-id="8a3fc-132">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8a3fc-132">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8a3fc-133">請參閱 [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)中的 *WindowSize* 。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-133">See *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`StartPadding`

<span data-ttu-id="8a3fc-134">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8a3fc-134">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8a3fc-135">請參閱 [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)中的 *StartPadding* 。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-135">See *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`EndPadding`

<span data-ttu-id="8a3fc-136">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8a3fc-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8a3fc-137">請參閱 [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)中的 *EndPadding* 。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-137">See *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`Dilations`

<span data-ttu-id="8a3fc-138">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8a3fc-138">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8a3fc-139">請參閱 [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)中的 *Dilations* 。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-139">See *Dilations* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

## <a name="availability"></a><span data-ttu-id="8a3fc-140">可用性</span><span class="sxs-lookup"><span data-stu-id="8a3fc-140">Availability</span></span>
<span data-ttu-id="8a3fc-141">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-141">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8a3fc-142">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="8a3fc-142">Tensor constraints</span></span>
* <span data-ttu-id="8a3fc-143">*InputTensor* 和 *OutputGradientTensor* 的 *大小* 必須相同。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-143">*InputTensor* and *OutputGradientTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="8a3fc-144">*InputGradientTensor*、 *InputTensor* 和 *OutputGradientTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="8a3fc-144">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8a3fc-145">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="8a3fc-145">Tensor support</span></span>
| <span data-ttu-id="8a3fc-146">張</span><span class="sxs-lookup"><span data-stu-id="8a3fc-146">Tensor</span></span> | <span data-ttu-id="8a3fc-147">種類</span><span class="sxs-lookup"><span data-stu-id="8a3fc-147">Kind</span></span> | <span data-ttu-id="8a3fc-148">維度</span><span class="sxs-lookup"><span data-stu-id="8a3fc-148">Dimensions</span></span> | <span data-ttu-id="8a3fc-149">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="8a3fc-149">Supported dimension counts</span></span> | <span data-ttu-id="8a3fc-150">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="8a3fc-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="8a3fc-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8a3fc-151">InputTensor</span></span> | <span data-ttu-id="8a3fc-152">輸入</span><span class="sxs-lookup"><span data-stu-id="8a3fc-152">Input</span></span> | <span data-ttu-id="8a3fc-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="8a3fc-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="8a3fc-154">4</span><span class="sxs-lookup"><span data-stu-id="8a3fc-154">4</span></span> | <span data-ttu-id="8a3fc-155">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8a3fc-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="8a3fc-156">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="8a3fc-156">InputGradientTensor</span></span> | <span data-ttu-id="8a3fc-157">輸入</span><span class="sxs-lookup"><span data-stu-id="8a3fc-157">Input</span></span> | <span data-ttu-id="8a3fc-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="8a3fc-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="8a3fc-159">4</span><span class="sxs-lookup"><span data-stu-id="8a3fc-159">4</span></span> | <span data-ttu-id="8a3fc-160">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8a3fc-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="8a3fc-161">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="8a3fc-161">OutputGradientTensor</span></span> | <span data-ttu-id="8a3fc-162">輸出</span><span class="sxs-lookup"><span data-stu-id="8a3fc-162">Output</span></span> | <span data-ttu-id="8a3fc-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="8a3fc-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="8a3fc-164">4</span><span class="sxs-lookup"><span data-stu-id="8a3fc-164">4</span></span> | <span data-ttu-id="8a3fc-165">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8a3fc-165">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="8a3fc-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a3fc-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8a3fc-167">**標頭**</span><span class="sxs-lookup"><span data-stu-id="8a3fc-167">**Header**</span></span> | <span data-ttu-id="8a3fc-168">directml。h</span><span class="sxs-lookup"><span data-stu-id="8a3fc-168">directml.h</span></span> |