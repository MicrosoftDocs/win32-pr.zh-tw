---
description: 深入瞭解： JET_RETRIEVECOLUMN columnidNextTagged 屬性
title: JET_RETRIEVECOLUMN columnidNextTagged 屬性
TOCTitle: 'columnidNextTagged property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.columnidNextTagged
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.columnidnexttagged(v=EXCHG.10)
ms:contentKeyID: 55103812
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.columnidNextTagged
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_columnidNextTagged
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d0c1eb962a1b0768aeb0c7fea04c418a57d52061aa05d97b4bc796470ab92d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473508"
---
# <a name="jet_retrievecolumncolumnidnexttagged-property"></a>JET_RETRIEVECOLUMN columnidNextTagged 屬性

藉由將0傳遞為 columnid，取得已標記、多重值或稀疏資料行的 columnid。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidNextTagged As JET_COLUMNID
    Get
    Private Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As JET_COLUMNID

value = instance.columnidNextTagged
```

``` csharp
public JET_COLUMNID columnidNextTagged { get; private set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RETRIEVECOLUMN 類別](./jet-retrievecolumn-class.md)

[JET_RETRIEVECOLUMN 成員](./jet-retrievecolumn-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
