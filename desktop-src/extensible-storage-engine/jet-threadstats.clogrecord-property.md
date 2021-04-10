---
description: 深入瞭解： JET_THREADSTATS cLogRecord 屬性
title: 'JET_THREADSTATS. cLogRecord 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cLogRecord property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cLogRecord
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.clogrecord(v=EXCHG.10)
ms:contentKeyID: 39511382
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cLogRecord
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cLogRecord
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cLogRecord
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cLogRecord
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17947c0ea74f00ae51101d3e10b2eb54c78abe7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194292"
---
# <a name="jet_threadstatsclogrecord-property"></a>JET_THREADSTATS cLogRecord 屬性

取得目前線程上資料庫引擎所產生的交易記錄檔記錄總數。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cLogRecord As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cLogRecord
```

``` csharp
public int cLogRecord { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_THREADSTATS 結構](./jet-threadstats-structure2.md)

[JET_THREADSTATS 成員](./jet-threadstats-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
