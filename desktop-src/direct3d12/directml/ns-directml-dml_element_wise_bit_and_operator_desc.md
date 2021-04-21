---
UID: NS:directml.DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
description: 在輸入張量的每個對應元素之間計算位 AND，然後將結果寫入輸出 tensor。
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
ms.openlocfilehash: 468c1e1dc332bc3c1afac4e0cdb6b0546d0b2b69
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803251"
---
# <a name="dml_element_wise_bit_and_operator_desc-structure-directmlh"></a><span data-ttu-id="f3060-103">DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="f3060-103">DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f3060-104">在輸入張量的每個對應元素之間計算位 AND，然後將結果寫入輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="f3060-104">Computes the bitwise AND between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="f3060-105">輸入和輸出 tensor 必須有相同的 *DimensionCount*、 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="f3060-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="f3060-106">這個運算子支援就地執行，這表示允許輸出 tensor 在系結期間為一或多個輸入張量加上別名。</span><span class="sxs-lookup"><span data-stu-id="f3060-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3060-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f3060-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f3060-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="f3060-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3060-109">語法</span><span class="sxs-lookup"><span data-stu-id="f3060-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="f3060-110">成員</span><span class="sxs-lookup"><span data-stu-id="f3060-110">Members</span></span>

`ATensor`

<span data-ttu-id="f3060-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f3060-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f3060-112">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="f3060-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="f3060-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f3060-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f3060-114">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="f3060-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="f3060-115">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f3060-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f3060-116">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="f3060-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="f3060-117">可用性</span><span class="sxs-lookup"><span data-stu-id="f3060-117">Availability</span></span>
<span data-ttu-id="f3060-118">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="f3060-118">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f3060-119">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="f3060-119">Tensor constraints</span></span>
<span data-ttu-id="f3060-120">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="f3060-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f3060-121">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="f3060-121">Tensor support</span></span>
| <span data-ttu-id="f3060-122">張</span><span class="sxs-lookup"><span data-stu-id="f3060-122">Tensor</span></span> | <span data-ttu-id="f3060-123">類型</span><span class="sxs-lookup"><span data-stu-id="f3060-123">Kind</span></span> | <span data-ttu-id="f3060-124">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="f3060-124">Supported dimension counts</span></span> | <span data-ttu-id="f3060-125">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="f3060-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f3060-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="f3060-126">ATensor</span></span> | <span data-ttu-id="f3060-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f3060-127">Input</span></span> | <span data-ttu-id="f3060-128">1至8</span><span class="sxs-lookup"><span data-stu-id="f3060-128">1 to 8</span></span> | <span data-ttu-id="f3060-129">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="f3060-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f3060-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="f3060-130">BTensor</span></span> | <span data-ttu-id="f3060-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f3060-131">Input</span></span> | <span data-ttu-id="f3060-132">1至8</span><span class="sxs-lookup"><span data-stu-id="f3060-132">1 to 8</span></span> | <span data-ttu-id="f3060-133">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="f3060-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f3060-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f3060-134">OutputTensor</span></span> | <span data-ttu-id="f3060-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f3060-135">Output</span></span> | <span data-ttu-id="f3060-136">1至8</span><span class="sxs-lookup"><span data-stu-id="f3060-136">1 to 8</span></span> | <span data-ttu-id="f3060-137">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="f3060-137">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="f3060-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3060-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f3060-139">**標頭**</span><span class="sxs-lookup"><span data-stu-id="f3060-139">**Header**</span></span> | <span data-ttu-id="f3060-140">directml。h</span><span class="sxs-lookup"><span data-stu-id="f3060-140">directml.h</span></span> |