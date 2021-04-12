---
description: 深入瞭解： SystemParameters. EnableFileCache 屬性
title: SystemParameters. EnableFileCache 屬性
TOCTitle: 'EnableFileCache property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableFileCache
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enablefilecache(v=EXCHG.10)
ms:contentKeyID: 55104039
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableFileCache
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableFileCache
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableFileCache
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableFileCache
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a0714931860cf8dcce767995f9766bb5440743e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193023"
---
# <a name="systemparametersenablefilecache-property"></a>SystemParameters. EnableFileCache 屬性

取得或設定值，這個值表示資料庫引擎是否應使用所有 managed 檔案的 OS 檔案快取。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property EnableFileCache As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableFileCache

SystemParameters.EnableFileCache = value
```

``` csharp
public static bool EnableFileCache { get; set; }
```

#### <a name="property-value"></a>屬性值

型別： [system.object](/dotnet/api/system.boolean)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[SystemParameters 類別](./systemparameters-class.md)

[SystemParameters 成員](./systemparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
