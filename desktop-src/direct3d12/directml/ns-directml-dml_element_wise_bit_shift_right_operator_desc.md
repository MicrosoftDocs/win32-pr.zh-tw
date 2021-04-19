---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: 依 *BTensor* 的對應元素所指定的位數，對 *ATensor* 的每個元素執行邏輯右移位，將結果放入 *OutputTensor* 的對應元素。
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_right_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.openlocfilehash: 447b0f685b51bf8b146644de3b5f65390a492ffd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106975587"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="d5d92-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="d5d92-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="d5d92-104">依 *BTensor* 的對應元素所指定的位數，對 *ATensor* 的每個元素執行邏輯右移位，將結果放入 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="d5d92-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="d5d92-105">這個運算子支援就地執行，這表示允許 *OutputTensor* 在系結期間為其中一個輸入張量加上別名。</span><span class="sxs-lookup"><span data-stu-id="d5d92-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5d92-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="d5d92-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="d5d92-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="d5d92-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d92-108">語法</span><span class="sxs-lookup"><span data-stu-id="d5d92-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="d5d92-109">成員</span><span class="sxs-lookup"><span data-stu-id="d5d92-109">Members</span></span>

`ATensor`

<span data-ttu-id="d5d92-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d5d92-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d5d92-111">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="d5d92-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="d5d92-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d5d92-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d5d92-113">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="d5d92-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="d5d92-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d5d92-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d5d92-115">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="d5d92-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="d5d92-116">可用性</span><span class="sxs-lookup"><span data-stu-id="d5d92-116">Availability</span></span>
<span data-ttu-id="d5d92-117">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="d5d92-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d5d92-118">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="d5d92-118">Tensor constraints</span></span>
<span data-ttu-id="d5d92-119">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="d5d92-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d5d92-120">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="d5d92-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="d5d92-121">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="d5d92-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="d5d92-122">張</span><span class="sxs-lookup"><span data-stu-id="d5d92-122">Tensor</span></span> | <span data-ttu-id="d5d92-123">類型</span><span class="sxs-lookup"><span data-stu-id="d5d92-123">Kind</span></span> | <span data-ttu-id="d5d92-124">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="d5d92-124">Supported dimension counts</span></span> | <span data-ttu-id="d5d92-125">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="d5d92-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d5d92-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="d5d92-126">ATensor</span></span> | <span data-ttu-id="d5d92-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d5d92-127">Input</span></span> | <span data-ttu-id="d5d92-128">1至8</span><span class="sxs-lookup"><span data-stu-id="d5d92-128">1 to 8</span></span> | <span data-ttu-id="d5d92-129">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="d5d92-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d5d92-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="d5d92-130">BTensor</span></span> | <span data-ttu-id="d5d92-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d5d92-131">Input</span></span> | <span data-ttu-id="d5d92-132">1至8</span><span class="sxs-lookup"><span data-stu-id="d5d92-132">1 to 8</span></span> | <span data-ttu-id="d5d92-133">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="d5d92-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d5d92-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d5d92-134">OutputTensor</span></span> | <span data-ttu-id="d5d92-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d5d92-135">Output</span></span> | <span data-ttu-id="d5d92-136">1至8</span><span class="sxs-lookup"><span data-stu-id="d5d92-136">1 to 8</span></span> | <span data-ttu-id="d5d92-137">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="d5d92-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="d5d92-138">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="d5d92-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="d5d92-139">張</span><span class="sxs-lookup"><span data-stu-id="d5d92-139">Tensor</span></span> | <span data-ttu-id="d5d92-140">類型</span><span class="sxs-lookup"><span data-stu-id="d5d92-140">Kind</span></span> | <span data-ttu-id="d5d92-141">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="d5d92-141">Supported dimension counts</span></span> | <span data-ttu-id="d5d92-142">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="d5d92-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d5d92-143">ATensor</span><span class="sxs-lookup"><span data-stu-id="d5d92-143">ATensor</span></span> | <span data-ttu-id="d5d92-144">輸入</span><span class="sxs-lookup"><span data-stu-id="d5d92-144">Input</span></span> | <span data-ttu-id="d5d92-145">4</span><span class="sxs-lookup"><span data-stu-id="d5d92-145">4</span></span> | <span data-ttu-id="d5d92-146">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="d5d92-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d5d92-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="d5d92-147">BTensor</span></span> | <span data-ttu-id="d5d92-148">輸入</span><span class="sxs-lookup"><span data-stu-id="d5d92-148">Input</span></span> | <span data-ttu-id="d5d92-149">4</span><span class="sxs-lookup"><span data-stu-id="d5d92-149">4</span></span> | <span data-ttu-id="d5d92-150">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="d5d92-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d5d92-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d5d92-151">OutputTensor</span></span> | <span data-ttu-id="d5d92-152">輸出</span><span class="sxs-lookup"><span data-stu-id="d5d92-152">Output</span></span> | <span data-ttu-id="d5d92-153">4</span><span class="sxs-lookup"><span data-stu-id="d5d92-153">4</span></span> | <span data-ttu-id="d5d92-154">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="d5d92-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="d5d92-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5d92-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d5d92-156">**標頭**</span><span class="sxs-lookup"><span data-stu-id="d5d92-156">**Header**</span></span> | <span data-ttu-id="d5d92-157">directml。h</span><span class="sxs-lookup"><span data-stu-id="d5d92-157">directml.h</span></span> |