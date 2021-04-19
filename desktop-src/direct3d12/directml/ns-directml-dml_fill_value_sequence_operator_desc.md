---
UID: NS:directml.DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
title: DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
description: 使用序列填滿 tensor。
helpviewer_keywords:
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure
- direct3d12.dml_fill_value_sequence_operator_desc
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
ms.openlocfilehash: ec356568c0860d330234cd990e8cf42ff4ccd120
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106985792"
---
# <a name="dml_fill_value_sequence_operator_desc-structure-directmlh"></a><span data-ttu-id="90d76-103">DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="90d76-103">DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="90d76-104">使用序列填滿 tensor。</span><span class="sxs-lookup"><span data-stu-id="90d76-104">Fills a tensor with a sequence.</span></span> <span data-ttu-id="90d76-105">這個運算子會執行下列虛擬虛擬。</span><span class="sxs-lookup"><span data-stu-id="90d76-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
    Value += Delta
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="90d76-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="90d76-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="90d76-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="90d76-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="90d76-108">語法</span><span class="sxs-lookup"><span data-stu-id="90d76-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      ValueStart;
  DML_SCALAR_UNION      ValueDelta;
};
```



## <a name="members"></a><span data-ttu-id="90d76-109">成員</span><span class="sxs-lookup"><span data-stu-id="90d76-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="90d76-110">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="90d76-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="90d76-111">要寫入結果的 tensor。</span><span class="sxs-lookup"><span data-stu-id="90d76-111">The tensor to write the results to.</span></span> <span data-ttu-id="90d76-112">這個 tensor 可能會有任何大小。</span><span class="sxs-lookup"><span data-stu-id="90d76-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="90d76-113">類型： **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="90d76-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="90d76-114">*值* 欄位的資料類型，必須符合 *OutputTensor。*</span><span class="sxs-lookup"><span data-stu-id="90d76-114">The data type of *Value* field, which must match *OutputTensor.DataType*.</span></span>


`ValueStart`

<span data-ttu-id="90d76-115">類型： **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="90d76-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="90d76-116">用來填滿輸出中第一個元素的初始值， *ValueDataType* 決定如何解讀欄位。</span><span class="sxs-lookup"><span data-stu-id="90d76-116">The initial value to fill the first element in the output, with *ValueDataType* determining how to interpret the field.</span></span>


`ValueDelta`

<span data-ttu-id="90d76-117">類型： **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="90d76-117">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="90d76-118">要加入每個所寫入專案之值的步驟，並 *ValueDataType* 判斷如何解讀欄位。</span><span class="sxs-lookup"><span data-stu-id="90d76-118">A step to add to the value for each element written, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="90d76-119">範例</span><span class="sxs-lookup"><span data-stu-id="90d76-119">Examples</span></span>

### <a name="example-1-1d-ascending-step"></a><span data-ttu-id="90d76-120">範例 1.</span><span class="sxs-lookup"><span data-stu-id="90d76-120">Example 1.</span></span> <span data-ttu-id="90d76-121">1D 遞增步驟</span><span class="sxs-lookup"><span data-stu-id="90d76-121">1D ascending step</span></span>

```
ValueStart = 3
ValueDelta = 2
ValueDataType = DML_TENSOR_DATA_TYPE_FLOAT32

OutputTensor: (Sizes:{1,1,1,3}, DataType:FLOAT32)
    [[[[3, 5, 7]]]]
```

### <a name="example-2-2d-ascending-step"></a><span data-ttu-id="90d76-122">範例 2.</span><span class="sxs-lookup"><span data-stu-id="90d76-122">Example 2.</span></span> <span data-ttu-id="90d76-123">2D 遞增步驟</span><span class="sxs-lookup"><span data-stu-id="90d76-123">2D ascending step</span></span>

```
ValueStart = 10
ValueDelta = -2
ValueDataType = DML_TENSOR_DATA_TYPE_UINT8

OutputTensor: (Sizes:{1,1,2,2}, DataType:UINT8)
    [[[[10, 8],
       [ 6, 4]]]]
```

## <a name="availability"></a><span data-ttu-id="90d76-124">可用性</span><span class="sxs-lookup"><span data-stu-id="90d76-124">Availability</span></span>
<span data-ttu-id="90d76-125">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="90d76-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="90d76-126">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="90d76-126">Tensor support</span></span>
| <span data-ttu-id="90d76-127">張</span><span class="sxs-lookup"><span data-stu-id="90d76-127">Tensor</span></span> | <span data-ttu-id="90d76-128">類型</span><span class="sxs-lookup"><span data-stu-id="90d76-128">Kind</span></span> | <span data-ttu-id="90d76-129">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="90d76-129">Supported dimension counts</span></span> | <span data-ttu-id="90d76-130">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="90d76-130">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="90d76-131">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="90d76-131">OutputTensor</span></span> | <span data-ttu-id="90d76-132">輸出</span><span class="sxs-lookup"><span data-stu-id="90d76-132">Output</span></span> | <span data-ttu-id="90d76-133">4</span><span class="sxs-lookup"><span data-stu-id="90d76-133">4</span></span> | <span data-ttu-id="90d76-134">FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8</span><span class="sxs-lookup"><span data-stu-id="90d76-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="90d76-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="90d76-135">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="90d76-136">**標頭**</span><span class="sxs-lookup"><span data-stu-id="90d76-136">**Header**</span></span> | <span data-ttu-id="90d76-137">directml。h</span><span class="sxs-lookup"><span data-stu-id="90d76-137">directml.h</span></span> |