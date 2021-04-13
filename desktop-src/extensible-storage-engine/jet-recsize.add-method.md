---
description: 深入瞭解： JET_RECSIZE。新增方法
title: 'JET_RECSIZE。將方法新增 (的 < a0/&gt; < a1/&gt;) '
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.add(v=EXCHG.10)
ms:contentKeyID: 39509872
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e12a78a0a32bcca02afec100b0b238f4444a6ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510936"
---
# <a name="jet_recsizeadd-method"></a>JET_RECSIZE。新增方法

將大小新增至兩個 JET_RECSIZE 結構。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Function Add ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Add(s1, s2)
```

``` csharp
public static JET_RECSIZE Add(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a>參數

  - s1  
    類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    第一個 JET_RECSIZE。

<!-- end list -->

  - s2  
    類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    第二個 JET_RECSIZE。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
JET_RECSIZE，其中包含在 s1 和 s2 中新增大小的結果。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RECSIZE 結構](./jet-recsize-structure2.md)

[JET_RECSIZE 成員](./jet-recsize-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
