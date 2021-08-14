---
description: 深入瞭解： SystemParameters. ExceptionAction 屬性
title: SystemParameters. ExceptionAction 屬性
TOCTitle: 'ExceptionAction property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.ExceptionAction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.exceptionaction(v=EXCHG.10)
ms:contentKeyID: 55104042
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.ExceptionAction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.ExceptionAction
- Microsoft.Isam.Esent.Interop.SystemParameters.get_ExceptionAction
- Microsoft.Isam.Esent.Interop.SystemParameters.set_ExceptionAction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 217942d9827a715858c76a704092259a5c3df25f98bf4eac7d5835450f502e3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484894"
---
# <a name="systemparametersexceptionaction-property"></a>SystemParameters. ExceptionAction 屬性

取得或設定在 JET 內產生之例外狀況的編碼方式。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property ExceptionAction As JET_ExceptionAction
    Get
    Set
'Usage
Dim value As JET_ExceptionAction

value = SystemParameters.ExceptionAction

SystemParameters.ExceptionAction = value
```

``` csharp
public static JET_ExceptionAction ExceptionAction { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_ExceptionAction](./jet-exceptionaction-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[SystemParameters 類別](./systemparameters-class.md)

[SystemParameters 成員](./systemparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
