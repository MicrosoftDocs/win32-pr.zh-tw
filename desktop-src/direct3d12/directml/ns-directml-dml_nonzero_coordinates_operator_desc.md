---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: 計算輸入 tensor 的所有非零元素的 N 維座標。
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: 39463ba57bc90b35d5ac5dc7fc43993169137221
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417237"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a><span data-ttu-id="4f3b6-103">DML_NONZERO_COORDINATES_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="4f3b6-103">DML_NONZERO_COORDINATES_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="4f3b6-104">計算輸入 tensor 的所有非零元素的 N 維座標。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-104">Computes the N-dimensional coordinates of all non-zero elements of the input tensor.</span></span>

<span data-ttu-id="4f3b6-105">這個運算子會產生值的 MxN 矩陣，其中每個資料列 M 包含輸入中非零值的 N 維座標。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-105">This operator produces an MxN matrix of values, where each row M contains an N-dimensional coordinate of a non-zero value from the input.</span></span> <span data-ttu-id="4f3b6-106">使用 **FLOAT32** 或 **FLOAT16** 輸入時，負號和正 0 (0.0 f 和-0.0 f) 會視為零，以供此運算子的用途使用。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-106">When using **FLOAT32** or **FLOAT16** inputs, both negative and positive 0 (0.0f and -0.0f) are treated as zero for the purposes of this operator.</span></span>

<span data-ttu-id="4f3b6-107">運算子要求 *OutputCoordinatesTensor* 的大小必須夠大，才能容納最糟的情況，其中輸入的每個元素都不是零。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-107">The operator requires that the *OutputCoordinatesTensor* has a size large enough to accommodate a worst-case scenario where every element of the input is non-zero.</span></span> <span data-ttu-id="4f3b6-108">這個運算子會透過 *OutputCountTensor* 傳回非零元素的計數，而呼叫端可以檢查以判斷寫入 *OutputCoordinatesTensor* 的座標數目。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-108">This operator returns the count of of non-zero elements via the *OutputCountTensor*, which callers can inspect to determine the number of coordinates written to the *OutputCoordinatesTensor*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f3b6-109">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4f3b6-110">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f3b6-111">語法</span><span class="sxs-lookup"><span data-stu-id="4f3b6-111">Syntax</span></span>

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a><span data-ttu-id="4f3b6-112">成員</span><span class="sxs-lookup"><span data-stu-id="4f3b6-112">Members</span></span>

`InputTensor`

<span data-ttu-id="4f3b6-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4f3b6-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4f3b6-114">輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-114">An input tensor.</span></span>

`OutputCountTensor`

<span data-ttu-id="4f3b6-115">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4f3b6-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4f3b6-116">在輸入 tensor 中保存非零元素計數的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-116">An output tensor that holds the count of non-zero elements in the input tensor.</span></span> <span data-ttu-id="4f3b6-117">這個 tensor 必須是純量， &mdash; 也就是這個 tensor 的大小必須全部為1。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-117">This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1.</span></span> <span data-ttu-id="4f3b6-118">這個 tensor 的型別必須是 **UINT32**。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-118">The type of this tensor must be **UINT32**.</span></span>

`OutputCoordinatesTensor`

<span data-ttu-id="4f3b6-119">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4f3b6-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4f3b6-120">輸出 tensor，其中保存非零之輸入元素的 N 維座標。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-120">An output tensor that holds the N-dimensional coordinates of the input elements which are non-zero.</span></span> 

<span data-ttu-id="4f3b6-121">如果 DimensionCount 為 4) ，則此 tensor 的 *大小* 必須是 (，如果 `{1,1,M,N}`  `{1,1,1,M,N}` *DimensionCount* 為 5) ，則為 (，其中 M 是 *InputTensor* 中的專案總數，而 N 大於或等於有效的 *InputTensor\*\*次序*，最多可達輸入的 *DimensionCount* 。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-121">This tensor must have *Sizes* of `{1,1,M,N}` (if *DimensionCount* is 4), or `{1,1,1,M,N}` (if *DimensionCount* is 5), where M is the total number of elements in the *InputTensor*, and N is greater or equal to the *effective rank* of *InputTensor*, up to the *DimensionCount* of the input.</span></span>

<span data-ttu-id="4f3b6-122">Tensor 的有效順位是由該 tensor 的 *DimensionCount* 所決定，而不是大小為1的開頭維度。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-122">The effective rank of a tensor is determined by the *DimensionCount* of that tensor excluding leading dimensions of size 1.</span></span> <span data-ttu-id="4f3b6-123">例如，大小為的 tensor `{1,2,3,4}` 具有有效的順位3，與大小的 tensor 相同 `{1,1,5,5,5}` 。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-123">For example a tensor with sizes of `{1,2,3,4}` has effective rank 3, as does a tensor with sizes of `{1,1,5,5,5}`.</span></span> <span data-ttu-id="4f3b6-124">具有大小的 tensor `{1,1,1,1}` 具有有效的順位0。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-124">A tensor with sizes `{1,1,1,1}` has effective rank 0.</span></span>

<span data-ttu-id="4f3b6-125">考慮使用 *大小* 為的 *InputTensor* `{1,1,12,5}` 。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-125">Consider an *InputTensor* with *Sizes* of `{1,1,12,5}`.</span></span> <span data-ttu-id="4f3b6-126">此輸入 tensor 包含60個元素，且具有有效的順位2。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-126">This input tensor contains 60 elements, and has an effective rank of 2.</span></span> <span data-ttu-id="4f3b6-127">在此範例中，所有有效的 *OutputCoordinatesTensor* 大小都屬於表單 `{1,1,60,N}` ，其中 N >= 2，但在此範例) 中不大於 *DimensionCount* (4。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-127">In this example all valid sizes of *OutputCoordinatesTensor* are of the form `{1,1,60,N}`, where N >= 2 but no greater than the *DimensionCount* (4 in this example).</span></span>

<span data-ttu-id="4f3b6-128">寫入此 tensor 的座標保證會以遞增的元素索引來排序。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-128">The coordinates written into this tensor are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="4f3b6-129">例如，如果輸入 tensor 在座標、和上有3個非零值， {1,0} {1,2} {0,5} 則寫入 *OutputCoordinatesTensor* 的值將會是 `[[0,5], [1,0], [1,2]]` 。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-129">For example if the input tensor has 3 non-zero values at coordinates {1,0}, {1,2}, and {0,5}, the values written to the *OutputCoordinatesTensor* will be `[[0,5], [1,0], [1,2]]`.</span></span>

<span data-ttu-id="4f3b6-130">雖然此 tensor 需要其維度 M 等於輸入 tensor 中的元素數目，但這個運算子只會將 OutputCount 元素最多寫入此 tensor。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-130">While this tensor requires its dimension M to equal the number of elements in the input tensor, this operator will only write a maximum of OutputCount elements to this tensor.</span></span> <span data-ttu-id="4f3b6-131">OutputCount 會透過純量 *OutputCountTensor* 傳回。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-131">The OutputCount is returned through the scalar *OutputCountTensor*.</span></span>

> [!NOTE]
> <span data-ttu-id="4f3b6-132">當這個運算子完成之後，此 tensor 的其餘元素就不會定義。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-132">The remaining elements of this tensor beyond the OutputCount are undefined once this operator completes.</span></span> <span data-ttu-id="4f3b6-133">您不應該依賴這些元素的值。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-133">You shouldn't rely on the values of these elements.</span></span>

## <a name="example"></a><span data-ttu-id="4f3b6-134">範例</span><span class="sxs-lookup"><span data-stu-id="4f3b6-134">Example</span></span>

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a><span data-ttu-id="4f3b6-135">可用性</span><span class="sxs-lookup"><span data-stu-id="4f3b6-135">Availability</span></span>
<span data-ttu-id="4f3b6-136">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-136">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4f3b6-137">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="4f3b6-137">Tensor constraints</span></span>
<span data-ttu-id="4f3b6-138">*InputTensor*、 *OutputCoordinatesTensor* 和 `OutputCountTensor` 必須有相同的 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="4f3b6-138">*InputTensor*, *OutputCoordinatesTensor*, and `OutputCountTensor` must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4f3b6-139">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="4f3b6-139">Tensor support</span></span>
| <span data-ttu-id="4f3b6-140">張</span><span class="sxs-lookup"><span data-stu-id="4f3b6-140">Tensor</span></span> | <span data-ttu-id="4f3b6-141">種類</span><span class="sxs-lookup"><span data-stu-id="4f3b6-141">Kind</span></span> | <span data-ttu-id="4f3b6-142">維度</span><span class="sxs-lookup"><span data-stu-id="4f3b6-142">Dimensions</span></span> | <span data-ttu-id="4f3b6-143">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="4f3b6-143">Supported dimension counts</span></span> | <span data-ttu-id="4f3b6-144">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="4f3b6-144">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="4f3b6-145">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4f3b6-145">InputTensor</span></span> | <span data-ttu-id="4f3b6-146">輸入</span><span class="sxs-lookup"><span data-stu-id="4f3b6-146">Input</span></span> | <span data-ttu-id="4f3b6-147">{[D0]、D1、D2、D3、D4}</span><span class="sxs-lookup"><span data-stu-id="4f3b6-147">{ [D0], D1, D2, D3, D4 }</span></span> | <span data-ttu-id="4f3b6-148">4到5</span><span class="sxs-lookup"><span data-stu-id="4f3b6-148">4 to 5</span></span> | <span data-ttu-id="4f3b6-149">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="4f3b6-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="4f3b6-150">OutputCountTensor</span><span class="sxs-lookup"><span data-stu-id="4f3b6-150">OutputCountTensor</span></span> | <span data-ttu-id="4f3b6-151">輸出</span><span class="sxs-lookup"><span data-stu-id="4f3b6-151">Output</span></span> | <span data-ttu-id="4f3b6-152">{[1]，1，1，1，1}</span><span class="sxs-lookup"><span data-stu-id="4f3b6-152">{ [1], 1, 1, 1, 1 }</span></span> | <span data-ttu-id="4f3b6-153">4到5</span><span class="sxs-lookup"><span data-stu-id="4f3b6-153">4 to 5</span></span> | <span data-ttu-id="4f3b6-154">UINT32</span><span class="sxs-lookup"><span data-stu-id="4f3b6-154">UINT32</span></span> |
| <span data-ttu-id="4f3b6-155">OutputCoordinatesTensor</span><span class="sxs-lookup"><span data-stu-id="4f3b6-155">OutputCoordinatesTensor</span></span> | <span data-ttu-id="4f3b6-156">輸出</span><span class="sxs-lookup"><span data-stu-id="4f3b6-156">Output</span></span> | <span data-ttu-id="4f3b6-157">{[1]，1，1，M，N}</span><span class="sxs-lookup"><span data-stu-id="4f3b6-157">{ [1], 1, 1, M, N }</span></span> | <span data-ttu-id="4f3b6-158">4到5</span><span class="sxs-lookup"><span data-stu-id="4f3b6-158">4 to 5</span></span> | <span data-ttu-id="4f3b6-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="4f3b6-159">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="4f3b6-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f3b6-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4f3b6-161">**標頭**</span><span class="sxs-lookup"><span data-stu-id="4f3b6-161">**Header**</span></span> | <span data-ttu-id="4f3b6-162">directml。h</span><span class="sxs-lookup"><span data-stu-id="4f3b6-162">directml.h</span></span> |