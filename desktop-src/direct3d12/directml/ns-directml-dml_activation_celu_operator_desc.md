---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTI加值稅ION_CELU_OPERATOR_DESC
description: 在 *InputTensor* 中的每個元素上執行連續 differentiable 指數線性單位 (CELU) 啟動函式，並將結果放入 *OutputTensor* 的對應元素。
helpviewer_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- DML_ACTIVATION_CELU_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_CELU_OPERATOR_DESC, DML_ACTIVATION_CELU_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
ms.openlocfilehash: d474bd44c8a830117bb62927f4bda954a753b612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106993772"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a><span data-ttu-id="2766c-103">DML_ACTI加值稅ION_CELU_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="2766c-103">DML_ACTIVATION_CELU_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="2766c-104">在 *InputTensor* 中的每個元素上執行連續 differentiable 指數線性單位 (CELU) 啟動函式，並將結果放入 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="2766c-104">Performs the continuously differentiable exponential linear unit (CELU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

<span data-ttu-id="2766c-105">其中：</span><span class="sxs-lookup"><span data-stu-id="2766c-105">Where:</span></span>
* <span data-ttu-id="2766c-106">exp (x) 是自然乘冪函數</span><span class="sxs-lookup"><span data-stu-id="2766c-106">exp(x) is the natural exponentiation function</span></span>
* <span data-ttu-id="2766c-107">max (a，b) 傳回兩個值 a，b 的較大值</span><span class="sxs-lookup"><span data-stu-id="2766c-107">max(a,b) returns the larger of the two values a,b</span></span>
* <span data-ttu-id="2766c-108">min (a，b) 傳回兩個值 a，b 的較小者</span><span class="sxs-lookup"><span data-stu-id="2766c-108">min(a,b) returns the smaller of the two values a,b</span></span>

<span data-ttu-id="2766c-109">這個運算子支援就地執行，這表示在系結期間允許輸出 tensor 別名 *InputTensor* 。</span><span class="sxs-lookup"><span data-stu-id="2766c-109">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2766c-110">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="2766c-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="2766c-111">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="2766c-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2766c-112">語法</span><span class="sxs-lookup"><span data-stu-id="2766c-112">Syntax</span></span>
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a><span data-ttu-id="2766c-113">成員</span><span class="sxs-lookup"><span data-stu-id="2766c-113">Members</span></span>

`InputTensor`

<span data-ttu-id="2766c-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2766c-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2766c-115">要從中讀取的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="2766c-115">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="2766c-116">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2766c-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2766c-117">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="2766c-117">The output tensor to write the results to.</span></span>

`Alpha`

<span data-ttu-id="2766c-118">類型： <b> <a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="2766c-118">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="2766c-119">Alpha 係數。</span><span class="sxs-lookup"><span data-stu-id="2766c-119">The alpha coefficient.</span></span> <span data-ttu-id="2766c-120">此值的典型預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="2766c-120">A typical default for this value is 1.0.</span></span>

## <a name="availability"></a><span data-ttu-id="2766c-121">可用性</span><span class="sxs-lookup"><span data-stu-id="2766c-121">Availability</span></span>
<span data-ttu-id="2766c-122">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="2766c-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2766c-123">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="2766c-123">Tensor constraints</span></span>
<span data-ttu-id="2766c-124">*InputTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="2766c-124">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2766c-125">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="2766c-125">Tensor support</span></span>
| <span data-ttu-id="2766c-126">張</span><span class="sxs-lookup"><span data-stu-id="2766c-126">Tensor</span></span> | <span data-ttu-id="2766c-127">類型</span><span class="sxs-lookup"><span data-stu-id="2766c-127">Kind</span></span> | <span data-ttu-id="2766c-128">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="2766c-128">Supported Dimension Counts</span></span> | <span data-ttu-id="2766c-129">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="2766c-129">Supported Data Types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2766c-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="2766c-130">InputTensor</span></span> | <span data-ttu-id="2766c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2766c-131">Input</span></span> | <span data-ttu-id="2766c-132">1至8</span><span class="sxs-lookup"><span data-stu-id="2766c-132">1 to 8</span></span> | <span data-ttu-id="2766c-133">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2766c-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2766c-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="2766c-134">OutputTensor</span></span> | <span data-ttu-id="2766c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2766c-135">Output</span></span> | <span data-ttu-id="2766c-136">1至8</span><span class="sxs-lookup"><span data-stu-id="2766c-136">1 to 8</span></span> | <span data-ttu-id="2766c-137">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2766c-137">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="2766c-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="2766c-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2766c-139">**標頭**</span><span class="sxs-lookup"><span data-stu-id="2766c-139">**Header**</span></span> | <span data-ttu-id="2766c-140">directml。h</span><span class="sxs-lookup"><span data-stu-id="2766c-140">directml.h</span></span> |