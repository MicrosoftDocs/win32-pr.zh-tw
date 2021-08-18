---
description: 深入瞭解： JET_DBINFOMISC logtimeBadChecksum 屬性
title: JET_DBINFOMISC logtimeBadChecksum 屬性
TOCTitle: 'logtimeBadChecksum property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeBadChecksum
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.logtimebadchecksum(v=EXCHG.10)
ms:contentKeyID: 39516801
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeBadChecksum
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_logtimeBadChecksum
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeBadChecksum
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_logtimeBadChecksum
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70675ddbeb37ba3f32b23f02a801c9236d4d6695e551245be99033755c04c5a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112187"
---
# <a name="jet_dbinfomisclogtimebadchecksum-property"></a>JET_DBINFOMISC logtimeBadChecksum 屬性

取得上次找到不可更正的總和檢查碼錯誤的時間。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property logtimeBadChecksum As JET_LOGTIME
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LOGTIME

value = instance.logtimeBadChecksum
```

``` csharp
public JET_LOGTIME logtimeBadChecksum { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
