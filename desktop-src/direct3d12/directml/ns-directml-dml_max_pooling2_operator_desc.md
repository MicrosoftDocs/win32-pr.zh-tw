---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: 在 [輸入] tensor 上，計算滑動視窗內各元素的最大值，並選擇性地傳回所選最大值的索引。
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803669"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a><span data-ttu-id="cbb59-103">DML_MAX_POOLING2_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="cbb59-103">DML_MAX_POOLING2_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="cbb59-104">在 [輸入] tensor 上，計算滑動視窗內各元素的最大值，並選擇性地傳回所選最大值的索引。</span><span class="sxs-lookup"><span data-stu-id="cbb59-104">Computes the maximum value across the elements within the sliding window over the input tensor, and optionally returns the indices of the maximum values selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbb59-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="cbb59-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="cbb59-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="cbb59-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cbb59-107">語法</span><span class="sxs-lookup"><span data-stu-id="cbb59-107">Syntax</span></span>
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a><span data-ttu-id="cbb59-108">成員</span><span class="sxs-lookup"><span data-stu-id="cbb59-108">Members</span></span>

`InputTensor`

<span data-ttu-id="cbb59-109">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbb59-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbb59-110"> `{ BatchCount, ChannelCount, Height, Width }` 如果 *InputTensor. DimensionCount* 是4，則為大小的輸入 Tensor， `{ BatchCount, ChannelCount, Depth, Height, Weight } ` 如果 *InputTensor. DimensionCount* 為5。</span><span class="sxs-lookup"><span data-stu-id="cbb59-110">An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` if *InputTensor.DimensionCount* is 4, and `{ BatchCount, ChannelCount, Depth, Height, Weight } `if *InputTensor.DimensionCount* is 5.</span></span>


`OutputTensor`

<span data-ttu-id="cbb59-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbb59-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbb59-112">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="cbb59-112">An output tensor to write the results to.</span></span> <span data-ttu-id="cbb59-113">輸出 tensor 的大小可以計算如下。</span><span class="sxs-lookup"><span data-stu-id="cbb59-113">The sizes of the output tensor can be computed as follows.</span></span>

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

<span data-ttu-id="cbb59-114">類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbb59-114">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbb59-115">針對輸入 tensor *InputTensor* 所產生並儲存在 *OutputTensor* 中的最大值之索引的選擇性輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="cbb59-115">An optional output tensor of indices to the input tensor *InputTensor* of the maximum values produced and stored in the *OutputTensor*.</span></span> <span data-ttu-id="cbb59-116">這些索引值是以零為基底，並將輸入 tensor 視為連續的一維陣列。</span><span class="sxs-lookup"><span data-stu-id="cbb59-116">These index values are zero-based and treat the input tensor as a contiguous one-dimensional array.</span></span> <span data-ttu-id="cbb59-117">當滑動視窗中的多個專案具有相同值時，會忽略較晚的相等值，且索引會指向第一個遇到的值。</span><span class="sxs-lookup"><span data-stu-id="cbb59-117">When multiple elements within the sliding window have the same value, the later equal values are ignored and the index points to the first value encountered.</span></span> <span data-ttu-id="cbb59-118">*OutputTensor* 和 *OutputIndicesTensor* 都有相同的 tensor 大小。</span><span class="sxs-lookup"><span data-stu-id="cbb59-118">Both the *OutputTensor* and *OutputIndicesTensor* have the same tensor sizes.</span></span>


`DimensionCount`

<span data-ttu-id="cbb59-119">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cbb59-119">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="cbb59-120">輸入 tensor *InputTensor* 的空間維度數目，也會對應至滑動視窗 *WindowSize* 的維度數目。</span><span class="sxs-lookup"><span data-stu-id="cbb59-120">The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*.</span></span> <span data-ttu-id="cbb59-121">此值也會決定進展、 *StartPadding* 和 *EndPadding* *陣列的大小*。</span><span class="sxs-lookup"><span data-stu-id="cbb59-121">This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="cbb59-122">當 *InputTensor* 為4d 時，應設定為2，而當它是 5d tensor 時，則應設為3。</span><span class="sxs-lookup"><span data-stu-id="cbb59-122">It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.</span></span>


`Strides`

