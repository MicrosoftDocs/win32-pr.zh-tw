---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: 檢查 *InputTensor* 的每個專案是否為 IEEE-754-inf、inf 或兩者（視指定的 *InfinityMode* 而定），並將結果 (1 表示 true、0表示 false) 至 *OutputTensor* 的對應元素。
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417318"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="3c244-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="3c244-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="3c244-104">檢查 *InputTensor* 的每個專案是否為 IEEE-754-inf、inf 或兩者（視指定的 *InfinityMode* 而定），並將結果 (1 表示 true、0表示 false) 至 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="3c244-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="3c244-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="3c244-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="3c244-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="3c244-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c244-107">語法</span><span class="sxs-lookup"><span data-stu-id="3c244-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="3c244-108">成員</span><span class="sxs-lookup"><span data-stu-id="3c244-108">Members</span></span>

`InputTensor`

<span data-ttu-id="3c244-109">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3c244-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3c244-110">要從中讀取的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="3c244-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="3c244-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3c244-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3c244-112">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="3c244-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="3c244-113">類型： **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="3c244-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="3c244-114">[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) ，判斷要檢查的無限大正負號。</span><span class="sxs-lookup"><span data-stu-id="3c244-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="3c244-115">如果 **DML_IS_INFINITY_MODE_EITHER**，則如果專案為-inf 或 inf，則會傳回1，否則會傳回0。</span><span class="sxs-lookup"><span data-stu-id="3c244-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="3c244-116">如果 **DML_IS_INFINITY_MODE_POSITIVE**，則如果元素為 inf，則會傳回1，否則會傳回0。</span><span class="sxs-lookup"><span data-stu-id="3c244-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="3c244-117">如果 **DML_IS_INFINITY_MODE_NEGATIVE**'，則如果元素為-inf，則會傳回1，否則會傳回0。</span><span class="sxs-lookup"><span data-stu-id="3c244-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="3c244-118">備註</span><span class="sxs-lookup"><span data-stu-id="3c244-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="3c244-119">可用性</span><span class="sxs-lookup"><span data-stu-id="3c244-119">Availability</span></span>
<span data-ttu-id="3c244-120">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="3c244-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="3c244-121">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="3c244-121">Tensor constraints</span></span>
<span data-ttu-id="3c244-122">*InputTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="3c244-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="3c244-123">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="3c244-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="3c244-124">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="3c244-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="3c244-125">張</span><span class="sxs-lookup"><span data-stu-id="3c244-125">Tensor</span></span> | <span data-ttu-id="3c244-126">種類</span><span class="sxs-lookup"><span data-stu-id="3c244-126">Kind</span></span> | <span data-ttu-id="3c244-127">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="3c244-127">Supported dimension counts</span></span> | <span data-ttu-id="3c244-128">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="3c244-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="3c244-129">InputTensor</span><span class="sxs-lookup"><span data-stu-id="3c244-129">InputTensor</span></span> | <span data-ttu-id="3c244-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3c244-130">Input</span></span> | <span data-ttu-id="3c244-131">1至8</span><span class="sxs-lookup"><span data-stu-id="3c244-131">1 to 8</span></span> | <span data-ttu-id="3c244-132">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="3c244-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="3c244-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="3c244-133">OutputTensor</span></span> | <span data-ttu-id="3c244-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3c244-134">Output</span></span> | <span data-ttu-id="3c244-135">1至8</span><span class="sxs-lookup"><span data-stu-id="3c244-135">1 to 8</span></span> | <span data-ttu-id="3c244-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="3c244-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="3c244-137">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="3c244-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="3c244-138">張</span><span class="sxs-lookup"><span data-stu-id="3c244-138">Tensor</span></span> | <span data-ttu-id="3c244-139">種類</span><span class="sxs-lookup"><span data-stu-id="3c244-139">Kind</span></span> | <span data-ttu-id="3c244-140">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="3c244-140">Supported dimension counts</span></span> | <span data-ttu-id="3c244-141">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="3c244-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="3c244-142">InputTensor</span><span class="sxs-lookup"><span data-stu-id="3c244-142">InputTensor</span></span> | <span data-ttu-id="3c244-143">輸入</span><span class="sxs-lookup"><span data-stu-id="3c244-143">Input</span></span> | <span data-ttu-id="3c244-144">4</span><span class="sxs-lookup"><span data-stu-id="3c244-144">4</span></span> | <span data-ttu-id="3c244-145">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="3c244-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="3c244-146">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="3c244-146">OutputTensor</span></span> | <span data-ttu-id="3c244-147">輸出</span><span class="sxs-lookup"><span data-stu-id="3c244-147">Output</span></span> | <span data-ttu-id="3c244-148">4</span><span class="sxs-lookup"><span data-stu-id="3c244-148">4</span></span> | <span data-ttu-id="3c244-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="3c244-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="3c244-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c244-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3c244-151">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="3c244-151">**Minimum supported client**</span></span> | <span data-ttu-id="3c244-152">Windows 10，版本 2004 (10.0;組建 19041) </span><span class="sxs-lookup"><span data-stu-id="3c244-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="3c244-153">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="3c244-153">**Minimum supported server**</span></span> | <span data-ttu-id="3c244-154">Windows Server，版本 2004 (10.0;組建 19041) </span><span class="sxs-lookup"><span data-stu-id="3c244-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="3c244-155">**標頭**</span><span class="sxs-lookup"><span data-stu-id="3c244-155">**Header**</span></span> | <span data-ttu-id="3c244-156">directml。h</span><span class="sxs-lookup"><span data-stu-id="3c244-156">directml.h</span></span> |