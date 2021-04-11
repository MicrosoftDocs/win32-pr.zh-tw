---
description: 深入瞭解： JET_COLUMNBASE 的 cp 屬性
title: JET_COLUMNBASE cp 屬性
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.cp(v=EXCHG.10)
ms:contentKeyID: 55103468
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8928ba3ae46283f856359b36d8f7c4c12f5891b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027556"
---
# <a name="jet_columnbasecp-property"></a>JET_COLUMNBASE cp 屬性

取得資料行的字碼頁。 只有 [Text](./jet-coltyp-enumeration.md) 和 [LongText](./jet-coltyp-enumeration.md)類型的資料行才有意義。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As JET_CP

value = instance.cp
```

``` csharp
public JET_CP cp { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COLUMNBASE 類別](./jet-columnbase-class.md)

[JET_COLUMNBASE 成員](./jet-columnbase-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
