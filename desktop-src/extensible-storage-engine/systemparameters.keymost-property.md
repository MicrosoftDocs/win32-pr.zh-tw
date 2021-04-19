---
description: 深入瞭解： SystemParameters. KeyMost 屬性
title: SystemParameters. KeyMost 屬性
TOCTitle: 'KeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.KeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.keymost(v=EXCHG.10)
ms:contentKeyID: 55104043
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.KeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_KeyMost
- Microsoft.Isam.Esent.Interop.SystemParameters.KeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f211e6d5a93679c49ae26e08152190d105f05ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983843"
---
# <a name="systemparameterskeymost-property"></a>SystemParameters. KeyMost 屬性

取得最大索引鍵大小。 這取決於 Esent 版本和資料庫頁面大小。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared ReadOnly Property KeyMost As Integer
    Get
'Usage
Dim value As Integer

value = SystemParameters.KeyMost
```

``` csharp
public static int KeyMost { get; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[SystemParameters 類別](./systemparameters-class.md)

[SystemParameters 成員](./systemparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
