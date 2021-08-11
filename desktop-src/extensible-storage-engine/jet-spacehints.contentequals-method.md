---
description: 深入瞭解： JET_SPACEHINTS。ContentEquals 方法
title: JET_SPACEHINTS。ContentEquals 方法
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ContentEquals(Microsoft.Isam.Esent.Interop.JET_SPACEHINTS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103958
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d24676244a49fd884238072bb139b1d01b7cfd8cfbbd2a464dc470de949a434f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252225"
---
# <a name="jet_spacehintscontentequals-method"></a>JET_SPACEHINTS。ContentEquals 方法

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_SPACEHINTS _
) As Boolean
'Usage
Dim instance As JET_SPACEHINTS
Dim other As JET_SPACEHINTS
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_SPACEHINTS other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_SPACEHINTS](./jet-spacehints-class.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IContentEquatable \<T\> 。ContentEquals (T) ](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SPACEHINTS 類別](./jet-spacehints-class.md)

[JET_SPACEHINTS 成員](./jet-spacehints-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
