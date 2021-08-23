---
description: 深入瞭解： InstanceParameters. MaxOpenTables 屬性
title: InstanceParameters. MaxOpenTables 屬性
TOCTitle: 'MaxOpenTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxopentables(v=EXCHG.10)
ms:contentKeyID: 55107442
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxOpenTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxOpenTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30129e66a05116bfaab28fe737584c89b8b74fb0c8722b3d772c643f5165cffe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039386"
---
# <a name="instanceparametersmaxopentables-property"></a>InstanceParameters. MaxOpenTables 屬性

取得或設定保留給此實例的 B + 樹系資源數目。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property MaxOpenTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxOpenTables

instance.MaxOpenTables = value
```

``` csharp
public int MaxOpenTables { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
