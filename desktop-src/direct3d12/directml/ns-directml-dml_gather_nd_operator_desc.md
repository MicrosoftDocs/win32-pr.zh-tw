---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: 使用索引 tensor 將索引重新對應到輸入的整個 subblocks，以收集輸入 tensor 中的元素。 |DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 8e74078eaf55f209fba92ba97737d22047a5e67c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802901"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="f8316-104">DML_GATHER_ND_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="f8316-104">DML_GATHER_ND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f8316-105">使用索引 tensor 將索引重新對應到輸入的整個 subblocks，以收集輸入 tensor 中的元素。</span><span class="sxs-lookup"><span data-stu-id="f8316-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="f8316-106">這個運算子會執行下列虛擬虛擬，其中 "..."代表一系列的座標，其行為取決於輸入和索引維度計數。</span><span class="sxs-lookup"><span data-stu-id="f8316-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the input and indices dimension count.</span></span>

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> <span data-ttu-id="f8316-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f8316-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f8316-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="f8316-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8316-109">語法</span><span class="sxs-lookup"><span data-stu-id="f8316-109">Syntax</span></span>
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="f8316-110">成員</span><span class="sxs-lookup"><span data-stu-id="f8316-110">Members</span></span>

`InputTensor`

<span data-ttu-id="f8316-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f8316-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f8316-112">要從中讀取的 tensor。</span><span class="sxs-lookup"><span data-stu-id="f8316-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="f8316-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f8316-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f8316-114">包含索引的 tensor。</span><span class="sxs-lookup"><span data-stu-id="f8316-114">The tensor containing the indices.</span></span> <span data-ttu-id="f8316-115">此 tensor 的 *DimensionCount* 必須符合 *InputTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="f8316-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="f8316-116">*IndicesTensor* 的最後一個維度實際上是每個索引元組的座標數目，不能超過 *InputTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="f8316-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="f8316-117">例如， *大小* `{1,4,5,2}` 為 *IndicesDimensionCount* = 3 的索引 Tensor，表示索引為 *InputTensor* 的2座標元組4x5 陣列。</span><span class="sxs-lookup"><span data-stu-id="f8316-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="f8316-118">從開始 `DML_FEATURE_LEVEL_3_0` ，當使用帶正負號的整數型別搭配這個 tensor 時，這個運算子支援負的索引值。</span><span class="sxs-lookup"><span data-stu-id="f8316-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="f8316-119">負索引會解讀為相對於個別維度的結尾。</span><span class="sxs-lookup"><span data-stu-id="f8316-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="f8316-120">例如，-1 的索引指的是該維度的最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="f8316-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="f8316-121">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f8316-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f8316-122">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="f8316-122">The tensor to write the results to.</span></span> <span data-ttu-id="f8316-123">此 tensor 的 *DimensionCount* 和 *資料類型* 必須符合 *InputTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="f8316-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="f8316-124">預期的 *OutputTensor。* 大小是 IndicesTensor 的串連 *。* 大小的開頭區段和 *InputTensor。大小* 的尾端區段會產生：</span><span class="sxs-lookup"><span data-stu-id="f8316-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield:</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="f8316-125">輸出維度會靠右對齊，並在必要時前置1值，以滿足最多 *OutputTensor DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="f8316-125">The output dimensions are right-aligned, with leading 1 values prepended if needed to satisfy up to *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="f8316-126">以下為範例。</span><span class="sxs-lookup"><span data-stu-id="f8316-126">Here's an example.</span></span>

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```


`InputDimensionCount`

<span data-ttu-id="f8316-127">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f8316-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f8316-128">略過任何不相關的開頭維度之後， *InputTensor* 內實際輸入維度的數目，範圍為 `[1, *InputTensor.DimensionCount*]` 。</span><span class="sxs-lookup"><span data-stu-id="f8316-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="f8316-129">例如，假設 *InputTensor 大小*  =  `{1,1,4,6}` 和 `InputDimensionCount` = 3，則實際有意義的索引為 `{1,4,6}` 。</span><span class="sxs-lookup"><span data-stu-id="f8316-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="f8316-130">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f8316-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f8316-131">在忽略任何不相關的前置專案（範圍 [1， *IndicesTensor. DimensionCount*]）之後， *IndicesTensor* 中的實際索引維度數目。</span><span class="sxs-lookup"><span data-stu-id="f8316-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="f8316-132">例如，假設 *IndicesTensor 大小*  =  `{1,1,4,6}` 和 *IndicesDimensionCount* = 3，則實際有意義的索引為 `{1,4,6}` 。</span><span class="sxs-lookup"><span data-stu-id="f8316-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

## <a name="examples"></a><span data-ttu-id="f8316-133">範例</span><span class="sxs-lookup"><span data-stu-id="f8316-133">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="f8316-134">範例 1.</span><span class="sxs-lookup"><span data-stu-id="f8316-134">Example 1.</span></span> <span data-ttu-id="f8316-135">1D 重新對應</span><span class="sxs-lookup"><span data-stu-id="f8316-135">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a><span data-ttu-id="f8316-136">範例 2.</span><span class="sxs-lookup"><span data-stu-id="f8316-136">Example 2.</span></span> <span data-ttu-id="f8316-137">2D 重新對應</span><span class="sxs-lookup"><span data-stu-id="f8316-137">2D remapping</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a><span data-ttu-id="f8316-138">備註</span><span class="sxs-lookup"><span data-stu-id="f8316-138">Remarks</span></span>
<span data-ttu-id="f8316-139">在中引進了這個運算子的較新版本 `DML_OPERATOR_GATHER_ND1` `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="f8316-139">A newer version of this operator, `DML_OPERATOR_GATHER_ND1`, was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="availability"></a><span data-ttu-id="f8316-140">可用性</span><span class="sxs-lookup"><span data-stu-id="f8316-140">Availability</span></span>
<span data-ttu-id="f8316-141">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="f8316-141">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f8316-142">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="f8316-142">Tensor constraints</span></span>
* <span data-ttu-id="f8316-143">*IndicesTensor*、 *InputTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="f8316-143">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="f8316-144">*InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="f8316-144">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f8316-145">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="f8316-145">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="f8316-146">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="f8316-146">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="f8316-147">張</span><span class="sxs-lookup"><span data-stu-id="f8316-147">Tensor</span></span> | <span data-ttu-id="f8316-148">類型</span><span class="sxs-lookup"><span data-stu-id="f8316-148">Kind</span></span> | <span data-ttu-id="f8316-149">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="f8316-149">Supported dimension counts</span></span> | <span data-ttu-id="f8316-150">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="f8316-150">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f8316-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f8316-151">InputTensor</span></span> | <span data-ttu-id="f8316-152">輸入</span><span class="sxs-lookup"><span data-stu-id="f8316-152">Input</span></span> | <span data-ttu-id="f8316-153">1至8</span><span class="sxs-lookup"><span data-stu-id="f8316-153">1 to 8</span></span> | <span data-ttu-id="f8316-154">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="f8316-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f8316-155">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="f8316-155">IndicesTensor</span></span> | <span data-ttu-id="f8316-156">輸入</span><span class="sxs-lookup"><span data-stu-id="f8316-156">Input</span></span> | <span data-ttu-id="f8316-157">1至8</span><span class="sxs-lookup"><span data-stu-id="f8316-157">1 to 8</span></span> | <span data-ttu-id="f8316-158">INT64、INT32、UINT64、UINT32</span><span class="sxs-lookup"><span data-stu-id="f8316-158">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="f8316-159">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f8316-159">OutputTensor</span></span> | <span data-ttu-id="f8316-160">輸出</span><span class="sxs-lookup"><span data-stu-id="f8316-160">Output</span></span> | <span data-ttu-id="f8316-161">1至8</span><span class="sxs-lookup"><span data-stu-id="f8316-161">1 to 8</span></span> | <span data-ttu-id="f8316-162">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="f8316-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="f8316-163">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="f8316-163">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="f8316-164">張</span><span class="sxs-lookup"><span data-stu-id="f8316-164">Tensor</span></span> | <span data-ttu-id="f8316-165">類型</span><span class="sxs-lookup"><span data-stu-id="f8316-165">Kind</span></span> | <span data-ttu-id="f8316-166">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="f8316-166">Supported dimension counts</span></span> | <span data-ttu-id="f8316-167">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="f8316-167">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f8316-168">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f8316-168">InputTensor</span></span> | <span data-ttu-id="f8316-169">輸入</span><span class="sxs-lookup"><span data-stu-id="f8316-169">Input</span></span> | <span data-ttu-id="f8316-170">4</span><span class="sxs-lookup"><span data-stu-id="f8316-170">4</span></span> | <span data-ttu-id="f8316-171">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="f8316-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f8316-172">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="f8316-172">IndicesTensor</span></span> | <span data-ttu-id="f8316-173">輸入</span><span class="sxs-lookup"><span data-stu-id="f8316-173">Input</span></span> | <span data-ttu-id="f8316-174">4</span><span class="sxs-lookup"><span data-stu-id="f8316-174">4</span></span> | <span data-ttu-id="f8316-175">UINT32</span><span class="sxs-lookup"><span data-stu-id="f8316-175">UINT32</span></span> |
| <span data-ttu-id="f8316-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f8316-176">OutputTensor</span></span> | <span data-ttu-id="f8316-177">輸出</span><span class="sxs-lookup"><span data-stu-id="f8316-177">Output</span></span> | <span data-ttu-id="f8316-178">4</span><span class="sxs-lookup"><span data-stu-id="f8316-178">4</span></span> | <span data-ttu-id="f8316-179">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="f8316-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="f8316-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8316-180">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f8316-181">**標頭**</span><span class="sxs-lookup"><span data-stu-id="f8316-181">**Header**</span></span> | <span data-ttu-id="f8316-182">directml。h</span><span class="sxs-lookup"><span data-stu-id="f8316-182">directml.h</span></span> |
