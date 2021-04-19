---
description: 深入瞭解： JET_SETCOLUMN columnid 屬性
title: JET_SETCOLUMN columnid 屬性
TOCTitle: 'columnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.columnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.columnid(v=EXCHG.10)
ms:contentKeyID: 55107683
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.columnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_columnid
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_columnid
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.columnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a899e81b5dcc4386f8262a371206d7c361911be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967100"
---
# <a name="jet_setcolumncolumnid-property"></a>JET_SETCOLUMN columnid 屬性

取得或設定要設定之資料行的資料行識別碼。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnid As JET_COLUMNID
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As JET_COLUMNID

value = instance.columnid

instance.columnid = value
```

``` csharp
public JET_COLUMNID columnid { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SETCOLUMN 類別](./jet-setcolumn-class.md)

[JET_SETCOLUMN 成員](./jet-setcolumn-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
