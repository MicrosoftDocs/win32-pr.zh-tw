---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: 將 tensor 的元素乘以軸，並將執行中的產品計數寫入輸出 tensor 中。
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 68b001467496ab9affc559e76ecac5461902399c
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521194"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a><span data-ttu-id="36ed5-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml) </span><span class="sxs-lookup"><span data-stu-id="36ed5-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="36ed5-104">將 tensor 的元素乘以軸，並將執行中的產品計數寫入輸出 tensor 中。</span><span class="sxs-lookup"><span data-stu-id="36ed5-104">Multiplies the elements of a tensor along an axis, writing the running tally of the product into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36ed5-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="36ed5-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="36ed5-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="36ed5-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="36ed5-107">語法</span><span class="sxs-lookup"><span data-stu-id="36ed5-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a><span data-ttu-id="36ed5-108">成員</span><span class="sxs-lookup"><span data-stu-id="36ed5-108">Members</span></span>

`InputTensor`

<span data-ttu-id="36ed5-109">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="36ed5-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="36ed5-110">包含輸入資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="36ed5-110">A tensor containing the input data.</span></span> <span data-ttu-id="36ed5-111">這通常是在轉寄行程中提供作為 *InputTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="36ed5-111">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="36ed5-112">包含要相乘之元素的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="36ed5-112">The input tensor containing elements to be multiplied.</span></span>

`OutputTensor`

<span data-ttu-id="36ed5-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="36ed5-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="36ed5-114">要將產生的累計產品寫入其中的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="36ed5-114">The output tensor to write the resulting cumulative products to.</span></span> <span data-ttu-id="36ed5-115">這個 tensor 的大小和資料類型必須與 *InputTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="36ed5-115">This tensor must have the same sizes and data type as *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="36ed5-116">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="36ed5-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="36ed5-117">要將元素相乘的維度索引。</span><span class="sxs-lookup"><span data-stu-id="36ed5-117">The index of the dimension to multiply elements over.</span></span> <span data-ttu-id="36ed5-118">這個值必須小於 *InputTensor* 的 *DimensionCount* 。</span><span class="sxs-lookup"><span data-stu-id="36ed5-118">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="36ed5-119">類型： **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="36ed5-119">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="36ed5-120">[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)列舉的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="36ed5-120">One of the values of the [DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction) enumeration.</span></span> <span data-ttu-id="36ed5-121">如果設定為 **DML_AXIS_DIRECTION_INCREASING**，則會依指定的軸沿著遞增的元素索引來進行 tensor，以進行產品。</span><span class="sxs-lookup"><span data-stu-id="36ed5-121">If set to **DML_AXIS_DIRECTION_INCREASING**, then the product occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="36ed5-122">如果設定為 **DML_AXIS_DIRECTION_DECREASING**，則反向會是 true，而產品是藉由遞減索引來進行專案來進行。</span><span class="sxs-lookup"><span data-stu-id="36ed5-122">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true and the product occurs by traversing elements by descending index.</span></span>

`HasExclusiveProduct`

<span data-ttu-id="36ed5-123">類型： <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="36ed5-123">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="36ed5-124">若 **為 TRUE**，則將執行計數寫入至輸出 tensor 時，會排除目前元素的值。</span><span class="sxs-lookup"><span data-stu-id="36ed5-124">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="36ed5-125">如果 **為 FALSE**，則表示目前專案的值包含在執行中的計數內。</span><span class="sxs-lookup"><span data-stu-id="36ed5-125">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="36ed5-126">範例</span><span class="sxs-lookup"><span data-stu-id="36ed5-126">Examples</span></span>

<span data-ttu-id="36ed5-127">本節中的範例都使用相同的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="36ed5-127">The examples in this section all use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a><span data-ttu-id="36ed5-128">範例 1.</span><span class="sxs-lookup"><span data-stu-id="36ed5-128">Example 1.</span></span> <span data-ttu-id="36ed5-129">跨水準薄片的累積乘積</span><span class="sxs-lookup"><span data-stu-id="36ed5-129">Cumulative product across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a><span data-ttu-id="36ed5-130">範例 2.</span><span class="sxs-lookup"><span data-stu-id="36ed5-130">Example 2.</span></span> <span data-ttu-id="36ed5-131">專屬產品</span><span class="sxs-lookup"><span data-stu-id="36ed5-131">Exclusive products</span></span>

