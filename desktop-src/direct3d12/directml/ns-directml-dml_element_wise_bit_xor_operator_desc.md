---
UID: NS:directml.DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
description: 在輸入張量的每個對應專案之間計算位 XOR (獨佔或) ，然後將結果寫入輸出 tensor。
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.openlocfilehash: fcedb2c33f1c63196a9e6783daaa9f2d863e99f0
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417303"
---
# <a name="dml_element_wise_bit_xor_operator_desc-structure-directmlh"></a><span data-ttu-id="a5792-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="a5792-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a5792-104">在輸入張量的每個對應專案之間計算位 XOR (獨佔或) ，然後將結果寫入輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="a5792-104">Computes the bitwise XOR (eXclusive OR) between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="a5792-105">輸入和輸出 tensor 必須有相同的 *DimensionCount*、 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="a5792-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="a5792-106">這個運算子支援就地執行，這表示允許輸出 tensor 在系結期間為一或多個輸入張量加上別名。</span><span class="sxs-lookup"><span data-stu-id="a5792-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5792-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="a5792-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a5792-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="a5792-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5792-109">語法</span><span class="sxs-lookup"><span data-stu-id="a5792-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="a5792-110">成員</span><span class="sxs-lookup"><span data-stu-id="a5792-110">Members</span></span>

`ATensor`

<span data-ttu-id="a5792-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a5792-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a5792-112">包含左手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="a5792-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="a5792-113">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a5792-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a5792-114">包含右手邊輸入的 tensor。</span><span class="sxs-lookup"><span data-stu-id="a5792-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="a5792-115">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a5792-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a5792-116">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="a5792-116">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="a5792-117">範例</span><span class="sxs-lookup"><span data-stu-id="a5792-117">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="a5792-118">可用性</span><span class="sxs-lookup"><span data-stu-id="a5792-118">Availability</span></span>
<span data-ttu-id="a5792-119">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="a5792-119">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a5792-120">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="a5792-120">Tensor constraints</span></span>
<span data-ttu-id="a5792-121">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="a5792-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a5792-122">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="a5792-122">Tensor support</span></span>
| <span data-ttu-id="a5792-123">張</span><span class="sxs-lookup"><span data-stu-id="a5792-123">Tensor</span></span> | <span data-ttu-id="a5792-124">種類</span><span class="sxs-lookup"><span data-stu-id="a5792-124">Kind</span></span> | <span data-ttu-id="a5792-125">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="a5792-125">Supported dimension counts</span></span> | <span data-ttu-id="a5792-126">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="a5792-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a5792-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="a5792-127">ATensor</span></span> | <span data-ttu-id="a5792-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a5792-128">Input</span></span> | <span data-ttu-id="a5792-129">1至8</span><span class="sxs-lookup"><span data-stu-id="a5792-129">1 to 8</span></span> | <span data-ttu-id="a5792-130">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a5792-130">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a5792-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="a5792-131">BTensor</span></span> | <span data-ttu-id="a5792-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a5792-132">Input</span></span> | <span data-ttu-id="a5792-133">1至8</span><span class="sxs-lookup"><span data-stu-id="a5792-133">1 to 8</span></span> | <span data-ttu-id="a5792-134">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a5792-134">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a5792-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a5792-135">OutputTensor</span></span> | <span data-ttu-id="a5792-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a5792-136">Output</span></span> | <span data-ttu-id="a5792-137">1至8</span><span class="sxs-lookup"><span data-stu-id="a5792-137">1 to 8</span></span> | <span data-ttu-id="a5792-138">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="a5792-138">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="a5792-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5792-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a5792-140">**標頭**</span><span class="sxs-lookup"><span data-stu-id="a5792-140">**Header**</span></span> | <span data-ttu-id="a5792-141">directml。h</span><span class="sxs-lookup"><span data-stu-id="a5792-141">directml.h</span></span> |