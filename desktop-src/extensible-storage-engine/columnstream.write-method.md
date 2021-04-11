---
description: 深入瞭解： ColumnStream 撰寫方法
title: ColumnStream 撰寫方法
TOCTitle: 'Write method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Write(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.write(v=EXCHG.10)
ms:contentKeyID: 55100987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77b62e7dd028da3452082c973690ce0c0210b438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027388"
---
# <a name="columnstreamwrite-method"></a>ColumnStream 撰寫方法

將位元組序列寫入至目前的資料流，並依寫入的位元組數將資料流中目前的位置往前移。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Overrides Sub Write ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
)
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer

instance.Write(buffer, offset, count)
```

``` csharp
public override void Write(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a>參數

  - 緩衝區  
    類型： \[\]  
    
    要寫入的緩衝區。

<!-- end list -->

  - Offset  
    類型： [system.object](/dotnet/api/system.int32)  
    
    緩衝區中要寫入的位移。

<!-- end list -->

  - count  
    類型： [system.object](/dotnet/api/system.int32)  
    
    要寫入的位元組數。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnStream 類別](./columnstream-class.md)

[ColumnStream 成員](./columnstream-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
