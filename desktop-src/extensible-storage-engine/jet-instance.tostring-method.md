---
description: 深入瞭解： JET_INSTANCE。ToString 方法
title: JET_INSTANCE。ToString 方法
TOCTitle: 'ToString method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.tostring(v=EXCHG.10)
ms:contentKeyID: 39510019
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0945cf6e5c40b1587b6bcae05331d391ab18685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975795"
---
# <a name="jet_instancetostring-method"></a>JET_INSTANCE。ToString 方法

產生結構的字串表示。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Overrides Function ToString As String
'Usage
Dim instance As JET_INSTANCE
Dim returnValue As String

returnValue = instance.ToString()
```

``` csharp
public override string ToString()
```

#### <a name="return-value"></a>傳回值

類型： [system.string](/dotnet/api/system.string)  
字串形式的結構。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INSTANCE 結構](./jet-instance-structure.md)

[JET_INSTANCE 成員](./jet-instance-members.md)

[ToString 多載](./jet-instance.tostring-method2.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
