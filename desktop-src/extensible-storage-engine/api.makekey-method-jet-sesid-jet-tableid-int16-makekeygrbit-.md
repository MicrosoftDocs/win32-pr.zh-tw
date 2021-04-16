---
description: '深入瞭解： MakeKey 方法 (JET_SESID、JET_TABLEID、Int16、MakeKeyGrbit) '
title: 'MakeKey 方法 (JET_SESID、JET_TABLEID、Int16、MakeKeyGrbit) '
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Int16, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int16,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100840
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42162f699510c2ef99c6001532adc7574fe8c99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512376"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-int16-makekeygrbit"></a>MakeKey 方法 (JET_SESID、JET_TABLEID、Int16、MakeKeyGrbit) 

建立可供 [JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) ](./api.jetseek-method.md) 和 [JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.jetsetindexrange-method.md)使用的搜尋索引鍵。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Short, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Short
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    short data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要在其上建立索引鍵的資料指標。

<!-- end list -->

  - data  
    類型： [system.object](/dotnet/api/system.int16)  
    
    目前索引之目前索引鍵資料行的資料行資料。

<!-- end list -->

  - grbit  
    型別： [MakeKeyGrbit](./makekeygrbit-enumeration.md) 。  
    
    索引鍵選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[MakeKey 多載](./api.makekey-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
