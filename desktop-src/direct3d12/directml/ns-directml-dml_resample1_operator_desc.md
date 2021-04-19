---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: 使用縮放因數來計算目的地 tensor 大小，以將來源中的專案 Resamples 至目的地 tensor。 您可以使用線性或最接近的相鄰插補模式。
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 669e828c4d8376e081ef6638aba4a13d517afd88
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106991385"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a><span data-ttu-id="e8dc1-104">DML_RESAMPLE1_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="e8dc1-104">DML_RESAMPLE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="e8dc1-105">使用縮放因數來計算目的地 tensor 大小，以將來源中的專案 Resamples 至目的地 tensor。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-105">Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size.</span></span> <span data-ttu-id="e8dc1-106">您可以使用線性或最接近的相鄰插補模式。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-106">You can use a linear or nearest-neighbor interpolation mode.</span></span> <span data-ttu-id="e8dc1-107">運算子支援跨多個維度（而不只是2D）的插補。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-107">The operator supports interpolation across multiple dimensions, not just 2D.</span></span> <span data-ttu-id="e8dc1-108">因此，您可以保留相同的空間大小，但會在通道之間或在批次之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-108">So you can keep the same spatial size, but interpolate across channels or across batches.</span></span> <span data-ttu-id="e8dc1-109">輸入和輸出座標之間的關聯性如下所示。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-109">The relationship between the input and output coordinates is the following.</span></span>

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> <span data-ttu-id="e8dc1-110">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e8dc1-111">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8dc1-112">語法</span><span class="sxs-lookup"><span data-stu-id="e8dc1-112">Syntax</span></span>
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a><span data-ttu-id="e8dc1-113">成員</span><span class="sxs-lookup"><span data-stu-id="e8dc1-113">Members</span></span>

`InputTensor`

<span data-ttu-id="e8dc1-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8dc1-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8dc1-115">包含輸入資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-115">The tensor containing the input data.</span></span>


`OutputTensor`

<span data-ttu-id="e8dc1-116">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8dc1-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8dc1-117">要寫入輸出資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-117">The tensor to write the output data to.</span></span>


`InterpolationMode`

