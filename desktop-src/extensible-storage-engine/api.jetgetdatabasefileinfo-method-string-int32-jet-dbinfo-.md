---
description: '深入瞭解： JetGetDatabaseFileInfo 方法 (字串、Int32、JET_DbInfo) '
title: 'JetGetDatabaseFileInfo 方法 (字串、Int32、JET_DbInfo) '
TOCTitle: JetGetDatabaseFileInfo method (String, Int32, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int32@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100698
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a7d873d3688d6c18ff01a20c5e5c53809fbcdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966691"
---
# <a name="apijetgetdatabasefileinfo-method-string-int32-jet_dbinfo"></a>JetGetDatabaseFileInfo 方法 (字串、Int32、JET_DbInfo) 

抓取特定資料庫的特定資訊。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Integer, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Integer
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out int value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a>參數

  - databaseName  
    類型： [system.string](/dotnet/api/system.string)  
    
    資料庫的檔案名。

<!-- end list -->

  - value  
    類型： [system.object](/dotnet/api/system.int32)  
    
    要擷取的值。

<!-- end list -->

  - infoLevel  
    類型： [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)  
    
    要取出的特定資料。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[JetGetDatabaseFileInfo 多載](./api.jetgetdatabasefileinfo-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
