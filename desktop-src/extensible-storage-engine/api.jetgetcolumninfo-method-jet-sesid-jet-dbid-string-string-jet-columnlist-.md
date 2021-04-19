---
description: '深入瞭解： JetGetColumnInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_COLUMNLIST) '
title: 'JetGetColumnInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_COLUMNLIST) '
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100703
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
ms.openlocfilehash: 6f3f0ea95e82217f0d9b44e6a00558d3530a7616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970968"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnlist"></a>JetGetColumnInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_COLUMNLIST) 

抓取資料表中所有資料行的相關資訊。

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
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnlist)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNLIST columnlist
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
    
    這個參數已忽略。

<!-- end list -->

  - columnlist  
    類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)  
    
    填入資料表中資料行的相關資訊。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[JetGetColumnInfo 多載](./api.jetgetcolumninfo-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
