---
description: 深入瞭解： JET_TABLECREATE grbit 屬性
title: JET_TABLECREATE grbit 屬性
TOCTitle: 'grbit property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.grbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.grbit(v=EXCHG.10)
ms:contentKeyID: 55103963
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.grbit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_grbit
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.grbit
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_grbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc18b415ef168d982f5b00b272a665842f7eb77d9c37d1803906250bdf9fa82b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115848"
---
# <a name="jet_tablecreategrbit-property"></a>JET_TABLECREATE grbit 屬性

取得或設定資料表選項。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property grbit As CreateTableColumnIndexGrbit
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As CreateTableColumnIndexGrbit

value = instance.grbit

instance.grbit = value
```

``` csharp
public CreateTableColumnIndexGrbit grbit { get; set; }
```

#### <a name="property-value"></a>屬性值

型別： [CreateTableColumnIndexGrbit](./createtablecolumnindexgrbit-enumeration.md) 。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_TABLECREATE 類別](./jet-tablecreate-class.md)

[JET_TABLECREATE 成員](./jet-tablecreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
