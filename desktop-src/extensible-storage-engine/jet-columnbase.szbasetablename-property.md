---
description: 深入瞭解： JET_COLUMNBASE szBaseTableName 屬性
title: JET_COLUMNBASE szBaseTableName 屬性
TOCTitle: 'szBaseTableName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.szBaseTableName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.szbasetablename(v=EXCHG.10)
ms:contentKeyID: 55103375
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.szBaseTableName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_szBaseTableName
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_szBaseTableName
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.szBaseTableName
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 072bb967f4ed021a69dd6b275007bf47bcb4fcb8fc342cf639d1f98a6bf17cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118076074"
---
# <a name="jet_columnbaseszbasetablename-property"></a>JET_COLUMNBASE szBaseTableName 屬性

取得目前資料表繼承其 DDL 的資料表。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szBaseTableName As String
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As String

value = instance.szBaseTableName
```

``` csharp
public string szBaseTableName { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.string](/dotnet/api/system.string)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COLUMNBASE 類別](./jet-columnbase-class.md)

[JET_COLUMNBASE 成員](./jet-columnbase-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
