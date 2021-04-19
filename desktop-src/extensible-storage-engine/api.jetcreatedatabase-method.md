---
description: 深入瞭解： JetCreateDatabase 方法
title: JetCreateDatabase 方法
TOCTitle: 'JetCreateDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase(v=EXCHG.10)
ms:contentKeyID: 55100748
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe427c270baf8a6d05e5d0ae99e1dc393208da01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986318"
---
# <a name="apijetcreatedatabase-method"></a>JetCreateDatabase 方法

建立和附加資料庫檔案。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetCreateDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase(sesid, database, _
    connect, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - [資料庫]  
    類型： [system.string](/dotnet/api/system.string)  
    
    要建立之資料庫檔案的路徑。

<!-- end list -->

  - 連線  
    類型： [system.string](/dotnet/api/system.string)  
    
    不使用參數。

<!-- end list -->

  - dbid  
    類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    傳回新資料庫的 dbid。

<!-- end list -->

  - grbit  
    型別： [CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md) 。  
    
    資料庫建立選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
