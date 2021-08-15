---
description: 深入瞭解： ColumnStream。位置屬性
title: ColumnStream。 Position 屬性
TOCTitle: 'Position property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnStream.Position
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.position(v=EXCHG.10)
ms:contentKeyID: 55100958
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Position
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.get_Position
- Microsoft.Isam.Esent.Interop.ColumnStream.set_Position
- Microsoft.Isam.Esent.Interop.ColumnStream.Position
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0f5a3709224e2c231ea35b53d2af823d19ec083974a0fbb4acd7a124d35153f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982628"
---
# <a name="columnstreamposition-property"></a>ColumnStream。 Position 屬性

取得或設定資料流中目前的位置。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Overrides Property Position As Long
    Get
    Set
'Usage
Dim instance As ColumnStream
Dim value As Long

value = instance.Position

instance.Position = value
```

``` csharp
public override long Position { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnStream 類別](./columnstream-class.md)

[ColumnStream 成員](./columnstream-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
