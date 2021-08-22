---
description: '深入瞭解： Update。 Save 方法 (Byte，Int32，Int32) '
title: 'Update。 Save 方法 (Byte，Int32，Int32) '
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e586177075a34f3832486a9ace4a919abaad65dad21c0e54eba47b79f207be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603538"
---
# <a name="updatesave-method-byte--int32-int32"></a>Update。 Save 方法 (Byte，Int32，Int32) 

更新 tableid。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>參數

  - 書籤 (bookmark)  
    類型： \[\]  
    
    傳回已更新之記錄的書簽。 這個可以是 null。

<!-- end list -->

  - bookmarkSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    書簽緩衝區的大小。

<!-- end list -->

  - actualBookmarkSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    傳回書簽的實際大小。

## <a name="remarks"></a>備註

[儲存] 是執行插入或更新的最後一個步驟。 更新的開始方式是呼叫建立更新物件，然後呼叫 JetSetColumn 或 JetSetColumns 一或多次來設定記錄狀態。 最後，會呼叫 Update 來完成更新作業。 索引只有在 Update 或 JetSetColumn 或 JetSetColumns 期間才會更新。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Update 類別](./update-class.md)

[更新成員](./update-members.md)

[儲存多載](./update.save-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
