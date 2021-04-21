---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870). 總而言之，此作業會解壓縮來自輸入影像 tensor 的裁剪，並使用指定的 *InterpolationMode*，將其調整為 *OutputTensor* 最後2個維度所指定的一般輸出大小。
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: b9004a77d3b325dd3394d1a3a6b596e94997e9fd
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804012"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a><span data-ttu-id="03911-104">DML_ROI_ALIGN_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="03911-104">DML_ROI_ALIGN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="03911-105">Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870).</span><span class="sxs-lookup"><span data-stu-id="03911-105">Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870).</span></span> <span data-ttu-id="03911-106">總而言之，此作業會解壓縮來自輸入影像 tensor 的裁剪，並使用指定的 *InterpolationMode*，將其調整為 *OutputTensor* 最後2個維度所指定的一般輸出大小。</span><span class="sxs-lookup"><span data-stu-id="03911-106">In summary, the operation extracts crops from the input image tensor and resizes them to a common output size specified by the last 2 dimensions of *OutputTensor* using the specified *InterpolationMode*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03911-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="03911-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="03911-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="03911-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03911-109">語法</span><span class="sxs-lookup"><span data-stu-id="03911-109">Syntax</span></span>

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a><span data-ttu-id="03911-110">成員</span><span class="sxs-lookup"><span data-stu-id="03911-110">Members</span></span>

`InputTensor`

<span data-ttu-id="03911-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="03911-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="03911-112">Tensor，其中包含具有維度的輸入資料 `{ BatchCount, ChannelCount, InputHeight, InputWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="03911-112">A tensor containing the input data with dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }`.</span></span>

`ROITensor`

<span data-ttu-id="03911-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="03911-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="03911-114">Tensor，其中包含感興趣的區域 (ROI) 資料。</span><span class="sxs-lookup"><span data-stu-id="03911-114">A tensor containing the regions of interest (ROI) data.</span></span> <span data-ttu-id="03911-115">允許的維度 `ROITensor` 為 `{ NumROIs, 4 }` 、 `{ 1, NumROIs, 4 }` 或 `{ 1, 1, NumROIs, 4 }` 。</span><span class="sxs-lookup"><span data-stu-id="03911-115">The allowed dimensions of `ROITensor` are `{ NumROIs, 4 }`, `{ 1, NumROIs, 4 }`, or `{ 1, 1, NumROIs, 4 }`.</span></span> <span data-ttu-id="03911-116">針對每個投資報酬率，值會是其左上角和右下角的座標（依序排列） `[x1, y1, x2, y2]` 。</span><span class="sxs-lookup"><span data-stu-id="03911-116">For each ROI, the values will be the coordinates of its top-left and bottom-right corners in the order `[x1, y1, x2, y2]`.</span></span>

`BatchIndicesTensor`

<span data-ttu-id="03911-117">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="03911-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="03911-118">包含要從中解壓縮 ROIs 之批次索引的 tensor。</span><span class="sxs-lookup"><span data-stu-id="03911-118">A tensor containing the batch indices to extract the ROIs from.</span></span> <span data-ttu-id="03911-119">允許的維度 `BatchIndicesTensor` 為 `{ NumROIs }` 、 `{ 1, NumROIs }` 、 `{ 1, 1, NumROIs }` 或 `{ 1, 1, 1, NumROIs }` 。</span><span class="sxs-lookup"><span data-stu-id="03911-119">The allowed dimensions of `BatchIndicesTensor` are `{ NumROIs }`, `{ 1, NumROIs }`, `{ 1, 1, NumROIs }`, or `{ 1, 1, 1, NumROIs }`.</span></span> <span data-ttu-id="03911-120">每個值都是來自 *InputTensor* 之批次的索引。</span><span class="sxs-lookup"><span data-stu-id="03911-120">Each value is the index of a batch from *InputTensor*.</span></span> <span data-ttu-id="03911-121">如果值不在範圍 [0，BatchCount) 中，則行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="03911-121">The behavior is undefined if the values are not in the range [0, BatchCount).</span></span>

`OutputTensor`

