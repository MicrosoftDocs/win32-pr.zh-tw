---
UID: NS:directml.DML_INPUT_GRAPH_EDGE_DESC
title: DML_INPUT_GRAPH_EDGE_DESC
description: 描述 [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) 所定義的 DirectML 運算子圖形內的連接，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。 此結構是用來定義從圖形輸入到內部節點輸入的連接。
helpviewer_keywords:
- DML_INPUT_GRAPH_EDGE_DESC
- DML_INPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_input_graph_edge_desc
- directml/DML_INPUT_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INPUT_GRAPH_EDGE_DESC, DML_INPUT_GRAPH_EDGE_DESC structure, direct3d12.dml_input_graph_edge_desc, directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
- directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: 00fcece76f4cb7ac46589914df4d74321d957fbc
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802892"
---
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="2159d-104">DML_INPUT_GRAPH_EDGE_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="2159d-104">DML_INPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="2159d-105">描述 [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) 所定義的 DirectML 運算子圖形內的連接，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。</span><span class="sxs-lookup"><span data-stu-id="2159d-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="2159d-106">此結構是用來定義從圖形輸入到內部節點輸入的連接。</span><span class="sxs-lookup"><span data-stu-id="2159d-106">This structure is used to define a connection from a graph input to an input of an internal node.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2159d-107">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="2159d-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="2159d-108">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="2159d-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2159d-109">語法</span><span class="sxs-lookup"><span data-stu-id="2159d-109">Syntax</span></span>
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="2159d-110">成員</span><span class="sxs-lookup"><span data-stu-id="2159d-110">Members</span></span>

`GraphInputIndex`

<span data-ttu-id="2159d-111">類型： **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2159d-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="2159d-112">指定內部節點輸入之連接的圖形輸入索引。</span><span class="sxs-lookup"><span data-stu-id="2159d-112">The index of the graph input from which a connection to an internal node input is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="2159d-113">類型： **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2159d-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="2159d-114">內部節點的索引，此節點會指定圖形輸入的連接。</span><span class="sxs-lookup"><span data-stu-id="2159d-114">The index of the internal node onto which the connection from the graph input is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="2159d-115">類型： **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2159d-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="2159d-116">指定連接之內部節點上的輸入索引。</span><span class="sxs-lookup"><span data-stu-id="2159d-116">The index of the input on the internal node where the connection is specified.</span></span>


`Name`

<span data-ttu-id="2159d-117">類型： \_ Field \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="2159d-117">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="2159d-118">圖形連接的選擇性名稱。</span><span class="sxs-lookup"><span data-stu-id="2159d-118">An optional name for the graph connection.</span></span> <span data-ttu-id="2159d-119">如果有提供，可能會在 DirectML debug 層發出的特定錯誤訊息中使用。</span><span class="sxs-lookup"><span data-stu-id="2159d-119">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="2159d-120">可用性</span><span class="sxs-lookup"><span data-stu-id="2159d-120">Availability</span></span>

<span data-ttu-id="2159d-121">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="2159d-121">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="2159d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2159d-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2159d-123">**標頭**</span><span class="sxs-lookup"><span data-stu-id="2159d-123">**Header**</span></span> | <span data-ttu-id="2159d-124">directml。h</span><span class="sxs-lookup"><span data-stu-id="2159d-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="2159d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2159d-125">See also</span></span>

* [<span data-ttu-id="2159d-126">IDMLDevice1：： CompileGraph 方法</span><span class="sxs-lookup"><span data-stu-id="2159d-126">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="2159d-127">DML_GRAPH_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="2159d-127">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="2159d-128">DML_GRAPH_EDGE_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="2159d-128">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)