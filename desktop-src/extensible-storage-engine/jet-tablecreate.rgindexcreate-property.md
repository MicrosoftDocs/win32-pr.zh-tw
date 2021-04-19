---
description: 深入瞭解： JET_TABLECREATE rgindexcreate 屬性
title: JET_TABLECREATE rgindexcreate 屬性
TOCTitle: 'rgindexcreate property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgindexcreate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.rgindexcreate(v=EXCHG.10)
ms:contentKeyID: 55103970
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgindexcreate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgindexcreate
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_rgindexcreate
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_rgindexcreate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 305db4e84c8ac08396217c8278042ab40a846952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979341"
---
# <a name="jet_tablecreatergindexcreate-property"></a>JET_TABLECREATE rgindexcreate 屬性

取得或設定要建立之索引的陣列，其類型為 [JET_INDEXCREATE](./jet-indexcreate-class.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property rgindexcreate As JET_INDEXCREATE()
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As JET_INDEXCREATE()

value = instance.rgindexcreate

instance.rgindexcreate = value
```

``` csharp
public JET_INDEXCREATE[] rgindexcreate { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_TABLECREATE 類別](./jet-tablecreate-class.md)

[JET_TABLECREATE 成員](./jet-tablecreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
