---
description: 深入瞭解： JET_INDEXCREATE cbKey 屬性
title: JET_INDEXCREATE cbKey 屬性
TOCTitle: 'cbKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkey(v=EXCHG.10)
ms:contentKeyID: 55103585
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 40f607dc7c38a0e44abb2a2bfa326df5d25155d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694716"
---
# <a name="jet_indexcreatecbkey-property"></a>JET_INDEXCREATE cbKey 屬性

取得或設定 szKey 的長度（以字元為單位），包括兩個終止的 null。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbKey As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKey

instance.cbKey = value
```

``` csharp
public int cbKey { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXCREATE 類別](./jet-indexcreate-class.md)

[JET_INDEXCREATE 成員](./jet-indexcreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
