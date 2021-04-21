---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: 在整數資料上執行矩陣乘法函數。
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802839"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="3a007-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="3a007-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="3a007-104">在整數資料上執行矩陣乘法函數。</span><span class="sxs-lookup"><span data-stu-id="3a007-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="3a007-105">此運算子要求矩陣乘以輸入張量為4D，格式為 `{ BatchCount, ChannelCount, Height, Width }` 。</span><span class="sxs-lookup"><span data-stu-id="3a007-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="3a007-106">矩陣乘法運算子將會執行 BatchCount \* ChannelCount number of 獨立矩陣乘法運算。</span><span class="sxs-lookup"><span data-stu-id="3a007-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="3a007-107">例如，如果 *ATensor* 的 *大小* 為， `{ BatchCount, ChannelCount, M, K }` 且 *BTensor* *的大小* 為 `{ BatchCount, ChannelCount, K, N }` ，而 *OutputTensor* 的大小為， `{ BatchCount, ChannelCount, M, N }` 則矩陣乘法運算子將會執行 BatchCount \* ChannelCount 獨立矩陣乘法運算的維度 {M，K} x {K，n} = {M，n}。</span><span class="sxs-lookup"><span data-stu-id="3a007-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a007-108">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="3a007-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="3a007-109">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="3a007-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a007-110">語法</span><span class="sxs-lookup"><span data-stu-id="3a007-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="3a007-111">成員</span><span class="sxs-lookup"><span data-stu-id="3a007-111">Members</span></span>

`ATensor`

