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
ms.openlocfilehash: 759bf25d4b6a97e70c6de7708a5c9fd0bccae439
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803401"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="74c7a-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="74c7a-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="74c7a-105">在輸入 tensor 上執行 mean 變異數正規化函數。</span><span class="sxs-lookup"><span data-stu-id="74c7a-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="74c7a-106">這個運算子會計算輸入 tensor 的平均數和變異數，以執行正規化。</span><span class="sxs-lookup"><span data-stu-id="74c7a-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="74c7a-107">這個運算子會執行下列計算。</span><span class="sxs-lookup"><span data-stu-id="74c7a-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="74c7a-108">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="74c7a-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="74c7a-109">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="74c7a-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="74c7a-110">語法</span><span class="sxs-lookup"><span data-stu-id="74c7a-110">Syntax</span></span>
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
## <a name="members"></a><span data-ttu-id="74c7a-111">成員</span><span class="sxs-lookup"><span data-stu-id="74c7a-111">Members</span></span>

`InputTensor`

<span data-ttu-id="74c7a-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="74c7a-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="74c7a-113">包含輸入資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="74c7a-113">A tensor containing the Input data.</span></span> <span data-ttu-id="74c7a-114">此 tensor 的維度應該是 `{ BatchCount, ChannelCount, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="74c7a-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="74c7a-115">類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="74c7a-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="74c7a-116">包含調整資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="74c7a-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="74c7a-117">如果 **DML_FEATURE_LEVEL** 小於 **DML_FEATURE_LEVEL_4_0**，則此 tensor 的維度應該是 `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="74c7a-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="74c7a-118">ScaleBatchCount、ScaleHeight 和 ScaleWidth 的維度應該符合 *InputTensor*，或設定為1，以自動在輸入之間廣播這些維度。</span><span class="sxs-lookup"><span data-stu-id="74c7a-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="74c7a-119">如果 **DML_FEATURE_LEVEL** 大於或等於 **DML_FEATURE_LEVEL_4_0**，則任何維度都可以設定為1，並自動廣播以符合 *InputTensor*。</span><span class="sxs-lookup"><span data-stu-id="74c7a-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="74c7a-120">如果使用 *BiasTensor* ，則需要此 tensor。</span><span class="sxs-lookup"><span data-stu-id="74c7a-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="74c7a-121">類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="74c7a-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="74c7a-122">包含偏差資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="74c7a-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="74c7a-123">如果 **DML_FEATURE_LEVEL** 小於 **DML_FEATURE_LEVEL_4_0**，則此 tensor 的維度應該是 `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` 。</span><span class="sxs-lookup"><span data-stu-id="74c7a-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="74c7a-124">BiasBatchCount、BiasHeight 和 BiasWidth 的維度應該符合 *InputTensor*，或設定為1，以自動在輸入之間廣播這些維度。</span><span class="sxs-lookup"><span data-stu-id="74c7a-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="74c7a-125">如果 **DML_FEATURE_LEVEL** 大於或等於 **DML_FEATURE_LEVEL_4_0**，則任何維度都可以設定為1，並自動廣播以符合 *InputTensor*。</span><span class="sxs-lookup"><span data-stu-id="74c7a-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="74c7a-126">如果使用 *ScaleTensor* ，則需要此 tensor。</span><span class="sxs-lookup"><span data-stu-id="74c7a-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="74c7a-127">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="74c7a-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="74c7a-128">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="74c7a-128">A tensor to write the results to.</span></span> <span data-ttu-id="74c7a-129">這個 tensor 的維度是 `{ BatchCount, ChannelCount, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="74c7a-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="74c7a-130">類型： <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="74c7a-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="74c7a-131">軸的數目。</span><span class="sxs-lookup"><span data-stu-id="74c7a-131">The number of axes.</span></span> <span data-ttu-id="74c7a-132">此欄位會決定 *軸* 陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="74c7a-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="74c7a-133">類型： \_ 欄位 \_ 大小 \_ (AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="74c7a-133">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span> 

<span data-ttu-id="74c7a-134">要計算平均值和變異數的座標軸。</span><span class="sxs-lookup"><span data-stu-id="74c7a-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="74c7a-135">類型： <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="74c7a-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="74c7a-136">如果正規化層包含正規化計算中的變異數，**則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="74c7a-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="74c7a-137">否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="74c7a-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="74c7a-138">如果 **為 FALSE**，則正規化方程式為 `Output = FusedActivation(Scale * (Input - Mean) + Bias)` 。</span><span class="sxs-lookup"><span data-stu-id="74c7a-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="74c7a-139">類型： <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="74c7a-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="74c7a-140">用來避免除以零的 epsilon 值。</span><span class="sxs-lookup"><span data-stu-id="74c7a-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="74c7a-141">預設值為0.00001 的建議值。</span><span class="sxs-lookup"><span data-stu-id="74c7a-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="74c7a-142">類型： \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="74c7a-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="74c7a-143">要在正規化之後套用的選擇性融合啟用層。</span><span class="sxs-lookup"><span data-stu-id="74c7a-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="74c7a-144">備註</span><span class="sxs-lookup"><span data-stu-id="74c7a-144">Remarks</span></span>
<span data-ttu-id="74c7a-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** 是 [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc)功能的超集合。</span><span class="sxs-lookup"><span data-stu-id="74c7a-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="74c7a-146">在這裡，將 **座標軸** 陣列設定為 `{ 0, 2, 3 }` 相當於 **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC** 中將 *CrossChannel* 設定為 **FALSE** ，而將 **座標軸** 陣列設定為 `{ 1, 2, 3 }` 相當於將 *CrossChannel* 設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="74c7a-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="74c7a-147">可用性</span><span class="sxs-lookup"><span data-stu-id="74c7a-147">Availability</span></span>
<span data-ttu-id="74c7a-148">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="74c7a-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="74c7a-149">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="74c7a-149">Tensor constraints</span></span>

<span data-ttu-id="74c7a-150">*BiasTensor*、 *InputTensor*、 *OutputTensor* 和 *ScaleTensor* 必須具有相同的 *資料類型* 和 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="74c7a-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="74c7a-151">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="74c7a-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="74c7a-152">DML_FEATURE_LEVEL_3_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="74c7a-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="74c7a-153">張</span><span class="sxs-lookup"><span data-stu-id="74c7a-153">Tensor</span></span> | <span data-ttu-id="74c7a-154">類型</span><span class="sxs-lookup"><span data-stu-id="74c7a-154">Kind</span></span> | <span data-ttu-id="74c7a-155">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="74c7a-155">Supported dimension counts</span></span> | <span data-ttu-id="74c7a-156">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="74c7a-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="74c7a-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="74c7a-157">InputTensor</span></span> | <span data-ttu-id="74c7a-158">輸入</span><span class="sxs-lookup"><span data-stu-id="74c7a-158">Input</span></span> | <span data-ttu-id="74c7a-159">1至8</span><span class="sxs-lookup"><span data-stu-id="74c7a-159">1 to 8</span></span> | <span data-ttu-id="74c7a-160">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="74c7a-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="74c7a-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="74c7a-161">ScaleTensor</span></span> | <span data-ttu-id="74c7a-162">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="74c7a-162">Optional input</span></span> | <span data-ttu-id="74c7a-163">1至8</span><span class="sxs-lookup"><span data-stu-id="74c7a-163">1 to 8</span></span> | <span data-ttu-id="74c7a-164">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="74c7a-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="74c7a-165">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="74c7a-165">BiasTensor</span></span> | <span data-ttu-id="74c7a-166">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="74c7a-166">Optional input</span></span> | <span data-ttu-id="74c7a-167">1至8</span><span class="sxs-lookup"><span data-stu-id="74c7a-167">1 to 8</span></span> | <span data-ttu-id="74c7a-168">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="74c7a-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="74c7a-169">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="74c7a-169">OutputTensor</span></span> | <span data-ttu-id="74c7a-170">輸出</span><span class="sxs-lookup"><span data-stu-id="74c7a-170">Output</span></span> | <span data-ttu-id="74c7a-171">1至8</span><span class="sxs-lookup"><span data-stu-id="74c7a-171">1 to 8</span></span> | <span data-ttu-id="74c7a-172">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="74c7a-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="74c7a-173">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="74c7a-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="74c7a-174">張</span><span class="sxs-lookup"><span data-stu-id="74c7a-174">Tensor</span></span> | <span data-ttu-id="74c7a-175">類型</span><span class="sxs-lookup"><span data-stu-id="74c7a-175">Kind</span></span> | <span data-ttu-id="74c7a-176">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="74c7a-176">Supported dimension counts</span></span> | <span data-ttu-id="74c7a-177">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="74c7a-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="74c7a-178">InputTensor</span><span class="sxs-lookup"><span data-stu-id="74c7a-178">InputTensor</span></span> | <span data-ttu-id="74c7a-179">輸入</span><span class="sxs-lookup"><span data-stu-id="74c7a-179">Input</span></span> | <span data-ttu-id="74c7a-180">4</span><span class="sxs-lookup"><span data-stu-id="74c7a-180">4</span></span> | <span data-ttu-id="74c7a-181">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="74c7a-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="74c7a-182">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="74c7a-182">ScaleTensor</span></span> | <span data-ttu-id="74c7a-183">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="74c7a-183">Optional input</span></span> | <span data-ttu-id="74c7a-184">4</span><span class="sxs-lookup"><span data-stu-id="74c7a-184">4</span></span> | <span data-ttu-id="74c7a-185">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="74c7a-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="74c7a-186">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="74c7a-186">BiasTensor</span></span> | <span data-ttu-id="74c7a-187">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="74c7a-187">Optional input</span></span> | <span data-ttu-id="74c7a-188">4</span><span class="sxs-lookup"><span data-stu-id="74c7a-188">4</span></span> | <span data-ttu-id="74c7a-189">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="74c7a-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="74c7a-190">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="74c7a-190">OutputTensor</span></span> | <span data-ttu-id="74c7a-191">輸出</span><span class="sxs-lookup"><span data-stu-id="74c7a-191">Output</span></span> | <span data-ttu-id="74c7a-192">4</span><span class="sxs-lookup"><span data-stu-id="74c7a-192">4</span></span> | <span data-ttu-id="74c7a-193">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="74c7a-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="74c7a-194">規格需求</span><span class="sxs-lookup"><span data-stu-id="74c7a-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="74c7a-195">**標頭**</span><span class="sxs-lookup"><span data-stu-id="74c7a-195">**Header**</span></span> | <span data-ttu-id="74c7a-196">directml。h</span><span class="sxs-lookup"><span data-stu-id="74c7a-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="74c7a-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74c7a-197">See also</span></span>

[<span data-ttu-id="74c7a-198">使用融合的運算子改善效能</span><span class="sxs-lookup"><span data-stu-id="74c7a-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)
