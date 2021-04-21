---
UID: NS:directml.DML_GATHER_ELEMENTS_OPERATOR_DESC
title: DML_GATHER_ELEMENTS_OPERATOR_DESC
description: 使用索引 tensor，在指定的軸上收集輸入 tensor 的元素，以重新對應至輸入。
helpviewer_keywords:
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- DML_GATHER_ELEMENTS_OPERATOR_DESC structure
- direct3d12.dml_gather_elements_operator_desc
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.openlocfilehash: 89a4f2017f6adec8cce206e9261eb0fa6563e94c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803016"
---
# <a name="dml_gather_elements_operator_desc-structure-directmlh"></a><span data-ttu-id="c22d4-103">DML_GATHER_ELEMENTS_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="c22d4-103">DML_GATHER_ELEMENTS_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="c22d4-104">使用索引 tensor，在指定的軸上收集輸入 tensor 的元素，以重新對應至輸入。</span><span class="sxs-lookup"><span data-stu-id="c22d4-104">Gathers elements from the input tensor along the given axis using the indices tensor to remap into the input.</span></span> <span data-ttu-id="c22d4-105">這個運算子會執行下列虛擬型，其確切行為取決於軸、輸入維度計數和索引維度計數。</span><span class="sxs-lookup"><span data-stu-id="c22d4-105">This operator performs the following pseudocode, with the exact behavior dependent on the axis, input dimension count, and indices dimension count.</span></span>

```
output[i, j, k, ...] = input[index[i, j, k, ...], j, k, ...] // if axis == 0
output[i, j, k, ...] = input[i, index[i, j, k, ...], k, ...] // if axis == 1
output[i, j, k, ...] = input[i, j, index[i, j, k, ...], ...] // if axis == 2
...
```

> [!IMPORTANT]
> <span data-ttu-id="c22d4-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c22d4-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="c22d4-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="c22d4-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c22d4-108">語法</span><span class="sxs-lookup"><span data-stu-id="c22d4-108">Syntax</span></span>
```cpp
struct DML_GATHER_ELEMENTS_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="c22d4-109">成員</span><span class="sxs-lookup"><span data-stu-id="c22d4-109">Members</span></span>

`InputTensor`

<span data-ttu-id="c22d4-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c22d4-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c22d4-111">要從中讀取的 tensor。</span><span class="sxs-lookup"><span data-stu-id="c22d4-111">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="c22d4-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c22d4-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c22d4-113">沿著現用軸之輸入 tensor 的索引。</span><span class="sxs-lookup"><span data-stu-id="c22d4-113">The indices into the input tensor along the active axis.</span></span> <span data-ttu-id="c22d4-114">*大小* 必須符合 *InputTensor。* 每個維度的大小，但 *軸* 除外。</span><span class="sxs-lookup"><span data-stu-id="c22d4-114">The *Sizes* must match *InputTensor.Sizes* for every dimension except *Axis*.</span></span>

<span data-ttu-id="c22d4-115">從開始 `DML_FEATURE_LEVEL_3_0` ，當使用帶正負號的整數型別搭配這個 tensor 時，這個運算子支援負的索引值。</span><span class="sxs-lookup"><span data-stu-id="c22d4-115">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="c22d4-116">負索引會視為相對於軸維度的結尾。</span><span class="sxs-lookup"><span data-stu-id="c22d4-116">Negative indices are interpreted as being relative to the end of the axis dimension.</span></span> <span data-ttu-id="c22d4-117">例如，-1 的索引指的是該維度的最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="c22d4-117">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="c22d4-118">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c22d4-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c22d4-119">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="c22d4-119">The tensor to write the results to.</span></span> <span data-ttu-id="c22d4-120">*大小* 必須符合 *IndicesTensor 的大小*，且 *資料類型* 必須符合 *InputTensor 的資料類型*。</span><span class="sxs-lookup"><span data-stu-id="c22d4-120">The *Sizes* must match *IndicesTensor.Sizes*, and *DataType* must match *InputTensor.DataType*.</span></span>


`Axis`

<span data-ttu-id="c22d4-121">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c22d4-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c22d4-122">要收集的 *InputTensor* 軸維度，範圍為 `[0, *InputTensor.DimensionCount*)` 。</span><span class="sxs-lookup"><span data-stu-id="c22d4-122">The axis dimension of *InputTensor* to gather along, ranging `[0, *InputTensor.DimensionCount*)`.</span></span>

## <a name="examples"></a><span data-ttu-id="c22d4-123">範例</span><span class="sxs-lookup"><span data-stu-id="c22d4-123">Examples</span></span>

```
Axis = 0

InputTensor: (Sizes:{3,3}, DataType:FLOAT32)
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]

