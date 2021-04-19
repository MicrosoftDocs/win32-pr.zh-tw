---
description: 深入瞭解： JET_INSTANCE。GetHashCode 方法
title: JET_INSTANCE。GetHashCode 方法
TOCTitle: 'GetHashCode method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.GetHashCode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.gethashcode(v=EXCHG.10)
ms:contentKeyID: 39512476
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.GetHashCode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.GetHashCode
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c622424acc691dfe6a4611c5e1525bcef942189f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994402"
---
# <a name="jet_instancegethashcode-method"></a>JET_INSTANCE。GetHashCode 方法

傳回這個執行個體的雜湊碼。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Overrides Function GetHashCode As Integer
'Usage
Dim instance As JET_INSTANCE
Dim returnValue As Integer

returnValue = instance.GetHashCode()
```

``` csharp
public override int GetHashCode()
```

#### <a name="return-value"></a>傳回值

類型： [system.object](/dotnet/api/system.int32)  
這個執行個體的雜湊碼。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INSTANCE 結構](./jet-instance-structure.md)

[JET_INSTANCE 成員](./jet-instance-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
