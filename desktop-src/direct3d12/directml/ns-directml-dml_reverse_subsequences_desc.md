---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: 反轉 tensor 的一或多個 *個子序列* 元素。 根據提供的軸和序列長度，選擇要反轉的個子序列集。
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 5baf16c5acd1ce5c5f44e68420e93aabaa276ea7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106997222"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a><span data-ttu-id="45000-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="45000-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="45000-105">反轉 tensor 的一或多個 *個子序列* 元素。</span><span class="sxs-lookup"><span data-stu-id="45000-105">Reverses the elements of one or more *subsequences* of a tensor.</span></span> <span data-ttu-id="45000-106">根據提供的軸和序列長度，選擇要反轉的個子序列集。</span><span class="sxs-lookup"><span data-stu-id="45000-106">The set of subsequences to be reversed is chosen based on the provided axis and sequence lengths.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45000-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="45000-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="45000-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="45000-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="45000-109">語法</span><span class="sxs-lookup"><span data-stu-id="45000-109">Syntax</span></span>
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="45000-110">成員</span><span class="sxs-lookup"><span data-stu-id="45000-110">Members</span></span>

`InputTensor`

<span data-ttu-id="45000-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="45000-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="45000-112">包含要反轉之元素的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="45000-112">The input tensor containing elements to be reversed.</span></span>


`SequenceLengthsTensor`

<span data-ttu-id="45000-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="45000-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="45000-114">Tensor，其中包含要反轉之每個子序列的值，表示該子序列的元素長度。</span><span class="sxs-lookup"><span data-stu-id="45000-114">A tensor containing a value for each subsequence to be reversed, denoting the length in elements of that subsequence.</span></span> <span data-ttu-id="45000-115">只有子序列長度內的元素會反轉;沿著該軸的其餘元素都會複製到未變更的輸出。</span><span class="sxs-lookup"><span data-stu-id="45000-115">Only the elements within the length of the subsequence are reversed; the remaining elements along that axis are copied to the output unchanged.</span></span>

<span data-ttu-id="45000-116">此 tensor 的維度計數和大小必須等於 *InputTensor*，但 *軸* 參數所指定的維度 *除外*。</span><span class="sxs-lookup"><span data-stu-id="45000-116">This tensor must have dimension count and sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter.</span></span> <span data-ttu-id="45000-117">*軸* 維度的大小必須為1。</span><span class="sxs-lookup"><span data-stu-id="45000-117">The size of the *Axis* dimension must be 1.</span></span> <span data-ttu-id="45000-118">例如，如果 *InputTensor* 的大小 `{2,3,4,5}` 是，而 *軸* 是1，則 *SequenceLengthsTensor* 的大小必須是 `{2,1,4,5}` 。</span><span class="sxs-lookup"><span data-stu-id="45000-118">For example if the *InputTensor* has sizes of `{2,3,4,5}`, and *Axis* is 1, then the sizes of the *SequenceLengthsTensor* must be `{2,1,4,5}`.</span></span>

<span data-ttu-id="45000-119">如果子序列的長度超過該軸的元素數目上限，則這個運算子的行為會如同將值壓制到最大值一樣。</span><span class="sxs-lookup"><span data-stu-id="45000-119">If the length of a subsequence exceeds the maximum number of elements along that axis, then this operator behaves as if the value were clamped to the maximum.</span></span>


`OutputTensor`

<span data-ttu-id="45000-120">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="45000-120">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="45000-121">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="45000-121">The output tensor to write the results to.</span></span> <span data-ttu-id="45000-122">這個 tensor 的大小和資料類型必須與 *InputTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="45000-122">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="45000-123">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="45000-123">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="45000-124">要反轉元素的維度索引。</span><span class="sxs-lookup"><span data-stu-id="45000-124">The index of the dimension to reverse elements over.</span></span> <span data-ttu-id="45000-125">這個值必須小於 *InputTensor* 的 DimensionCount。</span><span class="sxs-lookup"><span data-stu-id="45000-125">This value must be less than the DimensionCount of the *InputTensor*.</span></span>

