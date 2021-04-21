---
UID: NS:directml.DML_SPACE_TO_DEPTH1_OPERATOR_DESC
title: DML_SPACE_TO_DEPTH1_OPERATOR_DESC
description: 將空間資料的區塊重新排列為深度。 運算子會輸出輸入 tensor 的複本，其中高度和寬度維度的值會移至深度維度。
helpviewer_keywords:
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure
- direct3d12.dml_space_to_depth1_operator_desc
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
ms.openlocfilehash: 35e64d83fa6b8df42428869f72249e9846e50596
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802868"
---
# <a name="dml_space_to_depth1_operator_desc-structure-directmlh"></a><span data-ttu-id="f72f9-104">DML_SPACE_TO_DEPTH1_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="f72f9-104">DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="f72f9-105">將空間資料的區塊重新排列為深度。</span><span class="sxs-lookup"><span data-stu-id="f72f9-105">Rearranges blocks of spatial data into depth.</span></span> <span data-ttu-id="f72f9-106">運算子會輸出輸入 tensor 的複本，其中高度和寬度維度的值會移至深度維度。</span><span class="sxs-lookup"><span data-stu-id="f72f9-106">The operator outputs a copy of the input tensor where values from the height and width dimensions are moved to the depth dimension.</span></span>

<span data-ttu-id="f72f9-107">這是 [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md)的反向轉換。</span><span class="sxs-lookup"><span data-stu-id="f72f9-107">This is the inverse transformation of [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f72f9-108">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f72f9-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f72f9-109">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="f72f9-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f72f9-110">語法</span><span class="sxs-lookup"><span data-stu-id="f72f9-110">Syntax</span></span>
```cpp
struct DML_SPACE_TO_DEPTH1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="f72f9-111">成員</span><span class="sxs-lookup"><span data-stu-id="f72f9-111">Members</span></span>

`InputTensor`

<span data-ttu-id="f72f9-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f72f9-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f72f9-113">要從中讀取的 tensor。</span><span class="sxs-lookup"><span data-stu-id="f72f9-113">The tensor to read from.</span></span> <span data-ttu-id="f72f9-114">輸入 tensor 的維度是 `{ Batch, Channels, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="f72f9-114">The input tensor's dimensions are `{ Batch, Channels, Height, Width }`.</span></span>


`OutputTensor`

<span data-ttu-id="f72f9-115">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f72f9-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f72f9-116">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="f72f9-116">The tensor to write the results to.</span></span> <span data-ttu-id="f72f9-117">輸出 tensor 的維度是 `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }` 。</span><span class="sxs-lookup"><span data-stu-id="f72f9-117">The output tensor's dimensions are `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }`.</span></span>


`BlockSize`

<span data-ttu-id="f72f9-118">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f72f9-118">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f72f9-119">移動之區塊的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="f72f9-119">The width and height of the Blocks that are moved.</span></span>


`Order`

<span data-ttu-id="f72f9-120">類型： **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="f72f9-120">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="f72f9-121">請參閱 [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)。</span><span class="sxs-lookup"><span data-stu-id="f72f9-121">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f72f9-122">範例</span><span class="sxs-lookup"><span data-stu-id="f72f9-122">Examples</span></span>

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="f72f9-123">範例 1.</span><span class="sxs-lookup"><span data-stu-id="f72f9-123">Example 1.</span></span> <span data-ttu-id="f72f9-124">深度資料行資料列順序</span><span class="sxs-lookup"><span data-stu-id="f72f9-124">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]

OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
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

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="f72f9-125">範例 2.</span><span class="sxs-lookup"><span data-stu-id="f72f9-125">Example 2.</span></span> <span data-ttu-id="f72f9-126">資料行資料列深度順序</span><span class="sxs-lookup"><span data-stu-id="f72f9-126">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
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


## <a name="remarks"></a><span data-ttu-id="f72f9-127">備註</span><span class="sxs-lookup"><span data-stu-id="f72f9-127">Remarks</span></span>
<span data-ttu-id="f72f9-128">當 *Order* 參數設定為 [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md)時，這個運算子相當於 [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc)。</span><span class="sxs-lookup"><span data-stu-id="f72f9-128">When the *Order* parameter is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), this operator is equivalent to [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="f72f9-129">可用性</span><span class="sxs-lookup"><span data-stu-id="f72f9-129">Availability</span></span>
<span data-ttu-id="f72f9-130">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="f72f9-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f72f9-131">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="f72f9-131">Tensor constraints</span></span>
<span data-ttu-id="f72f9-132">*InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="f72f9-132">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f72f9-133">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="f72f9-133">Tensor support</span></span>
| <span data-ttu-id="f72f9-134">張</span><span class="sxs-lookup"><span data-stu-id="f72f9-134">Tensor</span></span> | <span data-ttu-id="f72f9-135">類型</span><span class="sxs-lookup"><span data-stu-id="f72f9-135">Kind</span></span> | <span data-ttu-id="f72f9-136">維度</span><span class="sxs-lookup"><span data-stu-id="f72f9-136">Dimensions</span></span> | <span data-ttu-id="f72f9-137">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="f72f9-137">Supported dimension counts</span></span> | <span data-ttu-id="f72f9-138">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="f72f9-138">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="f72f9-139">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f72f9-139">InputTensor</span></span> | <span data-ttu-id="f72f9-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f72f9-140">Input</span></span> | <span data-ttu-id="f72f9-141">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="f72f9-141">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="f72f9-142">4</span><span class="sxs-lookup"><span data-stu-id="f72f9-142">4</span></span> | <span data-ttu-id="f72f9-143">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="f72f9-143">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f72f9-144">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f72f9-144">OutputTensor</span></span> | <span data-ttu-id="f72f9-145">輸出</span><span class="sxs-lookup"><span data-stu-id="f72f9-145">Output</span></span> | <span data-ttu-id="f72f9-146">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="f72f9-146">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="f72f9-147">4</span><span class="sxs-lookup"><span data-stu-id="f72f9-147">4</span></span> | <span data-ttu-id="f72f9-148">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="f72f9-148">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="f72f9-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="f72f9-149">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f72f9-150">**標頭**</span><span class="sxs-lookup"><span data-stu-id="f72f9-150">**Header**</span></span> | <span data-ttu-id="f72f9-151">directml。h</span><span class="sxs-lookup"><span data-stu-id="f72f9-151">directml.h</span></span> |