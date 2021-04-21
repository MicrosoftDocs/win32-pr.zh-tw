---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
description: 在輸入張量的每一對對應元素上執行邏輯 *大於或等於* ，將結果 (1 表示 true，將0設為 true) 至對應的 *OutputTensor* 元素。
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: 4c20580a67117e6a605dfb0bf6611aca5cfd9e56
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803087"
---
# <a name="dml_element_wise_logical_greater_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="aa198-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="aa198-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="aa198-104">在輸入張量的每一對對應元素上執行邏輯 *大於或等於* ，將結果 (1 表示 true，將0設為 true) 至對應的 *OutputTensor* 元素。</span><span class="sxs-lookup"><span data-stu-id="aa198-104">Performs a logical *greater than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >= b)
```

> [!IMPORTANT]
> <span data-ttu-id="aa198-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="aa198-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="aa198-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="aa198-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa198-107">語法</span><span class="sxs-lookup"><span data-stu-id="aa198-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="aa198-108">成員</span><span class="sxs-lookup"><span data-stu-id="aa198-108">Members</span></span>

`ATensor`

<span data-ttu-id="aa198-109">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aa198-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aa198-110">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="aa198-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="aa198-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aa198-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aa198-112">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="aa198-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="aa198-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aa198-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aa198-114">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="aa198-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="aa198-115">可用性</span><span class="sxs-lookup"><span data-stu-id="aa198-115">Availability</span></span>
<span data-ttu-id="aa198-116">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="aa198-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="aa198-117">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="aa198-117">Tensor constraints</span></span>
* <span data-ttu-id="aa198-118">*ATensor* 和 *BTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="aa198-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="aa198-119">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="aa198-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="aa198-120">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="aa198-120">Tensor support</span></span>
| <span data-ttu-id="aa198-121">張</span><span class="sxs-lookup"><span data-stu-id="aa198-121">Tensor</span></span> | <span data-ttu-id="aa198-122">類型</span><span class="sxs-lookup"><span data-stu-id="aa198-122">Kind</span></span> | <span data-ttu-id="aa198-123">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="aa198-123">Supported dimension counts</span></span> | <span data-ttu-id="aa198-124">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="aa198-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="aa198-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="aa198-125">ATensor</span></span> | <span data-ttu-id="aa198-126">輸入</span><span class="sxs-lookup"><span data-stu-id="aa198-126">Input</span></span> | <span data-ttu-id="aa198-127">1至8</span><span class="sxs-lookup"><span data-stu-id="aa198-127">1 to 8</span></span> | <span data-ttu-id="aa198-128">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="aa198-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="aa198-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="aa198-129">BTensor</span></span> | <span data-ttu-id="aa198-130">輸入</span><span class="sxs-lookup"><span data-stu-id="aa198-130">Input</span></span> | <span data-ttu-id="aa198-131">1至8</span><span class="sxs-lookup"><span data-stu-id="aa198-131">1 to 8</span></span> | <span data-ttu-id="aa198-132">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="aa198-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="aa198-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="aa198-133">OutputTensor</span></span> | <span data-ttu-id="aa198-134">輸出</span><span class="sxs-lookup"><span data-stu-id="aa198-134">Output</span></span> | <span data-ttu-id="aa198-135">1至8</span><span class="sxs-lookup"><span data-stu-id="aa198-135">1 to 8</span></span> | <span data-ttu-id="aa198-136">UINT32、UINT8</span><span class="sxs-lookup"><span data-stu-id="aa198-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="aa198-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa198-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="aa198-138">**標頭**</span><span class="sxs-lookup"><span data-stu-id="aa198-138">**Header**</span></span> | <span data-ttu-id="aa198-139">directml。h</span><span class="sxs-lookup"><span data-stu-id="aa198-139">directml.h</span></span> |