---
description: 深入瞭解： JET_DBINFOMISC signLog 屬性
title: JET_DBINFOMISC signLog 屬性
TOCTitle: 'signLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.signlog(v=EXCHG.10)
ms:contentKeyID: 39511875
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_signLog
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_signLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3235224ab65ef32eabb5567215284eed7a938672f8e77ccdade40f70e8b85538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118486226"
---
# <a name="jet_dbinfomiscsignlog-property"></a>JET_DBINFOMISC signLog 屬性

取得用來修改資料庫之記錄檔的記錄檔簽章。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property signLog As JET_SIGNATURE
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_SIGNATURE

value = instance.signLog
```

``` csharp
public JET_SIGNATURE signLog { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
