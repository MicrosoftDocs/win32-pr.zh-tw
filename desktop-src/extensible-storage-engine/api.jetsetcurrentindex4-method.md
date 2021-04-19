---
description: 深入瞭解： JetSetCurrentIndex4 方法
title: JetSetCurrentIndex4 方法
TOCTitle: 'JetSetCurrentIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex4(v=EXCHG.10)
ms:contentKeyID: 55100806
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2b9319554b998175b3f533c6cd5f4c2d05ba02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970780"
---
# <a name="apijetsetcurrentindex4-method"></a>JetSetCurrentIndex4 方法

設定資料指標的目前索引。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    indexid As JET_INDEXID, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim indexid As JET_INDEXID
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex4(sesid, _
    tableid, index, indexid, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    JET_INDEXID indexid,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要在其上設定索引的資料指標。

<!-- end list -->

  - 索引  
    類型： [system.string](/dotnet/api/system.string)  
    
    要選取之索引的名稱。 如果這是 null 或空白，則會選取主要索引。

<!-- end list -->

  - indexid  
    類型： [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)  
    
    要選取之索引的識別碼。 您可以使用 JetGetIndexInfo 或 JetGetTableIndexInfo 搭配 [IndexId](./jet-idxinfo-enumeration.md) 選項來取得此識別碼。

<!-- end list -->

  - grbit  
    型別： [SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md) 。  
    
    設定索引選項。

<!-- end list -->

  - itagSequence  
    類型： [system.object](/dotnet/api/system.int32)  
    
    多值資料行值的序號，此值會用來將資料指標放置在新的索引上。 此參數只會與 [NoMove](./setcurrentindexgrbit-enumeration.md)搭配使用。 當這個參數不存在或設為零時，其值會假設為1。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
