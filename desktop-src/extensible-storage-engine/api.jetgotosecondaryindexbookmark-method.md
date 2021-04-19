---
description: 深入瞭解： JetGotoSecondaryIndexBookmark 方法
title: JetGotoSecondaryIndexBookmark 方法
TOCTitle: 'JetGotoSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotosecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100755
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af146236a2a5398dfb0b7b81f42dcfc6227a6de9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980058"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a>JetGotoSecondaryIndexBookmark 方法

將游標放置在與指定次要索引書簽相關聯的索引項目目。 次要索引書簽必須與原始抓取的相同資料表上的相同索引一起使用。 您可以使用 JetGotoSecondaryIndexBookmark (JET_SESID、JET_TABLEID、 \[ \] 、int32、 \[ \] 、int32、GotoSecondaryIndexBookmarkGrbit) ，來抓取索引項目的次要索引書簽。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetGotoSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    grbit As GotoSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim grbit As GotoSecondaryIndexBookmarkGrbitApi.JetGotoSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    primaryKey, primaryKeySize, grbit)
```

``` csharp
public static void JetGotoSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    GotoSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要放置的資料表資料指標。

<!-- end list -->

  - secondaryKey  
    類型： \[\]  
    
    包含次要索引鍵的緩衝區。

<!-- end list -->

  - secondaryKeySize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    次要索引鍵的大小。

<!-- end list -->

  - primaryKey  
    類型： \[\]  
    
    包含主要索引鍵的緩衝區。

<!-- end list -->

  - primaryKeySize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    主要索引鍵的大小。

<!-- end list -->

  - grbit  
    型別： [GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md) 。  
    
    用於定位書簽的選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
