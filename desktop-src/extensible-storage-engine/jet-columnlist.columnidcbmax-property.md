---
description: 深入瞭解： JET_COLUMNLIST columnidcbMax 屬性
title: JET_COLUMNLIST columnidcbMax 屬性
TOCTitle: 'columnidcbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.columnidcbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnlist.columnidcbmax(v=EXCHG.10)
ms:contentKeyID: 55103518
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.columnidcbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.get_columnidcbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.set_columnidcbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.columnidcbMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 956b0ec5dd51a56e7acc752339cc98aea1a76e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320511"
---
# <a name="jet_columnlistcolumnidcbmax-property"></a>JET_COLUMNLIST columnidcbMax 屬性

取得臨時表中的資料行 columnid，其中儲存資料行的最大長度。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidcbMax As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNLIST
Dim value As JET_COLUMNID

value = instance.columnidcbMax
```

``` csharp
public JET_COLUMNID columnidcbMax { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COLUMNLIST 類別](./jet-columnlist-class.md)

[JET_COLUMNLIST 成員](./jet-columnlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
