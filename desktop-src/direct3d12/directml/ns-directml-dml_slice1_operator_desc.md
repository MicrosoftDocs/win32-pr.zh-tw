---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: " (輸入 tensor 的「配量」 ) 解壓縮單一子領域。"
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: 06721a7484426eb293494156a2ec23db6fbf0a6b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106981916"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a><span data-ttu-id="c7fd6-103">DML_SLICE1_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="c7fd6-103">DML_SLICE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="c7fd6-104"> (輸入 tensor 的「配量」 ) 解壓縮單一子領域。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-104">Extracts a single subregion (a "slice") of an input tensor.</span></span>

<span data-ttu-id="c7fd6-105">[ *輸入] 視窗* 描述配量中要考慮的輸入 tensor 範圍。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-105">The *input window* describes the bounds of the input tensor to consider in the slice.</span></span> <span data-ttu-id="c7fd6-106">此視窗會使用每個維度的三個值來定義。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-106">The window is defined using three values for each dimension.</span></span>

- <span data-ttu-id="c7fd6-107">*位移* 會將 *視窗的開頭* 標示為維度。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-107">The *offset* marks the *beginning of the window* in a dimension.</span></span>
- <span data-ttu-id="c7fd6-108">*大小* 會在維度中標示視窗的範圍。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-108">The *size* marks the extent of the window in a dimension.</span></span> <span data-ttu-id="c7fd6-109">維度中 *視窗的結尾* 是 `offset + size - 1` 。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-109">The *end of the window* in a dimension is `offset + size - 1`.</span></span>
- <span data-ttu-id="c7fd6-110">*Stride* 表示如何遍歷維度中的元素。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-110">The *stride* indicates how to traverse the elements in a dimension.</span></span>
  - <span data-ttu-id="c7fd6-111">Stride 的大小表示在視窗中複製時要前進的元素數目。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-111">The magnitude of the stride indicates how many elements to advance when copying within the window.</span></span>
  - <span data-ttu-id="c7fd6-112">如果 stride 是正數，則會從維度中視窗的 *開頭* 開始複製元素。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-112">If a stride is positive, elements are copied starting at the *beginning* of the window in the dimension.</span></span>
  - <span data-ttu-id="c7fd6-113">如果跨距是負數，則會從維度中視窗的 *結尾* 開始複製專案。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-113">If a stride is negative, elements are copied starting at the *end* of the window in the dimension.</span></span>

<span data-ttu-id="c7fd6-114">下列虛擬程式碼說明如何使用 [輸入] 視窗複製元素。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-114">The following pseudo-code illustrates how elements are copied using the input window.</span></span> <span data-ttu-id="c7fd6-115">請注意，維度中的元素如何從開頭到結尾以正面的跨距複製，並從結尾複製到以負的 stride 開始。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-115">Note how elements in a dimension are copied from start to end with a positive stride, and copied from end to start with a negative stride.</span></span>

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

<span data-ttu-id="c7fd6-116">輸入視窗不得在任何維度中都是空的，而且視窗不得延伸到超出輸入 (tensor 的維度，) 不允許超出範圍的讀取。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-116">The input window mustn't be empty in any dimension, and the window mustn't extend beyond the dimensions of the input tensor (out-of-bounds reads aren't permitted).</span></span> <span data-ttu-id="c7fd6-117">視窗的大小和進展實際上會限制可從輸入 tensor 的每個維度複製的元素數目 `i` 。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-117">The window's size and strides effectively limit the number of elements that may be copied from each dimension `i` of the input tensor.</span></span>

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

<span data-ttu-id="c7fd6-118">輸出 tensor 不需要複製視窗內所有可連接的元素。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-118">The output tensor isn't required to copy all reachable elements within the window.</span></span> <span data-ttu-id="c7fd6-119">配量有效，只要 `1 <= OutputSizes[i] <= MaxCopiedElements[i]` 。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-119">The slice is valid so long as `1 <= OutputSizes[i] <= MaxCopiedElements[i]`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7fd6-120">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-120">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="c7fd6-121">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-121">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fd6-122">語法</span><span class="sxs-lookup"><span data-stu-id="c7fd6-122">Syntax</span></span>
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a><span data-ttu-id="c7fd6-123">成員</span><span class="sxs-lookup"><span data-stu-id="c7fd6-123">Members</span></span>

`InputTensor`

<span data-ttu-id="c7fd6-124">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c7fd6-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c7fd6-125">要從中解壓縮配量的 tensor。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-125">The tensor to extract slices from.</span></span>


`OutputTensor`

<span data-ttu-id="c7fd6-126">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c7fd6-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c7fd6-127">寫入切割資料結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-127">The tensor to write the sliced data results to.</span></span>


`DimensionCount`

