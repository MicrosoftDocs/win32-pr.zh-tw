---
description: 深入瞭解： InstanceParameters. MaxVerPages 屬性
title: InstanceParameters. MaxVerPages 屬性
TOCTitle: 'MaxVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxverpages(v=EXCHG.10)
ms:contentKeyID: 55103318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxVerPages
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ce33867409725a017ee5e80a936e40ecdb0c280f37d92718412d97502002452
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039376"
---
# <a name="instanceparametersmaxverpages-property"></a>InstanceParameters. MaxVerPages 屬性

取得或設定保留給此實例的版本存放區頁面數目上限。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property MaxVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxVerPages

instance.MaxVerPages = value
```

``` csharp
public int MaxVerPages { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
