---
description: 深入瞭解： JET_THREADSTATS cbLogRecord 屬性
title: 'JET_THREADSTATS. cbLogRecord 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cbLogRecord property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cbLogRecord
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cblogrecord(v=EXCHG.10)
ms:contentKeyID: 39511575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cbLogRecord
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cbLogRecord
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cbLogRecord
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cbLogRecord
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04325435f090d1549fe7e742e9d4554fb9c61720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318047"
---
# <a name="jet_threadstatscblogrecord-property"></a>JET_THREADSTATS cbLogRecord 屬性

取得目前線程上資料庫引擎所產生的交易記錄大小總計（以位元組為單位）。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbLogRecord As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cbLogRecord
```

``` csharp
public int cbLogRecord { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_THREADSTATS 結構](./jet-threadstats-structure2.md)

[JET_THREADSTATS 成員](./jet-threadstats-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
