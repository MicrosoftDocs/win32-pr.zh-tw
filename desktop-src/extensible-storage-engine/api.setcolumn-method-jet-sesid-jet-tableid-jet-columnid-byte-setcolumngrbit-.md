---
description: '深入瞭解： SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、SetColumnGrbit) '
title: 'SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、SetColumnGrbit) '
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , SetColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],Microsoft.Isam.Esent.Interop.SetColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100881
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7265bf9115cea216a18a4b4e150c26d807e8908f00f6fecaabe78a3513761332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117717653"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--setcolumngrbit"></a>SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、SetColumnGrbit) 

修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    grbit As SetColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim grbit As SetColumnGrbitApi.SetColumn(sesid, tableid, columnid, _
    data, grbit)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    SetColumnGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要更新的資料指標。 應備妥更新。

<!-- end list -->

  - columnid  
    類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    要設定的 columnid。

<!-- end list -->

  - data  
    類型： \[\]  
    
    要設定的資料。

<!-- end list -->

  - grbit  
    型別： [SetColumnGrbit](./setcolumngrbit-enumeration.md) 。  
    
    SetColumn 選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[SetColumn 多載](./api.setcolumn-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
