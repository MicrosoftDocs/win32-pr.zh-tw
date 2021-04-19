---
UID: NE:directml.DML_GRAPH_NODE_TYPE
title: DML_GRAPH_NODE_TYPE
description: 定義指定圖形節點類型的常數。 如需此列舉的用法，請參閱 [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) 。
helpviewer_keywords:
- DML_GRAPH_NODE_TYPE
- DML_GRAPH_NODE_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_GRAPH_NODE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_TYPE, DML_GRAPH_NODE_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
- directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
ms.openlocfilehash: 1788dfcce20ce2a9e490bf7ed6e8ef84e306d659
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106976391"
---
# <a name="dml_graph_node_type-enumeration-directmlh"></a><span data-ttu-id="d5d31-104">DML_GRAPH_NODE_TYPE 列舉 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="d5d31-104">DML_GRAPH_NODE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="d5d31-105">定義指定圖形節點類型的常數。</span><span class="sxs-lookup"><span data-stu-id="d5d31-105">Defines constants that specify a type of graph node.</span></span> <span data-ttu-id="d5d31-106">如需此列舉的用法，請參閱 [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) 。</span><span class="sxs-lookup"><span data-stu-id="d5d31-106">See [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5d31-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="d5d31-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="d5d31-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="d5d31-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d31-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5d31-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_NODE_TYPE {
  DML_GRAPH_NODE_TYPE_INVALID,
  DML_GRAPH_NODE_TYPE_OPERATOR
} ;
```

## <a name="constants"></a><span data-ttu-id="d5d31-110">常數</span><span class="sxs-lookup"><span data-stu-id="d5d31-110">Constants</span></span>

| <span data-ttu-id="d5d31-111">Name</span><span class="sxs-lookup"><span data-stu-id="d5d31-111">Name</span></span> | <span data-ttu-id="d5d31-112">描述</span><span class="sxs-lookup"><span data-stu-id="d5d31-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="d5d31-113">DML_GRAPH_NODE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="d5d31-113">DML_GRAPH_NODE_TYPE_INVALID</span></span> | <span data-ttu-id="d5d31-114">指定未知的圖形邊緣類型，而且永遠不會有效。</span><span class="sxs-lookup"><span data-stu-id="d5d31-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="d5d31-115">使用此值會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5d31-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="d5d31-116">DML_GRAPH_NODE_TYPE_OPERATOR</span><span class="sxs-lookup"><span data-stu-id="d5d31-116">DML_GRAPH_NODE_TYPE_OPERATOR</span></span> | <span data-ttu-id="d5d31-117">指定圖表邊緣由 [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) 結構描述。</span><span class="sxs-lookup"><span data-stu-id="d5d31-117">Specifies that the graph edge is described by the [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) structure.</span></span><br><br><span data-ttu-id="d5d31-118"># # 可用性</span><span class="sxs-lookup"><span data-stu-id="d5d31-118">## Availability</span></span><br><br><span data-ttu-id="d5d31-119">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="d5d31-119">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="d5d31-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5d31-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d5d31-121">**標頭**</span><span class="sxs-lookup"><span data-stu-id="d5d31-121">**Header**</span></span> | <span data-ttu-id="d5d31-122">directml。h</span><span class="sxs-lookup"><span data-stu-id="d5d31-122">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="d5d31-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5d31-123">See also</span></span>

* [<span data-ttu-id="d5d31-124">IDMLDevice1：： CompileGraph 方法</span><span class="sxs-lookup"><span data-stu-id="d5d31-124">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="d5d31-125">DML_GRAPH_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="d5d31-125">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="d5d31-126">DML_GRAPH_NODE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="d5d31-126">DML_GRAPH_NODE_DESC structure</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="d5d31-127">DML_OPERATOR_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="d5d31-127">DML_OPERATOR_GRAPH_NODE_DESC</span></span>](./ns-directml-dml_operator_graph_node_desc.md)