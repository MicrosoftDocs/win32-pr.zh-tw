---
UID: NS:directml.DML_GRAPH_EDGE_DESC
title: DML_GRAPH_EDGE_DESC
description: '[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)所定義的 DirectML 運算子圖形內之連接的一般容器，並傳遞至[IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。'
helpviewer_keywords:
- DML_GRAPH_EDGE_DESC
- DML_GRAPH_EDGE_DESC structure
- direct3d12.dml_graph_edge_desc
- directml/DML_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_DESC, DML_GRAPH_EDGE_DESC structure, direct3d12.dml_graph_edge_desc, directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
- directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
ms.openlocfilehash: 58cdf22dd85b1464d68cf1db75ff47a34817514c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802922"
---
# <a name="dml_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="d7f13-103">DML_GRAPH_EDGE_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="d7f13-103">DML_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="d7f13-104">[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)所定義的 DirectML 運算子圖形內之連接的一般容器，並傳遞至[IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。</span><span class="sxs-lookup"><span data-stu-id="d7f13-104">A generic container for a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7f13-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="d7f13-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="d7f13-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="d7f13-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f13-107">語法</span><span class="sxs-lookup"><span data-stu-id="d7f13-107">Syntax</span></span>
```cpp
struct DML_GRAPH_EDGE_DESC {
  DML_GRAPH_EDGE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a><span data-ttu-id="d7f13-108">成員</span><span class="sxs-lookup"><span data-stu-id="d7f13-108">Members</span></span>

`Type`

<span data-ttu-id="d7f13-109">類型： **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f13-109">Type: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span></span>

<span data-ttu-id="d7f13-110">圖形邊緣的型別。</span><span class="sxs-lookup"><span data-stu-id="d7f13-110">The type of graph edge.</span></span> <span data-ttu-id="d7f13-111">請參閱適用于可用類型的 [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) ，以及每種類型的使用 [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) 。</span><span class="sxs-lookup"><span data-stu-id="d7f13-111">See [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) for available types, and [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) for where to use each type.</span></span>


`Desc`

<span data-ttu-id="d7f13-112">類型： \_ 欄位 \_ 大小 \_ (\_ Inexpressible \_ ( 「相依于邊緣類型」 ) ) **const void \***</span><span class="sxs-lookup"><span data-stu-id="d7f13-112">Type: \_Field\_size\_(\_Inexpressible\_("Dependent on edge type")) **const void\***</span></span>

<span data-ttu-id="d7f13-113">圖形邊緣描述的指標。</span><span class="sxs-lookup"><span data-stu-id="d7f13-113">A pointer to the graph edge description.</span></span> <span data-ttu-id="d7f13-114">指向結構的型別必須符合 *型* 別中所指定的值。</span><span class="sxs-lookup"><span data-stu-id="d7f13-114">The type of the pointed-to struct must match the value specified in *Type*.</span></span>

## <a name="availability"></a><span data-ttu-id="d7f13-115">可用性</span><span class="sxs-lookup"><span data-stu-id="d7f13-115">Availability</span></span>

<span data-ttu-id="d7f13-116">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="d7f13-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="d7f13-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7f13-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d7f13-118">**標頭**</span><span class="sxs-lookup"><span data-stu-id="d7f13-118">**Header**</span></span> | <span data-ttu-id="d7f13-119">directml。h</span><span class="sxs-lookup"><span data-stu-id="d7f13-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="d7f13-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7f13-120">See also</span></span>

* [<span data-ttu-id="d7f13-121">IDMLDevice1：： CompileGraph 方法</span><span class="sxs-lookup"><span data-stu-id="d7f13-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="d7f13-122">DML_GRAPH_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="d7f13-122">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)