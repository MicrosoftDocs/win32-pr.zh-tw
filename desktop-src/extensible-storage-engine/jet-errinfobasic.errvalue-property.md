---
description: 深入瞭解： JET_ERRINFOBASIC errValue 屬性
title: ErrValue 屬性 (Windows8) 的 JET_ERRINFOBASIC。
TOCTitle: 'errValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.errValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errinfobasic.errvalue(v=EXCHG.10)
ms:contentKeyID: 55104309
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.errValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.errValue
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.set_errValue
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.get_errValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4ecdc72c98494e84e11baad5d4df8d868448576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849553"
---
# <a name="jet_errinfobasicerrvalue-property"></a>JET_ERRINFOBASIC errValue 屬性

取得或設定要求的資訊層級的錯誤值。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property errValue As JET_err
    Get
    Set
'Usage
Dim instance As JET_ERRINFOBASIC
Dim value As JET_err

value = instance.errValue

instance.errValue = value
```

``` csharp
public JET_err errValue { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_ERRINFOBASIC 類別](./jet-errinfobasic-class.md)

[JET_ERRINFOBASIC 成員](./jet-errinfobasic-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