<span data-ttu-id="e8dc1-118">類型： [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="e8dc1-118">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="e8dc1-119">此欄位會決定用來選擇輸出圖元的插補種類。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-119">This field determines the kind of interpolation used to choose output pixels.</span></span>

- <span data-ttu-id="e8dc1-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span></span> <span data-ttu-id="e8dc1-121">使用 *最接近的鄰近* 演算法，為每個輸出元素選擇最接近對應圖元中心的輸入元素。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-121">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>

- <span data-ttu-id="e8dc1-122">**DML_INTERPOLATION_MODE_LINEAR**。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-122">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="e8dc1-123">使用 *Quadrilinear* 演算法，其會針對每個維度執行2個最接近相鄰輸入元素的加權平均值，以計算輸出元素。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-123">Uses the *Quadrilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="e8dc1-124">由於所有4個維度都可以重新取樣，因此每個輸出元素總共會計算16個輸入元素的加權平均值。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-124">Since all 4 dimensions can be resampled, the weighted average is computed on a total of 16 input elements for each output element.</span></span>


`DimensionCount`

<span data-ttu-id="e8dc1-125">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e8dc1-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="e8dc1-126">陣列中的值數目，這些值會 *調整*、 *InputPixelOffsets* 和 *OutputPixelOffsets* 點。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-126">The number of values in the arrays that *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* point to.</span></span> <span data-ttu-id="e8dc1-127">此值必須符合 *InputTensor* 和 *OutputTensor* 的維度計數，其必須是4。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-127">This value must match the dimension count of *InputTensor* and *OutputTensor*, which has to be 4.</span></span>


`Scales`

<span data-ttu-id="e8dc1-128">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e8dc1-128">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="e8dc1-129">重新取樣輸入時要套用的比例，其中尺規 > 1 會向上延展影像，並將 < 1 縮小該維度的影像。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-129">The scales to apply when resampling the input, where scales > 1 scale up the image and scales < 1 scale down the image for that dimension.</span></span> <span data-ttu-id="e8dc1-130">請注意，調整不需要完全相同 `OutputSize / InputSize` 。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-130">Note that the scales don't need to be exactly `OutputSize / InputSize`.</span></span> <span data-ttu-id="e8dc1-131">如果在調整之後的輸入大於輸出系結，則會將其裁剪為輸出大小。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-131">If the input after scaling is larger than the output bound, then we crop it to the output size.</span></span> <span data-ttu-id="e8dc1-132">另一方面，如果在調整之後的輸入小於輸出系結，則會壓制輸出邊緣。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-132">On the other hand, if the input after scaling is smaller than the output bound, the output edges are clamped.</span></span>


`InputPixelOffsets`

<span data-ttu-id="e8dc1-133">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e8dc1-133">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="e8dc1-134">要在重新取樣之前套用至輸入圖元的位移。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-134">The offsets to apply to the input pixels before resampling.</span></span> <span data-ttu-id="e8dc1-135">當此值為時 `0` ，就會使用圖元的左上角，而不是其中心，這通常不會提供預期的結果。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-135">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="e8dc1-136">若要使用圖元的中心來重新取樣影像，並取得與 [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)相同的行為，此值必須是 `0.5` 。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-136">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `0.5`.</span></span>


`OutputPixelOffsets`

<span data-ttu-id="e8dc1-137">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e8dc1-137">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="e8dc1-138">重新取樣後要套用至輸出圖元的位移。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-138">The offsets to apply to the output pixels after resampling.</span></span> <span data-ttu-id="e8dc1-139">當此值為時 `0` ，就會使用圖元的左上角，而不是其中心，這通常不會提供預期的結果。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-139">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="e8dc1-140">若要使用圖元的中心來重新取樣影像，並取得與 [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)相同的行為，此值必須是 `-0.5` 。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-140">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `-0.5`.</span></span>


## <a name="remarks"></a><span data-ttu-id="e8dc1-141">備註</span><span class="sxs-lookup"><span data-stu-id="e8dc1-141">Remarks</span></span>
<span data-ttu-id="e8dc1-142">當 *InputPixelOffsets* 設定為0.5，而 *OutputPixelOffsets* 設定為-0.5 時，此運算子相當於 [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-142">When the *InputPixelOffsets* are set to 0.5, and the *OutputPixelOffsets* are set to -0.5, this operator is equivalent to [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="e8dc1-143">可用性</span><span class="sxs-lookup"><span data-stu-id="e8dc1-143">Availability</span></span>
<span data-ttu-id="e8dc1-144">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-144">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e8dc1-145">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="e8dc1-145">Tensor constraints</span></span>
<span data-ttu-id="e8dc1-146">*InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="e8dc1-146">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e8dc1-147">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="e8dc1-147">Tensor support</span></span>
| <span data-ttu-id="e8dc1-148">張</span><span class="sxs-lookup"><span data-stu-id="e8dc1-148">Tensor</span></span> | <span data-ttu-id="e8dc1-149">類型</span><span class="sxs-lookup"><span data-stu-id="e8dc1-149">Kind</span></span> | <span data-ttu-id="e8dc1-150">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="e8dc1-150">Supported dimension counts</span></span> | <span data-ttu-id="e8dc1-151">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="e8dc1-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e8dc1-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e8dc1-152">InputTensor</span></span> | <span data-ttu-id="e8dc1-153">輸入</span><span class="sxs-lookup"><span data-stu-id="e8dc1-153">Input</span></span> | <span data-ttu-id="e8dc1-154">4</span><span class="sxs-lookup"><span data-stu-id="e8dc1-154">4</span></span> | <span data-ttu-id="e8dc1-155">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e8dc1-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e8dc1-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e8dc1-156">OutputTensor</span></span> | <span data-ttu-id="e8dc1-157">輸出</span><span class="sxs-lookup"><span data-stu-id="e8dc1-157">Output</span></span> | <span data-ttu-id="e8dc1-158">4</span><span class="sxs-lookup"><span data-stu-id="e8dc1-158">4</span></span> | <span data-ttu-id="e8dc1-159">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e8dc1-159">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="e8dc1-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8dc1-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e8dc1-161">**標頭**</span><span class="sxs-lookup"><span data-stu-id="e8dc1-161">**Header**</span></span> | <span data-ttu-id="e8dc1-162">directml。h</span><span class="sxs-lookup"><span data-stu-id="e8dc1-162">directml.h</span></span> |