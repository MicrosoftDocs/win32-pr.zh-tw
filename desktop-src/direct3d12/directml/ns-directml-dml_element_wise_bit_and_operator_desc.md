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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417398"
---
# <a name="dml_element_wise_bit_and_operator_desc-structure-directmlh"></a><span data-ttu-id="13655-103">DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="13655-103">DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="13655-104">在輸入張量的每個對應元素之間計算位 AND，然後將結果寫入輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="13655-104">Computes the bitwise AND between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="13655-105">輸入和輸出 tensor 必須有相同的 *DimensionCount*、 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="13655-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="13655-106">這個運算子支援就地執行，這表示允許輸出 tensor 在系結期間為一或多個輸入張量加上別名。</span><span class="sxs-lookup"><span data-stu-id="13655-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13655-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="13655-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="13655-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="13655-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="13655-109">語法</span><span class="sxs-lookup"><span data-stu-id="13655-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="13655-110">成員</span><span class="sxs-lookup"><span data-stu-id="13655-110">Members</span></span>

`ATensor`

<span data-ttu-id="13655-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="13655-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="13655-112">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="13655-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="13655-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="13655-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="13655-114">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="13655-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="13655-115">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="13655-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="13655-116">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="13655-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="13655-117">可用性</span><span class="sxs-lookup"><span data-stu-id="13655-117">Availability</span></span>
<span data-ttu-id="13655-118">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="13655-118">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="13655-119">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="13655-119">Tensor constraints</span></span>
<span data-ttu-id="13655-120">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="13655-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="13655-121">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="13655-121">Tensor support</span></span>
| <span data-ttu-id="13655-122">張</span><span class="sxs-lookup"><span data-stu-id="13655-122">Tensor</span></span> | <span data-ttu-id="13655-123">種類</span><span class="sxs-lookup"><span data-stu-id="13655-123">Kind</span></span> | <span data-ttu-id="13655-124">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="13655-124">Supported dimension counts</span></span> | <span data-ttu-id="13655-125">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="13655-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="13655-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="13655-126">ATensor</span></span> | <span data-ttu-id="13655-127">輸入</span><span class="sxs-lookup"><span data-stu-id="13655-127">Input</span></span> | <span data-ttu-id="13655-128">1至8</span><span class="sxs-lookup"><span data-stu-id="13655-128">1 to 8</span></span> | <span data-ttu-id="13655-129">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="13655-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="13655-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="13655-130">BTensor</span></span> | <span data-ttu-id="13655-131">輸入</span><span class="sxs-lookup"><span data-stu-id="13655-131">Input</span></span> | <span data-ttu-id="13655-132">1至8</span><span class="sxs-lookup"><span data-stu-id="13655-132">1 to 8</span></span> | <span data-ttu-id="13655-133">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="13655-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="13655-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="13655-134">OutputTensor</span></span> | <span data-ttu-id="13655-135">輸出</span><span class="sxs-lookup"><span data-stu-id="13655-135">Output</span></span> | <span data-ttu-id="13655-136">1至8</span><span class="sxs-lookup"><span data-stu-id="13655-136">1 to 8</span></span> | <span data-ttu-id="13655-137">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="13655-137">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="13655-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="13655-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="13655-139">**標頭**</span><span class="sxs-lookup"><span data-stu-id="13655-139">**Header**</span></span> | <span data-ttu-id="13655-140">directml。h</span><span class="sxs-lookup"><span data-stu-id="13655-140">directml.h</span></span> |