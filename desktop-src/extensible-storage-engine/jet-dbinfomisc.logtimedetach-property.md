---
description: 深入瞭解： JET_DBINFOMISC logtimeDetach 屬性
title: JET_DBINFOMISC logtimeDetach 屬性
TOCTitle: 'logtimeDetach property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeDetach
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.logtimedetach(v=EXCHG.10)
ms:contentKeyID: 39509697
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeDetach
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_logtimeDetach
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_logtimeDetach
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeDetach
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55f623cf098cce8d0877249947d971857f2de5d9084b78f736f13746704dc5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766172"
---
# <a name="jet_dbinfomisclogtimedetach-property"></a>JET_DBINFOMISC logtimeDetach 屬性

取得上一次卸離的時間。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property logtimeDetach As JET_LOGTIME
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LOGTIME

value = instance.logtimeDetach
```

``` csharp
public JET_LOGTIME logtimeDetach { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
