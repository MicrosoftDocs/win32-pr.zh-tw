---
description: 深入瞭解： JET_DBINFOMISC signDb 屬性
title: JET_DBINFOMISC signDb 屬性
TOCTitle: 'signDb property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signDb
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.signdb(v=EXCHG.10)
ms:contentKeyID: 39512669
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signDb
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_signDb
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_signDb
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signDb
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4bec4a70cb461745bd8781784061e93e0c9914274e02fbc5f19d5cead7d9825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833711"
---
# <a name="jet_dbinfomiscsigndb-property"></a>JET_DBINFOMISC signDb 屬性

取得資料庫簽章。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property signDb As JET_SIGNATURE
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_SIGNATURE

value = instance.signDb
```

``` csharp
public JET_SIGNATURE signDb { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
