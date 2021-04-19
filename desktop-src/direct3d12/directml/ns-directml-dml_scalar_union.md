---
UID: NS:directml.DML_SCALAR_UNION
title: DML_SCALAR_UNION
description: 純量類型的聯集。
helpviewer_keywords:
- DML_SCALAR_UNION
- DML_SCALAR_UNION structure
- direct3d12.dml_scalar_union
- directml/DML_SCALAR_UNION
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
ms.keywords: DML_SCALAR_UNION, DML_SCALAR_UNION structure, direct3d12.dml_scalar_union, directml/DML_SCALAR_UNION
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
- DML_SCALAR_UNION
- directml/DML_SCALAR_UNION
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
- DML_SCALAR_UNION
ms.openlocfilehash: 0abef8cd5a694fa82e0e54e334834773f1f75e20
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106986427"
---
# <a name="dml_scalar_union-union-directmlh"></a>DML_SCALAR_UNION 聯集 (directml .h) 
純量類型的聯集。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
union DML_SCALAR_UNION {
  BYTE   Bytes[8];
  INT8   Int8;
  UINT8  UInt8;
  INT16  Int16;
  UINT16 UInt16;
  INT32  Int32;
  UINT32 UInt32;
  INT64  Int64;
  UINT64 UInt64;
  FLOAT  Float32;
  DOUBLE Float64;
};
```



## <a name="members"></a>成員

`Bytes`

8位元組陣列。


`Int8`

8 位元帶正負號的整數。


`UInt8`

8 位元不帶正負號的整數。


`Int16`

16 位元帶正負號的整數。


`UInt16`

16 位元不帶正負號的整數。


`Int32`

32 位元帶正負號的整數。


`UInt32`

32 位元不帶正負號的整數。


`Int64`

64 位元帶正負號的整數。


`UInt64`

64 位元不帶正負號的整數。


`Float32`

單一有效位數浮點數。


`Float64`

雙精確度浮點數。



## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |