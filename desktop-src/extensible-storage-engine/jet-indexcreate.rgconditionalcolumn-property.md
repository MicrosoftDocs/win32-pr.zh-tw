---
description: 深入瞭解： JET_INDEXCREATE rgconditionalcolumn 屬性
title: JET_INDEXCREATE rgconditionalcolumn 屬性
TOCTitle: 'rgconditionalcolumn property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.rgconditionalcolumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.rgconditionalcolumn(v=EXCHG.10)
ms:contentKeyID: 55103653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.rgconditionalcolumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_rgconditionalcolumn
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_rgconditionalcolumn
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.rgconditionalcolumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a77ff7d1ee2286ac7b0f2cb295c6d493823cb63deb93510a5c389349217593e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016968"
---
# <a name="jet_indexcreatergconditionalcolumn-property"></a>JET_INDEXCREATE rgconditionalcolumn 屬性

取得或設定選擇性的條件式資料行。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property rgconditionalcolumn As JET_CONDITIONALCOLUMN()
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As JET_CONDITIONALCOLUMN()

value = instance.rgconditionalcolumn

instance.rgconditionalcolumn = value
```

``` csharp
public JET_CONDITIONALCOLUMN[] rgconditionalcolumn { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXCREATE 類別](./jet-indexcreate-class.md)

[JET_INDEXCREATE 成員](./jet-indexcreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
