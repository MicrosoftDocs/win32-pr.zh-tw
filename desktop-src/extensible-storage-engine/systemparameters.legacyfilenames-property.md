---
description: 深入瞭解： SystemParameters. LegacyFileNames 屬性
title: SystemParameters. LegacyFileNames 屬性
TOCTitle: 'LegacyFileNames property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.LegacyFileNames
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.legacyfilenames(v=EXCHG.10)
ms:contentKeyID: 55104128
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.LegacyFileNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_LegacyFileNames
- Microsoft.Isam.Esent.Interop.SystemParameters.LegacyFileNames
- Microsoft.Isam.Esent.Interop.SystemParameters.set_LegacyFileNames
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73739bda83f83eddbbfa090925b873d78aaeaa1dcdbcce9c527e5467f0f0acf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015951"
---
# <a name="systemparameterslegacyfilenames-property"></a>SystemParameters. LegacyFileNames 屬性

取得或設定與舊版資料庫引擎的檔案命名慣例的回溯相容性。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property LegacyFileNames As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.LegacyFileNames

SystemParameters.LegacyFileNames = value
```

``` csharp
public static int LegacyFileNames { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[SystemParameters 類別](./systemparameters-class.md)

[SystemParameters 成員](./systemparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
