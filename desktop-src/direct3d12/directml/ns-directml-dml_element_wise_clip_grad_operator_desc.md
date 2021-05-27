---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: 計算 [元素取向剪輯](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)的反向傳播漸層。
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 3b993ca1c027119ae64157db2327a2836445bf43
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550203"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a><span data-ttu-id="66746-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml) </span><span class="sxs-lookup"><span data-stu-id="66746-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="66746-104">計算 [元素取向剪輯](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)的反向傳播漸層。</span><span class="sxs-lookup"><span data-stu-id="66746-104">Computes backpropagation gradients for [element-wise clip](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).</span></span>

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

<span data-ttu-id="66746-105">這個運算子支援就地執行，這表示在系結 `OutputTensor` 期間允許別名 *InputTensor* 。</span><span class="sxs-lookup"><span data-stu-id="66746-105">This operator supports in-place execution, meaning `OutputTensor` is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66746-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="66746-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="66746-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="66746-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="66746-108">語法</span><span class="sxs-lookup"><span data-stu-id="66746-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a><span data-ttu-id="66746-109">成員</span><span class="sxs-lookup"><span data-stu-id="66746-109">Members</span></span>

`InputTensor`

<span data-ttu-id="66746-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="66746-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="66746-111">輸入功能 tensor。</span><span class="sxs-lookup"><span data-stu-id="66746-111">The input feature tensor.</span></span> <span data-ttu-id="66746-112">這通常是在轉寄行程中提供作為 *InputTensor* [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) 的相同 tensor。</span><span class="sxs-lookup"><span data-stu-id="66746-112">This is typically the same tensor that was provided as the *InputTensor* to [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="66746-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="66746-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="66746-114">傳入的漸層 tensor。</span><span class="sxs-lookup"><span data-stu-id="66746-114">The incoming gradient tensor.</span></span> <span data-ttu-id="66746-115">這通常是從上一層的反向傳播輸出中取得。</span><span class="sxs-lookup"><span data-stu-id="66746-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="66746-116">一般來說，這個 tensor 的大小會和向前傳遞中對應 **DML_OPERATOR_ELEMENT_WISE_CLIP** 的 *輸出* 相同。</span><span class="sxs-lookup"><span data-stu-id="66746-116">Typically this tensor would have the same sizes as the *output* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="66746-117">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="66746-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="66746-118">包含 backpropagated 漸層的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="66746-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="66746-119">一般來說，這個 tensor 的大小會和向前傳遞中對應 **DML_OPERATOR_ELEMENT_WISE_CLIP** 的 *輸入* 相同。</span><span class="sxs-lookup"><span data-stu-id="66746-119">Typically this tensor would have the same sizes as the *input* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`Min`

<span data-ttu-id="66746-120">類型： **[FLOAT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66746-120">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66746-121">最小值。</span><span class="sxs-lookup"><span data-stu-id="66746-121">The minimum value.</span></span> <span data-ttu-id="66746-122">如果 x 位於或低於此值，則漸層結果為0。</span><span class="sxs-lookup"><span data-stu-id="66746-122">If x is at or below this value, then the gradient result is 0.</span></span>

`Max`

<span data-ttu-id="66746-123">類型： **[FLOAT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66746-123">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66746-124">最大值。</span><span class="sxs-lookup"><span data-stu-id="66746-124">The maximum value.</span></span> <span data-ttu-id="66746-125">如果 x 等於或高於此值，則漸層結果為0。</span><span class="sxs-lookup"><span data-stu-id="66746-125">If x is at or above this value, then the gradient result is 0.</span></span>

## <a name="availability"></a><span data-ttu-id="66746-126">可用性</span><span class="sxs-lookup"><span data-stu-id="66746-126">Availability</span></span>
<span data-ttu-id="66746-127">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。</span><span class="sxs-lookup"><span data-stu-id="66746-127">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="66746-128">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="66746-128">Tensor constraints</span></span>
<span data-ttu-id="66746-129">*InputGradientTensor*、 *InputTensor* 和 *OutputGradientTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="66746-129">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="66746-130">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="66746-130">Tensor support</span></span>
| <span data-ttu-id="66746-131">張</span><span class="sxs-lookup"><span data-stu-id="66746-131">Tensor</span></span> | <span data-ttu-id="66746-132">種類</span><span class="sxs-lookup"><span data-stu-id="66746-132">Kind</span></span> | <span data-ttu-id="66746-133">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="66746-133">Supported dimension counts</span></span> | <span data-ttu-id="66746-134">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="66746-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="66746-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="66746-135">InputTensor</span></span> | <span data-ttu-id="66746-136">輸入</span><span class="sxs-lookup"><span data-stu-id="66746-136">Input</span></span> | <span data-ttu-id="66746-137">1至8</span><span class="sxs-lookup"><span data-stu-id="66746-137">1 to 8</span></span> | <span data-ttu-id="66746-138">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="66746-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="66746-139">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="66746-139">InputGradientTensor</span></span> | <span data-ttu-id="66746-140">輸入</span><span class="sxs-lookup"><span data-stu-id="66746-140">Input</span></span> | <span data-ttu-id="66746-141">1至8</span><span class="sxs-lookup"><span data-stu-id="66746-141">1 to 8</span></span> | <span data-ttu-id="66746-142">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="66746-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="66746-143">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="66746-143">OutputGradientTensor</span></span> | <span data-ttu-id="66746-144">輸出</span><span class="sxs-lookup"><span data-stu-id="66746-144">Output</span></span> | <span data-ttu-id="66746-145">1至8</span><span class="sxs-lookup"><span data-stu-id="66746-145">1 to 8</span></span> | <span data-ttu-id="66746-146">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="66746-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="66746-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="66746-147">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="66746-148">**標頭**</span><span class="sxs-lookup"><span data-stu-id="66746-148">**Header**</span></span> | <span data-ttu-id="66746-149">directml。h</span><span class="sxs-lookup"><span data-stu-id="66746-149">directml.h</span></span> |