<span data-ttu-id="cbb59-123">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="cbb59-123">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="cbb59-124">`{ Height, Width }`當 *DimensionCount* 設定為2或 `{ Depth, Height, Width }` 設為3時，滑動視窗大小的進展。</span><span class="sxs-lookup"><span data-stu-id="cbb59-124">The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`WindowSize`

<span data-ttu-id="cbb59-125">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="cbb59-125">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="cbb59-126">`{ Height, Width }`當 *DimensionCount* 設定為2或 `{ Depth, Height, Width }` 設定為3時，滑動視窗的維度。</span><span class="sxs-lookup"><span data-stu-id="cbb59-126">The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`StartPadding`

<span data-ttu-id="cbb59-127">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="cbb59-127">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="cbb59-128">要套用至輸入 tensor *InputTensor* 中每個空間維度開頭的填補元素數目。</span><span class="sxs-lookup"><span data-stu-id="cbb59-128">The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="cbb59-129">`{ Height, Width }`當 *DimensionCount* 設定為2或 `{ Depth, Height, Width }` 設為3時，這些值就會在中。</span><span class="sxs-lookup"><span data-stu-id="cbb59-129">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`EndPadding`

<span data-ttu-id="cbb59-130">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="cbb59-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="cbb59-131">要套用至輸入 tensor *InputTensor* 中每個空間維度結尾的填補元素數目。</span><span class="sxs-lookup"><span data-stu-id="cbb59-131">The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="cbb59-132">`{ Height, Width }`當 *DimensionCount* 設定為2或 `{ Depth, Height, Width }` 設為3時，這些值就會在中。</span><span class="sxs-lookup"><span data-stu-id="cbb59-132">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`Dilations`

<span data-ttu-id="cbb59-133">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="cbb59-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="cbb59-134">輸入 tensor *InputTensor* 的每個空間維度的值，會根據該值的每個專案選取滑動視窗內的元素。</span><span class="sxs-lookup"><span data-stu-id="cbb59-134">The values for each spatial dimension of the input tensor *InputTensor* by which an element within the sliding window is selected for every elements of that value.</span></span> <span data-ttu-id="cbb59-135">`{ Height, Width }`當 *DimensionCount* 設定為2或 `{ Depth, Height, Width }` 設為3時，這些值就會在中。</span><span class="sxs-lookup"><span data-stu-id="cbb59-135">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


## <a name="remarks"></a><span data-ttu-id="cbb59-136">備註</span><span class="sxs-lookup"><span data-stu-id="cbb59-136">Remarks</span></span>
<span data-ttu-id="cbb59-137">**DML_MAX_POOLING2_OPERATOR_DESC** 會以額外的常數陣列 *Dilations* 取代舊版 [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) 。</span><span class="sxs-lookup"><span data-stu-id="cbb59-137">**DML_MAX_POOLING2_OPERATOR_DESC** supersedes the earlier version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) with an additional constant array *Dilations*.</span></span> <span data-ttu-id="cbb59-138">當 *Dilations* 設定為 `{ 1,1 }` 4D 輸入或5d 個輸入功能時，這兩個版本是相等的 `{ 1,1,1 }` 。</span><span class="sxs-lookup"><span data-stu-id="cbb59-138">The two versions are equivalent when *Dilations* is set to `{ 1,1 }` for 4D input, or `{ 1,1,1 }` for 5D input features.</span></span>

