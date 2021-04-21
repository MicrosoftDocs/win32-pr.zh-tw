---
UID: NS:directml.DML_INTERMEDIATE_GRAPH_EDGE_DESC
title: DML_INTERMEDIATE_GRAPH_EDGE_DESC
description: 描述 [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) 所定義的 DirectML 運算子圖形內的連接，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。 此結構是用來定義內部節點之間的連接。
helpviewer_keywords:
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- DML_INTERMEDIATE_GRAPH_EDGE_DESC structure
- direct3d12.dml_intermediate_graph_edge_desc
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INTERMEDIATE_GRAPH_EDGE_DESC, DML_INTERMEDIATE_GRAPH_EDGE_DESC structure, direct3d12.dml_intermediate_graph_edge_desc, directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.openlocfilehash: 17cf62def075e84ba86e97a5adfa48fb452f475e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802846"
---
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="b47c5-104">DML_INTERMEDIATE_GRAPH_EDGE_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="b47c5-104">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="b47c5-105">描述 [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) 所定義的 DirectML 運算子圖形內的連接，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。</span><span class="sxs-lookup"><span data-stu-id="b47c5-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="b47c5-106">此結構是用來定義內部節點之間的連接。</span><span class="sxs-lookup"><span data-stu-id="b47c5-106">This structure is used to define a connection between internal nodes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b47c5-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="b47c5-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b47c5-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="b47c5-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b47c5-109">語法</span><span class="sxs-lookup"><span data-stu-id="b47c5-109">Syntax</span></span>
```cpp
struct DML_INTERMEDIATE_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="b47c5-110">成員</span><span class="sxs-lookup"><span data-stu-id="b47c5-110">Members</span></span>

`FromNodeIndex`

<span data-ttu-id="b47c5-111">類型： **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b47c5-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="b47c5-112">與另一個節點的連接所指定之圖形節點的索引。</span><span class="sxs-lookup"><span data-stu-id="b47c5-112">The index of the graph node from which a connection to another node is specified.</span></span>


`FromNodeOutputIndex`

<span data-ttu-id="b47c5-113">類型： **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b47c5-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="b47c5-114">在索引 *FromNodeIndex* 上指定連接之節點的輸出索引。</span><span class="sxs-lookup"><span data-stu-id="b47c5-114">The index of the output on the node at index *FromNodeIndex* where the connection is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="b47c5-115">類型： **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b47c5-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="b47c5-116">從另一個節點指定連接之圖形節點的索引。</span><span class="sxs-lookup"><span data-stu-id="b47c5-116">The index of the graph node into which a connection from another node is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="b47c5-117">類型： **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b47c5-117">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="b47c5-118">在索引 *ToNodeIndex* 上指定連接之節點的輸入索引。</span><span class="sxs-lookup"><span data-stu-id="b47c5-118">The index of the input on the node at index *ToNodeIndex* where the connection is specified.</span></span>


`Name`

<span data-ttu-id="b47c5-119">類型： \_ Field \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="b47c5-119">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="b47c5-120">圖形連接的選擇性名稱。</span><span class="sxs-lookup"><span data-stu-id="b47c5-120">An optional name for the graph connection.</span></span> <span data-ttu-id="b47c5-121">如果有提供，可能會在 DirectML debug 層發出的特定錯誤訊息中使用。</span><span class="sxs-lookup"><span data-stu-id="b47c5-121">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="b47c5-122">可用性</span><span class="sxs-lookup"><span data-stu-id="b47c5-122">Availability</span></span>

<span data-ttu-id="b47c5-123">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="b47c5-123">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="b47c5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b47c5-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b47c5-125">**標頭**</span><span class="sxs-lookup"><span data-stu-id="b47c5-125">**Header**</span></span> | <span data-ttu-id="b47c5-126">directml。h</span><span class="sxs-lookup"><span data-stu-id="b47c5-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="b47c5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b47c5-127">See also</span></span>

* [<span data-ttu-id="b47c5-128">IDMLDevice1：： CompileGraph 方法</span><span class="sxs-lookup"><span data-stu-id="b47c5-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="b47c5-129">DML_GRAPH_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="b47c5-129">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="b47c5-130">DML_GRAPH_EDGE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="b47c5-130">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)