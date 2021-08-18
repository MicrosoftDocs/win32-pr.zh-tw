---
description: 深入瞭解： ColumnStream. Seek 方法
title: ColumnStream. Seek 方法
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883739bed33c17877dc86c33670233aab1afc67e9348009bb11c4e67ab27011c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738188"
---
# <a name="columnstreamseek-method"></a>ColumnStream. Seek 方法

在目前資料流中設定位置。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a>參數

  - Offset  
    類型： [Int64](/dotnet/api/system.int64)  
    
    相對於原始參數的位元組位移。

<!-- end list -->

  - 原始  
    類型： [SeekOrigin](/dotnet/api/system.io.seekorigin)  
    
    SeekOrigin，表示新位置的參考點。

#### <a name="return-value"></a>傳回值

類型： [Int64](/dotnet/api/system.int64)  
目前資料流程中的新位置。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnStream 類別](./columnstream-class.md)

[ColumnStream 成員](./columnstream-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
