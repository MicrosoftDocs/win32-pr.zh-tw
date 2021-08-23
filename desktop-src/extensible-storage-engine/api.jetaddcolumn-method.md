---
description: 深入瞭解： JetAddColumn 方法
title: JetAddColumn 方法
TOCTitle: 'JetAddColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAddColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.JET_COLUMNID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetaddcolumn(v=EXCHG.10)
ms:contentKeyID: 55100651
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d1972fdf9f19ad7a249df00a07cbe8481bcb133da81a748fda865639d934e4c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983688"
---
# <a name="apijetaddcolumn-method"></a>JetAddColumn 方法

將新的資料行加入至現有的資料表。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetAddColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    columndef As JET_COLUMNDEF, _
    defaultValue As Byte(), _
    defaultValueSize As Integer, _
    <OutAttribute> ByRef columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim columndef As JET_COLUMNDEF
Dim defaultValue As Byte()
Dim defaultValueSize As Integer
Dim columnid As JET_COLUMNIDApi.JetAddColumn(sesid, tableid, _
    column, columndef, defaultValue, _
    defaultValueSize, columnid)
```

``` csharp
public static void JetAddColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    JET_COLUMNDEF columndef,
    byte[] defaultValue,
    int defaultValueSize,
    out JET_COLUMNID columnid
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要加入資料行的資料表。

<!-- end list -->

  - 行  
    類型： [system.string](/dotnet/api/system.string)  
    
    資料行名稱。

<!-- end list -->

  - columndef  
    類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)  
    
    資料行的定義。

<!-- end list -->

  - defaultValue  
    類型： \[\]  
    
    資料行的預設值。

<!-- end list -->

  - defaultValueSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    預設值的大小。

<!-- end list -->

  - columnid  
    類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    傳回新資料行的 columnid。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
