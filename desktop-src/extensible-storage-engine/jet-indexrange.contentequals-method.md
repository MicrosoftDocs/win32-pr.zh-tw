---
description: 深入瞭解： JET_INDEXRANGE。ContentEquals 方法
title: JET_INDEXRANGE。ContentEquals 方法
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_INDEXRANGE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexrange.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXRANGE.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8934ed14339c24348199fe50b09bbf2da3e94207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193827"
---
# <a name="jet_indexrangecontentequals-method"></a>JET_INDEXRANGE。ContentEquals 方法

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_INDEXRANGE _
) As Boolean
'Usage
Dim instance As JET_INDEXRANGE
Dim other As JET_INDEXRANGE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_INDEXRANGE other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_INDEXRANGE](./jet-indexrange-class.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IContentEquatable \<T\> 。ContentEquals (T) ](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXRANGE 類別](./jet-indexrange-class.md)

[JET_INDEXRANGE 成員](./jet-indexrange-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
