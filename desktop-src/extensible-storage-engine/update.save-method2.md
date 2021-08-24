---
description: 深入瞭解： Update. Save 方法
title: 更新. 儲存方法
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75927144f887ab5cd7dbfe05c6d8fbf4c690a0e29786c1834fa00f8e29fae76c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890059"
---
# <a name="updatesave-method"></a>更新. 儲存方法

更新 tableid。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a>備註

[儲存] 是執行插入或更新的最後一個步驟。 更新的開始方式是呼叫建立更新物件，然後呼叫 JetSetColumn 或 JetSetColumns 一或多次來設定記錄狀態。 最後，會呼叫 Update 來完成更新作業。 索引只有在 Update 或 JetSetColumn 或 JetSetColumns 期間才會更新。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Update 類別](./update-class.md)

[更新成員](./update-members.md)

[儲存多載](./update.save-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
