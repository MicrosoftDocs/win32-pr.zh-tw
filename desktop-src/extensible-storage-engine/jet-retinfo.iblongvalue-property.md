---
description: 深入瞭解： JET_RETINFO ibLongValue 屬性
title: JET_RETINFO ibLongValue 屬性
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103801
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39b2ed312f7db54ff799ce2aa52554349d020dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972448"
---
# <a name="jet_retinfoiblongvalue-property"></a>JET_RETINFO ibLongValue 屬性

取得或設定要從 [LongBinary](./jet-coltyp-enumeration.md)或 [LongText](./jet-coltyp-enumeration.md)類型的資料行中抓取之第一個位元組的位移。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
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

[JET_RETINFO 類別](./jet-retinfo-class.md)

[JET_RETINFO 成員](./jet-retinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
