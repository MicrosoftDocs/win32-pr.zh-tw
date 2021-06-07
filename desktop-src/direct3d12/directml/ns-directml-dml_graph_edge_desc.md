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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417351"
---
# <a name="dml_graph_edge_desc-structure-directmlh"></a>DML_GRAPH_EDGE_DESC 結構 (directml .h) 
[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)所定義的 DirectML 運算子圖形內之連接的一般容器，並傳遞至[IDMLDevice1：： CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_GRAPH_EDGE_DESC {
  DML_GRAPH_EDGE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a>成員

`Type`

類型： **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**

圖形邊緣的型別。 請參閱適用于可用類型的 [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) ，以及每種類型的使用 [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) 。


`Desc`

類型： \_ 欄位 \_ 大小 \_ (\_ Inexpressible \_ ( 「相依于邊緣類型」 ) ) **const void \***

圖形邊緣描述的指標。 指向結構的型別必須符合 *型* 別中所指定的值。

## <a name="availability"></a>可用性

此 API 是在 DirectML 版本中引進 `1.1.0` 。



## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |

## <a name="see-also"></a>另請參閱

* [IDMLDevice1：： CompileGraph 方法](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC 結構](./ns-directml-dml_graph_desc.md)