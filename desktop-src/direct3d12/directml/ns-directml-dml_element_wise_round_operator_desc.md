---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: 將 *InputTensor* 的每個元素四捨五入為整數值，並將結果放入 *OutputTensor* 的對應元素。
helpviewer_keywords:
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure
- direct3d12.dml_element_wise_round_operator_desc
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.openlocfilehash: f0964ae133c61b3a596b644630d363f902635585
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106997305"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="6ccf2-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="6ccf2-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="6ccf2-104">將 *InputTensor* 的每個元素四捨五入為整數值，並將結果放入 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="6ccf2-105">這個運算子支援就地執行，這表示在系結期間允許 *OutputTensor* 別名 *InputTensor* 。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ccf2-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="6ccf2-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ccf2-108">語法</span><span class="sxs-lookup"><span data-stu-id="6ccf2-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="6ccf2-109">成員</span><span class="sxs-lookup"><span data-stu-id="6ccf2-109">Members</span></span>

`InputTensor`

<span data-ttu-id="6ccf2-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6ccf2-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6ccf2-111">要從中讀取的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="6ccf2-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6ccf2-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6ccf2-113">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="6ccf2-114">類型： **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="6ccf2-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="6ccf2-115">[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)判斷要來回的方向。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="6ccf2-116">如果 **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**：值會四捨五入為最接近的整數，中間的值 (例如，0.5) 舍入至最接近的偶數整數。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="6ccf2-117">如果 **DML_ROUNDING_MODE_TOWARD_ZERO**：將值舍入為零。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="6ccf2-118">這會有效地截斷小數部分。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="6ccf2-119">如果 **DML_ROUNDING_MODE_TOWARD_INFINITY**：值會舍入到最接近的整數，中間的值 (例如，0.5) 從 (零四捨五入到正無限大或負無限大，視值的正負號) 而定。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="6ccf2-120">可用性</span><span class="sxs-lookup"><span data-stu-id="6ccf2-120">Availability</span></span>
<span data-ttu-id="6ccf2-121">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6ccf2-122">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="6ccf2-122">Tensor constraints</span></span>
<span data-ttu-id="6ccf2-123">*InputTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="6ccf2-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6ccf2-124">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="6ccf2-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="6ccf2-125">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="6ccf2-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="6ccf2-126">張</span><span class="sxs-lookup"><span data-stu-id="6ccf2-126">Tensor</span></span> | <span data-ttu-id="6ccf2-127">類型</span><span class="sxs-lookup"><span data-stu-id="6ccf2-127">Kind</span></span> | <span data-ttu-id="6ccf2-128">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="6ccf2-128">Supported dimension counts</span></span> | <span data-ttu-id="6ccf2-129">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="6ccf2-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6ccf2-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="6ccf2-130">InputTensor</span></span> | <span data-ttu-id="6ccf2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6ccf2-131">Input</span></span> | <span data-ttu-id="6ccf2-132">1至8</span><span class="sxs-lookup"><span data-stu-id="6ccf2-132">1 to 8</span></span> | <span data-ttu-id="6ccf2-133">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6ccf2-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6ccf2-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="6ccf2-134">OutputTensor</span></span> | <span data-ttu-id="6ccf2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="6ccf2-135">Output</span></span> | <span data-ttu-id="6ccf2-136">1至8</span><span class="sxs-lookup"><span data-stu-id="6ccf2-136">1 to 8</span></span> | <span data-ttu-id="6ccf2-137">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6ccf2-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="6ccf2-138">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="6ccf2-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="6ccf2-139">張</span><span class="sxs-lookup"><span data-stu-id="6ccf2-139">Tensor</span></span> | <span data-ttu-id="6ccf2-140">類型</span><span class="sxs-lookup"><span data-stu-id="6ccf2-140">Kind</span></span> | <span data-ttu-id="6ccf2-141">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="6ccf2-141">Supported dimension counts</span></span> | <span data-ttu-id="6ccf2-142">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="6ccf2-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6ccf2-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="6ccf2-143">InputTensor</span></span> | <span data-ttu-id="6ccf2-144">輸入</span><span class="sxs-lookup"><span data-stu-id="6ccf2-144">Input</span></span> | <span data-ttu-id="6ccf2-145">4</span><span class="sxs-lookup"><span data-stu-id="6ccf2-145">4</span></span> | <span data-ttu-id="6ccf2-146">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6ccf2-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6ccf2-147">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="6ccf2-147">OutputTensor</span></span> | <span data-ttu-id="6ccf2-148">輸出</span><span class="sxs-lookup"><span data-stu-id="6ccf2-148">Output</span></span> | <span data-ttu-id="6ccf2-149">4</span><span class="sxs-lookup"><span data-stu-id="6ccf2-149">4</span></span> | <span data-ttu-id="6ccf2-150">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6ccf2-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="6ccf2-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ccf2-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6ccf2-152">**標頭**</span><span class="sxs-lookup"><span data-stu-id="6ccf2-152">**Header**</span></span> | <span data-ttu-id="6ccf2-153">directml。h</span><span class="sxs-lookup"><span data-stu-id="6ccf2-153">directml.h</span></span> |