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
ms.openlocfilehash: b10bb1a235fad4e88a716dd9baf8ea836117344c84a2ac91ec6de16e2b7ae1c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119360118"
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
