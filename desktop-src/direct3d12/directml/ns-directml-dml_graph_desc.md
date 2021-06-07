---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: 描述用來編譯結合、優化運算子的 DirectML 運算子圖形。
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
ms.openlocfilehash: a42996fc9fd7825e13232b245ab764c6439f9489
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417355"
---
# <a name="dml_graph_desc-structure-directmlh"></a><span data-ttu-id="25e8a-103">DML_GRAPH_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="25e8a-103">DML_GRAPH_DESC structure (directml.h)</span></span>

<span data-ttu-id="25e8a-104">描述用來編譯結合、優化運算子的 DirectML 運算子圖形。</span><span class="sxs-lookup"><span data-stu-id="25e8a-104">Describes a graph of DirectML operators used to compile a combined, optimized operator.</span></span> <span data-ttu-id="25e8a-105">請參閱 [IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。</span><span class="sxs-lookup"><span data-stu-id="25e8a-105">See [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25e8a-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="25e8a-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="25e8a-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="25e8a-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="25e8a-108">語法</span><span class="sxs-lookup"><span data-stu-id="25e8a-108">Syntax</span></span>
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a><span data-ttu-id="25e8a-109">成員</span><span class="sxs-lookup"><span data-stu-id="25e8a-109">Members</span></span>

`InputCount`

<span data-ttu-id="25e8a-110">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="25e8a-110">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="25e8a-111">整個圖形的輸入數目。</span><span class="sxs-lookup"><span data-stu-id="25e8a-111">The number of inputs of the overall graph.</span></span> <span data-ttu-id="25e8a-112">每個圖形輸入都可以連接到內部節點數目不定的數目，因此這可能與 *InputEdgeCount* 不同。</span><span class="sxs-lookup"><span data-stu-id="25e8a-112">Each graph input may be connected to a variable number of internal nodes, therefore this may be different from *InputEdgeCount*.</span></span>


`OutputCount`

<span data-ttu-id="25e8a-113">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="25e8a-113">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="25e8a-114">整體圖形的輸出數目。</span><span class="sxs-lookup"><span data-stu-id="25e8a-114">The number of outputs of the overall graph.</span></span> <span data-ttu-id="25e8a-115">每個圖表輸出都可以連接到內部節點的不定數目，因此這可能與 *OutputEdgeCount* 不同。</span><span class="sxs-lookup"><span data-stu-id="25e8a-115">Each graph output may be connected to a variable number of internal nodes, therefore this may be different from *OutputEdgeCount*.</span></span>


`NodeCount`

<span data-ttu-id="25e8a-116">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="25e8a-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="25e8a-117">圖形中的內部節點數目。</span><span class="sxs-lookup"><span data-stu-id="25e8a-117">The number of internal nodes in the graph.</span></span>


`Nodes`

<span data-ttu-id="25e8a-118">類型： \_ 欄位 \_ 大小 \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="25e8a-118">Type: \_Field\_size\_(NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)\***</span></span>

<span data-ttu-id="25e8a-119">圖形中的內部節點。</span><span class="sxs-lookup"><span data-stu-id="25e8a-119">The internal nodes in the graph.</span></span>


`InputEdgeCount`

<span data-ttu-id="25e8a-120">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="25e8a-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="25e8a-121">圖形輸入與圖形內部節點輸入之間的連接數目。</span><span class="sxs-lookup"><span data-stu-id="25e8a-121">The number of connections between graph inputs and inputs of internal nodes in the graph.</span></span>


`InputEdges`

<span data-ttu-id="25e8a-122">類型： \_ 欄位 \_ 大小 \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="25e8a-122">Type: \_Field\_size\_(InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="25e8a-123">圖形輸入與圖形內部節點輸入之間的連接陣列。</span><span class="sxs-lookup"><span data-stu-id="25e8a-123">An array of connections between graph inputs and inputs of internal nodes in the graph.</span></span> <span data-ttu-id="25e8a-124">每個元素內的 *類型* 欄位應該設定為 [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md)。</span><span class="sxs-lookup"><span data-stu-id="25e8a-124">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`OutputEdgeCount`

<span data-ttu-id="25e8a-125">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="25e8a-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="25e8a-126">圖形中內部節點的圖形輸出和輸出之間的連接數目。</span><span class="sxs-lookup"><span data-stu-id="25e8a-126">The number of connections between graph outputs and outputs of internal nodes in the graph.</span></span>


`OutputEdges`

<span data-ttu-id="25e8a-127">類型： \_ 欄位 \_ 大小 \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="25e8a-127">Type: \_Field\_size\_(OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="25e8a-128">圖形中內部節點的圖形輸出和輸出之間的連接陣列。</span><span class="sxs-lookup"><span data-stu-id="25e8a-128">An array of connections between graph outputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="25e8a-129">每個元素內的 *類型* 欄位應該設定為 [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md)。</span><span class="sxs-lookup"><span data-stu-id="25e8a-129">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`IntermediateEdgeCount`

<span data-ttu-id="25e8a-130">類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="25e8a-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="25e8a-131">圖形中節點之間的內部連接數目。</span><span class="sxs-lookup"><span data-stu-id="25e8a-131">The number of internal connections between nodes in the graph.</span></span>


`IntermediateEdges`

<span data-ttu-id="25e8a-132">類型： \_ 欄位 \_ 大小 \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="25e8a-132">Type: \_Field\_size\_(IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="25e8a-133">圖形中內部節點的輸入與輸出之間的連接陣列。</span><span class="sxs-lookup"><span data-stu-id="25e8a-133">An array of connections between inputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="25e8a-134">每個元素內的類型欄位應該設定為 [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span><span class="sxs-lookup"><span data-stu-id="25e8a-134">The Type field within each element should be set to [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span></span>


## <a name="remarks"></a><span data-ttu-id="25e8a-135">備註</span><span class="sxs-lookup"><span data-stu-id="25e8a-135">Remarks</span></span>
<span data-ttu-id="25e8a-136">此結構所描述的圖形必須是有向非循環圖表。</span><span class="sxs-lookup"><span data-stu-id="25e8a-136">The graph described by this structure must be a directed acyclic graph.</span></span> <span data-ttu-id="25e8a-137">您必須為每個提供的節點定義輸入和輸出的連接，但針對相關聯的運算子，其輸入和輸出是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="25e8a-137">You must define a connection for the input and output of each supplied node, except for inputs and outputs that are optional for the associated operator.</span></span>

<span data-ttu-id="25e8a-138">節點可能會使用針對特定輸入使用 [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) 旗標所建立的運算子。</span><span class="sxs-lookup"><span data-stu-id="25e8a-138">Nodes may use operators that were created using the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag for certain inputs.</span></span> <span data-ttu-id="25e8a-139">使用此旗標的任何運算子輸入都必須連接到圖形輸入。</span><span class="sxs-lookup"><span data-stu-id="25e8a-139">Any operator inputs using this flag must be connected to graph inputs.</span></span> <span data-ttu-id="25e8a-140">所有連接到相同圖形輸入的運算子輸入都必須使用或省略此旗標。</span><span class="sxs-lookup"><span data-stu-id="25e8a-140">All operator inputs connected to the same graph input must use or omit this flag equivalently.</span></span>

<span data-ttu-id="25e8a-141">連接其輸入和輸出的運算子會使用不同的維度計數、大小和資料類型，是合法的。</span><span class="sxs-lookup"><span data-stu-id="25e8a-141">It is legal to connect operators whose connected inputs and outputs use different dimension counts, sizes, and data types.</span></span> <span data-ttu-id="25e8a-142">這表示每個運算子都會以不同的方式來解讀 tensor 資料 blob。</span><span class="sxs-lookup"><span data-stu-id="25e8a-142">This implies that the tensor data blob is interpreted differently by each operator.</span></span> <span data-ttu-id="25e8a-143">不過，連接 tensor 輸入和輸出的 *TotalTensorSizeInBytes* 欄位必須相同。</span><span class="sxs-lookup"><span data-stu-id="25e8a-143">The *TotalTensorSizeInBytes* field of connected tensor inputs and outputs must be identical, though.</span></span> <span data-ttu-id="25e8a-144">操作員應該唯讀取先前運算子所撰寫的張量區域。</span><span class="sxs-lookup"><span data-stu-id="25e8a-144">Operators should only read regions of tensors written by earlier operators.</span></span> <span data-ttu-id="25e8a-145">作業輸出中的任何填補區域 (由於使用進展) 所產生的結果，並不保證會以零向下串流運算子的方式讀取。</span><span class="sxs-lookup"><span data-stu-id="25e8a-145">Any padding regions in the output of an operation (resulting from the use of strides) are not guaranteed to be read as zero by down-stream operators.</span></span>

## <a name="availability"></a><span data-ttu-id="25e8a-146">可用性</span><span class="sxs-lookup"><span data-stu-id="25e8a-146">Availability</span></span>

<span data-ttu-id="25e8a-147">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="25e8a-147">This API was introduced in DirectML version `1.1.0`.</span></span>


## <a name="requirements"></a><span data-ttu-id="25e8a-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="25e8a-148">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="25e8a-149">**標頭**</span><span class="sxs-lookup"><span data-stu-id="25e8a-149">**Header**</span></span> | <span data-ttu-id="25e8a-150">directml。h</span><span class="sxs-lookup"><span data-stu-id="25e8a-150">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="25e8a-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25e8a-151">See also</span></span>

* [<span data-ttu-id="25e8a-152">IDMLDevice1：： CompileGraph 方法</span><span class="sxs-lookup"><span data-stu-id="25e8a-152">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="25e8a-153">DML_GRAPH_NODE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="25e8a-153">DML_GRAPH_NODE_DESC struct</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="25e8a-154">DML_GRAPH_EDGE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="25e8a-154">DML_GRAPH_EDGE_DESC struct</span></span>](./ns-directml-dml_graph_edge_desc.md)