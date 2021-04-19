---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: 定義指定圖形邊緣類型的常數。 如需此列舉的用法，請參閱 [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) 。
helpviewer_keywords:
- DML_GRAPH_EDGE_TYPE
- DML_GRAPH_EDGE_TYPE structure
- direct3d12.dml_graph_edge_type
- directml/DML_GRAPH_EDGE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
- directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
ms.openlocfilehash: 19b11686f3741c386ca03e84af5a41af1ce5cb52
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106997311"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a><span data-ttu-id="05db8-104">DML_GRAPH_EDGE_TYPE 列舉 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="05db8-104">DML_GRAPH_EDGE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="05db8-105">定義指定圖形邊緣類型的常數。</span><span class="sxs-lookup"><span data-stu-id="05db8-105">Defines constants that specify a type of graph edge.</span></span> <span data-ttu-id="05db8-106">如需此列舉的用法，請參閱 [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) 。</span><span class="sxs-lookup"><span data-stu-id="05db8-106">See [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05db8-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="05db8-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="05db8-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="05db8-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="05db8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="05db8-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a><span data-ttu-id="05db8-110">常數</span><span class="sxs-lookup"><span data-stu-id="05db8-110">Constants</span></span>

| <span data-ttu-id="05db8-111">Name</span><span class="sxs-lookup"><span data-stu-id="05db8-111">Name</span></span> | <span data-ttu-id="05db8-112">描述</span><span class="sxs-lookup"><span data-stu-id="05db8-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="05db8-113">DML_GRAPH_EDGE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="05db8-113">DML_GRAPH_EDGE_TYPE_INVALID</span></span> | <span data-ttu-id="05db8-114">指定未知的圖形邊緣類型，而且永遠不會有效。</span><span class="sxs-lookup"><span data-stu-id="05db8-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="05db8-115">使用此值會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="05db8-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="05db8-116">DML_GRAPH_EDGE_TYPE_INPUT</span><span class="sxs-lookup"><span data-stu-id="05db8-116">DML_GRAPH_EDGE_TYPE_INPUT</span></span> | <span data-ttu-id="05db8-117">指定圖表邊緣由 [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) 結構描述。</span><span class="sxs-lookup"><span data-stu-id="05db8-117">Specifies that the graph edge is described by the [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="05db8-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05db8-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span></span> | <span data-ttu-id="05db8-119">指定圖表邊緣由 [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) 結構描述。</span><span class="sxs-lookup"><span data-stu-id="05db8-119">Specifies that the graph edge is described by the [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="05db8-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span><span class="sxs-lookup"><span data-stu-id="05db8-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span></span> | <span data-ttu-id="05db8-121">指定圖表邊緣由 [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) 結構描述。</span><span class="sxs-lookup"><span data-stu-id="05db8-121">Specifies that the graph edge is described by the [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) structure.</span></span><br><br><span data-ttu-id="05db8-122"># # 可用性</span><span class="sxs-lookup"><span data-stu-id="05db8-122">## Availability</span></span><br><br><span data-ttu-id="05db8-123">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="05db8-123">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="05db8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="05db8-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="05db8-125">**標頭**</span><span class="sxs-lookup"><span data-stu-id="05db8-125">**Header**</span></span> | <span data-ttu-id="05db8-126">directml。h</span><span class="sxs-lookup"><span data-stu-id="05db8-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="05db8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05db8-127">See also</span></span>

* [<span data-ttu-id="05db8-128">IDMLDevice1：： CompileGraph 方法</span><span class="sxs-lookup"><span data-stu-id="05db8-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="05db8-129">DML_GRAPH_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="05db8-129">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="05db8-130">DML_GRAPH_EDGE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="05db8-130">DML_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_graph_edge_desc.md)
* [<span data-ttu-id="05db8-131">DML_INPUT_GRAPH_EDGE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="05db8-131">DML_INPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_input_graph_edge_desc.md)
* [<span data-ttu-id="05db8-132">DML_OUTPUT_GRAPH_EDGE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="05db8-132">DML_OUTPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_output_graph_edge_desc.md)
* [<span data-ttu-id="05db8-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="05db8-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_intermediate_graph_edge_desc.md)