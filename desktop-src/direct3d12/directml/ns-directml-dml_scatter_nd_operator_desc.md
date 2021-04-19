---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: 'DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC) '
description: 將整個輸入 tensor 複製到輸出，然後使用 [更新] tensor 中的對應值來覆寫選取的索引。
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: ae9a3022a7070bbf0253e71550f2ca1ceced6768
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106998560"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="955d0-103">DML_SCATTER_ND_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="955d0-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="955d0-104">將整個輸入 tensor 複製到輸出，然後使用 [更新] tensor 中的對應值來覆寫選取的索引。</span><span class="sxs-lookup"><span data-stu-id="955d0-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="955d0-105">這個運算子會執行下列虛擬虛擬，其中 "..."代表一系列的座標，其確切行為取決於軸和索引的大小。</span><span class="sxs-lookup"><span data-stu-id="955d0-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="955d0-106">如果有兩個輸出元素索引 () 無效，則無法保證最後寫入的最後一個。</span><span class="sxs-lookup"><span data-stu-id="955d0-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="955d0-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="955d0-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="955d0-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="955d0-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="955d0-109">語法</span><span class="sxs-lookup"><span data-stu-id="955d0-109">Syntax</span></span>
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="955d0-110">成員</span><span class="sxs-lookup"><span data-stu-id="955d0-110">Members</span></span>

`InputTensor`

<span data-ttu-id="955d0-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="955d0-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="955d0-112">要從中讀取的 tensor。</span><span class="sxs-lookup"><span data-stu-id="955d0-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="955d0-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="955d0-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="955d0-114">包含索引的 tensor。</span><span class="sxs-lookup"><span data-stu-id="955d0-114">A tensor containing the indices.</span></span> <span data-ttu-id="955d0-115">此 tensor 的 *DimensionCount* 必須符合 *InputTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="955d0-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="955d0-116">*IndicesTensor* 的最後一個維度實際上是每個索引元組的座標數目，而不得超過 *InputTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="955d0-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="955d0-117">例如，大小 `{1,4,5,2}` 為 *IndicesDimensionCount* = 3 的索引 tensor，表示索引為 *InputTensor* 的2值座標元組4x5 陣列。</span><span class="sxs-lookup"><span data-stu-id="955d0-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="955d0-118">從開始 `DML_FEATURE_LEVEL_3_0` ，當使用帶正負號的整數型別搭配這個 tensor 時，這個運算子支援負的索引值。</span><span class="sxs-lookup"><span data-stu-id="955d0-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="955d0-119">負索引會解讀為相對於個別維度的結尾。</span><span class="sxs-lookup"><span data-stu-id="955d0-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="955d0-120">例如，-1 的索引指的是該維度的最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="955d0-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="955d0-121">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="955d0-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="955d0-122">包含新值的 tensor，用來取代對應索引的現有輸入值。</span><span class="sxs-lookup"><span data-stu-id="955d0-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="955d0-123">此 tensor 的 *DimensionCount* 必須符合 *InputTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="955d0-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="955d0-124">預期的 *UpdatesTensor 大小* 為 IndicesTensor 的串連 *。* 大小的前置區段和 *InputTensor。大小* 尾端區段可產生下列各項。</span><span class="sxs-lookup"><span data-stu-id="955d0-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="955d0-125">這些維度會靠右對齊，並在必要時前置1值以滿足 *UpdatesTensor. DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="955d0-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="955d0-126">以下為範例。</span><span class="sxs-lookup"><span data-stu-id="955d0-126">Here's an example.</span></span>

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

