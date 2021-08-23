---
description: 深入瞭解： InstanceParameters. PrereadIOMax 屬性
title: InstanceParameters. PrereadIOMax 屬性
TOCTitle: 'PrereadIOMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PrereadIOMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.prereadiomax(v=EXCHG.10)
ms:contentKeyID: 55103559
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PrereadIOMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PrereadIOMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PrereadIOMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PrereadIOMax
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc3af75d137b07df729d987ac4942612ac88aded08d546378b89146d5ae121ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617928"
---
# <a name="instanceparametersprereadiomax-property"></a>InstanceParameters. PrereadIOMax 屬性

取得或設定針對指定用途分派的 i/o 作業數目上限。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property PrereadIOMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PrereadIOMax

instance.PrereadIOMax = value
```

``` csharp
public int PrereadIOMax { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