<span data-ttu-id="03911-122">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="03911-122">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="03911-123">包含輸出資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="03911-123">A tensor containing the output data.</span></span> <span data-ttu-id="03911-124">*OutputTensor* 的預期維度是 `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="03911-124">The expected dimensions of *OutputTensor* are `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }`.</span></span>

`ReductionFunction`

<span data-ttu-id="03911-125">類型： **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span><span class="sxs-lookup"><span data-stu-id="03911-125">Type: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span></span>

<span data-ttu-id="03911-126">要在對輸出專案產生的所有輸入樣本之間進行縮減時所要使用的縮減函數 ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) 或 **DML_REDUCE_FUNCTION_MAX**) 。</span><span class="sxs-lookup"><span data-stu-id="03911-126">The reduction function to use when reducing across all input samples that contribute to an output element ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) or **DML_REDUCE_FUNCTION_MAX**).</span></span> <span data-ttu-id="03911-127">要減少的輸入樣本數會受到 *MinimumSamplesPerOutput* 和 *MaximumSamplesPerOutput* 的限制。</span><span class="sxs-lookup"><span data-stu-id="03911-127">The number of input samples to reduce across is bounded by *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`InterpolationMode`

<span data-ttu-id="03911-128">類型： **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span><span class="sxs-lookup"><span data-stu-id="03911-128">Type: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span></span>

<span data-ttu-id="03911-129">調整區域大小時要使用的插補模式。</span><span class="sxs-lookup"><span data-stu-id="03911-129">The interpolation mode to use when resizing the regions.</span></span>

- <span data-ttu-id="03911-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)。</span><span class="sxs-lookup"><span data-stu-id="03911-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span></span> <span data-ttu-id="03911-131">使用 *最接近的鄰近* 演算法，為每個輸出元素選擇最接近對應圖元中心的輸入元素。</span><span class="sxs-lookup"><span data-stu-id="03911-131">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>
- <span data-ttu-id="03911-132">**DML_INTERPOLATION_MODE_LINEAR**。</span><span class="sxs-lookup"><span data-stu-id="03911-132">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="03911-133">使用 *雙線性* 演算法，它會針對每個維度執行2個最接近相鄰輸入元素的加權平均值，以計算輸出元素。</span><span class="sxs-lookup"><span data-stu-id="03911-133">Uses the *Bilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="03911-134">由於只有2個維度會調整大小，因此每個輸出元素總共會計算4個輸入元素的加權平均值。</span><span class="sxs-lookup"><span data-stu-id="03911-134">Since only 2 dimensions are resized, the weighted average is computed on a total of 4 input elements for each output element.</span></span>

`SpatialScaleX`

<span data-ttu-id="03911-135">類型： <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="03911-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="03911-136">縮放係數的 X (或寬度) 元件，用以乘以 *ROITensor* 座標，以便讓它們與 *InputHeight* 和 *InputWidth* 成正比。</span><span class="sxs-lookup"><span data-stu-id="03911-136">The X (or width) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="03911-137">例如，如果 *ROITensor* 包含正規化座標 (範圍 [0 ..1] ) 中的值，則 *SpatialScaleX* 通常會具有與 *InputWidth* 相同的值。</span><span class="sxs-lookup"><span data-stu-id="03911-137">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), then *SpatialScaleX* would usually have the same value as *InputWidth*.</span></span>

`SpatialScaleY`

<span data-ttu-id="03911-138">類型： <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="03911-138">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="03911-139">縮放係數的 Y (或高度) 元件，用來乘以 *ROITensor* 座標，以便讓它們與 *InputHeight* 和 *InputWidth* 成正比。</span><span class="sxs-lookup"><span data-stu-id="03911-139">The Y (or height) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="03911-140">例如，如果 *ROITensor* 包含正規化座標 (範圍 [0 ..1] ) 中的值，則 *SpatialScaleY* 通常會具有與 *InputHeight* 相同的值。</span><span class="sxs-lookup"><span data-stu-id="03911-140">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), *SpatialScaleY* would usually have the same value as *InputHeight*.</span></span>

`OutOfBoundsInputValue`

<span data-ttu-id="03911-141">類型： <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="03911-141">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="03911-142">當 ROIs 超出 *InputTensor* 的界限時，從 *InputTensor* 讀取的值。</span><span class="sxs-lookup"><span data-stu-id="03911-142">The value to read from *InputTensor* when the ROIs are outside the bounds of *InputTensor*.</span></span> <span data-ttu-id="03911-143">當在 *SpatialScaleX* 和 *SpatialScaleY* 的調整 *ROITensor* 之後取得的值大於 *InputWidth* 和 *InputHeight* 時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="03911-143">This can happen when the values obtained after scaling *ROITensor* by *SpatialScaleX* and *SpatialScaleY* are bigger than *InputWidth* and *InputHeight*.</span></span>

`MinimumSamplesPerOutput`

<span data-ttu-id="03911-144">類型： <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="03911-144">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="03911-145">每個輸出元素要使用的輸入樣本數目下限。</span><span class="sxs-lookup"><span data-stu-id="03911-145">The minimum number of input samples to use for every output element.</span></span> <span data-ttu-id="03911-146">運算子會計算輸入樣本的數目 `ScaledCropSize / OutputSize` ，然後將其設為 *MinimumSamplesPerOutput* 和 *MaximumSamplesPerOutput*。</span><span class="sxs-lookup"><span data-stu-id="03911-146">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`MaximumSamplesPerOutput`

<span data-ttu-id="03911-147">類型： <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="03911-147">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="03911-148">每個輸出元素要使用的輸入樣本數上限。</span><span class="sxs-lookup"><span data-stu-id="03911-148">The maximum number of input samples to use for every output element.</span></span> <span data-ttu-id="03911-149">運算子會計算輸入樣本的數目 `ScaledCropSize / OutputSize` ，然後將其設為 *MinimumSamplesPerOutput* 和 *MaximumSamplesPerOutput*。</span><span class="sxs-lookup"><span data-stu-id="03911-149">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

## <a name="availability"></a><span data-ttu-id="03911-150">可用性</span><span class="sxs-lookup"><span data-stu-id="03911-150">Availability</span></span>
<span data-ttu-id="03911-151">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="03911-151">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="03911-152">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="03911-152">Tensor constraints</span></span>
<span data-ttu-id="03911-153">*InputTensor*、 *OutputTensor* 和 *ROITensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="03911-153">*InputTensor*, *OutputTensor*, and *ROITensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="03911-154">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="03911-154">Tensor support</span></span>
| <span data-ttu-id="03911-155">張</span><span class="sxs-lookup"><span data-stu-id="03911-155">Tensor</span></span> | <span data-ttu-id="03911-156">類型</span><span class="sxs-lookup"><span data-stu-id="03911-156">Kind</span></span> | <span data-ttu-id="03911-157">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="03911-157">Supported dimension counts</span></span> | <span data-ttu-id="03911-158">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="03911-158">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="03911-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="03911-159">InputTensor</span></span> | <span data-ttu-id="03911-160">輸入</span><span class="sxs-lookup"><span data-stu-id="03911-160">Input</span></span> | <span data-ttu-id="03911-161">4</span><span class="sxs-lookup"><span data-stu-id="03911-161">4</span></span> | <span data-ttu-id="03911-162">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="03911-162">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="03911-163">ROITensor</span><span class="sxs-lookup"><span data-stu-id="03911-163">ROITensor</span></span> | <span data-ttu-id="03911-164">輸入</span><span class="sxs-lookup"><span data-stu-id="03911-164">Input</span></span> | <span data-ttu-id="03911-165">2到4</span><span class="sxs-lookup"><span data-stu-id="03911-165">2 to 4</span></span> | <span data-ttu-id="03911-166">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="03911-166">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="03911-167">BatchIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="03911-167">BatchIndicesTensor</span></span> | <span data-ttu-id="03911-168">輸入</span><span class="sxs-lookup"><span data-stu-id="03911-168">Input</span></span> | <span data-ttu-id="03911-169">1到4</span><span class="sxs-lookup"><span data-stu-id="03911-169">1 to 4</span></span> | <span data-ttu-id="03911-170">UINT32</span><span class="sxs-lookup"><span data-stu-id="03911-170">UINT32</span></span> |
| <span data-ttu-id="03911-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="03911-171">OutputTensor</span></span> | <span data-ttu-id="03911-172">輸出</span><span class="sxs-lookup"><span data-stu-id="03911-172">Output</span></span> | <span data-ttu-id="03911-173">4</span><span class="sxs-lookup"><span data-stu-id="03911-173">4</span></span> | <span data-ttu-id="03911-174">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="03911-174">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="03911-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="03911-175">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="03911-176">**標頭**</span><span class="sxs-lookup"><span data-stu-id="03911-176">**Header**</span></span> | <span data-ttu-id="03911-177">directml。h</span><span class="sxs-lookup"><span data-stu-id="03911-177">directml.h</span></span> |