---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: 計算平均共用 (的反向傳播梯度，請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)) 。
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: aaa2b5d2becac421214afe7c643426c1c93cf899
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417323"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="36a51-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="36a51-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="36a51-104">計算平均共用 (的反向傳播梯度，請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)) 。</span><span class="sxs-lookup"><span data-stu-id="36a51-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="36a51-105">請考慮採用 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**，但不含填補和1的跨距，以執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="36a51-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="36a51-106">輸入 tensor 中的每個2x2 視窗平均是為了產生輸出的一個元素， (在邊緣) 以外的元素中讀取零。</span><span class="sxs-lookup"><span data-stu-id="36a51-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="36a51-107">以下是 **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** 指定類似參數的輸出範例。</span><span class="sxs-lookup"><span data-stu-id="36a51-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="36a51-108">請注意， *OutputGradientTensor* 中的值代表該元素在原始 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)運算子期間對 *OutputTensor* 的加權貢獻。</span><span class="sxs-lookup"><span data-stu-id="36a51-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36a51-109">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="36a51-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="36a51-110">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="36a51-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="36a51-111">語法</span><span class="sxs-lookup"><span data-stu-id="36a51-111">Syntax</span></span>

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a><span data-ttu-id="36a51-112">成員</span><span class="sxs-lookup"><span data-stu-id="36a51-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="36a51-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="36a51-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="36a51-114">傳入的漸層 tensor。</span><span class="sxs-lookup"><span data-stu-id="36a51-114">The incoming gradient tensor.</span></span> <span data-ttu-id="36a51-115">這通常是從上一層的反向傳播輸出中取得。</span><span class="sxs-lookup"><span data-stu-id="36a51-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="36a51-116">一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)的 *輸出* 相同。</span><span class="sxs-lookup"><span data-stu-id="36a51-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="36a51-117">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="36a51-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="36a51-118">包含 backpropagated 漸層的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="36a51-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="36a51-119">一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)的 *輸入* 相同。</span><span class="sxs-lookup"><span data-stu-id="36a51-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="36a51-120">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="36a51-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="36a51-121">*進步*、 *WindowSize*、 *StartPadding* 和 *EndPadding* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="36a51-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="36a51-122">這個值必須等於空間維度計數。</span><span class="sxs-lookup"><span data-stu-id="36a51-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="36a51-123">如果提供4D 張量，則空間維度計數是2，如果提供了5D 張量，則為3。</span><span class="sxs-lookup"><span data-stu-id="36a51-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="36a51-124">類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="36a51-124">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="36a51-125">請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)中的 *進步*。</span><span class="sxs-lookup"><span data-stu-id="36a51-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="36a51-126">類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="36a51-126">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="36a51-127">請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)中的 *WindowSize* 。</span><span class="sxs-lookup"><span data-stu-id="36a51-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="36a51-128">類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="36a51-128">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="36a51-129">請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)中的 *StartPadding* 。</span><span class="sxs-lookup"><span data-stu-id="36a51-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="36a51-130">類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="36a51-130">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="36a51-131">請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)中的 *EndPadding* 。</span><span class="sxs-lookup"><span data-stu-id="36a51-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="36a51-132">類型： <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="36a51-132">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="36a51-133">請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)中的 *IncludePadding* 。</span><span class="sxs-lookup"><span data-stu-id="36a51-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="36a51-134">可用性</span><span class="sxs-lookup"><span data-stu-id="36a51-134">Availability</span></span>
<span data-ttu-id="36a51-135">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="36a51-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="36a51-136">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="36a51-136">Tensor constraints</span></span>
<span data-ttu-id="36a51-137">*InputGradientTensor* 和 *OutputGradientTensor* 必須具有相同的 *資料類型* 和 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="36a51-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="36a51-138">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="36a51-138">Tensor support</span></span>
| <span data-ttu-id="36a51-139">張</span><span class="sxs-lookup"><span data-stu-id="36a51-139">Tensor</span></span> | <span data-ttu-id="36a51-140">種類</span><span class="sxs-lookup"><span data-stu-id="36a51-140">Kind</span></span> | <span data-ttu-id="36a51-141">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="36a51-141">Supported dimension counts</span></span> | <span data-ttu-id="36a51-142">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="36a51-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="36a51-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="36a51-143">InputGradientTensor</span></span> | <span data-ttu-id="36a51-144">輸入</span><span class="sxs-lookup"><span data-stu-id="36a51-144">Input</span></span> | <span data-ttu-id="36a51-145">4到5</span><span class="sxs-lookup"><span data-stu-id="36a51-145">4 to 5</span></span> | <span data-ttu-id="36a51-146">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="36a51-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="36a51-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="36a51-147">OutputGradientTensor</span></span> | <span data-ttu-id="36a51-148">輸出</span><span class="sxs-lookup"><span data-stu-id="36a51-148">Output</span></span> | <span data-ttu-id="36a51-149">4到5</span><span class="sxs-lookup"><span data-stu-id="36a51-149">4 to 5</span></span> | <span data-ttu-id="36a51-150">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="36a51-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="36a51-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="36a51-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="36a51-152">**標頭**</span><span class="sxs-lookup"><span data-stu-id="36a51-152">**Header**</span></span> | <span data-ttu-id="36a51-153">directml。h</span><span class="sxs-lookup"><span data-stu-id="36a51-153">directml.h</span></span> |