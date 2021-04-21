---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: 計算 [本機回應](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)正規化的反向傳播漸層。
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: eecf849a06ee8e99ac9c015ecd4568496120b2d9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804422"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="6187c-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml) </span><span class="sxs-lookup"><span data-stu-id="6187c-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="6187c-104">計算 [本機回應](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)正規化的反向傳播漸層。</span><span class="sxs-lookup"><span data-stu-id="6187c-104">Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span></span>

<span data-ttu-id="6187c-105">所有張量的資料類型和大小都必須相同。</span><span class="sxs-lookup"><span data-stu-id="6187c-105">The data type and size of all tensors must be the same.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6187c-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="6187c-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="6187c-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="6187c-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6187c-108">語法</span><span class="sxs-lookup"><span data-stu-id="6187c-108">Syntax</span></span>
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a><span data-ttu-id="6187c-109">成員</span><span class="sxs-lookup"><span data-stu-id="6187c-109">Members</span></span>

`InputTensor`

<span data-ttu-id="6187c-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6187c-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6187c-111">包含輸入資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="6187c-111">The tensor containing the input data.</span></span> <span data-ttu-id="6187c-112">此 tensor 的 *大小* 應該是 `{ BatchCount, ChannelCount, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="6187c-112">This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`InputGradientTensor`

<span data-ttu-id="6187c-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6187c-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6187c-114">傳入的漸層 tensor。</span><span class="sxs-lookup"><span data-stu-id="6187c-114">The incoming gradient tensor.</span></span> <span data-ttu-id="6187c-115">這通常是從上一層的反向傳播輸出中取得。</span><span class="sxs-lookup"><span data-stu-id="6187c-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span>

`OutputGradientTensor`

<span data-ttu-id="6187c-116">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6187c-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6187c-117">包含 backpropagated 漸層的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="6187c-117">An output tensor containing the backpropagated gradients.</span></span>

`CrossChannel`

<span data-ttu-id="6187c-118">類型： **[BOOL](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6187c-118">Type: **[BOOL](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="6187c-119">如果 LRN 圖層在各通道之間加總，則 **為 TRUE** ;如果 LRN 圖層加總空間維度，則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6187c-119">**TRUE** if the LRN layer sums across channels; **FALSE** if the LRN layer sums across spatial dimensions.</span></span>

`LocalSize`

<span data-ttu-id="6187c-120">類型： **[UINT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6187c-120">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="6187c-121">要在每個維度加總的元素數目上限 (本地區域會遭到裁剪，讓所有專案都在界限) 內。</span><span class="sxs-lookup"><span data-stu-id="6187c-121">The maximum number of elements to sum over per dimension (the local region is clipped so that all elements are within bounds).</span></span> <span data-ttu-id="6187c-122">如果 *CrossChannel* 為 **TRUE**，則這是本機區域的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="6187c-122">If *CrossChannel* is **TRUE**, then this is the width and height of the local region.</span></span> <span data-ttu-id="6187c-123">如果 *CrossChannel* 為 **FALSE**，則這是本機區域中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="6187c-123">If *CrossChannel* is **FALSE**, then this is the number of elements in the local region.</span></span> <span data-ttu-id="6187c-124">此值必須至少為 1。</span><span class="sxs-lookup"><span data-stu-id="6187c-124">This value must be at least 1.</span></span>

`Alpha`

<span data-ttu-id="6187c-125">類型： **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6187c-125">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="6187c-126">調整參數的值。</span><span class="sxs-lookup"><span data-stu-id="6187c-126">The value of the scaling parameter.</span></span> <span data-ttu-id="6187c-127">我們建議預設值為0.0001。</span><span class="sxs-lookup"><span data-stu-id="6187c-127">We recommend a value of 0.0001 as default.</span></span>

`Beta`

<span data-ttu-id="6187c-128">類型： **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6187c-128">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="6187c-129">指數值。</span><span class="sxs-lookup"><span data-stu-id="6187c-129">The value of the exponent.</span></span> <span data-ttu-id="6187c-130">我們建議預設值為0.75。</span><span class="sxs-lookup"><span data-stu-id="6187c-130">We recommend a value of 0.75 as default.</span></span>

`Bias`

<span data-ttu-id="6187c-131">類型： **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6187c-131">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="6187c-132">偏差的值。</span><span class="sxs-lookup"><span data-stu-id="6187c-132">The value of bias.</span></span> <span data-ttu-id="6187c-133">我們建議預設值為1。</span><span class="sxs-lookup"><span data-stu-id="6187c-133">We recommend a value of 1 as default.</span></span>

## <a name="availability"></a><span data-ttu-id="6187c-134">可用性</span><span class="sxs-lookup"><span data-stu-id="6187c-134">Availability</span></span>
<span data-ttu-id="6187c-135">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。</span><span class="sxs-lookup"><span data-stu-id="6187c-135">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6187c-136">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="6187c-136">Tensor constraints</span></span>
<span data-ttu-id="6187c-137">*InputGradientTensor*、 *InputTensor* 和 *OutputGradientTensor* 必須具有相同的 *資料類型* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="6187c-137">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6187c-138">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="6187c-138">Tensor support</span></span>
| <span data-ttu-id="6187c-139">張</span><span class="sxs-lookup"><span data-stu-id="6187c-139">Tensor</span></span> | <span data-ttu-id="6187c-140">類型</span><span class="sxs-lookup"><span data-stu-id="6187c-140">Kind</span></span> | <span data-ttu-id="6187c-141">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="6187c-141">Supported dimension counts</span></span> | <span data-ttu-id="6187c-142">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="6187c-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6187c-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="6187c-143">InputTensor</span></span> | <span data-ttu-id="6187c-144">輸入</span><span class="sxs-lookup"><span data-stu-id="6187c-144">Input</span></span> | <span data-ttu-id="6187c-145">4</span><span class="sxs-lookup"><span data-stu-id="6187c-145">4</span></span> | <span data-ttu-id="6187c-146">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6187c-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6187c-147">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="6187c-147">InputGradientTensor</span></span> | <span data-ttu-id="6187c-148">輸入</span><span class="sxs-lookup"><span data-stu-id="6187c-148">Input</span></span> | <span data-ttu-id="6187c-149">4</span><span class="sxs-lookup"><span data-stu-id="6187c-149">4</span></span> | <span data-ttu-id="6187c-150">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6187c-150">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6187c-151">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="6187c-151">OutputGradientTensor</span></span> | <span data-ttu-id="6187c-152">輸出</span><span class="sxs-lookup"><span data-stu-id="6187c-152">Output</span></span> | <span data-ttu-id="6187c-153">4</span><span class="sxs-lookup"><span data-stu-id="6187c-153">4</span></span> | <span data-ttu-id="6187c-154">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6187c-154">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="6187c-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="6187c-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6187c-156">**標頭**</span><span class="sxs-lookup"><span data-stu-id="6187c-156">**Header**</span></span> | <span data-ttu-id="6187c-157">directml。h</span><span class="sxs-lookup"><span data-stu-id="6187c-157">directml.h</span></span> |
