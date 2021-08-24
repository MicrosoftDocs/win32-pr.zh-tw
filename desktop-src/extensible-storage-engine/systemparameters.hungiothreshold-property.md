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
ms.openlocfilehash: 587893371aabb6d47e4560c0a8d113ae8e337d5f395b00edbcf32268635d1238
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603583"
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
