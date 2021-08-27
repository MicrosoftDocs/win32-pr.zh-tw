---
description: 深入瞭解： JET_COMMIT_ID CompareTo 方法
title: " (CompareTo 方法) 的 JET_COMMIT_ID. Windows8"
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.compareto(v=EXCHG.10)
ms:contentKeyID: 55104397
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a101cd38eb80598f907068d8fd27d2217ad73db1476dc41d42b2a6caaae3e6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766896"
---
# <a name="jet_commit_idcompareto-method"></a>JET_COMMIT_ID CompareTo 方法

傳回值，這個值會比較這個實例與另一個實例。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COMMIT_ID _
) As Integer
'Usage
Dim instance As JET_COMMIT_ID
Dim other As JET_COMMIT_ID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COMMIT_ID other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

類型： [system.object](/dotnet/api/system.int32)  
代表實例之相對位置的帶正負號值。  

#### <a name="implements"></a>實作

[IComparable \<T\> 。CompareTo (T) ](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COMMIT_ID 類別](./jet-commit-id-class.md)

[JET_COMMIT_ID 成員](./jet-commit-id-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
