---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTI加值稅ION_RELU_GRAD_OPERATOR_DESC
description: 計算 (ReLU) 的已更正線性單位反向傳播漸層。
helpviewer_keywords:
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC, DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.openlocfilehash: dea89f0e3366a07ee98f47703f07e2f5a9d4009d
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803682"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="4e13a-103">DML_ACTI加值稅ION_RELU_GRAD_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="4e13a-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="4e13a-104">計算 (ReLU) 的已更正線性單位反向傳播漸層。</span><span class="sxs-lookup"><span data-stu-id="4e13a-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="4e13a-105">這個運算子會執行下列元素的計算。</span><span class="sxs-lookup"><span data-stu-id="4e13a-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="4e13a-106">對應的向前傳遞運算子是 [DML_ACTI加值稅ION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)。</span><span class="sxs-lookup"><span data-stu-id="4e13a-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e13a-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="4e13a-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4e13a-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="4e13a-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e13a-109">語法</span><span class="sxs-lookup"><span data-stu-id="4e13a-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="4e13a-110">成員</span><span class="sxs-lookup"><span data-stu-id="4e13a-110">Members</span></span>

`InputTensor`

<span data-ttu-id="4e13a-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4e13a-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4e13a-112">輸入 (功能) tensor。</span><span class="sxs-lookup"><span data-stu-id="4e13a-112">The input (feature) tensor.</span></span> <span data-ttu-id="4e13a-113">這通常與向前傳遞期間所提供的輸入相同 (請參閱 [DML_ACTI加值稅ION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)) 。</span><span class="sxs-lookup"><span data-stu-id="4e13a-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="4e13a-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4e13a-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4e13a-115">傳入的漸層 tensor。</span><span class="sxs-lookup"><span data-stu-id="4e13a-115">The incoming gradient tensor.</span></span> <span data-ttu-id="4e13a-116">這通常是從上一層的反向傳播輸出中取得。</span><span class="sxs-lookup"><span data-stu-id="4e13a-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="4e13a-117">這個 tensor 的大小和資料類型必須完全符合 *InputTensor* 的 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="4e13a-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="4e13a-118">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4e13a-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4e13a-119">包含 backpropagated 漸層的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="4e13a-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="4e13a-120">這個 tensor 的大小和資料類型必須完全符合 *InputTensor* 的 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="4e13a-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="4e13a-121">可用性</span><span class="sxs-lookup"><span data-stu-id="4e13a-121">Availability</span></span>
<span data-ttu-id="4e13a-122">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="4e13a-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4e13a-123">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="4e13a-123">Tensor constraints</span></span>
<span data-ttu-id="4e13a-124">*InputGradientTensor*、 *InputTensor* 和 *OutputGradientTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="4e13a-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4e13a-125">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="4e13a-125">Tensor support</span></span>
| <span data-ttu-id="4e13a-126">張</span><span class="sxs-lookup"><span data-stu-id="4e13a-126">Tensor</span></span> | <span data-ttu-id="4e13a-127">類型</span><span class="sxs-lookup"><span data-stu-id="4e13a-127">Kind</span></span> | <span data-ttu-id="4e13a-128">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="4e13a-128">Supported dimension counts</span></span> | <span data-ttu-id="4e13a-129">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="4e13a-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4e13a-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4e13a-130">InputTensor</span></span> | <span data-ttu-id="4e13a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4e13a-131">Input</span></span> | <span data-ttu-id="4e13a-132">1至8</span><span class="sxs-lookup"><span data-stu-id="4e13a-132">1 to 8</span></span> | <span data-ttu-id="4e13a-133">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4e13a-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4e13a-134">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="4e13a-134">InputGradientTensor</span></span> | <span data-ttu-id="4e13a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4e13a-135">Input</span></span> | <span data-ttu-id="4e13a-136">1至8</span><span class="sxs-lookup"><span data-stu-id="4e13a-136">1 to 8</span></span> | <span data-ttu-id="4e13a-137">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4e13a-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4e13a-138">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="4e13a-138">OutputGradientTensor</span></span> | <span data-ttu-id="4e13a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="4e13a-139">Output</span></span> | <span data-ttu-id="4e13a-140">1至8</span><span class="sxs-lookup"><span data-stu-id="4e13a-140">1 to 8</span></span> | <span data-ttu-id="4e13a-141">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4e13a-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="4e13a-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e13a-142">See also</span></span>
[<span data-ttu-id="4e13a-143">DML_ACTI加值稅ION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="4e13a-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="4e13a-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e13a-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4e13a-145">**標頭**</span><span class="sxs-lookup"><span data-stu-id="4e13a-145">**Header**</span></span> | <span data-ttu-id="4e13a-146">directml。h</span><span class="sxs-lookup"><span data-stu-id="4e13a-146">directml.h</span></span> |