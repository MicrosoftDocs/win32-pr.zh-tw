---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
description: 依 *BTensor* 的對應元素所指定的位數，對 *ATensor* 的每個元素執行邏輯左移位，將結果放入 *OutputTensor* 的對應元素。
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_left_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
ms.openlocfilehash: 24f58a5c235b6d67ca2dee712398dacc828d8f51
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106981726"
---
# <a name="dml_element_wise_bit_shift_left_operator_desc-structure-directmlh"></a><span data-ttu-id="72d2a-103">DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="72d2a-103">DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="72d2a-104">依 *BTensor* 的對應元素所指定的位數，對 *ATensor* 的每個元素執行邏輯左移位，將結果放入 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="72d2a-104">Performs a logical left shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a << b)
```

<span data-ttu-id="72d2a-105">這個運算子支援就地執行，這表示允許 *OutputTensor* 在系結期間為其中一個輸入張量加上別名。</span><span class="sxs-lookup"><span data-stu-id="72d2a-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72d2a-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="72d2a-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="72d2a-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="72d2a-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="72d2a-108">語法</span><span class="sxs-lookup"><span data-stu-id="72d2a-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="72d2a-109">成員</span><span class="sxs-lookup"><span data-stu-id="72d2a-109">Members</span></span>

`ATensor`

<span data-ttu-id="72d2a-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="72d2a-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="72d2a-111">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="72d2a-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="72d2a-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="72d2a-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="72d2a-113">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="72d2a-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="72d2a-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="72d2a-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="72d2a-115">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="72d2a-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="72d2a-116">可用性</span><span class="sxs-lookup"><span data-stu-id="72d2a-116">Availability</span></span>
<span data-ttu-id="72d2a-117">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="72d2a-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="72d2a-118">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="72d2a-118">Tensor constraints</span></span>
<span data-ttu-id="72d2a-119">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="72d2a-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="72d2a-120">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="72d2a-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="72d2a-121">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="72d2a-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="72d2a-122">張</span><span class="sxs-lookup"><span data-stu-id="72d2a-122">Tensor</span></span> | <span data-ttu-id="72d2a-123">類型</span><span class="sxs-lookup"><span data-stu-id="72d2a-123">Kind</span></span> | <span data-ttu-id="72d2a-124">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="72d2a-124">Supported dimension counts</span></span> | <span data-ttu-id="72d2a-125">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="72d2a-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="72d2a-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="72d2a-126">ATensor</span></span> | <span data-ttu-id="72d2a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="72d2a-127">Input</span></span> | <span data-ttu-id="72d2a-128">1至8</span><span class="sxs-lookup"><span data-stu-id="72d2a-128">1 to 8</span></span> | <span data-ttu-id="72d2a-129">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="72d2a-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="72d2a-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="72d2a-130">BTensor</span></span> | <span data-ttu-id="72d2a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="72d2a-131">Input</span></span> | <span data-ttu-id="72d2a-132">1至8</span><span class="sxs-lookup"><span data-stu-id="72d2a-132">1 to 8</span></span> | <span data-ttu-id="72d2a-133">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="72d2a-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="72d2a-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="72d2a-134">OutputTensor</span></span> | <span data-ttu-id="72d2a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="72d2a-135">Output</span></span> | <span data-ttu-id="72d2a-136">1至8</span><span class="sxs-lookup"><span data-stu-id="72d2a-136">1 to 8</span></span> | <span data-ttu-id="72d2a-137">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="72d2a-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="72d2a-138">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="72d2a-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="72d2a-139">張</span><span class="sxs-lookup"><span data-stu-id="72d2a-139">Tensor</span></span> | <span data-ttu-id="72d2a-140">類型</span><span class="sxs-lookup"><span data-stu-id="72d2a-140">Kind</span></span> | <span data-ttu-id="72d2a-141">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="72d2a-141">Supported dimension counts</span></span> | <span data-ttu-id="72d2a-142">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="72d2a-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="72d2a-143">ATensor</span><span class="sxs-lookup"><span data-stu-id="72d2a-143">ATensor</span></span> | <span data-ttu-id="72d2a-144">輸入</span><span class="sxs-lookup"><span data-stu-id="72d2a-144">Input</span></span> | <span data-ttu-id="72d2a-145">4</span><span class="sxs-lookup"><span data-stu-id="72d2a-145">4</span></span> | <span data-ttu-id="72d2a-146">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="72d2a-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="72d2a-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="72d2a-147">BTensor</span></span> | <span data-ttu-id="72d2a-148">輸入</span><span class="sxs-lookup"><span data-stu-id="72d2a-148">Input</span></span> | <span data-ttu-id="72d2a-149">4</span><span class="sxs-lookup"><span data-stu-id="72d2a-149">4</span></span> | <span data-ttu-id="72d2a-150">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="72d2a-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="72d2a-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="72d2a-151">OutputTensor</span></span> | <span data-ttu-id="72d2a-152">輸出</span><span class="sxs-lookup"><span data-stu-id="72d2a-152">Output</span></span> | <span data-ttu-id="72d2a-153">4</span><span class="sxs-lookup"><span data-stu-id="72d2a-153">4</span></span> | <span data-ttu-id="72d2a-154">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="72d2a-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="72d2a-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="72d2a-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="72d2a-156">**標頭**</span><span class="sxs-lookup"><span data-stu-id="72d2a-156">**Header**</span></span> | <span data-ttu-id="72d2a-157">directml。h</span><span class="sxs-lookup"><span data-stu-id="72d2a-157">directml.h</span></span> |