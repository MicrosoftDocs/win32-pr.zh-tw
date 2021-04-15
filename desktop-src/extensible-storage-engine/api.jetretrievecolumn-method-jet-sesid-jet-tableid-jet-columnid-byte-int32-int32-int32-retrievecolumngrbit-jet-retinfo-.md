---
description: '深入瞭解： JetRetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、Int32、Int32、Int32、RetrieveColumnGrbit、JET_RETINFO) '
title: 'JetRetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、Int32、Int32、Int32、RetrieveColumnGrbit、JET_RETINFO) '
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100792
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 832e6d6cc123e4a85a2cacb2df688348732fcc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320816"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-int32-retrievecolumngrbit-jet_retinfo"></a>JetRetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、Int32、Int32、Int32、RetrieveColumnGrbit、JET_RETINFO) 

從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。 或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。 此函數也可以從參考目前記錄的索引項目抓取資料行資料。 除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, actualDataSize, grbit, _
    retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    從中取出資料行的資料指標。

<!-- end list -->

  - columnid  
    類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    要取出的 columnid。

<!-- end list -->

  - data  
    類型： \[\]  
    
    要取出的資料緩衝區。

<!-- end list -->

  - dataSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    資料緩衝區的大小。

<!-- end list -->

  - dataOffset  
    類型： [system.object](/dotnet/api/system.int32)  
    
    要將資料讀入資料緩衝區的位移。

<!-- end list -->

  - actualDataSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    傳回資料緩衝區的實際大小。

<!-- end list -->

  - grbit  
    型別： [RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md) 。  
    
    取出資料行選項。

<!-- end list -->

  - retinfo  
    類型： [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)  
    
    如果 pretinfo 為 Null，則函式的行為就如同 itagSequence 為1，而 ibLongValue 為 0 (零) 。 這會導致資料行抓取抓取多重值資料行的第一個值，並在位移 0 (零) 取出長資料。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
ESENT 警告碼。  

## <a name="remarks"></a>備註

這是採用緩衝區位移和大小的內部方法。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[JetRetrieveColumn 多載](./api.jetretrievecolumn-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
