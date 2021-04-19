---
description: 深入瞭解： InstanceParameters. MaxCursors 屬性
title: InstanceParameters. MaxCursors 屬性
TOCTitle: 'MaxCursors property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxcursors(v=EXCHG.10)
ms:contentKeyID: 55103565
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxCursors
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 029ff7c41916e668f532be60f018870f30e487ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992105"
---
# <a name="instanceparametersmaxcursors-property"></a>InstanceParameters. MaxCursors 屬性

取得或設定保留給這個實例的資料指標資源數目。 資料指標資源會直接對應至 JET_TABLEID。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property MaxCursors As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxCursors

instance.MaxCursors = value
```

``` csharp
public int MaxCursors { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
