---
description: 深入瞭解： InstanceParameters 修復屬性
title: InstanceParameters 修復屬性
TOCTitle: 'Recovery property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.Recovery
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.recovery(v=EXCHG.10)
ms:contentKeyID: 55103323
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.Recovery
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_Recovery
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_Recovery
- Microsoft.Isam.Esent.Interop.InstanceParameters.Recovery
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3849e7629cea54cf13caace0691288d24335f3aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320975"
---
# <a name="instanceparametersrecovery-property"></a>InstanceParameters 修復屬性

取得或設定值，指出是否開啟損毀復原。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property Recovery As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.Recovery

instance.Recovery = value
```

``` csharp
public bool Recovery { get; set; }
```

#### <a name="property-value"></a>屬性值

型別： [system.object](/dotnet/api/system.boolean)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
