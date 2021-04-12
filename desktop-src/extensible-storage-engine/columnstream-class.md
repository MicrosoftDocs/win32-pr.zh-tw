---
description: 深入瞭解： ColumnStream 類別
title: ColumnStream 類別
TOCTitle: ColumnStream class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100939
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eea249347acd18ec71f03fcdc82b8a2baa1da9ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193438"
---
# <a name="columnstream-class"></a>ColumnStream 類別

這個類別會提供 long 值資料行的串流介面 (亦即 [LongBinary](./jet-coltyp-enumeration.md) 或) [LongText](./jet-coltyp-enumeration.md) 類型的資料行。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.MarshalByRefObject](/dotnet/api/system.marshalbyrefobject)  
    [System.object](/dotnet/api/system.io.stream)  
      ColumnStream （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Class ColumnStream _
    Inherits Stream
'Usage
Dim instance As ColumnStream
```

``` csharp
public class ColumnStream : Stream
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnStream 成員](./columnstream-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