IndicesTensor: (Sizes:{2,3}, DataType:UINT32)
    [[1, 2, 0],
     [2, 0, 0]]

// output[y, x] = input[indices[y, x], x]
OutputTensor: (Sizes:{2,3}, DataType:UINT32)
    [[4, 8, 3], // select elements vertically from data
     [7, 2, 3]]
```

## <a name="availability"></a><span data-ttu-id="c22d4-124">可用性</span><span class="sxs-lookup"><span data-stu-id="c22d4-124">Availability</span></span>
<span data-ttu-id="c22d4-125">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="c22d4-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c22d4-126">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="c22d4-126">Tensor constraints</span></span>
* <span data-ttu-id="c22d4-127">`IndicesTensor`、 *InputTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount*。</span><span class="sxs-lookup"><span data-stu-id="c22d4-127">`IndicesTensor`, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="c22d4-128">*InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="c22d4-128">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c22d4-129">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="c22d4-129">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="c22d4-130">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="c22d4-130">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="c22d4-131">張</span><span class="sxs-lookup"><span data-stu-id="c22d4-131">Tensor</span></span> | <span data-ttu-id="c22d4-132">類型</span><span class="sxs-lookup"><span data-stu-id="c22d4-132">Kind</span></span> | <span data-ttu-id="c22d4-133">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="c22d4-133">Supported dimension counts</span></span> | <span data-ttu-id="c22d4-134">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="c22d4-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c22d4-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c22d4-135">InputTensor</span></span> | <span data-ttu-id="c22d4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c22d4-136">Input</span></span> | <span data-ttu-id="c22d4-137">1至8</span><span class="sxs-lookup"><span data-stu-id="c22d4-137">1 to 8</span></span> | <span data-ttu-id="c22d4-138">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="c22d4-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c22d4-139">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="c22d4-139">IndicesTensor</span></span> | <span data-ttu-id="c22d4-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c22d4-140">Input</span></span> | <span data-ttu-id="c22d4-141">1至8</span><span class="sxs-lookup"><span data-stu-id="c22d4-141">1 to 8</span></span> | <span data-ttu-id="c22d4-142">INT64、INT32、UINT64、UINT32</span><span class="sxs-lookup"><span data-stu-id="c22d4-142">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="c22d4-143">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c22d4-143">OutputTensor</span></span> | <span data-ttu-id="c22d4-144">輸出</span><span class="sxs-lookup"><span data-stu-id="c22d4-144">Output</span></span> | <span data-ttu-id="c22d4-145">1至8</span><span class="sxs-lookup"><span data-stu-id="c22d4-145">1 to 8</span></span> | <span data-ttu-id="c22d4-146">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="c22d4-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="c22d4-147">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="c22d4-147">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="c22d4-148">張</span><span class="sxs-lookup"><span data-stu-id="c22d4-148">Tensor</span></span> | <span data-ttu-id="c22d4-149">類型</span><span class="sxs-lookup"><span data-stu-id="c22d4-149">Kind</span></span> | <span data-ttu-id="c22d4-150">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="c22d4-150">Supported dimension counts</span></span> | <span data-ttu-id="c22d4-151">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="c22d4-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c22d4-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c22d4-152">InputTensor</span></span> | <span data-ttu-id="c22d4-153">輸入</span><span class="sxs-lookup"><span data-stu-id="c22d4-153">Input</span></span> | <span data-ttu-id="c22d4-154">4</span><span class="sxs-lookup"><span data-stu-id="c22d4-154">4</span></span> | <span data-ttu-id="c22d4-155">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="c22d4-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c22d4-156">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="c22d4-156">IndicesTensor</span></span> | <span data-ttu-id="c22d4-157">輸入</span><span class="sxs-lookup"><span data-stu-id="c22d4-157">Input</span></span> | <span data-ttu-id="c22d4-158">4</span><span class="sxs-lookup"><span data-stu-id="c22d4-158">4</span></span> | <span data-ttu-id="c22d4-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="c22d4-159">UINT32</span></span> |
| <span data-ttu-id="c22d4-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c22d4-160">OutputTensor</span></span> | <span data-ttu-id="c22d4-161">輸出</span><span class="sxs-lookup"><span data-stu-id="c22d4-161">Output</span></span> | <span data-ttu-id="c22d4-162">4</span><span class="sxs-lookup"><span data-stu-id="c22d4-162">4</span></span> | <span data-ttu-id="c22d4-163">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="c22d4-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="c22d4-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="c22d4-164">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c22d4-165">**標頭**</span><span class="sxs-lookup"><span data-stu-id="c22d4-165">**Header**</span></span> | <span data-ttu-id="c22d4-166">directml。h</span><span class="sxs-lookup"><span data-stu-id="c22d4-166">directml.h</span></span> |