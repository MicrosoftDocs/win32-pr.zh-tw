---
description: 深入瞭解： Windows8Api. JetCreateIndex4 方法
title: 'Windows8Api. JetCreateIndex4 方法 (Windows8 的) '
TOCTitle: 'JetCreateIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreateindex4(v=EXCHG.10)
ms:contentKeyID: 55104455
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc06fa47b8463c6c3b731a7e0e06b7ba13ae687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114257"
---
# <a name="windows8apijetcreateindex4-method"></a>Windows8Api. JetCreateIndex4 方法

對 ESE 資料庫中的資料建立索引。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetCreateIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerWindows8Api.JetCreateIndex4(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
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

  - indexcreates  
    類型： \[\]  
    
    物件的陣列，描述要建立的索引。

<!-- end list -->

  - numIndexCreates  
    類型： [system.object](/dotnet/api/system.int32)  
    
    索引描述物件的數目。

## <a name="remarks"></a>備註

建立多個索引時 (也就是 numIndexCreates 大於 1) 此方法必須在任何交易之外呼叫，且具有資料表的獨佔存取權。 JetCreateTable 所傳回的 JET_TABLEID 將擁有% 存取權，或者，您可以藉由將[DenyRead](./opentablegrbit-enumeration.md)傳遞至[JetOpenTable (JET_SESID、JET_DBID、字串、 \[ \] 、Int32、OpenTableGrbit、JET_TABLEID) ，](./api.jetopentable-method.md)來開啟該資料表以進行獨佔存取。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows8Api 類別](./windows8api-class.md)

[Windows8Api 成員](./windows8api-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
