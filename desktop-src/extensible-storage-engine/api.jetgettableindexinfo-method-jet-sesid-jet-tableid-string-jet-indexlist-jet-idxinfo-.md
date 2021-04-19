---
description: '深入瞭解： JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_INDEXLIST JET_IdxInfo) '
title: 'JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_INDEXLIST JET_IdxInfo) '
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100749
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42a938b2114cb379752f9a4f749782dd2b5b1757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985317"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-jet_indexlist-jet_idxinfo"></a>JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_INDEXLIST JET_IdxInfo) 

抓取資料表上索引的相關資訊。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As JET_INDEXLIST, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As JET_INDEXLIST
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out JET_INDEXLIST result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要取出相關索引資訊的資料表。

<!-- end list -->

  - indexname  
    類型： [system.string](/dotnet/api/system.string)  
    
    索引的名稱。

<!-- end list -->

  - result  
    類型： [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)  
    
    填入資料表上索引的相關資訊。

<!-- end list -->

  - infoLevel  
    類型： [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)  
    
    要取出的資訊類型。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[JetGetTableIndexInfo 多載](./api.jetgettableindexinfo-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