<span data-ttu-id="3a007-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3a007-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3a007-113">包含資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="3a007-113">A tensor containing the A data.</span></span> <span data-ttu-id="3a007-114">此 tensor 的維度應該是 `{ BatchCount, ChannelCount, M, K }` 。</span><span class="sxs-lookup"><span data-stu-id="3a007-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="3a007-115">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3a007-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3a007-116">包含 ATensor 零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="3a007-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="3a007-117">`AZeroPointTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, M, 1 }` 需要針對每個資料列的量化，則預期的維度為。</span><span class="sxs-lookup"><span data-stu-id="3a007-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="3a007-118">這些零點值是用來 dequantizing *ATensor* 值。</span><span class="sxs-lookup"><span data-stu-id="3a007-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="3a007-119">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3a007-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3a007-120">包含 B 資料的 tensor。</span><span class="sxs-lookup"><span data-stu-id="3a007-120">A tensor containing the B data.</span></span> <span data-ttu-id="3a007-121">此 tensor 的維度應該是 `{ BatchCount, ChannelCount, K, N }` 。</span><span class="sxs-lookup"><span data-stu-id="3a007-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="3a007-122">Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3a007-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3a007-123">包含 *BTensor* 零點資料的選擇性 tensor。</span><span class="sxs-lookup"><span data-stu-id="3a007-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="3a007-124">`BZeroPointTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, 1, N }` 每個資料行的量化是必要的，則預期的維度為。</span><span class="sxs-lookup"><span data-stu-id="3a007-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="3a007-125">這些零點值是用來 dequantizing BTensor 值。</span><span class="sxs-lookup"><span data-stu-id="3a007-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="3a007-126">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3a007-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3a007-127">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="3a007-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="3a007-128">這個 tensor 的維度是 `{ BatchCount, ChannelCount, M, N }` 。</span><span class="sxs-lookup"><span data-stu-id="3a007-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="3a007-129">可用性</span><span class="sxs-lookup"><span data-stu-id="3a007-129">Availability</span></span>
<span data-ttu-id="3a007-130">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="3a007-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="3a007-131">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="3a007-131">Tensor constraints</span></span>
* <span data-ttu-id="3a007-132">*ATensor* 和 `AZeroPointTensor` 必須具有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="3a007-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="3a007-133">*BTensor* 和 `BZeroPointTensor` 必須具有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="3a007-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="3a007-134">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="3a007-134">Tensor support</span></span>
| <span data-ttu-id="3a007-135">張</span><span class="sxs-lookup"><span data-stu-id="3a007-135">Tensor</span></span> | <span data-ttu-id="3a007-136">類型</span><span class="sxs-lookup"><span data-stu-id="3a007-136">Kind</span></span> | <span data-ttu-id="3a007-137">維度</span><span class="sxs-lookup"><span data-stu-id="3a007-137">Dimensions</span></span> | <span data-ttu-id="3a007-138">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="3a007-138">Supported dimension counts</span></span> | <span data-ttu-id="3a007-139">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="3a007-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="3a007-140">ATensor</span><span class="sxs-lookup"><span data-stu-id="3a007-140">ATensor</span></span> | <span data-ttu-id="3a007-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3a007-141">Input</span></span> | <span data-ttu-id="3a007-142">{BatchCount，ChannelCount，M，K}</span><span class="sxs-lookup"><span data-stu-id="3a007-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="3a007-143">4</span><span class="sxs-lookup"><span data-stu-id="3a007-143">4</span></span> | <span data-ttu-id="3a007-144">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="3a007-144">INT8, UINT8</span></span> |
| <span data-ttu-id="3a007-145">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="3a007-145">AZeroPointTensor</span></span> | <span data-ttu-id="3a007-146">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="3a007-146">Optional input</span></span> | <span data-ttu-id="3a007-147">{1，1，AZeroPointCount，1}</span><span class="sxs-lookup"><span data-stu-id="3a007-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="3a007-148">4</span><span class="sxs-lookup"><span data-stu-id="3a007-148">4</span></span> | <span data-ttu-id="3a007-149">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="3a007-149">INT8, UINT8</span></span> |
| <span data-ttu-id="3a007-150">BTensor</span><span class="sxs-lookup"><span data-stu-id="3a007-150">BTensor</span></span> | <span data-ttu-id="3a007-151">輸入</span><span class="sxs-lookup"><span data-stu-id="3a007-151">Input</span></span> | <span data-ttu-id="3a007-152">{BatchCount，ChannelCount，K，N}</span><span class="sxs-lookup"><span data-stu-id="3a007-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="3a007-153">4</span><span class="sxs-lookup"><span data-stu-id="3a007-153">4</span></span> | <span data-ttu-id="3a007-154">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="3a007-154">INT8, UINT8</span></span> |
| <span data-ttu-id="3a007-155">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="3a007-155">BZeroPointTensor</span></span> | <span data-ttu-id="3a007-156">選擇性輸入</span><span class="sxs-lookup"><span data-stu-id="3a007-156">Optional input</span></span> | <span data-ttu-id="3a007-157">{1，1，1，BZeroPointCount}</span><span class="sxs-lookup"><span data-stu-id="3a007-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="3a007-158">4</span><span class="sxs-lookup"><span data-stu-id="3a007-158">4</span></span> | <span data-ttu-id="3a007-159">INT8、UINT8</span><span class="sxs-lookup"><span data-stu-id="3a007-159">INT8, UINT8</span></span> |
| <span data-ttu-id="3a007-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="3a007-160">OutputTensor</span></span> | <span data-ttu-id="3a007-161">輸出</span><span class="sxs-lookup"><span data-stu-id="3a007-161">Output</span></span> | <span data-ttu-id="3a007-162">{BatchCount，ChannelCount，M，N}</span><span class="sxs-lookup"><span data-stu-id="3a007-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="3a007-163">4</span><span class="sxs-lookup"><span data-stu-id="3a007-163">4</span></span> | <span data-ttu-id="3a007-164">INT32</span><span class="sxs-lookup"><span data-stu-id="3a007-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="3a007-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a007-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3a007-166">**標頭**</span><span class="sxs-lookup"><span data-stu-id="3a007-166">**Header**</span></span> | <span data-ttu-id="3a007-167">directml。h</span><span class="sxs-lookup"><span data-stu-id="3a007-167">directml.h</span></span> |