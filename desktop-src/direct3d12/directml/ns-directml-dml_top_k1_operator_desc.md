---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: 選取每個序列中的最大或最小 *K* 元素，沿著 *InputTensor* 軸，然後分別傳回 *OutputValueTensor* 和 *OutputIndexTensor* 中這些元素的值和索引。
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 8c5b9bf58a8582588d19878c7e06c602584777fa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106981725"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a><span data-ttu-id="a8f47-103">DML_TOP_K1_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="a8f47-103">DML_TOP_K1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="a8f47-104">選取每個序列中的最大或最小 *K* 元素，沿著 *InputTensor* 軸，然後分別傳回 *OutputValueTensor* 和 *OutputIndexTensor* 中這些元素的值和索引。</span><span class="sxs-lookup"><span data-stu-id="a8f47-104">Selects the largest or smallest *K* elements from each sequence along an axis of the *InputTensor*, and returns the values and indices of those elements in the *OutputValueTensor* and *OutputIndexTensor*, respectively.</span></span> <span data-ttu-id="a8f47-105">*序列* 是指存在於 *InputTensor* 之 *軸* 維度中的其中一個專案集合。</span><span class="sxs-lookup"><span data-stu-id="a8f47-105">A *sequence* refers to one of the sets of elements that exist along the *Axis* dimension of the *InputTensor*.</span></span>

