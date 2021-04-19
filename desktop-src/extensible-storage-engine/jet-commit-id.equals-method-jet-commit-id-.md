---
description: '深入瞭解： JET_COMMIT_ID Equals 方法 (JET_COMMIT_ID) '
title: 'JET_COMMIT_ID. Equals 方法 (JET_COMMIT_ID)  (Windows8) '
TOCTitle: Equals method (JET_COMMIT_ID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Equals(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.equals(v=EXCHG.10)
ms:contentKeyID: 55104294
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c833b137b1e5df9f6d70e206b2f517977375e29b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998527"
---
# <a name="jet_commit_idequals-method-jet_commit_id"></a>JET_COMMIT_ID Equals 方法 (JET_COMMIT_ID) 

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function Equals ( _
    other As JET_COMMIT_ID _
) As Boolean
'Usage
Dim instance As JET_COMMIT_ID
Dim other As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_COMMIT_ID other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    與這個執行個體相互比較的物件。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 true。  

#### <a name="implements"></a>實作

[IEquatable \<T\> 。等於 (T) ](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COMMIT_ID 類別](./jet-commit-id-class.md)

[JET_COMMIT_ID 成員](./jet-commit-id-members.md)

[等於多載](./jet-commit-id.equals-method.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
