---
description: 深入瞭解： SystemParameters. HungIOActions 屬性
title: SystemParameters. HungIOActions 屬性
TOCTitle: 'HungIOActions property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.HungIOActions
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.hungioactions(v=EXCHG.10)
ms:contentKeyID: 55104126
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.HungIOActions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_HungIOActions
- Microsoft.Isam.Esent.Interop.SystemParameters.HungIOActions
- Microsoft.Isam.Esent.Interop.SystemParameters.set_HungIOActions
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a2e1acd3d7fe377ad352a5b98569207cbd5110034e5dca5beaa28cedc39b4c26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603628"
---
# <a name="systemparametershungioactions-property"></a>SystemParameters. HungIOActions 屬性

取得或設定要在出現無回應的 IOs 上執行的動作集合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property HungIOActions As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.HungIOActions

SystemParameters.HungIOActions = value
```

``` csharp
public static int HungIOActions { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[SystemParameters 類別](./systemparameters-class.md)

[SystemParameters 成員](./systemparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
