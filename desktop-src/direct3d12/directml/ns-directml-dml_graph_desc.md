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
# <a name="dml_graph_desc-structure-directmlh"></a>DML_GRAPH_DESC 結構 (directml .h) 

描述用來編譯結合、優化運算子的 DirectML 運算子圖形。 請參閱 [IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
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



## <a name="members"></a>成員

`InputCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

整個圖形的輸入數目。 每個圖形輸入都可以連接到內部節點數目不定的數目，因此這可能與 *InputEdgeCount* 不同。


`OutputCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

整體圖形的輸出數目。 每個圖表輸出都可以連接到內部節點的不定數目，因此這可能與 *OutputEdgeCount* 不同。


`NodeCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

圖形中的內部節點數目。


`Nodes`

類型： \_ 欄位 \_ 大小 \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***

圖形中的內部節點。


`InputEdgeCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

圖形輸入與圖形內部節點輸入之間的連接數目。


`InputEdges`

類型： \_ 欄位 \_ 大小 \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

圖形輸入與圖形內部節點輸入之間的連接陣列。 每個元素內的 *類型* 欄位應該設定為 [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md)。


`OutputEdgeCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

圖形中內部節點的圖形輸出和輸出之間的連接數目。


`OutputEdges`

類型： \_ 欄位 \_ 大小 \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

圖形中內部節點的圖形輸出和輸出之間的連接陣列。 每個元素內的 *類型* 欄位應該設定為 [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md)。


`IntermediateEdgeCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

圖形中節點之間的內部連接數目。


`IntermediateEdges`

類型： \_ 欄位 \_ 大小 \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

圖形中內部節點的輸入與輸出之間的連接陣列。 每個元素內的類型欄位應該設定為 [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)


## <a name="remarks"></a>備註
此結構所描述的圖形必須是有向非循環圖表。 您必須為每個提供的節點定義輸入和輸出的連接，但針對相關聯的運算子，其輸入和輸出是選擇性的。

節點可能會使用針對特定輸入使用 [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) 旗標所建立的運算子。 使用此旗標的任何運算子輸入都必須連接到圖形輸入。 所有連接到相同圖形輸入的運算子輸入都必須使用或省略此旗標。

連接其輸入和輸出的運算子會使用不同的維度計數、大小和資料類型，是合法的。 這表示每個運算子都會以不同的方式來解讀 tensor 資料 blob。 不過，連接 tensor 輸入和輸出的 *TotalTensorSizeInBytes* 欄位必須相同。 操作員應該唯讀取先前運算子所撰寫的張量區域。 作業輸出中的任何填補區域 (由於使用進展) 所產生的結果，並不保證會以零向下串流運算子的方式讀取。

## <a name="availability"></a>可用性

此 API 是在 DirectML 版本中引進 `1.1.0` 。


## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |

## <a name="see-also"></a>另請參閱

* [IDMLDevice1：： CompileGraph 方法](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_NODE_DESC 結構](./ns-directml-dml_graph_node_desc.md)
* [DML_GRAPH_EDGE_DESC 結構](./ns-directml-dml_graph_edge_desc.md)