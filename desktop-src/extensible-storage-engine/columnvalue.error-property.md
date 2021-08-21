---
description: 深入瞭解： ColumnValue。 Error 屬性
title: ColumnValue。 Error 屬性
TOCTitle: 'Error property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Error
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.error(v=EXCHG.10)
ms:contentKeyID: 55101202
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Error
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Error
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Error
- Microsoft.Isam.Esent.Interop.ColumnValue.set_Error
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ffbbb66992ecff218b7fdbd7577e2ffbd9f63694ae41967ebc8240f84ebe3f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042356"
---
# <a name="columnvalueerror-property"></a>ColumnValue。 Error 屬性

取得藉由取得或設定此資料行所產生的警告。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property Error As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As ColumnValue
Dim value As JET_wrn

value = instance.Error
```

``` csharp
public JET_wrn Error { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnValue 類別](./columnvalue-class.md)

[ColumnValue 成員](./columnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
