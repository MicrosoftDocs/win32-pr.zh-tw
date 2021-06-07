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
ms.openlocfilehash: e54d2abed3843ea9b2a22cb3c385f9edd1541ba5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417219"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a><span data-ttu-id="81781-103">DML_AXIS_DIRECTION 列舉 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="81781-103">DML_AXIS_DIRECTION enumeration (directml.h)</span></span>

<span data-ttu-id="81781-104">定義常數，以指定運算子的指定軸的方向 (例如，加總，選取最小的專案，然後選取) 的最小元素。</span><span class="sxs-lookup"><span data-stu-id="81781-104">Defines constants that specify the direction of an operation along the given axis for the operator (for example, summation, selecting the top-k elements, selecting the minimum element).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81781-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="81781-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="81781-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="81781-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="81781-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81781-107">Syntax</span></span>
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a><span data-ttu-id="81781-108">常數</span><span class="sxs-lookup"><span data-stu-id="81781-108">Constants</span></span>

| <span data-ttu-id="81781-109">Name</span><span class="sxs-lookup"><span data-stu-id="81781-109">Name</span></span> | <span data-ttu-id="81781-110">描述</span><span class="sxs-lookup"><span data-stu-id="81781-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="81781-111">DML_AXIS_DIRECTION_INCREASING</span><span class="sxs-lookup"><span data-stu-id="81781-111">DML_AXIS_DIRECTION_INCREASING</span></span> | <span data-ttu-id="81781-112">指定從低索引到高索引) 的遞增順序 (。</span><span class="sxs-lookup"><span data-stu-id="81781-112">Specifies increasing order (from the low index to the high index).</span></span> |
| <span data-ttu-id="81781-113">DML_AXIS_DIRECTION_DECREASING</span><span class="sxs-lookup"><span data-stu-id="81781-113">DML_AXIS_DIRECTION_DECREASING</span></span> | <span data-ttu-id="81781-114">指定從高索引到低索引) 的遞減順序 (。</span><span class="sxs-lookup"><span data-stu-id="81781-114">Specifies decreasing order (from the high index to the low index).</span></span> |


## <a name="requirements"></a><span data-ttu-id="81781-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="81781-115">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="81781-116">**標頭**</span><span class="sxs-lookup"><span data-stu-id="81781-116">**Header**</span></span> | <span data-ttu-id="81781-117">directml。h</span><span class="sxs-lookup"><span data-stu-id="81781-117">directml.h</span></span> |