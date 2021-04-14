---
description: 深入瞭解： JET_SETINFO ibLongValue 屬性
title: JET_SETINFO ibLongValue 屬性
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103918
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 324b3cd5c45be8f463ff9b2a9cfe11f1dcad4554
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511116"
---
# <a name="jet_setinfoiblongvalue-property"></a>JET_SETINFO ibLongValue 屬性

取得或設定要在 [LongBinary](./jet-coltyp-enumeration.md) 或 [LongText](./jet-coltyp-enumeration.md)類型的資料行中設定之第一個位元組的位移。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
Dim value As Integer

value = instance.ibLongValue

instance.ibLongValue = value
```

``` csharp
public int ibLongValue { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SETINFO 類別](./jet-setinfo-class.md)

[JET_SETINFO 成員](./jet-setinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
