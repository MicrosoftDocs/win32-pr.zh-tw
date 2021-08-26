---
description: 深入瞭解： ColumnStream. Read 方法
title: ColumnStream. Read 方法
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 34c2bd13a2cc436ea192433e4f70098e328d1658a484c5dca9b092fe18f99a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976619"
---
# <a name="columnstreamread-method"></a>ColumnStream. Read 方法

從目前的資料流讀取位元組序列，並依讀取的位元組數將資料流中的位置往前移。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a>參數

  - 緩衝區  
    類型： \[\]  
    
    要讀入的緩衝區。

<!-- end list -->

  - Offset  
    類型： [system.object](/dotnet/api/system.int32)  
    
    緩衝區中要讀入的位移。

<!-- end list -->

  - count  
    類型： [system.object](/dotnet/api/system.int32)  
    
    要讀取的位元組數。

#### <a name="return-value"></a>傳回值

類型： [system.object](/dotnet/api/system.int32)  
讀入緩衝區的位元組數目。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnStream 類別](./columnstream-class.md)

[ColumnStream 成員](./columnstream-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
