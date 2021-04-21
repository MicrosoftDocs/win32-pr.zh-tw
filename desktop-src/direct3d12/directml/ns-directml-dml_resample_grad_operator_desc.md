---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: 計算重新取樣的反向傳播漸層 (請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)) 。
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 0caba1a560b72a94ed04cacd824414964af82c35
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804049"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="b7d70-103">DML_RESAMPLE_GRAD_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="b7d70-103">DML_RESAMPLE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b7d70-104">計算重新取樣的反向傳播漸層 (請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)) 。</span><span class="sxs-lookup"><span data-stu-id="b7d70-104">Computes backpropagation gradients for Resample (see [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span></span>

<span data-ttu-id="b7d70-105">**DML_RESAMPLE1_OPERATOR_DESC** 使用最接近的鄰近取樣或雙線性插補，方式將輸入 tensor 的任意維度。</span><span class="sxs-lookup"><span data-stu-id="b7d70-105">**DML_RESAMPLE1_OPERATOR_DESC** rescales arbitrary dimensions of the input tensor using either nearest-neighbor sampling or bilinear interpolation.</span></span> <span data-ttu-id="b7d70-106">由於 *InputGradientTensor* 的大小與對等 **DML_RESAMPLE1_OPERATOR_DESC** 的 *輸出* 相同，因此這個運算子會產生與 \**DML_RESAMPLE1_OPERATOR_DESC\*\*\*輸入* 相同大小的 *OutputGradientTensor* 。</span><span class="sxs-lookup"><span data-stu-id="b7d70-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_RESAMPLE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of the **DML_RESAMPLE1_OPERATOR_DESC**.</span></span>

<span data-ttu-id="b7d70-107">例如，假設有一個 **DML_RESAMPLE1_OPERATOR_DESC** ，其會在寬度中執行 1.5 x 的最接近鄰近比例，以及高度的 0.5 x。</span><span class="sxs-lookup"><span data-stu-id="b7d70-107">As an example, consider a **DML_RESAMPLE1_OPERATOR_DESC** that performs a nearest-neighbor scaling of 1.5x in the width, and 0.5x in the height.</span></span>

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

<span data-ttu-id="b7d70-108">請注意，輸入 tensor (值) 1 的第0個元素如何在輸出中提供兩個元素，第1個元素 (值 2) 會提供給輸出中的一個專案，而第二個和第三個元素（值3和4） (則不會構成輸出的元素。</span><span class="sxs-lookup"><span data-stu-id="b7d70-108">Notice how the 0th element of the input tensor (with value 1) contributes to two elements in the output, the 1st element (with value 2) contributes to one element in the output, and the 2nd and 3rd elements (with values 3 and 4) contribute to no elements of the output.</span></span>

<span data-ttu-id="b7d70-109">對應的 **DML_RESAMPLE_GRAD_OPERATOR_DESC** 會執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="b7d70-109">The corresponding **DML_RESAMPLE_GRAD_OPERATOR_DESC** would perform the following.</span></span>

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

<span data-ttu-id="b7d70-110">請注意， *OutputGradientTensor* 中的值代表該元素在原始 **DML_RESAMPLE1_OPERATOR_DESC** 運算子期間對 *OutputTensor* 的加權貢獻。</span><span class="sxs-lookup"><span data-stu-id="b7d70-110">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original **DML_RESAMPLE1_OPERATOR_DESC** operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7d70-111">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="b7d70-111">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b7d70-112">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="b7d70-112">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d70-113">語法</span><span class="sxs-lookup"><span data-stu-id="b7d70-113">Syntax</span></span>

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a><span data-ttu-id="b7d70-114">成員</span><span class="sxs-lookup"><span data-stu-id="b7d70-114">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="b7d70-115">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b7d70-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b7d70-116">傳入的漸層 tensor。</span><span class="sxs-lookup"><span data-stu-id="b7d70-116">The incoming gradient tensor.</span></span> <span data-ttu-id="b7d70-117">這通常是從上一層的反向傳播輸出中取得。</span><span class="sxs-lookup"><span data-stu-id="b7d70-117">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="b7d70-118">一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)的 *輸出* 相同。</span><span class="sxs-lookup"><span data-stu-id="b7d70-118">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="b7d70-119">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b7d70-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b7d70-120">包含 backpropagated 漸層的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="b7d70-120">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="b7d70-121">一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)的 *輸入* 相同。</span><span class="sxs-lookup"><span data-stu-id="b7d70-121">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`InterpolationMode`

<span data-ttu-id="b7d70-122">類型： [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="b7d70-122">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="b7d70-123">請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)中的 *InterpolationMode* 。</span><span class="sxs-lookup"><span data-stu-id="b7d70-123">See *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`DimensionCount`

<span data-ttu-id="b7d70-124">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b7d70-124">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b7d70-125">*刻度*、 *InputPixelOffsets* 和 *OutputPixelOffsets* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="b7d70-125">The number of elements in the *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* arrays.</span></span> <span data-ttu-id="b7d70-126">此值必須等於 *InputGradientTensor* 和 *OutputGradientTensor* 中提供的 *DimensionCount* 。</span><span class="sxs-lookup"><span data-stu-id="b7d70-126">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`Scales`

<span data-ttu-id="b7d70-127">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b7d70-127">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="b7d70-128">請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)中的 *刻度*。</span><span class="sxs-lookup"><span data-stu-id="b7d70-128">See *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`InputPixelOffsets`

<span data-ttu-id="b7d70-129">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b7d70-129">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="b7d70-130">請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)中的 *InputPixelOffsets* 。</span><span class="sxs-lookup"><span data-stu-id="b7d70-130">See *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`OutputPixelOffsets`

<span data-ttu-id="b7d70-131">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b7d70-131">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="b7d70-132">請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)中的 *OutputPixelOffsets* 。</span><span class="sxs-lookup"><span data-stu-id="b7d70-132">See *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="b7d70-133">可用性</span><span class="sxs-lookup"><span data-stu-id="b7d70-133">Availability</span></span>
<span data-ttu-id="b7d70-134">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="b7d70-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b7d70-135">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="b7d70-135">Tensor constraints</span></span>
<span data-ttu-id="b7d70-136">*InputGradientTensor* 和 *OutputGradientTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="b7d70-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b7d70-137">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="b7d70-137">Tensor support</span></span>
| <span data-ttu-id="b7d70-138">張</span><span class="sxs-lookup"><span data-stu-id="b7d70-138">Tensor</span></span> | <span data-ttu-id="b7d70-139">類型</span><span class="sxs-lookup"><span data-stu-id="b7d70-139">Kind</span></span> | <span data-ttu-id="b7d70-140">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="b7d70-140">Supported dimension counts</span></span> | <span data-ttu-id="b7d70-141">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="b7d70-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b7d70-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="b7d70-142">InputGradientTensor</span></span> | <span data-ttu-id="b7d70-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b7d70-143">Input</span></span> | <span data-ttu-id="b7d70-144">4</span><span class="sxs-lookup"><span data-stu-id="b7d70-144">4</span></span> | <span data-ttu-id="b7d70-145">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b7d70-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="b7d70-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="b7d70-146">OutputGradientTensor</span></span> | <span data-ttu-id="b7d70-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b7d70-147">Output</span></span> | <span data-ttu-id="b7d70-148">4</span><span class="sxs-lookup"><span data-stu-id="b7d70-148">4</span></span> | <span data-ttu-id="b7d70-149">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b7d70-149">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="b7d70-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7d70-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b7d70-151">**標頭**</span><span class="sxs-lookup"><span data-stu-id="b7d70-151">**Header**</span></span> | <span data-ttu-id="b7d70-152">directml。h</span><span class="sxs-lookup"><span data-stu-id="b7d70-152">directml.h</span></span> |