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
ms.openlocfilehash: 5803b40520e3735d24d00eb7260eb527ab857c33
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417319"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="a79d1-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="a79d1-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a79d1-104">依 *BTensor* 的對應元素所指定的位數，對 *ATensor* 的每個元素執行邏輯右移位，將結果放入 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="a79d1-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="a79d1-105">這個運算子支援就地執行，這表示允許 *OutputTensor* 在系結期間為其中一個輸入張量加上別名。</span><span class="sxs-lookup"><span data-stu-id="a79d1-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a79d1-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="a79d1-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a79d1-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="a79d1-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a79d1-108">語法</span><span class="sxs-lookup"><span data-stu-id="a79d1-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="a79d1-109">成員</span><span class="sxs-lookup"><span data-stu-id="a79d1-109">Members</span></span>

`ATensor`

<span data-ttu-id="a79d1-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a79d1-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a79d1-111">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="a79d1-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="a79d1-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a79d1-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a79d1-113">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="a79d1-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="a79d1-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a79d1-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a79d1-115">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="a79d1-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="a79d1-116">可用性</span><span class="sxs-lookup"><span data-stu-id="a79d1-116">Availability</span></span>
<span data-ttu-id="a79d1-117">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="a79d1-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a79d1-118">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="a79d1-118">Tensor constraints</span></span>
<span data-ttu-id="a79d1-119">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="a79d1-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a79d1-120">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="a79d1-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="a79d1-121">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="a79d1-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="a79d1-122">張</span><span class="sxs-lookup"><span data-stu-id="a79d1-122">Tensor</span></span> | <span data-ttu-id="a79d1-123">種類</span><span class="sxs-lookup"><span data-stu-id="a79d1-123">Kind</span></span> | <span data-ttu-id="a79d1-124">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="a79d1-124">Supported dimension counts</span></span> | <span data-ttu-id="a79d1-125">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="a79d1-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a79d1-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="a79d1-126">ATensor</span></span> | <span data-ttu-id="a79d1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a79d1-127">Input</span></span> | <span data-ttu-id="a79d1-128">1至8</span><span class="sxs-lookup"><span data-stu-id="a79d1-128">1 to 8</span></span> | <span data-ttu-id="a79d1-129">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a79d1-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a79d1-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="a79d1-130">BTensor</span></span> | <span data-ttu-id="a79d1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a79d1-131">Input</span></span> | <span data-ttu-id="a79d1-132">1至8</span><span class="sxs-lookup"><span data-stu-id="a79d1-132">1 to 8</span></span> | <span data-ttu-id="a79d1-133">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a79d1-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a79d1-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a79d1-134">OutputTensor</span></span> | <span data-ttu-id="a79d1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a79d1-135">Output</span></span> | <span data-ttu-id="a79d1-136">1至8</span><span class="sxs-lookup"><span data-stu-id="a79d1-136">1 to 8</span></span> | <span data-ttu-id="a79d1-137">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a79d1-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="a79d1-138">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="a79d1-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="a79d1-139">張</span><span class="sxs-lookup"><span data-stu-id="a79d1-139">Tensor</span></span> | <span data-ttu-id="a79d1-140">種類</span><span class="sxs-lookup"><span data-stu-id="a79d1-140">Kind</span></span> | <span data-ttu-id="a79d1-141">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="a79d1-141">Supported dimension counts</span></span> | <span data-ttu-id="a79d1-142">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="a79d1-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a79d1-143">ATensor</span><span class="sxs-lookup"><span data-stu-id="a79d1-143">ATensor</span></span> | <span data-ttu-id="a79d1-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a79d1-144">Input</span></span> | <span data-ttu-id="a79d1-145">4</span><span class="sxs-lookup"><span data-stu-id="a79d1-145">4</span></span> | <span data-ttu-id="a79d1-146">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a79d1-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a79d1-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="a79d1-147">BTensor</span></span> | <span data-ttu-id="a79d1-148">輸入</span><span class="sxs-lookup"><span data-stu-id="a79d1-148">Input</span></span> | <span data-ttu-id="a79d1-149">4</span><span class="sxs-lookup"><span data-stu-id="a79d1-149">4</span></span> | <span data-ttu-id="a79d1-150">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a79d1-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a79d1-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a79d1-151">OutputTensor</span></span> | <span data-ttu-id="a79d1-152">輸出</span><span class="sxs-lookup"><span data-stu-id="a79d1-152">Output</span></span> | <span data-ttu-id="a79d1-153">4</span><span class="sxs-lookup"><span data-stu-id="a79d1-153">4</span></span> | <span data-ttu-id="a79d1-154">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a79d1-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="a79d1-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="a79d1-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a79d1-156">**標頭**</span><span class="sxs-lookup"><span data-stu-id="a79d1-156">**Header**</span></span> | <span data-ttu-id="a79d1-157">directml。h</span><span class="sxs-lookup"><span data-stu-id="a79d1-157">directml.h</span></span> |