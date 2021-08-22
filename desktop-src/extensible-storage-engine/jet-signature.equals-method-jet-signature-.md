---
description: '深入瞭解： JET_SIGNATURE。Equals 方法 (JET_SIGNATURE) '
title: 'JET_SIGNATURE。Equals 方法 (JET_SIGNATURE) '
TOCTitle: Equals method (JET_SIGNATURE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equals(Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.equals(v=EXCHG.10)
ms:contentKeyID: 39511830
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb7b1bb73c611ce65d0c2d07059eb14e7ceba6b59b648c474bd753988d7b9232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616138"
---
# <a name="jet_signatureequals-method-jet_signature"></a>JET_SIGNATURE。Equals 方法 (JET_SIGNATURE) 

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function Equals ( _
    other As JET_SIGNATURE _
) As Boolean
'Usage
Dim instance As JET_SIGNATURE
Dim other As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_SIGNATURE other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IEquatable \<T\> 。等於 (T) ](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SIGNATURE 結構](./jet-signature-structure2.md)

[JET_SIGNATURE 成員](./jet-signature-members.md)

[等於多載](./jet-signature.equals-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
