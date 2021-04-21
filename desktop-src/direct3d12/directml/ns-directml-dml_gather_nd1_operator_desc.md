---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: 使用索引 tensor 將索引重新對應到輸入的整個 subblocks，以收集輸入 tensor 中的元素。 |DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: b92c8aece88d8466357bb8e48fd3ce5a3b73d2e3
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802860"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a><span data-ttu-id="d7b12-104">DML_GATHER_ND1_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="d7b12-104">DML_GATHER_ND1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="d7b12-105">使用索引 tensor 將索引重新對應到輸入的整個 subblocks，以收集輸入 tensor 中的元素。</span><span class="sxs-lookup"><span data-stu-id="d7b12-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="d7b12-106">這個運算子會執行下列虛擬虛擬，其中 "..."代表一系列的座標，其行為取決於批次、輸入和索引維度計數。</span><span class="sxs-lookup"><span data-stu-id="d7b12-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the batch, input, and indices dimension count.</span></span>

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> <span data-ttu-id="d7b12-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="d7b12-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="d7b12-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="d7b12-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b12-109">語法</span><span class="sxs-lookup"><span data-stu-id="d7b12-109">Syntax</span></span>

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a><span data-ttu-id="d7b12-110">成員</span><span class="sxs-lookup"><span data-stu-id="d7b12-110">Members</span></span>

`InputTensor`

<span data-ttu-id="d7b12-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d7b12-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d7b12-112">要從中讀取的 tensor。</span><span class="sxs-lookup"><span data-stu-id="d7b12-112">The tensor to read from.</span></span>

`IndicesTensor`

<span data-ttu-id="d7b12-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d7b12-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d7b12-114">包含索引的 tensor。</span><span class="sxs-lookup"><span data-stu-id="d7b12-114">The tensor containing the indices.</span></span> <span data-ttu-id="d7b12-115">此 tensor 的 *DimensionCount* 必須符合 *InputTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="d7b12-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="d7b12-116">*IndicesTensor* 的最後一個維度實際上是每個索引元組的座標數目，不能超過 *InputTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="d7b12-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="d7b12-117">例如， *大小* `{1,4,5,2}` 為 *IndicesDimensionCount* = 3 的索引 Tensor，表示索引為 *InputTensor* 的2座標元組4x5 陣列。</span><span class="sxs-lookup"><span data-stu-id="d7b12-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="d7b12-118">從開始 `DML_FEATURE_LEVEL_3_0` ，當使用帶正負號的整數型別搭配這個 tensor 時，這個運算子支援負的索引值。</span><span class="sxs-lookup"><span data-stu-id="d7b12-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="d7b12-119">負索引會解讀為相對於個別維度的結尾。</span><span class="sxs-lookup"><span data-stu-id="d7b12-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="d7b12-120">例如，-1 的索引指的是該維度的最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="d7b12-120">For example, an index of -1 refers to the last element along that dimension.</span></span>

`OutputTensor`

<span data-ttu-id="d7b12-121">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d7b12-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d7b12-122">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="d7b12-122">The tensor to write the results to.</span></span> <span data-ttu-id="d7b12-123">此 tensor 的 *DimensionCount* 和 *資料類型* 必須符合 *InputTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="d7b12-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="d7b12-124">預期的 *OutputTensor。* 大小是 IndicesTensor 的串連 *。* 大小的尾端區段和 *InputTensor 的大小* 會產生下列各項。</span><span class="sxs-lookup"><span data-stu-id="d7b12-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment, which yields the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="d7b12-125">這些維度會靠右對齊，並在必要時前置1值以滿足 *OutputTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="d7b12-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="d7b12-126">以下為範例。</span><span class="sxs-lookup"><span data-stu-id="d7b12-126">Here's an example.</span></span>

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

<span data-ttu-id="d7b12-127">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d7b12-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d7b12-128">略過任何不相關的開頭維度之後， *InputTensor* 內實際輸入維度的數目，範圍為 `[1, *InputTensor.DimensionCount*]` 。</span><span class="sxs-lookup"><span data-stu-id="d7b12-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="d7b12-129">例如，假設 *InputTensor 大小*  =  `{1,1,4,6}` 和 `InputDimensionCount` = 3，則實際有意義的索引為 `{1,4,6}` 。</span><span class="sxs-lookup"><span data-stu-id="d7b12-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`IndicesDimensionCount`

<span data-ttu-id="d7b12-130">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d7b12-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d7b12-131">在忽略任何不相關的前置專案（範圍 [1， *IndicesTensor. DimensionCount*]）之後， *IndicesTensor* 中的實際索引維度數目。</span><span class="sxs-lookup"><span data-stu-id="d7b12-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="d7b12-132">例如，假設 *IndicesTensor 大小*  =  `{1,1,4,6}` 和 *IndicesDimensionCount* = 3，則實際有意義的索引為 `{1,4,6}` 。</span><span class="sxs-lookup"><span data-stu-id="d7b12-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`BatchDimensionCount`

