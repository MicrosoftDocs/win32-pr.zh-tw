---
description: '深入瞭解： JetGetObjectInfo 方法 (JET_SESID、JET_DBID、JET_objtyp、字串、JET_OBJECTINFO) '
title: 'JetGetObjectInfo 方法 (JET_SESID、JET_DBID、JET_objtyp、字串、JET_OBJECTINFO) '
TOCTitle: JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_objtyp,System.String,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetobjectinfo(v=EXCHG.10)
ms:contentKeyID: 55100733
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01311dcfbba226405a3c46c1be4c4553eac4eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972186"
---
# <a name="apijetgetobjectinfo-method-jet_sesid-jet_dbid-jet_objtyp-string-jet_objectinfo"></a>JetGetObjectInfo 方法 (JET_SESID、JET_DBID、JET_objtyp、字串、JET_OBJECTINFO) 

抓取資料庫物件的相關資訊。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetGetObjectInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    objtyp As JET_objtyp, _
    objectName As String, _
    <OutAttribute> ByRef objectinfo As JET_OBJECTINFO _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim objtyp As JET_objtyp
Dim objectName As String
Dim objectinfo As JET_OBJECTINFOApi.JetGetObjectInfo(sesid, dbid, _
    objtyp, objectName, objectinfo)
```

``` csharp
public static void JetGetObjectInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_objtyp objtyp,
    string objectName,
    out JET_OBJECTINFO objectinfo
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - dbid  
    類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    要使用的資料庫。

<!-- end list -->

  - objtyp  
    類型： [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)  
    
    物件的類型。

<!-- end list -->

  - objectName  
    類型： [system.string](/dotnet/api/system.string)  
    
    要取得其資訊的物件名稱。

<!-- end list -->

  - objectinfo  
    類型： [Microsoft.Isam.Esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)  
    
    填入資料庫中物件的相關資訊。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[JetGetObjectInfo 多載](./api.jetgetobjectinfo-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
