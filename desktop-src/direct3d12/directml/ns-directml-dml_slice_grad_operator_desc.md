---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: 計算配量的反向傳播漸層 (請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)) 。
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 63ea67454965d976247c3cdd50aa183f6a676138
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106982132"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="86405-103">DML_SLICE_GRAD_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="86405-103">DML_SLICE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="86405-104">計算配量的反向傳播漸層 (請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)) 。</span><span class="sxs-lookup"><span data-stu-id="86405-104">Computes backpropagation gradients for Slice (see [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span></span>

<span data-ttu-id="86405-105">回想一下， [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) 會解壓縮輸入 tensor 的子領域。</span><span class="sxs-lookup"><span data-stu-id="86405-105">Recall that [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extracts a subregion of an input tensor.</span></span> <span data-ttu-id="86405-106">由於 *InputGradientTensor* 的大小與對等 **DML_SLICE1_OPERATOR_DESC** 的 *輸出* 相同，因此這個運算子會產生與 \**DML_SLICE1_OPERATOR_DESC\*\*\*輸入* 相同大小的 *OutputGradientTensor* 。</span><span class="sxs-lookup"><span data-stu-id="86405-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_SLICE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of **DML_SLICE1_OPERATOR_DESC**.</span></span> <span data-ttu-id="86405-107">配量的元素會傳播至輸出，而所有其他元素則會設定為0。</span><span class="sxs-lookup"><span data-stu-id="86405-107">The sliced elements are propagated to the output, and all other elements are set to 0.</span></span>

<span data-ttu-id="86405-108">例如，請考慮從 tensor 中解壓縮下列元素的 **DML_SLICE1_OPERATOR_DESC** ：</span><span class="sxs-lookup"><span data-stu-id="86405-108">As an example, consider a **DML_SLICE1_OPERATOR_DESC** that extracts the following elements from a tensor:</span></span>

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

<span data-ttu-id="86405-109">如果提供的 *InputWindowOffsets* / *大小* / *與* 上述範例相同，則此運算子接著會執行下列轉換。</span><span class="sxs-lookup"><span data-stu-id="86405-109">If provided the same *InputWindowOffsets*/*Sizes*/*Strides* as in the above example, this operator would then perform the following transform.</span></span>

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> <span data-ttu-id="86405-110">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="86405-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="86405-111">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="86405-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86405-112">語法</span><span class="sxs-lookup"><span data-stu-id="86405-112">Syntax</span></span>

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a><span data-ttu-id="86405-113">成員</span><span class="sxs-lookup"><span data-stu-id="86405-113">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="86405-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="86405-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="86405-115">傳入的漸層 tensor。</span><span class="sxs-lookup"><span data-stu-id="86405-115">The incoming gradient tensor.</span></span> <span data-ttu-id="86405-116">這通常是從上一層的反向傳播輸出中取得。</span><span class="sxs-lookup"><span data-stu-id="86405-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="86405-117">一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)的 *輸出* 大小相同。</span><span class="sxs-lookup"><span data-stu-id="86405-117">Typically, this tensor would have the same sizes as the *output* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="86405-118">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="86405-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="86405-119">包含 backpropagated 漸層的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="86405-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="86405-120">一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)的 *輸入* 相同。</span><span class="sxs-lookup"><span data-stu-id="86405-120">Typically, this tensor would have the same sizes as the *input* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="86405-121">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="86405-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="86405-122">*InputWindowOffsets*、 *InputWindowSizes* 和 *InputWindowStrides* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="86405-122">The number of elements in the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="86405-123">此值必須等於 *InputGradientTensor* 和 *OutputGradientTensor* 中提供的 *DimensionCount* 。</span><span class="sxs-lookup"><span data-stu-id="86405-123">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`InputWindowOffsets`

<span data-ttu-id="86405-124">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="86405-124">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="86405-125">請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)中的 *InputWindowOffsets* 。</span><span class="sxs-lookup"><span data-stu-id="86405-125">See *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowSizes`

<span data-ttu-id="86405-126">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="86405-126">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="86405-127">請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)中的 *InputWindowSizes* 。</span><span class="sxs-lookup"><span data-stu-id="86405-127">See *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowStrides`

<span data-ttu-id="86405-128">類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="86405-128">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="86405-129">請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)中的 *InputWindowStrides* 。</span><span class="sxs-lookup"><span data-stu-id="86405-129">See *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

<span data-ttu-id="86405-130">請注意，與 **DML_SLICE1_OPERATOR_DESC** 不同的是，此運算子需要非零的進步。</span><span class="sxs-lookup"><span data-stu-id="86405-130">Note that unlike **DML_SLICE1_OPERATOR_DESC**, this operator requires non-zero strides.</span></span> <span data-ttu-id="86405-131">這是因為如果有零個 stride，則不明確的是輸入元素應對應至每個輸出元素，因此無法執行反向傳播。</span><span class="sxs-lookup"><span data-stu-id="86405-131">That's because with a zero stride, it's ambiguous as to which input element should map to each output element, and therefore backpropagation can't be performed.</span></span> <span data-ttu-id="86405-132">如同 **DML_SLICE1_OPERATOR_DESC**，負的進展會沿著該軸翻轉輸入視窗的方向。</span><span class="sxs-lookup"><span data-stu-id="86405-132">Like **DML_SLICE1_OPERATOR_DESC**, negative strides flip the input window direction along that axis.</span></span>

## <a name="availability"></a><span data-ttu-id="86405-133">可用性</span><span class="sxs-lookup"><span data-stu-id="86405-133">Availability</span></span>
<span data-ttu-id="86405-134">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="86405-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="86405-135">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="86405-135">Tensor constraints</span></span>
<span data-ttu-id="86405-136">*InputGradientTensor* 和 *OutputGradientTensor* 必須具有相同的 *資料類型* 和 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="86405-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="86405-137">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="86405-137">Tensor support</span></span>
| <span data-ttu-id="86405-138">張</span><span class="sxs-lookup"><span data-stu-id="86405-138">Tensor</span></span> | <span data-ttu-id="86405-139">類型</span><span class="sxs-lookup"><span data-stu-id="86405-139">Kind</span></span> | <span data-ttu-id="86405-140">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="86405-140">Supported dimension counts</span></span> | <span data-ttu-id="86405-141">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="86405-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="86405-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="86405-142">InputGradientTensor</span></span> | <span data-ttu-id="86405-143">輸入</span><span class="sxs-lookup"><span data-stu-id="86405-143">Input</span></span> | <span data-ttu-id="86405-144">1至8</span><span class="sxs-lookup"><span data-stu-id="86405-144">1 to 8</span></span> | <span data-ttu-id="86405-145">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="86405-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="86405-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="86405-146">OutputGradientTensor</span></span> | <span data-ttu-id="86405-147">輸出</span><span class="sxs-lookup"><span data-stu-id="86405-147">Output</span></span> | <span data-ttu-id="86405-148">1至8</span><span class="sxs-lookup"><span data-stu-id="86405-148">1 to 8</span></span> | <span data-ttu-id="86405-149">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="86405-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="86405-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="86405-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="86405-151">**標頭**</span><span class="sxs-lookup"><span data-stu-id="86405-151">**Header**</span></span> | <span data-ttu-id="86405-152">directml。h</span><span class="sxs-lookup"><span data-stu-id="86405-152">directml.h</span></span> |