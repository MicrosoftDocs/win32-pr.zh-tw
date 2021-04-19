---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
description: 在輸入張量的每一對對應元素上執行邏輯 *小於或等於，並* 將結果 (1 表示 true、0表示 false) 至 *OutputTensor* 的對應元素。
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: 815c7ea148d6754cb410da6aeedaf31ab6cd7ece
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106981722"
---
# <a name="dml_element_wise_logical_less_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="1efd2-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="1efd2-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="1efd2-104">在輸入張量的每一對對應元素上執行邏輯 *小於或等於，並* 將結果 (1 表示 true、0表示 false) 至 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="1efd2-104">Performs a logical *less than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a <= b)
```

> [!IMPORTANT]
> <span data-ttu-id="1efd2-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="1efd2-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="1efd2-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="1efd2-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1efd2-107">語法</span><span class="sxs-lookup"><span data-stu-id="1efd2-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="1efd2-108">成員</span><span class="sxs-lookup"><span data-stu-id="1efd2-108">Members</span></span>

`ATensor`

<span data-ttu-id="1efd2-109">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1efd2-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1efd2-110">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="1efd2-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="1efd2-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1efd2-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1efd2-112">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="1efd2-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="1efd2-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1efd2-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1efd2-114">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="1efd2-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="1efd2-115">可用性</span><span class="sxs-lookup"><span data-stu-id="1efd2-115">Availability</span></span>
<span data-ttu-id="1efd2-116">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="1efd2-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="1efd2-117">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="1efd2-117">Tensor constraints</span></span>
* <span data-ttu-id="1efd2-118">*ATensor* 和 *BTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="1efd2-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="1efd2-119">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="1efd2-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="1efd2-120">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="1efd2-120">Tensor support</span></span>
| <span data-ttu-id="1efd2-121">張</span><span class="sxs-lookup"><span data-stu-id="1efd2-121">Tensor</span></span> | <span data-ttu-id="1efd2-122">類型</span><span class="sxs-lookup"><span data-stu-id="1efd2-122">Kind</span></span> | <span data-ttu-id="1efd2-123">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="1efd2-123">Supported dimension counts</span></span> | <span data-ttu-id="1efd2-124">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="1efd2-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1efd2-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="1efd2-125">ATensor</span></span> | <span data-ttu-id="1efd2-126">輸入</span><span class="sxs-lookup"><span data-stu-id="1efd2-126">Input</span></span> | <span data-ttu-id="1efd2-127">1至8</span><span class="sxs-lookup"><span data-stu-id="1efd2-127">1 to 8</span></span> | <span data-ttu-id="1efd2-128">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="1efd2-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1efd2-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="1efd2-129">BTensor</span></span> | <span data-ttu-id="1efd2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1efd2-130">Input</span></span> | <span data-ttu-id="1efd2-131">1至8</span><span class="sxs-lookup"><span data-stu-id="1efd2-131">1 to 8</span></span> | <span data-ttu-id="1efd2-132">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="1efd2-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1efd2-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="1efd2-133">OutputTensor</span></span> | <span data-ttu-id="1efd2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1efd2-134">Output</span></span> | <span data-ttu-id="1efd2-135">1至8</span><span class="sxs-lookup"><span data-stu-id="1efd2-135">1 to 8</span></span> | <span data-ttu-id="1efd2-136">UINT32、UINT8</span><span class="sxs-lookup"><span data-stu-id="1efd2-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="1efd2-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="1efd2-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1efd2-138">**標頭**</span><span class="sxs-lookup"><span data-stu-id="1efd2-138">**Header**</span></span> | <span data-ttu-id="1efd2-139">directml。h</span><span class="sxs-lookup"><span data-stu-id="1efd2-139">directml.h</span></span> |