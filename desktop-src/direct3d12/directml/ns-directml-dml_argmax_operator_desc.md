---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: 輸出一或多個輸入 tensor 維度內最大值元素的索引。
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 17ccadc1228ea833ea1f1b3235e97430ac000514
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106984266"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a><span data-ttu-id="096b3-103">DML_ARGMAX_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="096b3-103">DML_ARGMAX_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="096b3-104">輸出一或多個輸入 tensor 維度內最大值元素的索引。</span><span class="sxs-lookup"><span data-stu-id="096b3-104">Outputs the indices of the maximum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="096b3-105">每個輸出元素都是在輸入 tensor 的子集上套用 *argmax* 減少的結果。</span><span class="sxs-lookup"><span data-stu-id="096b3-105">Each output element is the result of applying an *argmax* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="096b3-106">*Argmax* 函式會輸出一組輸入元素內最大值元素的索引。</span><span class="sxs-lookup"><span data-stu-id="096b3-106">The *argmax* function outputs the index of the maximum-valued element within a set of input elements.</span></span> <span data-ttu-id="096b3-107">每個減少所涉及的輸入元素是由提供的輸入軸所決定。</span><span class="sxs-lookup"><span data-stu-id="096b3-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="096b3-108">同樣地，每個輸出索引都與提供的輸入軸有關。</span><span class="sxs-lookup"><span data-stu-id="096b3-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="096b3-109">如果指定了所有的輸入軸，則運算子會套用單一 *argmax* 減少，並產生單一的輸出元素。</span><span class="sxs-lookup"><span data-stu-id="096b3-109">If all input axes are specified, then the operator applies a single *argmax* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="096b3-110">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="096b3-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="096b3-111">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="096b3-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="096b3-112">語法</span><span class="sxs-lookup"><span data-stu-id="096b3-112">Syntax</span></span>
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="096b3-113">成員</span><span class="sxs-lookup"><span data-stu-id="096b3-113">Members</span></span>

`InputTensor`

<span data-ttu-id="096b3-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="096b3-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="096b3-115">要從中讀取的 tensor。</span><span class="sxs-lookup"><span data-stu-id="096b3-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="096b3-116">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="096b3-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="096b3-117">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="096b3-117">The tensor to write the results to.</span></span> <span data-ttu-id="096b3-118">每個輸出元素都是從 *InputTensor* 的元素子集 *argmax* 減少的結果。</span><span class="sxs-lookup"><span data-stu-id="096b3-118">Each output element is the result of an *argmax* reduction on a subset of elements from the *InputTensor*.</span></span> 

