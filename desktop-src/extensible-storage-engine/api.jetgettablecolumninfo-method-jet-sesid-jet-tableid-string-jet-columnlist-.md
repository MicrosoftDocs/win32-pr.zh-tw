---
description: '深入瞭解： JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、字串 JET_COLUMNLIST) '
title: 'JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_COLUMNLIST) '
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100723
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 516dad3bbc93a12ec216c5c3caa35617ea989bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694631"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-string-jet_columnlist"></a>JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_COLUMNLIST) 

抓取資料表中所有資料行的相關資訊。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String, _
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetTableColumnInfo(sesid, _
    tableid, columnName, columnlist)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName,
    out JET_COLUMNLIST columnlist
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    包含資料行的資料表。

<!-- end list -->

  - columnName  
    類型： [system.string](/dotnet/api/system.string)  
    
    參數已忽略。

<!-- end list -->

  - columnlist  
    類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)  
    
    填入資料表中資料行的相關資訊。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[JetGetTableColumnInfo 多載](./api.jetgettablecolumninfo-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
