---
description: 深入瞭解： JetGetBookmark 方法
title: JetGetBookmark 方法
TOCTitle: 'JetGetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetbookmark(v=EXCHG.10)
ms:contentKeyID: 55100702
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0eaac3c0c92fa9d6cfa1a5bca660791b81efe5ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973236"
---
# <a name="apijetgetbookmark-method"></a>JetGetBookmark 方法

抓取與資料指標目前位置的索引項目目相關聯之記錄的書簽。 然後，您可以使用[JetGotoBookmark (JET_SESID、JET_TABLEID、 \[ \] Int32) ](./api.jetgotobookmark-method.md)，利用這個書簽將該資料指標重新置放回相同記錄。 書簽將不再超過 [BookmarkMost](./systemparameters.bookmarkmost-property.md) 個位元組。 另請參閱 [GetBookmark (JET_SESID JET_TABLEID) ](./api.getbookmark-method.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetGetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetGetBookmark(sesid, tableid, _
    bookmark, bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetGetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要從中取出書簽的資料指標。

<!-- end list -->

  - 書籤 (bookmark)  
    類型： \[\]  
    
    包含書簽的緩衝區。

<!-- end list -->

  - bookmarkSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    書簽緩衝區的大小。

<!-- end list -->

  - actualBookmarkSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    傳回書簽的實際大小。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
