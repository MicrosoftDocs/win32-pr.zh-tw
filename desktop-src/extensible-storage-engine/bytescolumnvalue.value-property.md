---
description: 深入瞭解： BytesColumnValue。 Value 屬性
title: BytesColumnValue。 Value 屬性
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55107249
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Value
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0804a7a05640336be77e5f446ad99227db592f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996875"
---
# <a name="bytescolumnvaluevalue-property"></a>BytesColumnValue。 Value 屬性

取得或設定資料行的值。 使用[SetColumns (JET_SESID、JET_TABLEID \[ \]) ](./api.setcolumns-method.md)來更新具有資料行值的記錄。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property Value As Byte()
    Get
    Set
'Usage
Dim instance As BytesColumnValue
Dim value As Byte()

value = instance.Value

instance.Value = value
```

``` csharp
public byte[] Value { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[BytesColumnValue 類別](./bytescolumnvalue-class.md)

[BytesColumnValue 成員](./bytescolumnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
