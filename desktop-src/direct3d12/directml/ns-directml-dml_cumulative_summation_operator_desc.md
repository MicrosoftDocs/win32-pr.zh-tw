---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: 將 tensor 的專案加總在軸上，將總和的執行總和寫入輸出 tensor 中。
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106989106"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="04ed9-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="04ed9-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="04ed9-104">將 tensor 的專案加總在軸上，將總和的執行總和寫入輸出 tensor 中。</span><span class="sxs-lookup"><span data-stu-id="04ed9-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04ed9-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="04ed9-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="04ed9-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="04ed9-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="04ed9-107">語法</span><span class="sxs-lookup"><span data-stu-id="04ed9-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a><span data-ttu-id="04ed9-108">成員</span><span class="sxs-lookup"><span data-stu-id="04ed9-108">Members</span></span>

`InputTensor`

<span data-ttu-id="04ed9-109">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04ed9-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04ed9-110">包含要加總之元素的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="04ed9-110">The input tensor containing elements to be summed.</span></span>


`OutputTensor`

<span data-ttu-id="04ed9-111">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04ed9-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04ed9-112">要寫入所產生累計總和的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="04ed9-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="04ed9-113">這個 tensor 的大小和資料類型必須與 *InputTensor* 相同。</span><span class="sxs-lookup"><span data-stu-id="04ed9-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="04ed9-114">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="04ed9-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="04ed9-115">要加總元素之維度的索引。</span><span class="sxs-lookup"><span data-stu-id="04ed9-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="04ed9-116">這個值必須小於 *InputTensor* 的 *DimensionCount* 。</span><span class="sxs-lookup"><span data-stu-id="04ed9-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`AxisDirection`

<span data-ttu-id="04ed9-117">類型： **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="04ed9-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="04ed9-118">[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)列舉的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="04ed9-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="04ed9-119">如果設定為 **DML_AXIS_DIRECTION_INCREASING**，則會以遞增的元素索引沿著指定的軸沿著 tensor 來進行總和。</span><span class="sxs-lookup"><span data-stu-id="04ed9-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="04ed9-120">如果設定為 **DML_AXIS_DIRECTION_DECREASING**，則反轉為 true，而且會藉由遞減索引來進行專案的總和。</span><span class="sxs-lookup"><span data-stu-id="04ed9-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>


`HasExclusiveSum`




## <a name="remarks"></a><span data-ttu-id="04ed9-121">備註</span><span class="sxs-lookup"><span data-stu-id="04ed9-121">Remarks</span></span>
<span data-ttu-id="04ed9-122">這個運算子支援就地執行，這表示允許 *OutputTensor* 在系結期間為 *InputTensor* 加上別名。</span><span class="sxs-lookup"><span data-stu-id="04ed9-122">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="04ed9-123">可用性</span><span class="sxs-lookup"><span data-stu-id="04ed9-123">Availability</span></span>
<span data-ttu-id="04ed9-124">這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="04ed9-124">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="04ed9-125">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="04ed9-125">Tensor constraints</span></span>
<span data-ttu-id="04ed9-126">*InputTensor* 和 *OutputTensor* 必須具有相同的 *資料類型* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="04ed9-126">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="04ed9-127">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="04ed9-127">Tensor support</span></span>
| <span data-ttu-id="04ed9-128">張</span><span class="sxs-lookup"><span data-stu-id="04ed9-128">Tensor</span></span> | <span data-ttu-id="04ed9-129">類型</span><span class="sxs-lookup"><span data-stu-id="04ed9-129">Kind</span></span> | <span data-ttu-id="04ed9-130">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="04ed9-130">Supported dimension counts</span></span> | <span data-ttu-id="04ed9-131">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="04ed9-131">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="04ed9-132">InputTensor</span><span class="sxs-lookup"><span data-stu-id="04ed9-132">InputTensor</span></span> | <span data-ttu-id="04ed9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="04ed9-133">Input</span></span> | <span data-ttu-id="04ed9-134">4</span><span class="sxs-lookup"><span data-stu-id="04ed9-134">4</span></span> | <span data-ttu-id="04ed9-135">FLOAT32、FLOAT16、UINT32、UINT16</span><span class="sxs-lookup"><span data-stu-id="04ed9-135">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="04ed9-136">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="04ed9-136">OutputTensor</span></span> | <span data-ttu-id="04ed9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="04ed9-137">Output</span></span> | <span data-ttu-id="04ed9-138">4</span><span class="sxs-lookup"><span data-stu-id="04ed9-138">4</span></span> | <span data-ttu-id="04ed9-139">FLOAT32、FLOAT16、UINT32、UINT16</span><span class="sxs-lookup"><span data-stu-id="04ed9-139">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="04ed9-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="04ed9-140">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="04ed9-141">**標頭**</span><span class="sxs-lookup"><span data-stu-id="04ed9-141">**Header**</span></span> | <span data-ttu-id="04ed9-142">directml。h</span><span class="sxs-lookup"><span data-stu-id="04ed9-142">directml.h</span></span> |