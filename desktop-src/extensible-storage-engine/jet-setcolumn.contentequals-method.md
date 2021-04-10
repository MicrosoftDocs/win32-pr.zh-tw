---
description: 深入瞭解： JET_SETCOLUMN。ContentEquals 方法
title: JET_SETCOLUMN。ContentEquals 方法
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ContentEquals(Microsoft.Isam.Esent.Interop.JET_SETCOLUMN)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103936
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 489d42a72033ba942a359d8f3244b154dae9e3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026131"
---
# <a name="jet_setcolumncontentequals-method"></a>JET_SETCOLUMN。ContentEquals 方法

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_SETCOLUMN _
) As Boolean
'Usage
Dim instance As JET_SETCOLUMN
Dim other As JET_SETCOLUMN
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_SETCOLUMN other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_SETCOLUMN](./jet-setcolumn-class.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IContentEquatable \<T\> 。ContentEquals (T) ](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SETCOLUMN 類別](./jet-setcolumn-class.md)

[JET_SETCOLUMN 成員](./jet-setcolumn-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