<span data-ttu-id="955d0-127">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="955d0-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="955d0-128">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="955d0-128">The tensor to write the results to.</span></span> <span data-ttu-id="955d0-129">這個 tensor 的 *大小* 和 *資料類型* 必須符合 *InputTensor 的大小*。</span><span class="sxs-lookup"><span data-stu-id="955d0-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="955d0-130">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="955d0-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="955d0-131">*InputTensor* 中的實際輸入維度數目，在略過任何不相關的前置專案之後（範圍 [1， *InputTensor. DimensionCount*) ）。</span><span class="sxs-lookup"><span data-stu-id="955d0-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="955d0-132">例如，假設 *InputTensor 的大小* = {1,1,4,6} 和 *InputDimensionCount* = 3，則實際有意義的索引為 {1,4,6} 。</span><span class="sxs-lookup"><span data-stu-id="955d0-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="955d0-133">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="955d0-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="955d0-134">在忽略任何不相關的前置專案（範圍 [1， *IndicesTensor. DimensionCount*) ）後， *IndicesTensor* 內實際的索引維度數目。</span><span class="sxs-lookup"><span data-stu-id="955d0-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="955d0-135">例如，假設 *IndicesTensor 的大小* = {1,1,4,6} 和 *IndicesDimensionCount* = 3，則實際有意義的索引為 {1,4,6} 。</span><span class="sxs-lookup"><span data-stu-id="955d0-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="955d0-136">範例</span><span class="sxs-lookup"><span data-stu-id="955d0-136">Examples</span></span>

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a><span data-ttu-id="955d0-137">可用性</span><span class="sxs-lookup"><span data-stu-id="955d0-137">Availability</span></span>
<span data-ttu-id="955d0-138">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="955d0-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="955d0-139">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="955d0-139">Tensor constraints</span></span>
* <span data-ttu-id="955d0-140">*IndicesTensor*、 *InputTensor*、 *OutputTensor* 和 `UpdatesTensor` 必須有相同的 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="955d0-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="955d0-141">*InputTensor*、 *OutputTensor* 和 `UpdatesTensor` 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="955d0-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="955d0-142">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="955d0-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="955d0-143">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="955d0-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="955d0-144">張</span><span class="sxs-lookup"><span data-stu-id="955d0-144">Tensor</span></span> | <span data-ttu-id="955d0-145">類型</span><span class="sxs-lookup"><span data-stu-id="955d0-145">Kind</span></span> | <span data-ttu-id="955d0-146">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="955d0-146">Supported dimension counts</span></span> | <span data-ttu-id="955d0-147">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="955d0-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="955d0-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="955d0-148">InputTensor</span></span> | <span data-ttu-id="955d0-149">輸入</span><span class="sxs-lookup"><span data-stu-id="955d0-149">Input</span></span> | <span data-ttu-id="955d0-150">1至8</span><span class="sxs-lookup"><span data-stu-id="955d0-150">1 to 8</span></span> | <span data-ttu-id="955d0-151">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="955d0-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="955d0-152">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="955d0-152">IndicesTensor</span></span> | <span data-ttu-id="955d0-153">輸入</span><span class="sxs-lookup"><span data-stu-id="955d0-153">Input</span></span> | <span data-ttu-id="955d0-154">1至8</span><span class="sxs-lookup"><span data-stu-id="955d0-154">1 to 8</span></span> | <span data-ttu-id="955d0-155">INT64、INT32、UINT64、UINT32</span><span class="sxs-lookup"><span data-stu-id="955d0-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="955d0-156">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="955d0-156">UpdatesTensor</span></span> | <span data-ttu-id="955d0-157">輸入</span><span class="sxs-lookup"><span data-stu-id="955d0-157">Input</span></span> | <span data-ttu-id="955d0-158">1至8</span><span class="sxs-lookup"><span data-stu-id="955d0-158">1 to 8</span></span> | <span data-ttu-id="955d0-159">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="955d0-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="955d0-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="955d0-160">OutputTensor</span></span> | <span data-ttu-id="955d0-161">輸出</span><span class="sxs-lookup"><span data-stu-id="955d0-161">Output</span></span> | <span data-ttu-id="955d0-162">1至8</span><span class="sxs-lookup"><span data-stu-id="955d0-162">1 to 8</span></span> | <span data-ttu-id="955d0-163">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="955d0-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="955d0-164">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="955d0-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="955d0-165">張</span><span class="sxs-lookup"><span data-stu-id="955d0-165">Tensor</span></span> | <span data-ttu-id="955d0-166">類型</span><span class="sxs-lookup"><span data-stu-id="955d0-166">Kind</span></span> | <span data-ttu-id="955d0-167">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="955d0-167">Supported dimension counts</span></span> | <span data-ttu-id="955d0-168">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="955d0-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="955d0-169">InputTensor</span><span class="sxs-lookup"><span data-stu-id="955d0-169">InputTensor</span></span> | <span data-ttu-id="955d0-170">輸入</span><span class="sxs-lookup"><span data-stu-id="955d0-170">Input</span></span> | <span data-ttu-id="955d0-171">4</span><span class="sxs-lookup"><span data-stu-id="955d0-171">4</span></span> | <span data-ttu-id="955d0-172">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="955d0-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="955d0-173">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="955d0-173">IndicesTensor</span></span> | <span data-ttu-id="955d0-174">輸入</span><span class="sxs-lookup"><span data-stu-id="955d0-174">Input</span></span> | <span data-ttu-id="955d0-175">4</span><span class="sxs-lookup"><span data-stu-id="955d0-175">4</span></span> | <span data-ttu-id="955d0-176">UINT32</span><span class="sxs-lookup"><span data-stu-id="955d0-176">UINT32</span></span> |
| <span data-ttu-id="955d0-177">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="955d0-177">UpdatesTensor</span></span> | <span data-ttu-id="955d0-178">輸入</span><span class="sxs-lookup"><span data-stu-id="955d0-178">Input</span></span> | <span data-ttu-id="955d0-179">4</span><span class="sxs-lookup"><span data-stu-id="955d0-179">4</span></span> | <span data-ttu-id="955d0-180">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="955d0-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="955d0-181">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="955d0-181">OutputTensor</span></span> | <span data-ttu-id="955d0-182">輸出</span><span class="sxs-lookup"><span data-stu-id="955d0-182">Output</span></span> | <span data-ttu-id="955d0-183">4</span><span class="sxs-lookup"><span data-stu-id="955d0-183">4</span></span> | <span data-ttu-id="955d0-184">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="955d0-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="955d0-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="955d0-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="955d0-186">**標頭**</span><span class="sxs-lookup"><span data-stu-id="955d0-186">**Header**</span></span> | <span data-ttu-id="955d0-187">directml。h</span><span class="sxs-lookup"><span data-stu-id="955d0-187">directml.h</span></span> |