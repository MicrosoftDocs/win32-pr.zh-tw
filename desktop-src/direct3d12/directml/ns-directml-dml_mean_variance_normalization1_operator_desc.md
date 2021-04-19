---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: 在輸入 tensor 上執行 mean 變異數正規化函數。 這個運算子會計算輸入 tensor 的平均數和變異數，以執行正規化。
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
f1_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106982794"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="8b46c-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="8b46c-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="8b46c-105">在輸入 tensor 上執行 mean 變異數正規化函數。</span><span class="sxs-lookup"><span data-stu-id="8b46c-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="8b46c-106">這個運算子會計算輸入 tensor 的平均數和變異數，以執行正規化。</span><span class="sxs-lookup"><span data-stu-id="8b46c-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="8b46c-107">這個運算子會執行下列計算。</span><span class="sxs-lookup"><span data-stu-id="8b46c-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="8b46c-108">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="8b46c-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="8b46c-109">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="8b46c-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b46c-110">語法</span><span class="sxs-lookup"><span data-stu-id="8b46c-110">Syntax</span></span>
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```



## <a name="members"></a><span data-ttu-id="8b46c-111">成員</span><span class="sxs-lookup"><span data-stu-id="8b46c-111">Members</span></span>

`InputTensor`

<span data-ttu-id="8b46c-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8b46c-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8b46c-113">包含輸入資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="8b46c-113">A tensor containing the Input data.</span></span> <span data-ttu-id="8b46c-114">此 tensor 的維度應該是 `{ BatchCount, ChannelCount, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="8b46c-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`ScaleTensor`

<span data-ttu-id="8b46c-115">類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8b46c-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8b46c-116">包含調整資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="8b46c-116">An optional tensor containing the Scale data.</span></span> <span data-ttu-id="8b46c-117">此 tensor 的維度應該是 `{ BatchCount, ChannelCount, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="8b46c-117">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="8b46c-118">任何維度都可以取代為1，以便在該維度中廣播。</span><span class="sxs-lookup"><span data-stu-id="8b46c-118">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="8b46c-119">如果使用 *BiasTensor* ，則需要此 tensor。</span><span class="sxs-lookup"><span data-stu-id="8b46c-119">This tensor is required if the *BiasTensor* is used.</span></span>


`BiasTensor`

<span data-ttu-id="8b46c-120">類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8b46c-120">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8b46c-121">包含偏差資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="8b46c-121">An optional tensor containing the bias data.</span></span> <span data-ttu-id="8b46c-122">此 tensor 的維度應該是 `{ BatchCount, ChannelCount, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="8b46c-122">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="8b46c-123">任何維度都可以取代為1，以便在該維度中廣播。</span><span class="sxs-lookup"><span data-stu-id="8b46c-123">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="8b46c-124">如果使用 *ScaleTensor* ，則需要此 tensor。</span><span class="sxs-lookup"><span data-stu-id="8b46c-124">This tensor is required if the *ScaleTensor* is used.</span></span>


`OutputTensor`

<span data-ttu-id="8b46c-125">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8b46c-125">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8b46c-126">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="8b46c-126">A tensor to write the results to.</span></span> <span data-ttu-id="8b46c-127">這個 tensor 的維度是 `{ BatchCount, ChannelCount, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="8b46c-127">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`AxisCount`

<span data-ttu-id="8b46c-128">類型： <b> <a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="8b46c-128">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="8b46c-129">軸的數目。</span><span class="sxs-lookup"><span data-stu-id="8b46c-129">The number of axes.</span></span> <span data-ttu-id="8b46c-130">此欄位會決定 *軸* 陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="8b46c-130">This field determines the size of the *Axes* array.</span></span>


`Axes`

<span data-ttu-id="8b46c-131">類型： \_ 欄位 \_ 大小 \_ (AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="8b46c-131">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span> 

<span data-ttu-id="8b46c-132">要計算平均值和變異數的座標軸。</span><span class="sxs-lookup"><span data-stu-id="8b46c-132">The axes along which to calculate the Mean and Variance.</span></span>


`NormalizeVariance`

<span data-ttu-id="8b46c-133">類型： <b> <a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="8b46c-133">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="8b46c-134">如果正規化層包含正規化計算中的變異數，**則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="8b46c-134">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="8b46c-135">否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8b46c-135">Otherwise, **FALSE**.</span></span> <span data-ttu-id="8b46c-136">如果 **為 FALSE**，則正規化方程式為 `Output = FusedActivation(Scale * (Input - Mean) + Bias)` 。</span><span class="sxs-lookup"><span data-stu-id="8b46c-136">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>


`Epsilon`

<span data-ttu-id="8b46c-137">類型： <b> <a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="8b46c-137">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="8b46c-138">用來避免除以零的 epsilon 值。</span><span class="sxs-lookup"><span data-stu-id="8b46c-138">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="8b46c-139">預設值為0.00001 的建議值。</span><span class="sxs-lookup"><span data-stu-id="8b46c-139">A value of 0.00001 is recommended as default.</span></span>


`FusedActivation`

<span data-ttu-id="8b46c-140">類型： \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8b46c-140">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="8b46c-141">要在正規化之後套用的選擇性融合啟用層。</span><span class="sxs-lookup"><span data-stu-id="8b46c-141">An optional fused activation layer to apply after the normalization.</span></span>


## <a name="remarks"></a><span data-ttu-id="8b46c-142">備註</span><span class="sxs-lookup"><span data-stu-id="8b46c-142">Remarks</span></span>
<span data-ttu-id="8b46c-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** 是 [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc)功能的超集合。</span><span class="sxs-lookup"><span data-stu-id="8b46c-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="8b46c-144">在這裡，將 **座標軸** 陣列設定為 `{ 0, 2, 3 }` 相當於 **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC** 中將 *CrossChannel* 設定為 **FALSE** ，而將 **座標軸** 陣列設定為 `{ 1, 2, 3 }` 相當於將 *CrossChannel* 設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8b46c-144">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="8b46c-145">可用性</span><span class="sxs-lookup"><span data-stu-id="8b46c-145">Availability</span></span>
<span data-ttu-id="8b46c-146">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="8b46c-146">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8b46c-147">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="8b46c-147">Tensor constraints</span></span>
* <span data-ttu-id="8b46c-148">*InputTensor* 和 *OutputTensor* 的 *大小* 必須相同。</span><span class="sxs-lookup"><span data-stu-id="8b46c-148">*InputTensor* and *OutputTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="8b46c-149">*BiasTensor*、 *InputTensor*、 *OutputTensor* 和 *ScaleTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="8b46c-149">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8b46c-150">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="8b46c-150">Tensor support</span></span>
| <span data-ttu-id="8b46c-151">張</span><span class="sxs-lookup"><span data-stu-id="8b46c-151">Tensor</span></span> | <span data-ttu-id="8b46c-152">類型</span><span class="sxs-lookup"><span data-stu-id="8b46c-152">Kind</span></span> | <span data-ttu-id="8b46c-153">維度</span><span class="sxs-lookup"><span data-stu-id="8b46c-153">Dimensions</span></span> | <span data-ttu-id="8b46c-154">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="8b46c-154">Supported dimension counts</span></span> | <span data-ttu-id="8b46c-155">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="8b46c-155">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="8b46c-156">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8b46c-156">InputTensor</span></span> | <span data-ttu-id="8b46c-157">輸入</span><span class="sxs-lookup"><span data-stu-id="8b46c-157">Input</span></span> | <span data-ttu-id="8b46c-158">{BatchCount，ChannelCount，Height，Width}</span><span class="sxs-lookup"><span data-stu-id="8b46c-158">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="8b46c-159">4</span><span class="sxs-lookup"><span data-stu-id="8b46c-159">4</span></span> | <span data-ttu-id="8b46c-160">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8b46c-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="8b46c-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="8b46c-161">ScaleTensor</span></span> | <span data-ttu-id="8b46c-162">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="8b46c-162">Optional input</span></span> | <span data-ttu-id="8b46c-163">{ ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth }</span><span class="sxs-lookup"><span data-stu-id="8b46c-163">{ ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth }</span></span> | <span data-ttu-id="8b46c-164">4</span><span class="sxs-lookup"><span data-stu-id="8b46c-164">4</span></span> | <span data-ttu-id="8b46c-165">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8b46c-165">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="8b46c-166">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="8b46c-166">BiasTensor</span></span> | <span data-ttu-id="8b46c-167">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="8b46c-167">Optional input</span></span> | <span data-ttu-id="8b46c-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span><span class="sxs-lookup"><span data-stu-id="8b46c-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span></span> | <span data-ttu-id="8b46c-169">4</span><span class="sxs-lookup"><span data-stu-id="8b46c-169">4</span></span> | <span data-ttu-id="8b46c-170">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8b46c-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="8b46c-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8b46c-171">OutputTensor</span></span> | <span data-ttu-id="8b46c-172">輸出</span><span class="sxs-lookup"><span data-stu-id="8b46c-172">Output</span></span> | <span data-ttu-id="8b46c-173">{BatchCount，ChannelCount，Height，Width}</span><span class="sxs-lookup"><span data-stu-id="8b46c-173">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="8b46c-174">4</span><span class="sxs-lookup"><span data-stu-id="8b46c-174">4</span></span> | <span data-ttu-id="8b46c-175">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8b46c-175">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="8b46c-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b46c-176">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8b46c-177">**標頭**</span><span class="sxs-lookup"><span data-stu-id="8b46c-177">**Header**</span></span> | <span data-ttu-id="8b46c-178">directml。h</span><span class="sxs-lookup"><span data-stu-id="8b46c-178">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="8b46c-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b46c-179">See also</span></span>

[<span data-ttu-id="8b46c-180">使用融合的運算子改善效能</span><span class="sxs-lookup"><span data-stu-id="8b46c-180">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)