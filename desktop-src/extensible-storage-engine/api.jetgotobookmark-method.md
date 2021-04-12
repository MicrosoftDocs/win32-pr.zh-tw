---
description: 深入瞭解： JetGotoBookmark 方法
title: JetGotoBookmark 方法
TOCTitle: 'JetGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55100753
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 362a174e3da4dad864fd504e1678b4a3a1477e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514129"
---
# <a name="apijetgotobookmark-method"></a>JetGotoBookmark 方法

將游標放置在與指定書簽相關聯之記錄的索引項目目。 書簽可以搭配資料表上定義的任何索引使用。 您可以使用[JetGetBookmark (JET_SESID、JET_TABLEID、 \[ \] 、int32、int32) ](./api.jetgetbookmark-method.md)來取出記錄的書簽。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetGotoBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As IntegerApi.JetGotoBookmark(sesid, tableid, _
    bookmark, bookmarkSize)
```

``` csharp
public static void JetGotoBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize
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

  - 書籤 (bookmark)  
    類型： \[\]  
    
    用來定位游標的書簽。

<!-- end list -->

  - bookmarkSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    書簽的大小。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
