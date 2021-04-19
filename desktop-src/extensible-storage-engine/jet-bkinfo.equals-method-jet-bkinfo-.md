---
description: '深入瞭解： JET_BKINFO。Equals 方法 (JET_BKINFO) '
title: 'JET_BKINFO。Equals 方法 (JET_BKINFO) '
TOCTitle: Equals method (JET_BKINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKINFO.Equals(Microsoft.Isam.Esent.Interop.JET_BKINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo.equals(v=EXCHG.10)
ms:contentKeyID: 39511411
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 632582c08bb5d54e1b022c67925649fe7a68112a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986641"
---
# <a name="jet_bkinfoequals-method-jet_bkinfo"></a>JET_BKINFO。Equals 方法 (JET_BKINFO) 

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function Equals ( _
    other As JET_BKINFO _
) As Boolean
'Usage
Dim instance As JET_BKINFO
Dim other As JET_BKINFO
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_BKINFO other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IEquatable \<T\> 。等於 (T) ](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_BKINFO 結構](./jet-bkinfo-structure2.md)

[JET_BKINFO 成員](./jet-bkinfo-members.md)

[等於多載](./jet-bkinfo.equals-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