## <a name="examples"></a><span data-ttu-id="45000-126">範例</span><span class="sxs-lookup"><span data-stu-id="45000-126">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="45000-127">範例 1</span><span class="sxs-lookup"><span data-stu-id="45000-127">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a><span data-ttu-id="45000-128">範例 2.</span><span class="sxs-lookup"><span data-stu-id="45000-128">Example 2.</span></span> <span data-ttu-id="45000-129">沿著不同的軸反轉</span><span class="sxs-lookup"><span data-stu-id="45000-129">Reversing along a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a><span data-ttu-id="45000-130">可用性</span><span class="sxs-lookup"><span data-stu-id="45000-130">Availability</span></span>
<span data-ttu-id="45000-131">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="45000-131">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="45000-132">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="45000-132">Tensor constraints</span></span>
* <span data-ttu-id="45000-133">*InputTensor*、 *OutputTensor* 和 *SequenceLengthsTensor* 必須有相同的 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="45000-133">*InputTensor*, *OutputTensor*, and *SequenceLengthsTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="45000-134">*InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="45000-134">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="45000-135">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="45000-135">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="45000-136">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="45000-136">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="45000-137">張</span><span class="sxs-lookup"><span data-stu-id="45000-137">Tensor</span></span> | <span data-ttu-id="45000-138">類型</span><span class="sxs-lookup"><span data-stu-id="45000-138">Kind</span></span> | <span data-ttu-id="45000-139">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="45000-139">Supported dimension counts</span></span> | <span data-ttu-id="45000-140">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="45000-140">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="45000-141">InputTensor</span><span class="sxs-lookup"><span data-stu-id="45000-141">InputTensor</span></span> | <span data-ttu-id="45000-142">輸入</span><span class="sxs-lookup"><span data-stu-id="45000-142">Input</span></span> | <span data-ttu-id="45000-143">4到5</span><span class="sxs-lookup"><span data-stu-id="45000-143">4 to 5</span></span> | <span data-ttu-id="45000-144">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="45000-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="45000-145">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="45000-145">SequenceLengthsTensor</span></span> | <span data-ttu-id="45000-146">輸入</span><span class="sxs-lookup"><span data-stu-id="45000-146">Input</span></span> | <span data-ttu-id="45000-147">4到5</span><span class="sxs-lookup"><span data-stu-id="45000-147">4 to 5</span></span> | <span data-ttu-id="45000-148">UINT32</span><span class="sxs-lookup"><span data-stu-id="45000-148">UINT32</span></span> |
| <span data-ttu-id="45000-149">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="45000-149">OutputTensor</span></span> | <span data-ttu-id="45000-150">輸出</span><span class="sxs-lookup"><span data-stu-id="45000-150">Output</span></span> | <span data-ttu-id="45000-151">4到5</span><span class="sxs-lookup"><span data-stu-id="45000-151">4 to 5</span></span> | <span data-ttu-id="45000-152">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="45000-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="45000-153">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="45000-153">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="45000-154">張</span><span class="sxs-lookup"><span data-stu-id="45000-154">Tensor</span></span> | <span data-ttu-id="45000-155">類型</span><span class="sxs-lookup"><span data-stu-id="45000-155">Kind</span></span> | <span data-ttu-id="45000-156">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="45000-156">Supported dimension counts</span></span> | <span data-ttu-id="45000-157">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="45000-157">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="45000-158">InputTensor</span><span class="sxs-lookup"><span data-stu-id="45000-158">InputTensor</span></span> | <span data-ttu-id="45000-159">輸入</span><span class="sxs-lookup"><span data-stu-id="45000-159">Input</span></span> | <span data-ttu-id="45000-160">4</span><span class="sxs-lookup"><span data-stu-id="45000-160">4</span></span> | <span data-ttu-id="45000-161">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="45000-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="45000-162">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="45000-162">SequenceLengthsTensor</span></span> | <span data-ttu-id="45000-163">輸入</span><span class="sxs-lookup"><span data-stu-id="45000-163">Input</span></span> | <span data-ttu-id="45000-164">4</span><span class="sxs-lookup"><span data-stu-id="45000-164">4</span></span> | <span data-ttu-id="45000-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="45000-165">UINT32</span></span> |
| <span data-ttu-id="45000-166">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="45000-166">OutputTensor</span></span> | <span data-ttu-id="45000-167">輸出</span><span class="sxs-lookup"><span data-stu-id="45000-167">Output</span></span> | <span data-ttu-id="45000-168">4</span><span class="sxs-lookup"><span data-stu-id="45000-168">4</span></span> | <span data-ttu-id="45000-169">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="45000-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="45000-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="45000-170">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="45000-171">**標頭**</span><span class="sxs-lookup"><span data-stu-id="45000-171">**Header**</span></span> | <span data-ttu-id="45000-172">directml。h</span><span class="sxs-lookup"><span data-stu-id="45000-172">directml.h</span></span> |