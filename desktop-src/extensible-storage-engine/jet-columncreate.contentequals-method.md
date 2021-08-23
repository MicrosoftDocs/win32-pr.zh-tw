---
description: 深入瞭解： JET_COLUMNCREATE。ContentEquals 方法
title: JET_COLUMNCREATE。ContentEquals 方法
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103471
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a61917bab1d39df3a3b448a51da8bd40bb055b726f444a9cdb23f30c986f248a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668308"
---
# <a name="jet_columncreatecontentequals-method"></a>JET_COLUMNCREATE。ContentEquals 方法

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_COLUMNCREATE _
) As Boolean
'Usage
Dim instance As JET_COLUMNCREATE
Dim other As JET_COLUMNCREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_COLUMNCREATE other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE](./jet-columncreate-class.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IContentEquatable \<T\> 。ContentEquals (T) ](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COLUMNCREATE 類別](./jet-columncreate-class.md)

[JET_COLUMNCREATE 成員](./jet-columncreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
