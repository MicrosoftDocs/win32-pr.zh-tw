---
UID: NS:directml.DML_DEPTH_TO_SPACE1_OPERATOR_DESC
title: DML_DEPTH_TO_SPACE1_OPERATOR_DESC
description: 重新排列 (permutes) 資料從深度到空間資料的區塊。 運算子會輸出輸入 tensor 的複本，其中深度維度的值會移至 [高度] 和 [寬度] 維度的空間區塊中。
helpviewer_keywords:
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure
- direct3d12.dml_depth_to_space1_operator_desc
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.openlocfilehash: 639bda0b8d398d24b01649635d3cfcbd2301a211
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106988090"
---
# <a name="dml_depth_to_space1_operator_desc-structure-directmlh"></a><span data-ttu-id="ecaea-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="ecaea-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="ecaea-105">重新排列 (permutes) 資料從深度到空間資料的區塊。</span><span class="sxs-lookup"><span data-stu-id="ecaea-105">Rearranges (permutes) data from depth into blocks of spatial data.</span></span> <span data-ttu-id="ecaea-106">運算子會輸出輸入 tensor 的複本，其中深度維度的值會移至 [高度] 和 [寬度] 維度的空間區塊中。</span><span class="sxs-lookup"><span data-stu-id="ecaea-106">The operator outputs a copy of the input tensor where values from the depth dimension are moved in spatial blocks to the height and width dimensions.</span></span>

<span data-ttu-id="ecaea-107">這是 [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md)的反向轉換。</span><span class="sxs-lookup"><span data-stu-id="ecaea-107">This is the inverse transformation of [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ecaea-108">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="ecaea-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="ecaea-109">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="ecaea-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecaea-110">語法</span><span class="sxs-lookup"><span data-stu-id="ecaea-110">Syntax</span></span>
```cpp
struct DML_DEPTH_TO_SPACE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="ecaea-111">成員</span><span class="sxs-lookup"><span data-stu-id="ecaea-111">Members</span></span>

`InputTensor`

<span data-ttu-id="ecaea-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ecaea-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ecaea-113">要從中讀取的 tensor。</span><span class="sxs-lookup"><span data-stu-id="ecaea-113">The tensor to read from.</span></span> <span data-ttu-id="ecaea-114">輸入 tensor 的維度是 `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="ecaea-114">The input tensor's dimensions are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`OutputTensor`

<span data-ttu-id="ecaea-115">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ecaea-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ecaea-116">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="ecaea-116">The tensor to write the results to.</span></span> <span data-ttu-id="ecaea-117">輸出 tensor 的維度如下 `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` ：</span><span class="sxs-lookup"><span data-stu-id="ecaea-117">The output tensor's dimensions are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`, where:</span></span>

* <span data-ttu-id="ecaea-118">OutputChannelCount 會計算為 InputChannelCount/ (`BlockSize`  \*  `BlockSize`) </span><span class="sxs-lookup"><span data-stu-id="ecaea-118">OutputChannelCount is computed as InputChannelCount / (`BlockSize` \* `BlockSize`)</span></span>
* <span data-ttu-id="ecaea-119">OutputHeight 的計算方式為 InputHeight \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="ecaea-119">OutputHeight is computed as InputHeight \* `BlockSize`</span></span>
* <span data-ttu-id="ecaea-120">OutputWidth 的計算方式為 InputWidth \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="ecaea-120">OutputWidth is computed as InputWidth \* `BlockSize`</span></span>


`BlockSize`

<span data-ttu-id="ecaea-121">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ecaea-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ecaea-122">移動之區塊的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="ecaea-122">The width and height of the blocks that are moved.</span></span>


`Order`

<span data-ttu-id="ecaea-123">類型： **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="ecaea-123">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="ecaea-124">請參閱 [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)。</span><span class="sxs-lookup"><span data-stu-id="ecaea-124">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ecaea-125">範例</span><span class="sxs-lookup"><span data-stu-id="ecaea-125">Examples</span></span>

<span data-ttu-id="ecaea-126">本節中的範例都使用下列輸入。</span><span class="sxs-lookup"><span data-stu-id="ecaea-126">The examples in this section all use the input below.</span></span>

```
InputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="ecaea-127">範例 1.</span><span class="sxs-lookup"><span data-stu-id="ecaea-127">Example 1.</span></span> <span data-ttu-id="ecaea-128">深度資料行資料列順序</span><span class="sxs-lookup"><span data-stu-id="ecaea-128">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="ecaea-129">範例 2.</span><span class="sxs-lookup"><span data-stu-id="ecaea-129">Example 2.</span></span> <span data-ttu-id="ecaea-130">資料行資料列深度順序</span><span class="sxs-lookup"><span data-stu-id="ecaea-130">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
```


## <a name="remarks"></a><span data-ttu-id="ecaea-131">備註</span><span class="sxs-lookup"><span data-stu-id="ecaea-131">Remarks</span></span>
<span data-ttu-id="ecaea-132">當 *Order* 設定為 [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md)時， **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** 相當於 [DML_DEPTH_TO_SPACE_OPERATOR_DESC]()。</span><span class="sxs-lookup"><span data-stu-id="ecaea-132">When *Order* is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** is equivalent to [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span></span>

## <a name="availability"></a><span data-ttu-id="ecaea-133">可用性</span><span class="sxs-lookup"><span data-stu-id="ecaea-133">Availability</span></span>
<span data-ttu-id="ecaea-134">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="ecaea-134">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ecaea-135">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="ecaea-135">Tensor constraints</span></span>
<span data-ttu-id="ecaea-136">*InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="ecaea-136">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ecaea-137">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="ecaea-137">Tensor support</span></span>
| <span data-ttu-id="ecaea-138">張</span><span class="sxs-lookup"><span data-stu-id="ecaea-138">Tensor</span></span> | <span data-ttu-id="ecaea-139">類型</span><span class="sxs-lookup"><span data-stu-id="ecaea-139">Kind</span></span> | <span data-ttu-id="ecaea-140">維度</span><span class="sxs-lookup"><span data-stu-id="ecaea-140">Dimensions</span></span> | <span data-ttu-id="ecaea-141">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="ecaea-141">Supported dimension counts</span></span> | <span data-ttu-id="ecaea-142">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="ecaea-142">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="ecaea-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="ecaea-143">InputTensor</span></span> | <span data-ttu-id="ecaea-144">輸入</span><span class="sxs-lookup"><span data-stu-id="ecaea-144">Input</span></span> | <span data-ttu-id="ecaea-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="ecaea-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="ecaea-146">4</span><span class="sxs-lookup"><span data-stu-id="ecaea-146">4</span></span> | <span data-ttu-id="ecaea-147">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="ecaea-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="ecaea-148">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="ecaea-148">OutputTensor</span></span> | <span data-ttu-id="ecaea-149">輸出</span><span class="sxs-lookup"><span data-stu-id="ecaea-149">Output</span></span> | <span data-ttu-id="ecaea-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="ecaea-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="ecaea-151">4</span><span class="sxs-lookup"><span data-stu-id="ecaea-151">4</span></span> | <span data-ttu-id="ecaea-152">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="ecaea-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="ecaea-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecaea-153">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ecaea-154">**標頭**</span><span class="sxs-lookup"><span data-stu-id="ecaea-154">**Header**</span></span> | <span data-ttu-id="ecaea-155">directml。h</span><span class="sxs-lookup"><span data-stu-id="ecaea-155">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ecaea-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecaea-156">See also</span></span>

* [<span data-ttu-id="ecaea-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="ecaea-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc)
* [<span data-ttu-id="ecaea-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="ecaea-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)