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
ms.openlocfilehash: 900a29f9304f869712cd72fd51926fd15a030dca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981888"
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