<span data-ttu-id="36ed5-132">將 *HasExclusiveProduct* 設為 **TRUE** ，會在寫入至輸出 tensor 時，從執行中的計數中排除目前專案的值。</span><span class="sxs-lookup"><span data-stu-id="36ed5-132">Setting *HasExclusiveProduct* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="36ed5-133">範例 3.</span><span class="sxs-lookup"><span data-stu-id="36ed5-133">Example 3.</span></span> <span data-ttu-id="36ed5-134">軸方向</span><span class="sxs-lookup"><span data-stu-id="36ed5-134">Axis direction</span></span>

<span data-ttu-id="36ed5-135">將 *AxisDirection* 設定為 [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) 具有在計算執行中計數時反轉專案的遍歷順序的效果。</span><span class="sxs-lookup"><span data-stu-id="36ed5-135">Setting the *AxisDirection* to [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a><span data-ttu-id="36ed5-136">範例4。</span><span class="sxs-lookup"><span data-stu-id="36ed5-136">Example 4.</span></span> <span data-ttu-id="36ed5-137">沿著不同的軸相乘</span><span class="sxs-lookup"><span data-stu-id="36ed5-137">Multiplying along a different axis</span></span>

<span data-ttu-id="36ed5-138">在此範例中，產品會垂直發生，而且高度軸 (第二個維度) 。</span><span class="sxs-lookup"><span data-stu-id="36ed5-138">In this example, the product occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a><span data-ttu-id="36ed5-139">備註</span><span class="sxs-lookup"><span data-stu-id="36ed5-139">Remarks</span></span>
<span data-ttu-id="36ed5-140">這個運算子支援就地執行，這表示在系結期間允許輸出 tensor 別名 *InputTensor* 。</span><span class="sxs-lookup"><span data-stu-id="36ed5-140">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="36ed5-141">可用性</span><span class="sxs-lookup"><span data-stu-id="36ed5-141">Availability</span></span>
<span data-ttu-id="36ed5-142">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。</span><span class="sxs-lookup"><span data-stu-id="36ed5-142">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="36ed5-143">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="36ed5-143">Tensor constraints</span></span>
<span data-ttu-id="36ed5-144">*InputTensor* 和 *OutputTensor* 必須具有相同的 *資料類型* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="36ed5-144">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="36ed5-145">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="36ed5-145">Tensor support</span></span>
| <span data-ttu-id="36ed5-146">張</span><span class="sxs-lookup"><span data-stu-id="36ed5-146">Tensor</span></span> | <span data-ttu-id="36ed5-147">種類</span><span class="sxs-lookup"><span data-stu-id="36ed5-147">Kind</span></span> | <span data-ttu-id="36ed5-148">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="36ed5-148">Supported dimension counts</span></span> | <span data-ttu-id="36ed5-149">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="36ed5-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="36ed5-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="36ed5-150">InputTensor</span></span> | <span data-ttu-id="36ed5-151">輸入</span><span class="sxs-lookup"><span data-stu-id="36ed5-151">Input</span></span> | <span data-ttu-id="36ed5-152">4</span><span class="sxs-lookup"><span data-stu-id="36ed5-152">4</span></span> | <span data-ttu-id="36ed5-153">FLOAT32、FLOAT16、UINT32、UINT16</span><span class="sxs-lookup"><span data-stu-id="36ed5-153">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="36ed5-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="36ed5-154">OutputTensor</span></span> | <span data-ttu-id="36ed5-155">輸出</span><span class="sxs-lookup"><span data-stu-id="36ed5-155">Output</span></span> | <span data-ttu-id="36ed5-156">4</span><span class="sxs-lookup"><span data-stu-id="36ed5-156">4</span></span> | <span data-ttu-id="36ed5-157">FLOAT32、FLOAT16、UINT32、UINT16</span><span class="sxs-lookup"><span data-stu-id="36ed5-157">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="36ed5-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="36ed5-158">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="36ed5-159">**標頭**</span><span class="sxs-lookup"><span data-stu-id="36ed5-159">**Header**</span></span> | <span data-ttu-id="36ed5-160">directml。h</span><span class="sxs-lookup"><span data-stu-id="36ed5-160">directml.h</span></span> |