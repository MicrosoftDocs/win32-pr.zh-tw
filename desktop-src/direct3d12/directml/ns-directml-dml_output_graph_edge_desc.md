---
UID: NS:directml.DML_OUTPUT_GRAPH_EDGE_DESC
title: DML_OUTPUT_GRAPH_EDGE_DESC
description: 描述 [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) 所定義的 DirectML 運算子圖形內的連接，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。 此結構是用來定義從內部節點輸出到圖形輸出的連接。
helpviewer_keywords:
- DML_OUTPUT_GRAPH_EDGE_DESC
- DML_OUTPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_output_graph_edge_desc
- directml/DML_OUTPUT_GRAPH_EDGE_DESC
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
- DML_OUTPUT_GRAPH_EDGE_DESC
- directml/DML_OUTPUT_GRAPH_EDGE_DESC
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
- DML_OUTPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: d1d48de0fa3bf2665269ebf2226de4e9911a1670
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106992627"
---
# <a name="dml_output_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="095e8-104">DML_OUTPUT_GRAPH_EDGE_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="095e8-104">DML_OUTPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="095e8-105">描述 [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) 所定義的 DirectML 運算子圖形內的連接，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。</span><span class="sxs-lookup"><span data-stu-id="095e8-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="095e8-106">此結構是用來定義從內部節點輸出到圖形輸出的連接。</span><span class="sxs-lookup"><span data-stu-id="095e8-106">This structure is used to define a connection from an output of an internal node to a graph output.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="095e8-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="095e8-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="095e8-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="095e8-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="095e8-109">語法</span><span class="sxs-lookup"><span data-stu-id="095e8-109">Syntax</span></span>
```cpp
struct DML_OUTPUT_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       GraphOutputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="095e8-110">成員</span><span class="sxs-lookup"><span data-stu-id="095e8-110">Members</span></span>

`FromNodeIndex`




`FromNodeOutputIndex`




`GraphOutputIndex`

<span data-ttu-id="095e8-111">類型： **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="095e8-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="095e8-112">從內部節點輸出指定連接之圖形輸出的索引。</span><span class="sxs-lookup"><span data-stu-id="095e8-112">The index of the graph output to which a connection from an internal node output is specified.</span></span>


`Name`

<span data-ttu-id="095e8-113">類型： \_ Field \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="095e8-113">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="095e8-114">圖形連接的選擇性名稱。</span><span class="sxs-lookup"><span data-stu-id="095e8-114">An optional name for the graph connection.</span></span> <span data-ttu-id="095e8-115">如果有提供，可能會在 DirectML debug 層發出的特定錯誤訊息中使用。</span><span class="sxs-lookup"><span data-stu-id="095e8-115">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="095e8-116">可用性</span><span class="sxs-lookup"><span data-stu-id="095e8-116">Availability</span></span>

<span data-ttu-id="095e8-117">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="095e8-117">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="095e8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="095e8-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="095e8-119">**標頭**</span><span class="sxs-lookup"><span data-stu-id="095e8-119">**Header**</span></span> | <span data-ttu-id="095e8-120">directml。h</span><span class="sxs-lookup"><span data-stu-id="095e8-120">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="095e8-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="095e8-121">See also</span></span>

* [<span data-ttu-id="095e8-122">IDMLDevice1：： CompileGraph 方法</span><span class="sxs-lookup"><span data-stu-id="095e8-122">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="095e8-123">DML_GRAPH_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="095e8-123">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="095e8-124">DML_GRAPH_EDGE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="095e8-124">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)