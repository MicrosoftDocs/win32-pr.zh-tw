---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: 將 tensor 的專案加總在軸上，將總和的執行總和寫入輸出 tensor 中。
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 2862a2add207b0bb6c41f5c1aabbc390797cba23
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803350"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="b531e-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="b531e-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b531e-104">將 tensor 的專案加總在軸上，將總和的執行總和寫入輸出 tensor 中。</span><span class="sxs-lookup"><span data-stu-id="b531e-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b531e-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="b531e-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b531e-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="b531e-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b531e-107">語法</span><span class="sxs-lookup"><span data-stu-id="b531e-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```

## <a name="members"></a><span data-ttu-id="b531e-108">成員</span><span class="sxs-lookup"><span data-stu-id="b531e-108">Members</span></span>

`InputTensor`

<span data-ttu-id="b531e-109">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b531e-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b531e-110">包含要加總之元素的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="b531e-110">The input tensor containing elements to be summed.</span></span>

`OutputTensor`

<span data-ttu-id="b531e-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b531e-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b531e-112">要寫入所產生累計總和的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="b531e-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="b531e-113">這個 tensor 的大小和資料類型必須與 *InputTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="b531e-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="b531e-114">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b531e-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b531e-115">要加總元素之維度的索引。</span><span class="sxs-lookup"><span data-stu-id="b531e-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="b531e-116">這個值必須小於 *InputTensor* 的 *DimensionCount* 。</span><span class="sxs-lookup"><span data-stu-id="b531e-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="b531e-117">類型： **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="b531e-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="b531e-118">[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)列舉的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b531e-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="b531e-119">如果設定為 **DML_AXIS_DIRECTION_INCREASING**，則會以遞增的元素索引沿著指定的軸沿著 tensor 來進行總和。</span><span class="sxs-lookup"><span data-stu-id="b531e-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="b531e-120">如果設定為 **DML_AXIS_DIRECTION_DECREASING**，則反轉為 true，而且會藉由遞減索引來進行專案的總和。</span><span class="sxs-lookup"><span data-stu-id="b531e-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>

`HasExclusiveSum`

<span data-ttu-id="b531e-121">類型： <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="b531e-121">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="b531e-122">若 **為 TRUE**，則將執行計數寫入至輸出 tensor 時，會排除目前元素的值。</span><span class="sxs-lookup"><span data-stu-id="b531e-122">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="b531e-123">如果 **為 FALSE**，則表示目前專案的值包含在執行中的計數內。</span><span class="sxs-lookup"><span data-stu-id="b531e-123">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="b531e-124">範例</span><span class="sxs-lookup"><span data-stu-id="b531e-124">Examples</span></span>

<span data-ttu-id="b531e-125">本節中的範例都使用具有下列屬性的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="b531e-125">The examples in this section all use an input tensor with the following properties.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-summation-across-horizontal-slivers"></a><span data-ttu-id="b531e-126">範例 1.</span><span class="sxs-lookup"><span data-stu-id="b531e-126">Example 1.</span></span> <span data-ttu-id="b531e-127">水準薄片之間的累計總和</span><span class="sxs-lookup"><span data-stu-id="b531e-127">Cumulative summation across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  3,  6, 11],     // i.e. [2, 2+1, 2+1+3, 2+1+3+5]
   [3, 11, 18, 21],     //      [...                   ]
   [9, 15, 17, 21]]]]   //      [...                   ]
