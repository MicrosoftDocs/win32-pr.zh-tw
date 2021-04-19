---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: 定義常數，以指定運算子的指定軸的方向 (例如，加總，選取最小的專案，然後選取) 的最小元素。
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
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
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
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
- DML_AXIS_DIRECTION
ms.openlocfilehash: 18cd2189f88378245be0824e0a68e5f618008bc7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106985794"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a><span data-ttu-id="6380f-103">DML_AXIS_DIRECTION 列舉 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="6380f-103">DML_AXIS_DIRECTION enumeration (directml.h)</span></span>

<span data-ttu-id="6380f-104">定義常數，以指定運算子的指定軸的方向 (例如，加總，選取最小的專案，然後選取) 的最小元素。</span><span class="sxs-lookup"><span data-stu-id="6380f-104">Defines constants that specify the direction of an operation along the given axis for the operator (for example, summation, selecting the top-k elements, selecting the minimum element).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6380f-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="6380f-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="6380f-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="6380f-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6380f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6380f-107">Syntax</span></span>
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a><span data-ttu-id="6380f-108">常數</span><span class="sxs-lookup"><span data-stu-id="6380f-108">Constants</span></span>

| <span data-ttu-id="6380f-109">Name</span><span class="sxs-lookup"><span data-stu-id="6380f-109">Name</span></span> | <span data-ttu-id="6380f-110">描述</span><span class="sxs-lookup"><span data-stu-id="6380f-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="6380f-111">DML_AXIS_DIRECTION_INCREASING</span><span class="sxs-lookup"><span data-stu-id="6380f-111">DML_AXIS_DIRECTION_INCREASING</span></span> | <span data-ttu-id="6380f-112">指定從低索引到高索引) 的遞增順序 (。</span><span class="sxs-lookup"><span data-stu-id="6380f-112">Specifies increasing order (from the low index to the high index).</span></span> |
| <span data-ttu-id="6380f-113">DML_AXIS_DIRECTION_DECREASING</span><span class="sxs-lookup"><span data-stu-id="6380f-113">DML_AXIS_DIRECTION_DECREASING</span></span> | <span data-ttu-id="6380f-114">指定從高索引到低索引) 的遞減順序 (。</span><span class="sxs-lookup"><span data-stu-id="6380f-114">Specifies decreasing order (from the high index to the low index).</span></span> |


## <a name="requirements"></a><span data-ttu-id="6380f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6380f-115">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6380f-116">**標頭**</span><span class="sxs-lookup"><span data-stu-id="6380f-116">**Header**</span></span> | <span data-ttu-id="6380f-117">directml。h</span><span class="sxs-lookup"><span data-stu-id="6380f-117">directml.h</span></span> |