## <a name="availability"></a><span data-ttu-id="cbb59-139">可用性</span><span class="sxs-lookup"><span data-stu-id="cbb59-139">Availability</span></span>
<span data-ttu-id="cbb59-140">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="cbb59-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cbb59-141">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="cbb59-141">Tensor constraints</span></span>
* <span data-ttu-id="cbb59-142">*InputTensor*、 *OutputIndicesTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="cbb59-142">*InputTensor*, *OutputIndicesTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="cbb59-143">*InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="cbb59-143">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cbb59-144">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="cbb59-144">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="cbb59-145">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="cbb59-145">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="cbb59-146">張</span><span class="sxs-lookup"><span data-stu-id="cbb59-146">Tensor</span></span> | <span data-ttu-id="cbb59-147">類型</span><span class="sxs-lookup"><span data-stu-id="cbb59-147">Kind</span></span> | <span data-ttu-id="cbb59-148">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="cbb59-148">Supported dimension counts</span></span> | <span data-ttu-id="cbb59-149">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="cbb59-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cbb59-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cbb59-150">InputTensor</span></span> | <span data-ttu-id="cbb59-151">輸入</span><span class="sxs-lookup"><span data-stu-id="cbb59-151">Input</span></span> | <span data-ttu-id="cbb59-152">4到5</span><span class="sxs-lookup"><span data-stu-id="cbb59-152">4 to 5</span></span> | <span data-ttu-id="cbb59-153">FLOAT32、FLOAT16、INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="cbb59-153">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="cbb59-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cbb59-154">OutputTensor</span></span> | <span data-ttu-id="cbb59-155">輸出</span><span class="sxs-lookup"><span data-stu-id="cbb59-155">Output</span></span> | <span data-ttu-id="cbb59-156">4到5</span><span class="sxs-lookup"><span data-stu-id="cbb59-156">4 to 5</span></span> | <span data-ttu-id="cbb59-157">FLOAT32、FLOAT16、INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="cbb59-157">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="cbb59-158">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="cbb59-158">OutputIndicesTensor</span></span> | <span data-ttu-id="cbb59-159">選用輸出</span><span class="sxs-lookup"><span data-stu-id="cbb59-159">Optional output</span></span> | <span data-ttu-id="cbb59-160">4到5</span><span class="sxs-lookup"><span data-stu-id="cbb59-160">4 to 5</span></span> | <span data-ttu-id="cbb59-161">UINT32</span><span class="sxs-lookup"><span data-stu-id="cbb59-161">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="cbb59-162">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="cbb59-162">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="cbb59-163">張</span><span class="sxs-lookup"><span data-stu-id="cbb59-163">Tensor</span></span> | <span data-ttu-id="cbb59-164">類型</span><span class="sxs-lookup"><span data-stu-id="cbb59-164">Kind</span></span> | <span data-ttu-id="cbb59-165">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="cbb59-165">Supported dimension counts</span></span> | <span data-ttu-id="cbb59-166">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="cbb59-166">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cbb59-167">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cbb59-167">InputTensor</span></span> | <span data-ttu-id="cbb59-168">輸入</span><span class="sxs-lookup"><span data-stu-id="cbb59-168">Input</span></span> | <span data-ttu-id="cbb59-169">4到5</span><span class="sxs-lookup"><span data-stu-id="cbb59-169">4 to 5</span></span> | <span data-ttu-id="cbb59-170">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cbb59-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cbb59-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cbb59-171">OutputTensor</span></span> | <span data-ttu-id="cbb59-172">輸出</span><span class="sxs-lookup"><span data-stu-id="cbb59-172">Output</span></span> | <span data-ttu-id="cbb59-173">4到5</span><span class="sxs-lookup"><span data-stu-id="cbb59-173">4 to 5</span></span> | <span data-ttu-id="cbb59-174">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cbb59-174">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cbb59-175">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="cbb59-175">OutputIndicesTensor</span></span> | <span data-ttu-id="cbb59-176">選用輸出</span><span class="sxs-lookup"><span data-stu-id="cbb59-176">Optional output</span></span> | <span data-ttu-id="cbb59-177">4到5</span><span class="sxs-lookup"><span data-stu-id="cbb59-177">4 to 5</span></span> | <span data-ttu-id="cbb59-178">UINT32</span><span class="sxs-lookup"><span data-stu-id="cbb59-178">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="cbb59-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbb59-179">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cbb59-180">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="cbb59-180">**Minimum supported client**</span></span> | <span data-ttu-id="cbb59-181">Windows 10，版本 2004 (10.0;組建 19041) </span><span class="sxs-lookup"><span data-stu-id="cbb59-181">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="cbb59-182">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="cbb59-182">**Minimum supported server**</span></span> | <span data-ttu-id="cbb59-183">Windows Server，版本 2004 (10.0;組建 19041) </span><span class="sxs-lookup"><span data-stu-id="cbb59-183">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="cbb59-184">**標頭**</span><span class="sxs-lookup"><span data-stu-id="cbb59-184">**Header**</span></span> | <span data-ttu-id="cbb59-185">directml。h</span><span class="sxs-lookup"><span data-stu-id="cbb59-185">directml.h</span></span> |