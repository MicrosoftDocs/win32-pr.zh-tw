---
UID: NS:directml.DML_GRAPH_NODE_DESC
title: DML_GRAPH_NODE_DESC
description: '[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)所定義之 DirectML 運算子圖形內的節點泛型容器，並傳遞至[IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。'
helpviewer_keywords:
- DML_GRAPH_NODE_DESC
- DML_GRAPH_NODE_DESC structure
- direct3d12.dml_graph_node_desc
- directml/DML_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_DESC, DML_GRAPH_NODE_DESC structure, direct3d12.dml_graph_node_desc, directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
- directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
ms.openlocfilehash: 8c79719f51efb4a59f9459a28765d3442ed3f4ee
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106998939"
---
# <a name="dml_graph_node_desc-structure-directmlh"></a><span data-ttu-id="e194d-103">DML_GRAPH_NODE_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="e194d-103">DML_GRAPH_NODE_DESC structure (directml.h)</span></span>
<span data-ttu-id="e194d-104">[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)所定義之 DirectML 運算子圖形內的節點泛型容器，並傳遞至[IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。</span><span class="sxs-lookup"><span data-stu-id="e194d-104">A generic container for a node within a graph of DirectML operators defined by [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e194d-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="e194d-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e194d-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="e194d-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e194d-107">語法</span><span class="sxs-lookup"><span data-stu-id="e194d-107">Syntax</span></span>
```cpp
struct DML_GRAPH_NODE_DESC {
  DML_GRAPH_NODE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a><span data-ttu-id="e194d-108">成員</span><span class="sxs-lookup"><span data-stu-id="e194d-108">Members</span></span>

`Type`

<span data-ttu-id="e194d-109">類型： **[DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md)**</span><span class="sxs-lookup"><span data-stu-id="e194d-109">Type: **[DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md)**</span></span>

<span data-ttu-id="e194d-110">圖形節點的類型。</span><span class="sxs-lookup"><span data-stu-id="e194d-110">The type of graph node.</span></span> <span data-ttu-id="e194d-111">如需可用的類型，請參閱 [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) 。</span><span class="sxs-lookup"><span data-stu-id="e194d-111">See [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) for available types.</span></span>


`Desc`

<span data-ttu-id="e194d-112">類型： \_ 欄位 \_ 大小 \_ (\_ Inexpressible \_ ( 「相依于節點類型」 ) ) **const void \***</span><span class="sxs-lookup"><span data-stu-id="e194d-112">Type: \_Field\_size\_(\_Inexpressible\_("Dependent on node type")) **const void\***</span></span>

<span data-ttu-id="e194d-113">圖形節點描述的指標。</span><span class="sxs-lookup"><span data-stu-id="e194d-113">A pointer to the graph node description.</span></span> <span data-ttu-id="e194d-114">指向結構的型別必須符合 *型* 別中所指定的值。</span><span class="sxs-lookup"><span data-stu-id="e194d-114">The type of the pointed-to struct must match the value specified in *Type*.</span></span>

## <a name="availability"></a><span data-ttu-id="e194d-115">可用性</span><span class="sxs-lookup"><span data-stu-id="e194d-115">Availability</span></span>

<span data-ttu-id="e194d-116">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="e194d-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="e194d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e194d-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e194d-118">**標頭**</span><span class="sxs-lookup"><span data-stu-id="e194d-118">**Header**</span></span> | <span data-ttu-id="e194d-119">directml。h</span><span class="sxs-lookup"><span data-stu-id="e194d-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="e194d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e194d-120">See also</span></span>

* [<span data-ttu-id="e194d-121">IDMLDevice1：： CompileGraph 方法</span><span class="sxs-lookup"><span data-stu-id="e194d-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="e194d-122">DML_GRAPH_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="e194d-122">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)