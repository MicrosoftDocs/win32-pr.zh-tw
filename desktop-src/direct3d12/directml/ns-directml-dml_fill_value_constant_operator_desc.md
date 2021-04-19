---
UID: NS:directml.DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
title: DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
description: 使用指定的常 *數值* 來填滿 tensor。
helpviewer_keywords:
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure
- direct3d12.dml_fill_value_constant_operator_desc
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.openlocfilehash: d2b69f1f6b1c9768c24cab9a58bba3c3cadb04bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106989102"
---
# <a name="dml_fill_value_constant_operator_desc-structure-directmlh"></a><span data-ttu-id="af237-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="af237-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="af237-104">使用指定的常 *數值* 來填滿 tensor。</span><span class="sxs-lookup"><span data-stu-id="af237-104">Fills a tensor with the given constant *Value*.</span></span> <span data-ttu-id="af237-105">這個運算子會執行下列虛擬虛擬。</span><span class="sxs-lookup"><span data-stu-id="af237-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="af237-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="af237-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="af237-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="af237-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="af237-108">語法</span><span class="sxs-lookup"><span data-stu-id="af237-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_CONSTANT_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      Value;
};
```



## <a name="members"></a><span data-ttu-id="af237-109">成員</span><span class="sxs-lookup"><span data-stu-id="af237-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="af237-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="af237-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="af237-111">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="af237-111">The tensor to write the results to.</span></span> <span data-ttu-id="af237-112">這個 tensor 可能會有任何大小。</span><span class="sxs-lookup"><span data-stu-id="af237-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="af237-113">類型： **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="af237-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="af237-114">*值* 欄位的資料類型，必須符合 *OutputTensor。*</span><span class="sxs-lookup"><span data-stu-id="af237-114">The data type of the *Value* field, which must match *OutputTensor.DataType*.</span></span>


`Value`

<span data-ttu-id="af237-115">類型： **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="af237-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="af237-116">用來填滿輸出的常數值， *ValueDataType* 決定如何解讀欄位。</span><span class="sxs-lookup"><span data-stu-id="af237-116">A constant value to fill the output, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="af237-117">範例</span><span class="sxs-lookup"><span data-stu-id="af237-117">Examples</span></span>

```
Value = 13.0

OutputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
    [[[[13.0f, 13.0f, 13.0f, 13.0f],
       [13.0f, 13.0f, 13.0f, 13.0f]]]]
```

## <a name="availability"></a><span data-ttu-id="af237-118">可用性</span><span class="sxs-lookup"><span data-stu-id="af237-118">Availability</span></span>
<span data-ttu-id="af237-119">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="af237-119">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="af237-120">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="af237-120">Tensor support</span></span>
| <span data-ttu-id="af237-121">張</span><span class="sxs-lookup"><span data-stu-id="af237-121">Tensor</span></span> | <span data-ttu-id="af237-122">類型</span><span class="sxs-lookup"><span data-stu-id="af237-122">Kind</span></span> | <span data-ttu-id="af237-123">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="af237-123">Supported dimension counts</span></span> | <span data-ttu-id="af237-124">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="af237-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="af237-125">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="af237-125">OutputTensor</span></span> | <span data-ttu-id="af237-126">輸出</span><span class="sxs-lookup"><span data-stu-id="af237-126">Output</span></span> | <span data-ttu-id="af237-127">4</span><span class="sxs-lookup"><span data-stu-id="af237-127">4</span></span> | <span data-ttu-id="af237-128">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="af237-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="af237-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="af237-129">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="af237-130">**標頭**</span><span class="sxs-lookup"><span data-stu-id="af237-130">**Header**</span></span> | <span data-ttu-id="af237-131">directml。h</span><span class="sxs-lookup"><span data-stu-id="af237-131">directml.h</span></span> |