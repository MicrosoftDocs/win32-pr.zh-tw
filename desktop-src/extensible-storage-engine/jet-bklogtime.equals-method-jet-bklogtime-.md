---
description: '深入瞭解： JET_BKLOGTIME。Equals 方法 (JET_BKLOGTIME) '
title: 'JET_BKLOGTIME。Equals 方法 (JET_BKLOGTIME) '
TOCTitle: Equals method (JET_BKLOGTIME)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equals(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.equals(v=EXCHG.10)
ms:contentKeyID: 39516064
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07b9fe3383331aaa91e26589dd0768bbee56869d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512321"
---
# <a name="jet_bklogtimeequals-method-jet_bklogtime"></a>JET_BKLOGTIME。Equals 方法 (JET_BKLOGTIME) 

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function Equals ( _
    other As JET_BKLOGTIME _
) As Boolean
'Usage
Dim instance As JET_BKLOGTIME
Dim other As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_BKLOGTIME other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IEquatable \<T\> 。等於 (T) ](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_BKLOGTIME 結構](./jet-bklogtime-structure2.md)

[JET_BKLOGTIME 成員](./jet-bklogtime-members.md)

[等於多載](./jet-bklogtime.equals-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