<span data-ttu-id="a8f47-106">選擇是否要選取最大的 K 元素或最小的 K 元素，都可以使用 *AxisDirection* 來控制。</span><span class="sxs-lookup"><span data-stu-id="a8f47-106">The choice of whether to select the largest K elements or the smallest K elements can be controlled using *AxisDirection*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8f47-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="a8f47-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="a8f47-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="a8f47-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f47-109">語法</span><span class="sxs-lookup"><span data-stu-id="a8f47-109">Syntax</span></span>
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```



## <a name="members"></a><span data-ttu-id="a8f47-110">成員</span><span class="sxs-lookup"><span data-stu-id="a8f47-110">Members</span></span>

`InputTensor`

<span data-ttu-id="a8f47-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a8f47-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a8f47-112">包含要選取之元素的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="a8f47-112">The input tensor containing elements to select.</span></span>


`OutputValueTensor`

<span data-ttu-id="a8f47-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a8f47-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a8f47-114">用來將前 *K* 個元素的值寫入其中的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="a8f47-114">The output tensor to write the values of the top *K* elements to.</span></span> <span data-ttu-id="a8f47-115">依據 *AxisDirection* 的值而定，會根據最大或最小的專案來選取前 *K* 個元素。</span><span class="sxs-lookup"><span data-stu-id="a8f47-115">The top *K* elements are selected based on whether they are the largest or the smallest, depending on the value of *AxisDirection*.</span></span> <span data-ttu-id="a8f47-116">此 tensor 的大小必須等於 *InputTensor*，*但\*\*軸* 參數所指定的維度必須等於 *K* 的大小。</span><span class="sxs-lookup"><span data-stu-id="a8f47-116">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="a8f47-117">如果 *AxisDirection* 是 [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md)的，則在每個輸入序列中選取的 *K* 值保證會以遞減方式排序 (最大到最小的) 。</span><span class="sxs-lookup"><span data-stu-id="a8f47-117">The *K* values selected from each input sequence are guaranteed to be sorted descending (largest to smallest) if *AxisDirection* is [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span></span> <span data-ttu-id="a8f47-118">否則，相反的會是 true，而選取的值保證會以遞增方式排序 (最小到最大的) 。</span><span class="sxs-lookup"><span data-stu-id="a8f47-118">Otherwise, the opposite is true and the values selected are guaranteed to be sorted ascending (smallest to largest).</span></span>


`OutputIndexTensor`

<span data-ttu-id="a8f47-119">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a8f47-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a8f47-120">輸出 tensor，用來將前 *K* 個元素的索引寫入至。</span><span class="sxs-lookup"><span data-stu-id="a8f47-120">The output tensor to write the indices of the top *K* elements to.</span></span> <span data-ttu-id="a8f47-121">此 tensor 的大小必須等於 *InputTensor*，*但\*\*軸* 參數所指定的維度必須等於 *K* 的大小。</span><span class="sxs-lookup"><span data-stu-id="a8f47-121">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="a8f47-122">在這個 tensor 中傳回的索引是相對於順序的開頭來測量 (而不是 tensor) 的開頭。</span><span class="sxs-lookup"><span data-stu-id="a8f47-122">The indices returned in this tensor are measured relative to the beginning of their sequence (as opposed to the beginning of the tensor).</span></span> <span data-ttu-id="a8f47-123">例如，索引0一律會參考軸中所有序列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="a8f47-123">For example, an index of 0 always refers to the first element for all sequences in an axis.</span></span>

<span data-ttu-id="a8f47-124">如果頂端的兩個或多個專案具有相同的值 (也就是說，當有系結) 時，會包含這兩個專案的索引，並保證會以遞增的元素索引來排序。</span><span class="sxs-lookup"><span data-stu-id="a8f47-124">In cases where two or more elements in the top-K have the same value (that is, when there is a tie), the indices of both elements are included, and are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="a8f47-125">請注意，不論 *AxisDirection* 的值是什麼，都是如此。</span><span class="sxs-lookup"><span data-stu-id="a8f47-125">Note that this is true irrespective of the value of *AxisDirection*.</span></span>


`Axis`

<span data-ttu-id="a8f47-126">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a8f47-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="a8f47-127">要在其中選取元素的維度索引。</span><span class="sxs-lookup"><span data-stu-id="a8f47-127">The index of the dimension to select elements across.</span></span> <span data-ttu-id="a8f47-128">這個值必須小於 *InputTensor* 的 *DimensionCount* 。</span><span class="sxs-lookup"><span data-stu-id="a8f47-128">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`K`

<span data-ttu-id="a8f47-129">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a8f47-129">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="a8f47-130">要選取的元素數目。</span><span class="sxs-lookup"><span data-stu-id="a8f47-130">The number of elements to select.</span></span> <span data-ttu-id="a8f47-131">*K* 必須大於0，但小於 *軸* 所指定之維度中 *InputTensor* 的元素數目。</span><span class="sxs-lookup"><span data-stu-id="a8f47-131">*K* must be greater than 0, but less than the number of elements in the *InputTensor* along the dimension specified by *Axis*.</span></span>


`AxisDirection`

<span data-ttu-id="a8f47-132">類型： **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="a8f47-132">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="a8f47-133">[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)列舉中的值。</span><span class="sxs-lookup"><span data-stu-id="a8f47-133">A value from the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="a8f47-134">如果設定為 **DML_AXIS_DIRECTION_INCREASING**，則這個運算子會傳回 *最小* 的 *K* 元素（以遞增值的順序排列）。</span><span class="sxs-lookup"><span data-stu-id="a8f47-134">If set to **DML_AXIS_DIRECTION_INCREASING**, then this operator returns the *smallest* *K* elements in order of increasing value.</span></span> <span data-ttu-id="a8f47-135">否則，它會以遞減順序傳回 *最大* 的 *K* 元素。</span><span class="sxs-lookup"><span data-stu-id="a8f47-135">Otherwise, it returns the *largest* *K* elements in decreasing order.</span></span>

## <a name="examples"></a><span data-ttu-id="a8f47-136">範例</span><span class="sxs-lookup"><span data-stu-id="a8f47-136">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="a8f47-137">範例 1</span><span class="sxs-lookup"><span data-stu-id="a8f47-137">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a><span data-ttu-id="a8f47-138">範例 2.</span><span class="sxs-lookup"><span data-stu-id="a8f47-138">Example 2.</span></span> <span data-ttu-id="a8f47-139">使用不同的軸</span><span class="sxs-lookup"><span data-stu-id="a8f47-139">Using a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a><span data-ttu-id="a8f47-140">範例 3.</span><span class="sxs-lookup"><span data-stu-id="a8f47-140">Example 3.</span></span> <span data-ttu-id="a8f47-141">系結值</span><span class="sxs-lookup"><span data-stu-id="a8f47-141">Tied values</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a><span data-ttu-id="a8f47-142">範例4。</span><span class="sxs-lookup"><span data-stu-id="a8f47-142">Example 4.</span></span> <span data-ttu-id="a8f47-143">增加軸方向</span><span class="sxs-lookup"><span data-stu-id="a8f47-143">Increasing axis direction</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a><span data-ttu-id="a8f47-144">備註</span><span class="sxs-lookup"><span data-stu-id="a8f47-144">Remarks</span></span>
<span data-ttu-id="a8f47-145">當 *AxisDirection* 設定為 [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md)時，這個運算子相當於 [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc)。</span><span class="sxs-lookup"><span data-stu-id="a8f47-145">When *AxisDirection* is set to [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), this operator is equivalent to [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="a8f47-146">可用性</span><span class="sxs-lookup"><span data-stu-id="a8f47-146">Availability</span></span>
<span data-ttu-id="a8f47-147">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="a8f47-147">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a8f47-148">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="a8f47-148">Tensor constraints</span></span>
* <span data-ttu-id="a8f47-149">*InputTensor* 和 *OutputValueTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="a8f47-149">*InputTensor* and *OutputValueTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="a8f47-150">*OutputIndexTensor* 和 *OutputValueTensor* 的 *大小* 必須相同。</span><span class="sxs-lookup"><span data-stu-id="a8f47-150">*OutputIndexTensor* and *OutputValueTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a8f47-151">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="a8f47-151">Tensor support</span></span>
| <span data-ttu-id="a8f47-152">張</span><span class="sxs-lookup"><span data-stu-id="a8f47-152">Tensor</span></span> | <span data-ttu-id="a8f47-153">類型</span><span class="sxs-lookup"><span data-stu-id="a8f47-153">Kind</span></span> | <span data-ttu-id="a8f47-154">維度</span><span class="sxs-lookup"><span data-stu-id="a8f47-154">Dimensions</span></span> | <span data-ttu-id="a8f47-155">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="a8f47-155">Supported dimension counts</span></span> | <span data-ttu-id="a8f47-156">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="a8f47-156">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="a8f47-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a8f47-157">InputTensor</span></span> | <span data-ttu-id="a8f47-158">輸入</span><span class="sxs-lookup"><span data-stu-id="a8f47-158">Input</span></span> | <span data-ttu-id="a8f47-159">{ In0, In1, In2, In3 }</span><span class="sxs-lookup"><span data-stu-id="a8f47-159">{ In0, In1, In2, In3 }</span></span> | <span data-ttu-id="a8f47-160">4</span><span class="sxs-lookup"><span data-stu-id="a8f47-160">4</span></span> | <span data-ttu-id="a8f47-161">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a8f47-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a8f47-162">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="a8f47-162">OutputValueTensor</span></span> | <span data-ttu-id="a8f47-163">輸出</span><span class="sxs-lookup"><span data-stu-id="a8f47-163">Output</span></span> | <span data-ttu-id="a8f47-164">{ Out0, Out1, Out2, Out3 }</span><span class="sxs-lookup"><span data-stu-id="a8f47-164">{ Out0, Out1, Out2, Out3 }</span></span> | <span data-ttu-id="a8f47-165">4</span><span class="sxs-lookup"><span data-stu-id="a8f47-165">4</span></span> | <span data-ttu-id="a8f47-166">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a8f47-166">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a8f47-167">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="a8f47-167">OutputIndexTensor</span></span> | <span data-ttu-id="a8f47-168">輸出</span><span class="sxs-lookup"><span data-stu-id="a8f47-168">Output</span></span> | <span data-ttu-id="a8f47-169">{ Out0, Out1, Out2, Out3 }</span><span class="sxs-lookup"><span data-stu-id="a8f47-169">{ Out0, Out1, Out2, Out3 }</span></span> | <span data-ttu-id="a8f47-170">4</span><span class="sxs-lookup"><span data-stu-id="a8f47-170">4</span></span> | <span data-ttu-id="a8f47-171">UINT32</span><span class="sxs-lookup"><span data-stu-id="a8f47-171">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="a8f47-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8f47-172">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a8f47-173">**標頭**</span><span class="sxs-lookup"><span data-stu-id="a8f47-173">**Header**</span></span> | <span data-ttu-id="a8f47-174">directml。h</span><span class="sxs-lookup"><span data-stu-id="a8f47-174">directml.h</span></span> |