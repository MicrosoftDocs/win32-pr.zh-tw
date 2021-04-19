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
# <a name="dml_graph_edge_type-enumeration-directmlh"></a>DML_GRAPH_EDGE_TYPE 列舉 (directml .h) 

定義指定圖形邊緣類型的常數。 如需此列舉的用法，請參閱 [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) 。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>Syntax
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a>常數

| Name | 描述 |
| ---- |:---- |
| DML_GRAPH_EDGE_TYPE_INVALID | 指定未知的圖形邊緣類型，而且永遠不會有效。 使用此值會導致錯誤。 |
| DML_GRAPH_EDGE_TYPE_INPUT | 指定圖表邊緣由 [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) 結構描述。 |
| DML_GRAPH_EDGE_TYPE_OUTPUT | 指定圖表邊緣由 [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) 結構描述。 |
| DML_GRAPH_EDGE_TYPE_INTERMEDIATE | 指定圖表邊緣由 [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) 結構描述。<br><br># # 可用性<br><br>此 API 是在 DirectML 版本中引進 `1.1.0` 。 |


## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |

## <a name="see-also"></a>另請參閱

* [IDMLDevice1：： CompileGraph 方法](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC 結構](./ns-directml-dml_graph_desc.md)     
* [DML_GRAPH_EDGE_DESC 結構](./ns-directml-dml_graph_edge_desc.md)
* [DML_INPUT_GRAPH_EDGE_DESC 結構](./ns-directml-dml_input_graph_edge_desc.md)
* [DML_OUTPUT_GRAPH_EDGE_DESC 結構](./ns-directml-dml_output_graph_edge_desc.md)
* [DML_INTERMEDIATE_GRAPH_EDGE_DESC 結構](./ns-directml-dml_intermediate_graph_edge_desc.md)