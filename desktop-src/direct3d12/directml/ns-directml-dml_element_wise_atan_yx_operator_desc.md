---
UID: NS:directml.DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
title: DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
description: 針對 *ATensor* 和 *BTensor* 的每個專案計算雙引數反正切值，其中 *ATensor* 是 *Y 軸* ，而 *BTensor* 是 *X 軸*，將結果放入 *OutputTensor* 的對應元素。
helpviewer_keywords:
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.openlocfilehash: 6031f08dc99db943d26ab5212896b4fb44987269
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804450"
---
# <a name="dml_element_wise_atan_yx_operator_desc-directmlh"></a><span data-ttu-id="87a09-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml) </span><span class="sxs-lookup"><span data-stu-id="87a09-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="87a09-104">針對 *ATensor* 和 *BTensor* 的每個專案計算雙引數反正切值，其中 *ATensor* 是 *Y 軸* ，而 *BTensor* 是 *X 軸*，將結果放入 *OutputTensor* 的對應元素。</span><span class="sxs-lookup"><span data-stu-id="87a09-104">Computes the 2-argument arctangent for each element of *ATensor* and *BTensor*, where *ATensor* is the *Y-axis* and *BTensor* is the *X-axis*, placing the result into the corresponding element of *OutputTensor*.</span></span> <span data-ttu-id="87a09-105">來源 (的這個運算子是未定義的，也就是當對應元素) 的 *ATensor* 和 *BTensor* 都是0時。</span><span class="sxs-lookup"><span data-stu-id="87a09-105">This operator is undefined for the origin (that is, when *ATensor* and *BTensor* are both 0 for corresponding elements).</span></span>

![GRU_Forward](../images/atan2.png)

```
f(y, x) = atan2(y, x)
```

<span data-ttu-id="87a09-107">這個運算子支援就地執行，這表示在系結期間允許輸出 tensor 別名 *ATensor* 或 *BTensor* 。</span><span class="sxs-lookup"><span data-stu-id="87a09-107">This operator supports in-place execution, meaning that the output tensor is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87a09-108">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="87a09-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="87a09-109">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="87a09-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="87a09-110">語法</span><span class="sxs-lookup"><span data-stu-id="87a09-110">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="87a09-111">成員</span><span class="sxs-lookup"><span data-stu-id="87a09-111">Members</span></span>

`ATensor`

<span data-ttu-id="87a09-112">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="87a09-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="87a09-113">要從中讀取 Y 軸值的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="87a09-113">The input tensor to read the Y-axis values from.</span></span>

`BTensor`

<span data-ttu-id="87a09-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="87a09-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="87a09-115">要從中讀取 X 軸值的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="87a09-115">The input tensor to read the X-axis values from.</span></span>

`OutputTensor`

<span data-ttu-id="87a09-116">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="87a09-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="87a09-117">要寫入結果的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="87a09-117">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="87a09-118">可用性</span><span class="sxs-lookup"><span data-stu-id="87a09-118">Availability</span></span>
<span data-ttu-id="87a09-119">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。</span><span class="sxs-lookup"><span data-stu-id="87a09-119">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="87a09-120">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="87a09-120">Tensor constraints</span></span>
<span data-ttu-id="87a09-121">*ATensor*、 *BTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。</span><span class="sxs-lookup"><span data-stu-id="87a09-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="87a09-122">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="87a09-122">Tensor support</span></span>
| <span data-ttu-id="87a09-123">張</span><span class="sxs-lookup"><span data-stu-id="87a09-123">Tensor</span></span> | <span data-ttu-id="87a09-124">類型</span><span class="sxs-lookup"><span data-stu-id="87a09-124">Kind</span></span> | <span data-ttu-id="87a09-125">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="87a09-125">Supported dimension counts</span></span> | <span data-ttu-id="87a09-126">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="87a09-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="87a09-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="87a09-127">ATensor</span></span> | <span data-ttu-id="87a09-128">輸入</span><span class="sxs-lookup"><span data-stu-id="87a09-128">Input</span></span> | <span data-ttu-id="87a09-129">1至8</span><span class="sxs-lookup"><span data-stu-id="87a09-129">1 to 8</span></span> | <span data-ttu-id="87a09-130">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="87a09-130">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="87a09-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="87a09-131">BTensor</span></span> | <span data-ttu-id="87a09-132">輸入</span><span class="sxs-lookup"><span data-stu-id="87a09-132">Input</span></span> | <span data-ttu-id="87a09-133">1至8</span><span class="sxs-lookup"><span data-stu-id="87a09-133">1 to 8</span></span> | <span data-ttu-id="87a09-134">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="87a09-134">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="87a09-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="87a09-135">OutputTensor</span></span> | <span data-ttu-id="87a09-136">輸出</span><span class="sxs-lookup"><span data-stu-id="87a09-136">Output</span></span> | <span data-ttu-id="87a09-137">1至8</span><span class="sxs-lookup"><span data-stu-id="87a09-137">1 to 8</span></span> | <span data-ttu-id="87a09-138">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="87a09-138">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="87a09-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="87a09-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="87a09-140">**標頭**</span><span class="sxs-lookup"><span data-stu-id="87a09-140">**Header**</span></span> | <span data-ttu-id="87a09-141">directml。h</span><span class="sxs-lookup"><span data-stu-id="87a09-141">directml.h</span></span> |
