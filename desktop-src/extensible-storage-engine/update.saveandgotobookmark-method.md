---
description: 深入瞭解： SaveAndGotoBookmark 方法
title: SaveAndGotoBookmark 方法
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 566be9b1af403a794b6ac87259a0fd6b6c0fea46c0b45287c536f336ee734b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106952"
---
# <a name="updatesaveandgotobookmark-method"></a>SaveAndGotoBookmark 方法

更新 tableid，並將 tableid 放在修改過的記錄上。 這在插入記錄時很有用，因為 tableid 預設會保留在舊的位置。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a>備註

[儲存] 是執行插入或更新的最後一個步驟。 更新的開始方式是呼叫建立更新物件，然後呼叫 JetSetColumn 或 JetSetColumns 一或多次來設定記錄狀態。 最後，會呼叫 Update 來完成更新作業。 索引只有在 Update 或 JetSetColumn 或 JetSetColumns 期間才會更新。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Update 類別](./update-class.md)

[更新成員](./update-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
