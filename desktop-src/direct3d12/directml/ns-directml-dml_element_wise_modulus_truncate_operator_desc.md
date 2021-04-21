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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803057"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="13102-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="13102-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="13102-104">針對輸入張量的每一對對應元素計算 C 模數運算子，並將結果放入 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="13102-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="13102-105">因為商會舍入至0，所以結果會與被除數的正負號相同。</span><span class="sxs-lookup"><span data-stu-id="13102-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="13102-106">這個運算子支援就地執行，這表示允許 *OutputTensor* 在系結期間為其中一個輸入張量加上別名。</span><span class="sxs-lookup"><span data-stu-id="13102-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13102-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="13102-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="13102-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="13102-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="13102-109">語法</span><span class="sxs-lookup"><span data-stu-id="13102-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="13102-110">成員</span><span class="sxs-lookup"><span data-stu-id="13102-110">Members</span></span>

`ATensor`

<span data-ttu-id="13102-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="13102-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="13102-112">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="13102-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="13102-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="13102-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="13102-114">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="13102-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="13102-115">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="13102-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="13102-116">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="13102-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="13102-117">可用性</span><span class="sxs-lookup"><span data-stu-id="13102-117">Availability</span></span>
<span data-ttu-id="13102-118">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="13102-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="13102-119">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="13102-119">Tensor constraints</span></span>
<span data-ttu-id="13102-120">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="13102-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="13102-121">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="13102-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="13102-122">DML_FEATURE_LEVEL_3_0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="13102-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="13102-123">張</span><span class="sxs-lookup"><span data-stu-id="13102-123">Tensor</span></span> | <span data-ttu-id="13102-124">類型</span><span class="sxs-lookup"><span data-stu-id="13102-124">Kind</span></span> | <span data-ttu-id="13102-125">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="13102-125">Supported dimension counts</span></span> | <span data-ttu-id="13102-126">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="13102-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="13102-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="13102-127">ATensor</span></span> | <span data-ttu-id="13102-128">輸入</span><span class="sxs-lookup"><span data-stu-id="13102-128">Input</span></span> | <span data-ttu-id="13102-129">1至8</span><span class="sxs-lookup"><span data-stu-id="13102-129">1 to 8</span></span> | <span data-ttu-id="13102-130">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="13102-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="13102-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="13102-131">BTensor</span></span> | <span data-ttu-id="13102-132">輸入</span><span class="sxs-lookup"><span data-stu-id="13102-132">Input</span></span> | <span data-ttu-id="13102-133">1至8</span><span class="sxs-lookup"><span data-stu-id="13102-133">1 to 8</span></span> | <span data-ttu-id="13102-134">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="13102-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="13102-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="13102-135">OutputTensor</span></span> | <span data-ttu-id="13102-136">輸出</span><span class="sxs-lookup"><span data-stu-id="13102-136">Output</span></span> | <span data-ttu-id="13102-137">1至8</span><span class="sxs-lookup"><span data-stu-id="13102-137">1 to 8</span></span> | <span data-ttu-id="13102-138">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="13102-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="13102-139">DML_FEATURE_LEVEL_2_1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="13102-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="13102-140">張</span><span class="sxs-lookup"><span data-stu-id="13102-140">Tensor</span></span> | <span data-ttu-id="13102-141">類型</span><span class="sxs-lookup"><span data-stu-id="13102-141">Kind</span></span> | <span data-ttu-id="13102-142">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="13102-142">Supported dimension counts</span></span> | <span data-ttu-id="13102-143">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="13102-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="13102-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="13102-144">ATensor</span></span> | <span data-ttu-id="13102-145">輸入</span><span class="sxs-lookup"><span data-stu-id="13102-145">Input</span></span> | <span data-ttu-id="13102-146">4</span><span class="sxs-lookup"><span data-stu-id="13102-146">4</span></span> | <span data-ttu-id="13102-147">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="13102-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="13102-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="13102-148">BTensor</span></span> | <span data-ttu-id="13102-149">輸入</span><span class="sxs-lookup"><span data-stu-id="13102-149">Input</span></span> | <span data-ttu-id="13102-150">4</span><span class="sxs-lookup"><span data-stu-id="13102-150">4</span></span> | <span data-ttu-id="13102-151">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="13102-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="13102-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="13102-152">OutputTensor</span></span> | <span data-ttu-id="13102-153">輸出</span><span class="sxs-lookup"><span data-stu-id="13102-153">Output</span></span> | <span data-ttu-id="13102-154">4</span><span class="sxs-lookup"><span data-stu-id="13102-154">4</span></span> | <span data-ttu-id="13102-155">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="13102-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="13102-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="13102-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="13102-157">**標頭**</span><span class="sxs-lookup"><span data-stu-id="13102-157">**Header**</span></span> | <span data-ttu-id="13102-158">directml。h</span><span class="sxs-lookup"><span data-stu-id="13102-158">directml.h</span></span> |