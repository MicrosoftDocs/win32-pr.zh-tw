---
description: 深入瞭解： JET_LGPOS CompareTo 方法
title: JET_LGPOS CompareTo 方法
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo(Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.compareto(v=EXCHG.10)
ms:contentKeyID: 39514516
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83012ed755ab876618147c013e99868927e16f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987690"
---
# <a name="jet_lgposcompareto-method"></a>JET_LGPOS CompareTo 方法

將這個記錄檔位置與另一個記錄位置進行比較，並判斷這個實例是否在另一個實例之前、相同的或之後。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_LGPOS _
) As Integer
'Usage
Dim instance As JET_LGPOS
Dim other As JET_LGPOS
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_LGPOS other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    要與目前實例比較的記錄檔位置。

#### <a name="return-value"></a>傳回值

類型： [system.object](/dotnet/api/system.int32)  
帶正負號的數位，指出這個實例和值參數的相對位置。  

#### <a name="implements"></a>實作

[IComparable \<T\> 。CompareTo (T) ](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_LGPOS 結構](./jet-lgpos-structure2.md)

[JET_LGPOS 成員](./jet-lgpos-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