- <span data-ttu-id="096b3-119">*DimensionCount* 必須符合 *InputTensor。 DimensionCount* (保留) 的輸入 tensor 的次序。</span><span class="sxs-lookup"><span data-stu-id="096b3-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="096b3-120">*大小* 必須符合 *InputTensor 的大小*，但縮減 *軸* 中包含的維度除外，其大小必須為1。</span><span class="sxs-lookup"><span data-stu-id="096b3-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="096b3-121">類型： **[UINT](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="096b3-121">Type: **[UINT](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="096b3-122">要減少的軸數目。</span><span class="sxs-lookup"><span data-stu-id="096b3-122">The number of axes to reduce.</span></span> <span data-ttu-id="096b3-123">此欄位會決定 *軸* 陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="096b3-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="096b3-124">類型： \_ Field_size \_ (AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="096b3-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="096b3-125">要減少的軸。</span><span class="sxs-lookup"><span data-stu-id="096b3-125">The axes along which to reduce.</span></span> <span data-ttu-id="096b3-126">值必須在範圍內 `[0, InputTensor.DimensionCount - 1]` 。</span><span class="sxs-lookup"><span data-stu-id="096b3-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="096b3-127">類型： **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="096b3-127">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="096b3-128">決定當多個輸入專案具有相同值時要選取的索引。</span><span class="sxs-lookup"><span data-stu-id="096b3-128">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="096b3-129">**DML_AXIS_DIRECTION_INCREASING** 會傳回第一個最大值元素的索引 (例如， `argmax({3,2,1,2,3}) = 0`) </span><span class="sxs-lookup"><span data-stu-id="096b3-129">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first maximum-valued element (for example, `argmax({3,2,1,2,3}) = 0`)</span></span>
- <span data-ttu-id="096b3-130">**DML_AXIS_DIRECTION_DECREASING** 會傳回最後一個最大值元素的索引 (例如， `argmax({3,2,1,2,3}) = 4`) </span><span class="sxs-lookup"><span data-stu-id="096b3-130">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last maximum-valued element (for example, `argmax({3,2,1,2,3}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="096b3-131">範例</span><span class="sxs-lookup"><span data-stu-id="096b3-131">Examples</span></span>

<span data-ttu-id="096b3-132">本節中的範例都使用相同的二維輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="096b3-132">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a><span data-ttu-id="096b3-133">範例 1.</span><span class="sxs-lookup"><span data-stu-id="096b3-133">Example 1.</span></span> <span data-ttu-id="096b3-134">將 *argmax* 套用至資料行</span><span class="sxs-lookup"><span data-stu-id="096b3-134">Applying *argmax* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a><span data-ttu-id="096b3-135">範例 2.</span><span class="sxs-lookup"><span data-stu-id="096b3-135">Example 2.</span></span> <span data-ttu-id="096b3-136">將 *argmax* 套用至資料列</span><span class="sxs-lookup"><span data-stu-id="096b3-136">Applying *argmax* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a><span data-ttu-id="096b3-137">範例 3.</span><span class="sxs-lookup"><span data-stu-id="096b3-137">Example 3.</span></span> <span data-ttu-id="096b3-138">將 *argmax* 套用至所有座標軸 (整個 tensor) </span><span class="sxs-lookup"><span data-stu-id="096b3-138">Applying *argmax* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="096b3-139">備註</span><span class="sxs-lookup"><span data-stu-id="096b3-139">Remarks</span></span>
<span data-ttu-id="096b3-140">輸出 tensor 的大小必須與輸入 tensor 大小相同，但減少的軸必須是1。</span><span class="sxs-lookup"><span data-stu-id="096b3-140">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="096b3-141">當 [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) *AxisDirection* 時，此 API 相當於 [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc)與 [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function)。</span><span class="sxs-lookup"><span data-stu-id="096b3-141">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="096b3-142">這項功能的子集是透過 [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) 運算子公開，並且在先前的 DirectML 功能層級上受到支援。</span><span class="sxs-lookup"><span data-stu-id="096b3-142">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="096b3-143">可用性</span><span class="sxs-lookup"><span data-stu-id="096b3-143">Availability</span></span>
<span data-ttu-id="096b3-144">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="096b3-144">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="096b3-145">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="096b3-145">Tensor constraints</span></span>
<span data-ttu-id="096b3-146">*InputTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="096b3-146">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="096b3-147">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="096b3-147">Tensor support</span></span>
| <span data-ttu-id="096b3-148">張</span><span class="sxs-lookup"><span data-stu-id="096b3-148">Tensor</span></span> | <span data-ttu-id="096b3-149">類型</span><span class="sxs-lookup"><span data-stu-id="096b3-149">Kind</span></span> | <span data-ttu-id="096b3-150">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="096b3-150">Supported dimension counts</span></span> | <span data-ttu-id="096b3-151">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="096b3-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="096b3-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="096b3-152">InputTensor</span></span> | <span data-ttu-id="096b3-153">輸入</span><span class="sxs-lookup"><span data-stu-id="096b3-153">Input</span></span> | <span data-ttu-id="096b3-154">1至8</span><span class="sxs-lookup"><span data-stu-id="096b3-154">1 to 8</span></span> | <span data-ttu-id="096b3-155">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="096b3-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="096b3-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="096b3-156">OutputTensor</span></span> | <span data-ttu-id="096b3-157">輸出</span><span class="sxs-lookup"><span data-stu-id="096b3-157">Output</span></span> | <span data-ttu-id="096b3-158">1至8</span><span class="sxs-lookup"><span data-stu-id="096b3-158">1 to 8</span></span> | <span data-ttu-id="096b3-159">INT64、INT32、UINT64、UINT32</span><span class="sxs-lookup"><span data-stu-id="096b3-159">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="096b3-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="096b3-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="096b3-161">**標頭**</span><span class="sxs-lookup"><span data-stu-id="096b3-161">**Header**</span></span> | <span data-ttu-id="096b3-162">directml。h</span><span class="sxs-lookup"><span data-stu-id="096b3-162">directml.h</span></span> |