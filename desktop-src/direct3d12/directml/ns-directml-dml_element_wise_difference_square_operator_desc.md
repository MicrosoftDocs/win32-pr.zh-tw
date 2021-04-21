---
UID: NS:directml.DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
title: DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
description: 從 *ATensor* 的對應元素減去 *BTensor* 的每個元素，並將結果乘以本身，並將結果放入 *OutputTensor* 的對應元素。
helpviewer_keywords:
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.openlocfilehash: 3e3e7ab8f222f42def82a168ed861e58347f3b20
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804426"
---
# <a name="dml_element_wise_difference_square_operator_desc-directmlh"></a><span data-ttu-id="d7c96-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml) </span><span class="sxs-lookup"><span data-stu-id="d7c96-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="d7c96-104">從 *ATensor* 的對應元素減去 *BTensor* 的每個元素，並將結果乘以本身，並將結果放入 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="d7c96-104">Subtracts each element of *BTensor* from the corresponding element of *ATensor*, multiplies the result by itself, and places the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a - b) * (a - b)
```

<span data-ttu-id="d7c96-105">這個運算子支援就地執行，這表示在系結期間允許 *OutputTensor* 別名 *ATensor* 或 *BTensor* 。</span><span class="sxs-lookup"><span data-stu-id="d7c96-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7c96-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="d7c96-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="d7c96-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="d7c96-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c96-108">語法</span><span class="sxs-lookup"><span data-stu-id="d7c96-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="d7c96-109">成員</span><span class="sxs-lookup"><span data-stu-id="d7c96-109">Members</span></span>

`ATensor`

<span data-ttu-id="d7c96-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d7c96-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d7c96-111">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="d7c96-111">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="d7c96-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d7c96-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d7c96-113">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="d7c96-113">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="d7c96-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d7c96-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d7c96-115">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="d7c96-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="d7c96-116">可用性</span><span class="sxs-lookup"><span data-stu-id="d7c96-116">Availability</span></span>
<span data-ttu-id="d7c96-117">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。</span><span class="sxs-lookup"><span data-stu-id="d7c96-117">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d7c96-118">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="d7c96-118">Tensor constraints</span></span>
<span data-ttu-id="d7c96-119">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="d7c96-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d7c96-120">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="d7c96-120">Tensor support</span></span>
| <span data-ttu-id="d7c96-121">張</span><span class="sxs-lookup"><span data-stu-id="d7c96-121">Tensor</span></span> | <span data-ttu-id="d7c96-122">類型</span><span class="sxs-lookup"><span data-stu-id="d7c96-122">Kind</span></span> | <span data-ttu-id="d7c96-123">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="d7c96-123">Supported dimension counts</span></span> | <span data-ttu-id="d7c96-124">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="d7c96-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d7c96-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="d7c96-125">ATensor</span></span> | <span data-ttu-id="d7c96-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d7c96-126">Input</span></span> | <span data-ttu-id="d7c96-127">1至8</span><span class="sxs-lookup"><span data-stu-id="d7c96-127">1 to 8</span></span> | <span data-ttu-id="d7c96-128">FLOAT32、FLOAT16、INT32、UINT32</span><span class="sxs-lookup"><span data-stu-id="d7c96-128">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="d7c96-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="d7c96-129">BTensor</span></span> | <span data-ttu-id="d7c96-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d7c96-130">Input</span></span> | <span data-ttu-id="d7c96-131">1至8</span><span class="sxs-lookup"><span data-stu-id="d7c96-131">1 to 8</span></span> | <span data-ttu-id="d7c96-132">FLOAT32、FLOAT16、INT32、UINT32</span><span class="sxs-lookup"><span data-stu-id="d7c96-132">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="d7c96-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d7c96-133">OutputTensor</span></span> | <span data-ttu-id="d7c96-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d7c96-134">Output</span></span> | <span data-ttu-id="d7c96-135">1至8</span><span class="sxs-lookup"><span data-stu-id="d7c96-135">1 to 8</span></span> | <span data-ttu-id="d7c96-136">FLOAT32、FLOAT16、INT32、UINT32</span><span class="sxs-lookup"><span data-stu-id="d7c96-136">FLOAT32, FLOAT16, INT32, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="d7c96-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7c96-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d7c96-138">**標頭**</span><span class="sxs-lookup"><span data-stu-id="d7c96-138">**Header**</span></span> | <span data-ttu-id="d7c96-139">directml。h</span><span class="sxs-lookup"><span data-stu-id="d7c96-139">directml.h</span></span> |
