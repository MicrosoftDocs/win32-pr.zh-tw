---
description: 深入瞭解： JET_ERRINFOBASIC。ContentEquals 方法
title: JET_ERRINFOBASIC。Windows8) 的 ContentEquals 方法 (
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.ContentEquals(Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errinfobasic.contentequals(v=EXCHG.10)
ms:contentKeyID: 55104306
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b86417db68b6e538e9a3a5ab4300a5f31fb0a2138d7158490c18d5877009c422
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119362408"
---
# <a name="jet_errinfobasiccontentequals-method"></a>JET_ERRINFOBASIC。ContentEquals 方法

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_ERRINFOBASIC _
) As Boolean
'Usage
Dim instance As JET_ERRINFOBASIC
Dim other As JET_ERRINFOBASIC
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_ERRINFOBASIC other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IContentEquatable \<T\> 。ContentEquals (T) ](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_ERRINFOBASIC 類別](./jet-errinfobasic-class.md)

[JET_ERRINFOBASIC 成員](./jet-errinfobasic-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
