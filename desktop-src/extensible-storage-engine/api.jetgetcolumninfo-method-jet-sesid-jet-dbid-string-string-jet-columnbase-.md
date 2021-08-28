---
description: '深入瞭解： JetGetColumnInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_COLUMNBASE) '
title: 'JetGetColumnInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_COLUMNBASE) '
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100705
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8bd0dd2872ac22b2ab8c7d7e5b98857d223e38abd286e0d9554ecbea1f621855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983428"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnbase"></a>JetGetColumnInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_COLUMNBASE) 

抓取資料表中資料行的相關資訊。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnbase As JET_COLUMNBASEApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - dbid  
    類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    包含資料表的資料庫。

<!-- end list -->

  - tablename  
    類型： [system.string](/dotnet/api/system.string)  
    
    包含資料行的資料表名稱。

<!-- end list -->

  - columnName  
    類型： [system.string](/dotnet/api/system.string)  
    
    資料行名稱。

<!-- end list -->

  - columnbase  
    類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)  
    
    填入資料表中資料行的相關資訊。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[JetGetColumnInfo 多載](./api.jetgetcolumninfo-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
