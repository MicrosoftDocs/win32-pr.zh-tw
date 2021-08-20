---
description: 深入瞭解： InstanceParameters. CachePriority 屬性
title: InstanceParameters. CachePriority 屬性
TOCTitle: 'CachePriority property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CachePriority
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cachepriority(v=EXCHG.10)
ms:contentKeyID: 55107435
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachePriority
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachePriority
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CachePriority
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CachePriority
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b8b5664c55963c5c702c25f0250a472ec4df3d71105f23bd13d173e7252a4b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117895647"
---
# <a name="instanceparameterscachepriority-property"></a>InstanceParameters. CachePriority 屬性

取得或設定相對快取優先權 (預設 = 100) 的每個實例屬性。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property CachePriority As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CachePriority

instance.CachePriority = value
```

``` csharp
public int CachePriority { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
