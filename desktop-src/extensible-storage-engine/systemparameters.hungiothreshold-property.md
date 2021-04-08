---
description: 深入瞭解： SystemParameters. HungIOThreshold 屬性
title: SystemParameters. HungIOThreshold 屬性
TOCTitle: 'HungIOThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.HungIOThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.hungiothreshold(v=EXCHG.10)
ms:contentKeyID: 55104041
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.HungIOThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_HungIOThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.HungIOThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_HungIOThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6118cfb171966798ade924ccf55f0a42af443f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695024"
---
# <a name="systemparametershungiothreshold-property"></a>SystemParameters. HungIOThreshold 屬性

取得或設定視為應採取動作之無反應 IO 的臨界值。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property HungIOThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.HungIOThreshold

SystemParameters.HungIOThreshold = value
```

``` csharp
public static int HungIOThreshold { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[SystemParameters 類別](./systemparameters-class.md)

[SystemParameters 成員](./systemparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
