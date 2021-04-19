---
description: 深入瞭解： JET_THREADSTATS 結構
title: 'JET_THREADSTATS 結構 (的結構) '
TOCTitle: JET_THREADSTATS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats(v=EXCHG.10)
ms:contentKeyID: 39512342
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 764a9276543fbb7a5b1aa2762cc8ed1877c45ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972809"
---
# <a name="jet_threadstats-structure"></a>JET_THREADSTATS 結構

包含目前線程上資料庫引擎所執行之工作的累計統計資料。 這項資訊會透過 JetGetThreadStats 傳回。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_THREADSTATS _
    Implements IEquatable(Of JET_THREADSTATS)
'Usage
Dim instance As JET_THREADSTATS
```

``` csharp
[SerializableAttribute]
public struct JET_THREADSTATS : IEquatable<JET_THREADSTATS>
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_THREADSTATS 成員](./jet-threadstats-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