```

### <a name="example-2-exclusive-sums"></a><span data-ttu-id="b531e-128">範例 2.</span><span class="sxs-lookup"><span data-stu-id="b531e-128">Example 2.</span></span> <span data-ttu-id="b531e-129">獨佔總和</span><span class="sxs-lookup"><span data-stu-id="b531e-129">Exclusive sums</span></span>

<span data-ttu-id="b531e-130">將 *HasExclusiveSum* 設為 **TRUE** ，會在寫入至輸出 tensor 時，從執行中的計數中排除目前專案的值。</span><span class="sxs-lookup"><span data-stu-id="b531e-130">Setting *HasExclusiveSum* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[0, 2,  3,  6],      // Notice the sum is written before adding the input,
   [0, 3, 11, 18],      // and the final total is not written to any output.
   [0, 9, 15, 17]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="b531e-131">範例 3.</span><span class="sxs-lookup"><span data-stu-id="b531e-131">Example 3.</span></span> <span data-ttu-id="b531e-132">軸方向</span><span class="sxs-lookup"><span data-stu-id="b531e-132">Axis direction</span></span>

<span data-ttu-id="b531e-133">將 *AxisDirection* 設定為 [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) 具有在計算執行中計數時反轉專案的遍歷順序的效果。</span><span class="sxs-lookup"><span data-stu-id="b531e-133">Setting the *AxisDirection* to [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[11,  9,  8,  5],    // i.e. [2+1+3+5, 1+3+5, 3+5, 5]
   [21, 18, 10,  3],    //      [...                   ]
   [21, 12,  6,  4]]]]  //      [...                   ]
```

### <a name="example-4-summing-along-a-different-axis"></a><span data-ttu-id="b531e-134">範例4。</span><span class="sxs-lookup"><span data-stu-id="b531e-134">Example 4.</span></span> <span data-ttu-id="b531e-135">沿著不同軸的總和</span><span class="sxs-lookup"><span data-stu-id="b531e-135">Summing along a different axis</span></span>

<span data-ttu-id="b531e-136">在此範例中，總和會垂直發生，沿著高度軸 (第二個維度) 。</span><span class="sxs-lookup"><span data-stu-id="b531e-136">In this example, the summation occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 5,  9, 10,  8],   //      [2+3,  ...]
   [14, 15, 12, 12]]]] //      [2+3+9 ...]
```

## <a name="remarks"></a><span data-ttu-id="b531e-137">備註</span><span class="sxs-lookup"><span data-stu-id="b531e-137">Remarks</span></span>
<span data-ttu-id="b531e-138">這個運算子支援就地執行，這表示允許 *OutputTensor* 在系結期間為 *InputTensor* 加上別名。</span><span class="sxs-lookup"><span data-stu-id="b531e-138">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="b531e-139">可用性</span><span class="sxs-lookup"><span data-stu-id="b531e-139">Availability</span></span>
<span data-ttu-id="b531e-140">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="b531e-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b531e-141">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="b531e-141">Tensor constraints</span></span>
<span data-ttu-id="b531e-142">*InputTensor* 和 *OutputTensor* 必須具有相同的 *資料類型* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="b531e-142">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b531e-143">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="b531e-143">Tensor support</span></span>
| <span data-ttu-id="b531e-144">張</span><span class="sxs-lookup"><span data-stu-id="b531e-144">Tensor</span></span> | <span data-ttu-id="b531e-145">類型</span><span class="sxs-lookup"><span data-stu-id="b531e-145">Kind</span></span> | <span data-ttu-id="b531e-146">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="b531e-146">Supported dimension counts</span></span> | <span data-ttu-id="b531e-147">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="b531e-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b531e-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="b531e-148">InputTensor</span></span> | <span data-ttu-id="b531e-149">輸入</span><span class="sxs-lookup"><span data-stu-id="b531e-149">Input</span></span> | <span data-ttu-id="b531e-150">4</span><span class="sxs-lookup"><span data-stu-id="b531e-150">4</span></span> | <span data-ttu-id="b531e-151">FLOAT32、FLOAT16、UINT32、UINT16</span><span class="sxs-lookup"><span data-stu-id="b531e-151">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="b531e-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b531e-152">OutputTensor</span></span> | <span data-ttu-id="b531e-153">輸出</span><span class="sxs-lookup"><span data-stu-id="b531e-153">Output</span></span> | <span data-ttu-id="b531e-154">4</span><span class="sxs-lookup"><span data-stu-id="b531e-154">4</span></span> | <span data-ttu-id="b531e-155">FLOAT32、FLOAT16、UINT32、UINT16</span><span class="sxs-lookup"><span data-stu-id="b531e-155">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="b531e-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="b531e-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b531e-157">**標頭**</span><span class="sxs-lookup"><span data-stu-id="b531e-157">**Header**</span></span> | <span data-ttu-id="b531e-158">directml。h</span><span class="sxs-lookup"><span data-stu-id="b531e-158">directml.h</span></span> |
