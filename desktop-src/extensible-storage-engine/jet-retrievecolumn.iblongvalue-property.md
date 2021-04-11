---
description: 深入瞭解： JET_RETRIEVECOLUMN ibLongValue 屬性
title: JET_RETRIEVECOLUMN ibLongValue 屬性
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103819
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_ibLongValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbe403553acb3305b538d6f35f837ca7feab97db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113712"
---
# <a name="jet_retrievecolumniblongvalue-property"></a>JET_RETRIEVECOLUMN ibLongValue 屬性

取得或設定要從 [LongBinary](./jet-coltyp-enumeration.md) 或 [LongText](./jet-coltyp-enumeration.md)類型的資料行中抓取之第一個位元組的位移。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
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

[JET_RETRIEVECOLUMN 類別](./jet-retrievecolumn-class.md)

[JET_RETRIEVECOLUMN 成員](./jet-retrievecolumn-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
