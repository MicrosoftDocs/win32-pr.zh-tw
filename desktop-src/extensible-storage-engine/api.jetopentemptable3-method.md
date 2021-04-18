---
description: 深入瞭解： JetOpenTempTable3 方法
title: Api.JetOpenTempTable3 方法
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e88b5413492c0ae00ed41e569afb49ca6c18e51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978160"
---
# <a name="apijetopentemptable3-method"></a>Api.JetOpenTempTable3 方法

使用單一索引建立臨時表。 臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。 不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。 它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。 另請參閱[JetOpenTempTable (JET_SESID、 \[ \] 、Int32、TempTableGrbit、JET_TABLEID、 \[ \]) ](./api.jetopentemptable-method.md)、 [JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) ](./vistaapi.jetopentemporarytable-method.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - 資料行  
    類型： \[\]  
    
    在臨時表中建立之資料行的資料行定義。

<!-- end list -->

  - numColumns  
    類型： [system.object](/dotnet/api/system.int32)  
    
    資料行定義的數目。

<!-- end list -->

  - unicodeindex  
    類型： [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  
    
    地區設定識別碼和正規化旗標，將用來比較臨時表中的任何 Unicode 索引鍵資料行資料。 如果不存在，則會使用預設選項。

<!-- end list -->

  - grbit  
    型別： [TempTableGrbit](./temptablegrbit-enumeration.md) 。  
    
    資料表建立選項。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    傳回臨時表的 tableid。 使用 [JetCloseTable (JET_SESID 關閉此 tableid，JET_TABLEID) ](./api.jetclosetable-method.md) 會釋出與臨時表相關聯的資源。

<!-- end list -->

  - columnids  
    類型： \[\]  
    
    輸出緩衝區，接收在建立臨時表期間所產生的資料行識別碼陣列。 此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。 因此，這個緩衝區的大小必須對應到輸入陣列的大小。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
