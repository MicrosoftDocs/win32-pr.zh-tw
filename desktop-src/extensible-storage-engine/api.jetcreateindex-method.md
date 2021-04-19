---
description: 深入瞭解： JetCreateIndex 方法
title: JetCreateIndex 方法
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9b3549461324f396408bb7d370531907248e8c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972826"
---
# <a name="apijetcreateindex-method"></a>JetCreateIndex 方法

對 ESE 資料庫中的資料建立索引。 索引可以用來快速找出特定資料。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要在其上建立索引的資料表。

<!-- end list -->

  - IndexName  
    類型： [system.string](/dotnet/api/system.string)  
    
    指標，指向以 null 終止的字串，指定要建立之索引的名稱。

<!-- end list -->

  - grbit  
    型別： [CreateIndexGrbit](./createindexgrbit-enumeration.md) 。  
    
    索引建立選項。

<!-- end list -->

  - keyDescription  
    類型： [system.string](/dotnet/api/system.string)  
    
    Null 分隔標記的雙 null 結束字串指標。

<!-- end list -->

  - keyDescriptionLength  
    類型： [system.object](/dotnet/api/system.int32)  
    
    SzKey 的長度（以字元為單位），包括兩個終止的 null。

<!-- end list -->

  - 密度 (density)  
    類型： [system.object](/dotnet/api/system.int32)  
    
    初始 B + 樹狀結構密度。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
