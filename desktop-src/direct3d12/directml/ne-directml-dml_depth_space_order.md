---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: 定義常數，用於控制 DirectML 運算子 [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) 和 **DML_OPERATOR_SPACE_TO_DEPTH1** 中所套用的轉換。
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
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
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 009686adfc054c7b6344f01edafedaf2921693d5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417216"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a><span data-ttu-id="28757-103">DML_DEPTH_SPACE_ORDER 列舉 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="28757-103">DML_DEPTH_SPACE_ORDER enumeration (directml.h)</span></span>

<span data-ttu-id="28757-104">定義常數，用於控制 DirectML 運算子 [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) 和 **DML_OPERATOR_SPACE_TO_DEPTH1** 中所套用的轉換。</span><span class="sxs-lookup"><span data-stu-id="28757-104">Defines constants controlling the transform applied in the DirectML operators [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) and **DML_OPERATOR_SPACE_TO_DEPTH1**.</span></span> <span data-ttu-id="28757-105">這些會在 [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) 和 [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) 結構中使用。</span><span class="sxs-lookup"><span data-stu-id="28757-105">These are used within the [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) structures.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28757-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="28757-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="28757-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="28757-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="28757-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="28757-108">Syntax</span></span>
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a><span data-ttu-id="28757-109">常數</span><span class="sxs-lookup"><span data-stu-id="28757-109">Constants</span></span>

| <span data-ttu-id="28757-110">Name</span><span class="sxs-lookup"><span data-stu-id="28757-110">Name</span></span> | <span data-ttu-id="28757-111">描述</span><span class="sxs-lookup"><span data-stu-id="28757-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="28757-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span><span class="sxs-lookup"><span data-stu-id="28757-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span></span> | <span data-ttu-id="28757-113">使 [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) 中使用的張量和 [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) 以下列配置來解讀，其中括弧中的維度會一起壓平合併。</span><span class="sxs-lookup"><span data-stu-id="28757-113">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="28757-114">- **深度版本**： [批次、 (BlockHeight、BlockWidth、通道) 、高度、寬度]</span><span class="sxs-lookup"><span data-stu-id="28757-114">- **Depth version**: [Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span></span><br><span data-ttu-id="28757-115">- **空間版本**： [批次、通道、 (高度、BlockHeight) 、 (寬度、BlockWidth) ]</span><span class="sxs-lookup"><span data-stu-id="28757-115">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |
| <span data-ttu-id="28757-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span><span class="sxs-lookup"><span data-stu-id="28757-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span></span> | <span data-ttu-id="28757-117">使 [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) 中使用的張量和 [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) 以下列配置來解讀，其中括弧中的維度會一起壓平合併。</span><span class="sxs-lookup"><span data-stu-id="28757-117">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="28757-118">- **深度版本**： [批次、 (通道、BlockHeight、BlockWidth) 、高度、寬度]</span><span class="sxs-lookup"><span data-stu-id="28757-118">- **Depth version**: [Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span></span><br><span data-ttu-id="28757-119">- **空間版本**： [批次、通道、 (高度、BlockHeight) 、 (寬度、BlockWidth) ]</span><span class="sxs-lookup"><span data-stu-id="28757-119">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |

## <a name="remarks"></a><span data-ttu-id="28757-120">備註</span><span class="sxs-lookup"><span data-stu-id="28757-120">Remarks</span></span>

<span data-ttu-id="28757-121">如需顯示這些值效果的範例，請參閱 [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) 和 [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="28757-121">See [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) documentation for examples showing the effect of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="28757-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="28757-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="28757-123">**標頭**</span><span class="sxs-lookup"><span data-stu-id="28757-123">**Header**</span></span> | <span data-ttu-id="28757-124">directml。h</span><span class="sxs-lookup"><span data-stu-id="28757-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="28757-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28757-125">See also</span></span>

* [<span data-ttu-id="28757-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="28757-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span></span>](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [<span data-ttu-id="28757-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="28757-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a><span data-ttu-id="28757-128">可用性</span><span class="sxs-lookup"><span data-stu-id="28757-128">Availability</span></span>
<span data-ttu-id="28757-129">這個列舉是在中引進 `DML_FEATURE_LEVEL_2_1` 。</span><span class="sxs-lookup"><span data-stu-id="28757-129">This enumeration was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>