<span data-ttu-id="d7b12-133">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d7b12-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d7b12-134">每個 tensor 中的維度數目 (*InputTensor*、 *IndicesTensor*、 *OutputTensor*) 視為獨立的批次，範圍介於 [0， *InputTensor. DimensionCount*) 和 [0， *IndicesTensor. DimensionCount*) 中。</span><span class="sxs-lookup"><span data-stu-id="d7b12-134">The number of dimensions within each tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) that are considered independent batches, ranging within both [0, *InputTensor.DimensionCount*) and [0, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="d7b12-135">批次計數可以是0，這意味著單一批次。</span><span class="sxs-lookup"><span data-stu-id="d7b12-135">The batch count can be 0, implying a single batch.</span></span> <span data-ttu-id="d7b12-136">例如，假設有 *IndicesTensor*，  =  `{1,3,4,5,6,7}` 而 *IndicesDimensionCount* = 5 和 `BatchDimensionCount` = 2，則有批次 `{3,4}` 和有意義的索引 `{5,6,7}` 。</span><span class="sxs-lookup"><span data-stu-id="d7b12-136">For example, given *IndicesTensor.Sizes* = `{1,3,4,5,6,7}`, and *IndicesDimensionCount* = 5 and `BatchDimensionCount` = 2, there are batches `{3,4}` and meaningful indices `{5,6,7}`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7b12-137">備註</span><span class="sxs-lookup"><span data-stu-id="d7b12-137">Remarks</span></span>
<span data-ttu-id="d7b12-138">**DML_GATHER_ND1_OPERATOR_DESC** 會新增 *BatchDimensionCount*，且相當於 *BatchDimensionCount* = 0 時的 [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) 。</span><span class="sxs-lookup"><span data-stu-id="d7b12-138">**DML_GATHER_ND1_OPERATOR_DESC** adds *BatchDimensionCount*, and is equivalent to [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) when *BatchDimensionCount* = 0.</span></span>

## <a name="examples"></a><span data-ttu-id="d7b12-139">範例</span><span class="sxs-lookup"><span data-stu-id="d7b12-139">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="d7b12-140">範例 1.</span><span class="sxs-lookup"><span data-stu-id="d7b12-140">Example 1.</span></span> <span data-ttu-id="d7b12-141">1D 重新對應</span><span class="sxs-lookup"><span data-stu-id="d7b12-141">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a><span data-ttu-id="d7b12-142">範例 2.</span><span class="sxs-lookup"><span data-stu-id="d7b12-142">Example 2.</span></span> <span data-ttu-id="d7b12-143">使用批次計數進行2D 重新對應</span><span class="sxs-lookup"><span data-stu-id="d7b12-143">2D remapping with batch count</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a><span data-ttu-id="d7b12-144">可用性</span><span class="sxs-lookup"><span data-stu-id="d7b12-144">Availability</span></span>
<span data-ttu-id="d7b12-145">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="d7b12-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d7b12-146">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="d7b12-146">Tensor constraints</span></span>
* <span data-ttu-id="d7b12-147">*IndicesTensor*、 *InputTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="d7b12-147">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="d7b12-148">*InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="d7b12-148">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d7b12-149">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="d7b12-149">Tensor support</span></span>
| <span data-ttu-id="d7b12-150">張</span><span class="sxs-lookup"><span data-stu-id="d7b12-150">Tensor</span></span> | <span data-ttu-id="d7b12-151">類型</span><span class="sxs-lookup"><span data-stu-id="d7b12-151">Kind</span></span> | <span data-ttu-id="d7b12-152">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="d7b12-152">Supported dimension counts</span></span> | <span data-ttu-id="d7b12-153">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="d7b12-153">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d7b12-154">InputTensor</span><span class="sxs-lookup"><span data-stu-id="d7b12-154">InputTensor</span></span> | <span data-ttu-id="d7b12-155">輸入</span><span class="sxs-lookup"><span data-stu-id="d7b12-155">Input</span></span> | <span data-ttu-id="d7b12-156">1至8</span><span class="sxs-lookup"><span data-stu-id="d7b12-156">1 to 8</span></span> | <span data-ttu-id="d7b12-157">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="d7b12-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d7b12-158">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="d7b12-158">IndicesTensor</span></span> | <span data-ttu-id="d7b12-159">輸入</span><span class="sxs-lookup"><span data-stu-id="d7b12-159">Input</span></span> | <span data-ttu-id="d7b12-160">1至8</span><span class="sxs-lookup"><span data-stu-id="d7b12-160">1 to 8</span></span> | <span data-ttu-id="d7b12-161">INT64、INT32、UINT64、UINT32</span><span class="sxs-lookup"><span data-stu-id="d7b12-161">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="d7b12-162">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d7b12-162">OutputTensor</span></span> | <span data-ttu-id="d7b12-163">輸出</span><span class="sxs-lookup"><span data-stu-id="d7b12-163">Output</span></span> | <span data-ttu-id="d7b12-164">1至8</span><span class="sxs-lookup"><span data-stu-id="d7b12-164">1 to 8</span></span> | <span data-ttu-id="d7b12-165">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="d7b12-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="d7b12-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7b12-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d7b12-167">**標頭**</span><span class="sxs-lookup"><span data-stu-id="d7b12-167">**Header**</span></span> | <span data-ttu-id="d7b12-168">directml。h</span><span class="sxs-lookup"><span data-stu-id="d7b12-168">directml.h</span></span> |