<span data-ttu-id="c7fd6-128">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c7fd6-128">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c7fd6-129">維度的數目。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-129">The number of dimensions.</span></span> <span data-ttu-id="c7fd6-130">此欄位會決定 *InputWindowOffsets*、 *InputWindowSizes* 和 *InputWindowStrides* 陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-130">This field determines the size of the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="c7fd6-131">此值必須與輸入和輸出張量的 *DimensionCount* 相符。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-131">This value must match the *DimensionCount* of the input and output tensors.</span></span> <span data-ttu-id="c7fd6-132">此值必須介於1和8之間，其開頭 `DML_FEATURE_LEVEL_3_0` 為; 較早的功能層級需要值為4或5。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-132">This value must be between 1 and 8, inclusively, starting from `DML_FEATURE_LEVEL_3_0`; earlier feature levels require a value of either 4 or 5.</span></span>


`InputWindowOffsets`

<span data-ttu-id="c7fd6-133">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="c7fd6-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="c7fd6-134">陣列，其中包含每個維度之輸入視窗的元素) 中的開始 (。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-134">An array containing the beginning (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="c7fd6-135">陣列中的值必須滿足條件約束 `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="c7fd6-135">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowSizes`

<span data-ttu-id="c7fd6-136">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="c7fd6-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="c7fd6-137">陣列，其中包含每個維度之輸入視窗) 專案中的範圍 (。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-137">An array containing the extent (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="c7fd6-138">陣列中的值必須滿足條件約束 `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="c7fd6-138">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowStrides`

<span data-ttu-id="c7fd6-139">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="c7fd6-139">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="c7fd6-140">陣列，其中包含在專案中每個輸入 tensor 維度的配量跨距。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-140">An array containing the slice's stride along each dimension of the input tensor, in elements.</span></span> <span data-ttu-id="c7fd6-141">Stride 的大小表示在輸入視窗內複製時要前進的元素數目。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-141">The magnitude of the stride indicates how many elements to advance when copying within the input window.</span></span> <span data-ttu-id="c7fd6-142">Stride 的正負號可決定是否要從視窗的開頭開始複製專案 (正跨距) 或視窗結尾 (負 stride) 。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-142">The sign of the stride determines if elements are copied starting at the beginning of the window (positive stride) or end of the window (negative stride).</span></span> <span data-ttu-id="c7fd6-143">進步可能不是0。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-143">Strides may not be 0.</span></span>

## <a name="examples"></a><span data-ttu-id="c7fd6-144">範例</span><span class="sxs-lookup"><span data-stu-id="c7fd6-144">Examples</span></span>

<span data-ttu-id="c7fd6-145">下列範例會使用相同的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-145">The following examples use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a><span data-ttu-id="c7fd6-146">範例 1.</span><span class="sxs-lookup"><span data-stu-id="c7fd6-146">Example 1.</span></span> <span data-ttu-id="c7fd6-147">具有正面進步的 Strided 配量</span><span class="sxs-lookup"><span data-stu-id="c7fd6-147">Strided slice with positive strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

<span data-ttu-id="c7fd6-148">複製的元素的計算方式如下。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-148">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a><span data-ttu-id="c7fd6-149">範例 2.</span><span class="sxs-lookup"><span data-stu-id="c7fd6-149">Example 2.</span></span> <span data-ttu-id="c7fd6-150">具有負面進步的 Strided 配量</span><span class="sxs-lookup"><span data-stu-id="c7fd6-150">Strided slice with negative strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

<span data-ttu-id="c7fd6-151">回想一下，具有負面視窗進展的維度會在該維度的輸入視窗結束時開始複製;這是藉由加入 `InputWindowSize[i] - 1` 至視窗位移來完成。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-151">Recall that dimensions with negative window strides start copying at the end of the input window for that dimension; this is done by adding `InputWindowSize[i] - 1` to the window offset.</span></span> <span data-ttu-id="c7fd6-152">具有正面 stride 的維度只會從開始 `InputWindowOffset[i]` 。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-152">Dimensions with a positive stride simply start at `InputWindowOffset[i]`.</span></span>
- <span data-ttu-id="c7fd6-153">軸 0 (`+1` 視窗 stride) 開始複製的時間 `InputWindowOffsets[0] = 0` 。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-153">Axis 0 (`+1` window stride) starts copying at `InputWindowOffsets[0] = 0`.</span></span> 
- <span data-ttu-id="c7fd6-154">軸 1 (`+1` 視窗 stride) 開始複製 `InputWindowOffsets[1] = 0` 。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-154">Axis 1 (`+1` window stride) starts copying at `InputWindowOffsets[1] = 0`.</span></span> 
- <span data-ttu-id="c7fd6-155">軸 2 (`-2` 視窗 stride) 開始複製的時間 `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` 。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-155">Axis 2 (`-2` window stride) starts copying at `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3`.</span></span> 
- <span data-ttu-id="c7fd6-156">軸 3 (`+2` 視窗 stride) 開始複製 `InputWindowOffsets[3] = 1` 。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-156">Axis 3 (`+2` window stride) starts copying at `InputWindowOffsets[3] = 1`.</span></span> 

<span data-ttu-id="c7fd6-157">複製的元素的計算方式如下。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-157">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a><span data-ttu-id="c7fd6-158">備註</span><span class="sxs-lookup"><span data-stu-id="c7fd6-158">Remarks</span></span>
<span data-ttu-id="c7fd6-159">這個運算子類似于 [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc)，但它有兩種重要的差異。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-159">This operator is similar to [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), but it differs in two important ways.</span></span>

- <span data-ttu-id="c7fd6-160">配量的進展可能是負數，可讓維度的值反轉。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-160">Slice strides may be negative, which allows reversing values along dimensions.</span></span>
- <span data-ttu-id="c7fd6-161">輸入視窗大小與輸出 tensor 大小不一定相同。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-161">The input window sizes are not necessarily the same as the output tensor sizes.</span></span>

## <a name="availability"></a><span data-ttu-id="c7fd6-162">可用性</span><span class="sxs-lookup"><span data-stu-id="c7fd6-162">Availability</span></span>
<span data-ttu-id="c7fd6-163">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-163">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c7fd6-164">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="c7fd6-164">Tensor constraints</span></span>
<span data-ttu-id="c7fd6-165">*InputTensor* 和 *OutputTensor* 必須具有相同的 *資料類型* 和 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="c7fd6-165">*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c7fd6-166">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="c7fd6-166">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="c7fd6-167">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="c7fd6-167">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="c7fd6-168">張</span><span class="sxs-lookup"><span data-stu-id="c7fd6-168">Tensor</span></span> | <span data-ttu-id="c7fd6-169">類型</span><span class="sxs-lookup"><span data-stu-id="c7fd6-169">Kind</span></span> | <span data-ttu-id="c7fd6-170">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="c7fd6-170">Supported dimension counts</span></span> | <span data-ttu-id="c7fd6-171">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="c7fd6-171">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c7fd6-172">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c7fd6-172">InputTensor</span></span> | <span data-ttu-id="c7fd6-173">輸入</span><span class="sxs-lookup"><span data-stu-id="c7fd6-173">Input</span></span> | <span data-ttu-id="c7fd6-174">1至8</span><span class="sxs-lookup"><span data-stu-id="c7fd6-174">1 to 8</span></span> | <span data-ttu-id="c7fd6-175">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="c7fd6-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c7fd6-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c7fd6-176">OutputTensor</span></span> | <span data-ttu-id="c7fd6-177">輸出</span><span class="sxs-lookup"><span data-stu-id="c7fd6-177">Output</span></span> | <span data-ttu-id="c7fd6-178">1至8</span><span class="sxs-lookup"><span data-stu-id="c7fd6-178">1 to 8</span></span> | <span data-ttu-id="c7fd6-179">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="c7fd6-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="c7fd6-180">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="c7fd6-180">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="c7fd6-181">張</span><span class="sxs-lookup"><span data-stu-id="c7fd6-181">Tensor</span></span> | <span data-ttu-id="c7fd6-182">類型</span><span class="sxs-lookup"><span data-stu-id="c7fd6-182">Kind</span></span> | <span data-ttu-id="c7fd6-183">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="c7fd6-183">Supported dimension counts</span></span> | <span data-ttu-id="c7fd6-184">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="c7fd6-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c7fd6-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c7fd6-185">InputTensor</span></span> | <span data-ttu-id="c7fd6-186">輸入</span><span class="sxs-lookup"><span data-stu-id="c7fd6-186">Input</span></span> | <span data-ttu-id="c7fd6-187">4到5</span><span class="sxs-lookup"><span data-stu-id="c7fd6-187">4 to 5</span></span> | <span data-ttu-id="c7fd6-188">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="c7fd6-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c7fd6-189">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c7fd6-189">OutputTensor</span></span> | <span data-ttu-id="c7fd6-190">輸出</span><span class="sxs-lookup"><span data-stu-id="c7fd6-190">Output</span></span> | <span data-ttu-id="c7fd6-191">4到5</span><span class="sxs-lookup"><span data-stu-id="c7fd6-191">4 to 5</span></span> | <span data-ttu-id="c7fd6-192">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="c7fd6-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="c7fd6-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7fd6-193">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c7fd6-194">**標頭**</span><span class="sxs-lookup"><span data-stu-id="c7fd6-194">**Header**</span></span> | <span data-ttu-id="c7fd6-195">directml。h</span><span class="sxs-lookup"><span data-stu-id="c7fd6-195">directml.h</span></span> |