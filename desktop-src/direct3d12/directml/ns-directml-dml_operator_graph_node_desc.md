---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: 會說明由 [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) 所定義之 DirectML 運算子圖形內的節點，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。
helpviewer_keywords:
- DML_OPERATOR_GRAPH_NODE_DESC
- DML_OPERATOR_GRAPH_NODE_DESC structure
- direct3d12.dml_operator_graph_node_desc
- directml/DML_OPERATOR_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/05/2020
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
- DML_OPERATOR_GRAPH_NODE_DESC
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
ms.openlocfilehash: 6081f81044ff2ce384f7906af9c6e80f6b06f774
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106986428"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a><span data-ttu-id="82823-103">DML_OPERATOR_GRAPH_NODE_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="82823-103">DML_OPERATOR_GRAPH_NODE_DESC structure (directml.h)</span></span>
<span data-ttu-id="82823-104">會說明由 [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) 所定義之 DirectML 運算子圖形內的節點，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。</span><span class="sxs-lookup"><span data-stu-id="82823-104">Decribes a node within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

<span data-ttu-id="82823-105">此節點的行為是由 DirectML 運算子所定義。</span><span class="sxs-lookup"><span data-stu-id="82823-105">The behavior of this node is defined by a DirectML operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82823-106">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="82823-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="82823-107">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="82823-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="82823-108">語法</span><span class="sxs-lookup"><span data-stu-id="82823-108">Syntax</span></span>
```cpp
struct DML_OPERATOR_GRAPH_NODE_DESC {
  IDMLOperator *Operator;
  const char   *Name;
};
```



## <a name="members"></a><span data-ttu-id="82823-109">成員</span><span class="sxs-lookup"><span data-stu-id="82823-109">Members</span></span>

`Operator`

<span data-ttu-id="82823-110">類型： <b> [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span><span class="sxs-lookup"><span data-stu-id="82823-110">Type: <b>[IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span></span>

<span data-ttu-id="82823-111">定義節點行為的 DirectML 運算子。</span><span class="sxs-lookup"><span data-stu-id="82823-111">A DirectML operator defining the behavior of the node.</span></span>


`Name`

<span data-ttu-id="82823-112">類型： \_ Field \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="82823-112">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="82823-113">圖形連接的選擇性名稱。</span><span class="sxs-lookup"><span data-stu-id="82823-113">An optional name for the graph connection.</span></span> <span data-ttu-id="82823-114">如果有提供，可能會在 DirectML debug 層發出的特定錯誤訊息中使用。</span><span class="sxs-lookup"><span data-stu-id="82823-114">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="82823-115">可用性</span><span class="sxs-lookup"><span data-stu-id="82823-115">Availability</span></span>

<span data-ttu-id="82823-116">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="82823-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="82823-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="82823-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="82823-118">**標頭**</span><span class="sxs-lookup"><span data-stu-id="82823-118">**Header**</span></span> | <span data-ttu-id="82823-119">directml。h</span><span class="sxs-lookup"><span data-stu-id="82823-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="82823-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82823-120">See also</span></span>

* [<span data-ttu-id="82823-121">IDMLDevice1：： CompileGraph 方法</span><span class="sxs-lookup"><span data-stu-id="82823-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="82823-122">DML_GRAPH_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="82823-122">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="82823-123">DML_GRAPH_NODE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="82823-123">DML_GRAPH_NODE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)