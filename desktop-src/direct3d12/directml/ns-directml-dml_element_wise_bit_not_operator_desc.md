---
UID: NS:directml.DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
description: 針對輸入 tensor 的每個元素，計算位人口計數 (設定為 1) ，然後將結果寫入輸出 tensor。
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.openlocfilehash: 3c8dddc3159ebcd857c7423b76856fbeba465d2e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417307"
---
# <a name="dml_element_wise_bit_count_operator_desc-structure-directmlh"></a><span data-ttu-id="f1c41-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="f1c41-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f1c41-104">針對輸入 tensor 的每個元素，計算位人口計數 (設定為 1) ，然後將結果寫入輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="f1c41-104">Computes the bitwise population count (the number of bits set to 1) for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="f1c41-105">輸入和輸出 tensor 必須有相同的 *DimensionCount* 和 *大小*，不過它們在 *DataType* 中可能不同。</span><span class="sxs-lookup"><span data-stu-id="f1c41-105">The input and output tensor must have the same *DimensionCount* and *Sizes*, although they may differ in *DataType*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1c41-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f1c41-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f1c41-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="f1c41-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c41-108">語法</span><span class="sxs-lookup"><span data-stu-id="f1c41-108">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="f1c41-109">成員</span><span class="sxs-lookup"><span data-stu-id="f1c41-109">Members</span></span>

`InputTensor`

<span data-ttu-id="f1c41-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f1c41-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f1c41-111">要從中讀取的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="f1c41-111">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="f1c41-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f1c41-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f1c41-113">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="f1c41-113">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="f1c41-114">範例</span><span class="sxs-lookup"><span data-stu-id="f1c41-114">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0,   123], // 0b0000000000, 0b0001111011
 [456, 789]] // 0b0111001000, 0b1100010101

OutputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0, 6],
 [4, 5]]
```

## <a name="availability"></a><span data-ttu-id="f1c41-115">可用性</span><span class="sxs-lookup"><span data-stu-id="f1c41-115">Availability</span></span>
<span data-ttu-id="f1c41-116">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="f1c41-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f1c41-117">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="f1c41-117">Tensor constraints</span></span>
<span data-ttu-id="f1c41-118">*InputTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="f1c41-118">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f1c41-119">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="f1c41-119">Tensor support</span></span>
| <span data-ttu-id="f1c41-120">張</span><span class="sxs-lookup"><span data-stu-id="f1c41-120">Tensor</span></span> | <span data-ttu-id="f1c41-121">種類</span><span class="sxs-lookup"><span data-stu-id="f1c41-121">Kind</span></span> | <span data-ttu-id="f1c41-122">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="f1c41-122">Supported dimension counts</span></span> | <span data-ttu-id="f1c41-123">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="f1c41-123">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f1c41-124">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f1c41-124">InputTensor</span></span> | <span data-ttu-id="f1c41-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f1c41-125">Input</span></span> | <span data-ttu-id="f1c41-126">1至8</span><span class="sxs-lookup"><span data-stu-id="f1c41-126">1 to 8</span></span> | <span data-ttu-id="f1c41-127">UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="f1c41-127">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f1c41-128">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f1c41-128">OutputTensor</span></span> | <span data-ttu-id="f1c41-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f1c41-129">Output</span></span> | <span data-ttu-id="f1c41-130">1至8</span><span class="sxs-lookup"><span data-stu-id="f1c41-130">1 to 8</span></span> | <span data-ttu-id="f1c41-131">UINT32、UINT8</span><span class="sxs-lookup"><span data-stu-id="f1c41-131">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="f1c41-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1c41-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f1c41-133">**標頭**</span><span class="sxs-lookup"><span data-stu-id="f1c41-133">**Header**</span></span> | <span data-ttu-id="f1c41-134">directml。h</span><span class="sxs-lookup"><span data-stu-id="f1c41-134">directml.h</span></span> |