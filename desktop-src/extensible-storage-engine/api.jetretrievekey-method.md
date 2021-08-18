---
description: 深入瞭解： JetRetrieveKey 方法
title: JetRetrieveKey 方法
TOCTitle: 'JetRetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievekey(v=EXCHG.10)
ms:contentKeyID: 55100795
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 161840971181db3594257b1ae2440c3c1c06b35a871b21c4cbeddad56527a9d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118783899"
---
# <a name="apijetretrievekey-method"></a>JetRetrieveKey 方法

在資料指標的目前位置，抓取索引項目的索引鍵。 另請參閱 [RetrieveKey (JET_SESID、JET_TABLEID、RetrieveKeyGrbit) ](./api.retrievekey-method.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetRetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveKeyGrbitApi.JetRetrieveKey(sesid, tableid, _
    data, dataSize, actualDataSize, grbit)
```

``` csharp
public static void JetRetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    從中取出索引鍵的資料指標。

<!-- end list -->

  - data  
    類型： \[\]  
    
    要在其中取出索引鍵的緩衝區。

<!-- end list -->

  - dataSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    緩衝區的大小。

<!-- end list -->

  - actualDataSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    傳回資料的實際大小。

<!-- end list -->

  - grbit  
    型別： [RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md) 。  
    
    取得索引鍵選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
