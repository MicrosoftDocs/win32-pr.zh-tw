---
description: 深入瞭解： JetSeek 方法
title: JetSeek 方法
TOCTitle: 'JetSeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetseek(v=EXCHG.10)
ms:contentKeyID: 55100796
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 088a8a8e1fdf968a6a970658257bace3ab42ab65a04a7b39c7a4c57bda6f3741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118783801"
---
# <a name="apijetseek-method"></a>JetSeek 方法

有效率地將游標放在索引項目目，以符合該資料指標中的搜尋索引鍵所指定的搜尋條件，以及指定的不相等。 您先前必須使用[JetMakeKey (JET_SESID、JET_TABLEID、 \[ \] 、Int32、MakeKeyGrbit) ](./api.jetmakekey-method.md)來建立搜尋索引鍵。 另請參閱 [TrySeek (JET_SESID、JET_TABLEID、SeekGrbit) ](./api.tryseek-method.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Function JetSeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetSeek(sesid, _
    tableid, grbit)
```

``` csharp
public static JET_wrn JetSeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要放置的游標。

<!-- end list -->

  - grbit  
    型別： [SeekGrbit](./seekgrbit-enumeration.md) 。  
    
    搜尋選項。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
ESENT 警告。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
