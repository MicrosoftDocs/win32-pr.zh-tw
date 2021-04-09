---
description: 深入瞭解： EsentVersion. SupportsUnicodePaths 屬性
title: EsentVersion. SupportsUnicodePaths 屬性
TOCTitle: 'SupportsUnicodePaths property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentVersion.SupportsUnicodePaths
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversion.supportsunicodepaths(v=EXCHG.10)
ms:contentKeyID: 55103182
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsUnicodePaths
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersion.get_SupportsUnicodePaths
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsUnicodePaths
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af001881acb516c5c2ce100f8d4cf490ba49d546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692600"
---
# <a name="esentversionsupportsunicodepaths-property"></a>EsentVersion. SupportsUnicodePaths 屬性

取得值，這個值表示目前的 ESENT 版本是否可以使用非 ASCII 路徑來存取資料庫。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared ReadOnly Property SupportsUnicodePaths As Boolean
    Get
'Usage
Dim value As Boolean

value = EsentVersion.SupportsUnicodePaths
```

``` csharp
public static bool SupportsUnicodePaths { get; }
```

#### <a name="property-value"></a>屬性值

型別： [system.object](/dotnet/api/system.boolean)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentVersion 類別](./esentversion-class.md)

[EsentVersion 成員](./esentversion-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
