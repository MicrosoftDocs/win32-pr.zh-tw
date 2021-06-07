---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
description: 針對輸入張量的每一對對應元素計算 C 模數運算子，並將結果放入 *OutputTensor* 的對應元素。
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_truncate_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
ms.openlocfilehash: 461a7882e17d86b25cf27e0a28c05673f8899cea
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417274"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="875d9-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="875d9-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="875d9-104">針對輸入張量的每一對對應元素計算 C 模數運算子，並將結果放入 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="875d9-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="875d9-105">因為商會舍入至0，所以結果會與被除數的正負號相同。</span><span class="sxs-lookup"><span data-stu-id="875d9-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="875d9-106">這個運算子支援就地執行，這表示允許 *OutputTensor* 在系結期間為其中一個輸入張量加上別名。</span><span class="sxs-lookup"><span data-stu-id="875d9-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="875d9-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="875d9-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="875d9-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="875d9-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="875d9-109">語法</span><span class="sxs-lookup"><span data-stu-id="875d9-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="875d9-110">成員</span><span class="sxs-lookup"><span data-stu-id="875d9-110">Members</span></span>

`ATensor`

<span data-ttu-id="875d9-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="875d9-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="875d9-112">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="875d9-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="875d9-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="875d9-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="875d9-114">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="875d9-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="875d9-115">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="875d9-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="875d9-116">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="875d9-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="875d9-117">可用性</span><span class="sxs-lookup"><span data-stu-id="875d9-117">Availability</span></span>
<span data-ttu-id="875d9-118">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="875d9-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="875d9-119">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="875d9-119">Tensor constraints</span></span>
<span data-ttu-id="875d9-120">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="875d9-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="875d9-121">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="875d9-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="875d9-122">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="875d9-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="875d9-123">張</span><span class="sxs-lookup"><span data-stu-id="875d9-123">Tensor</span></span> | <span data-ttu-id="875d9-124">種類</span><span class="sxs-lookup"><span data-stu-id="875d9-124">Kind</span></span> | <span data-ttu-id="875d9-125">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="875d9-125">Supported dimension counts</span></span> | <span data-ttu-id="875d9-126">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="875d9-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="875d9-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="875d9-127">ATensor</span></span> | <span data-ttu-id="875d9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="875d9-128">Input</span></span> | <span data-ttu-id="875d9-129">1至8</span><span class="sxs-lookup"><span data-stu-id="875d9-129">1 to 8</span></span> | <span data-ttu-id="875d9-130">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="875d9-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="875d9-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="875d9-131">BTensor</span></span> | <span data-ttu-id="875d9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="875d9-132">Input</span></span> | <span data-ttu-id="875d9-133">1至8</span><span class="sxs-lookup"><span data-stu-id="875d9-133">1 to 8</span></span> | <span data-ttu-id="875d9-134">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="875d9-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="875d9-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="875d9-135">OutputTensor</span></span> | <span data-ttu-id="875d9-136">輸出</span><span class="sxs-lookup"><span data-stu-id="875d9-136">Output</span></span> | <span data-ttu-id="875d9-137">1至8</span><span class="sxs-lookup"><span data-stu-id="875d9-137">1 to 8</span></span> | <span data-ttu-id="875d9-138">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="875d9-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="875d9-139">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="875d9-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="875d9-140">張</span><span class="sxs-lookup"><span data-stu-id="875d9-140">Tensor</span></span> | <span data-ttu-id="875d9-141">種類</span><span class="sxs-lookup"><span data-stu-id="875d9-141">Kind</span></span> | <span data-ttu-id="875d9-142">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="875d9-142">Supported dimension counts</span></span> | <span data-ttu-id="875d9-143">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="875d9-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="875d9-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="875d9-144">ATensor</span></span> | <span data-ttu-id="875d9-145">輸入</span><span class="sxs-lookup"><span data-stu-id="875d9-145">Input</span></span> | <span data-ttu-id="875d9-146">4</span><span class="sxs-lookup"><span data-stu-id="875d9-146">4</span></span> | <span data-ttu-id="875d9-147">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="875d9-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="875d9-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="875d9-148">BTensor</span></span> | <span data-ttu-id="875d9-149">輸入</span><span class="sxs-lookup"><span data-stu-id="875d9-149">Input</span></span> | <span data-ttu-id="875d9-150">4</span><span class="sxs-lookup"><span data-stu-id="875d9-150">4</span></span> | <span data-ttu-id="875d9-151">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="875d9-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="875d9-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="875d9-152">OutputTensor</span></span> | <span data-ttu-id="875d9-153">輸出</span><span class="sxs-lookup"><span data-stu-id="875d9-153">Output</span></span> | <span data-ttu-id="875d9-154">4</span><span class="sxs-lookup"><span data-stu-id="875d9-154">4</span></span> | <span data-ttu-id="875d9-155">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="875d9-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="875d9-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="875d9-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="875d9-157">**標頭**</span><span class="sxs-lookup"><span data-stu-id="875d9-157">**Header**</span></span> | <span data-ttu-id="875d9-158">directml。h</span><span class="sxs-lookup"><span data-stu-id="875d9-158">directml.h</span></span> |