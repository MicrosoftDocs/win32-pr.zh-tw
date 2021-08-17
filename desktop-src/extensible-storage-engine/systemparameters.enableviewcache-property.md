---
description: 深入瞭解： SystemParameters. EnableViewCache 屬性
title: SystemParameters. EnableViewCache 屬性
TOCTitle: 'EnableViewCache property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableViewCache
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableviewcache(v=EXCHG.10)
ms:contentKeyID: 55104120
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableViewCache
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableViewCache
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableViewCache
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableViewCache
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 271039ad83ce67348cef93101e9f685589ecea51f6881a4d6f1109cc7098e985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107013"
---
# <a name="systemparametersenableviewcache-property"></a>SystemParameters. EnableViewCache 屬性

取得或設定值，這個值表示資料庫引擎是否應針對資料庫檔案使用記憶體對應的檔案 i/o。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property EnableViewCache As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableViewCache

SystemParameters.EnableViewCache = value
```

``` csharp
public static bool EnableViewCache { get; set; }
```

#### <a name="property-value"></a>屬性值

型別： [system.object](/dotnet/api/system.boolean)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[SystemParameters 類別](./systemparameters-class.md)

[SystemParameters 成員](./systemparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
