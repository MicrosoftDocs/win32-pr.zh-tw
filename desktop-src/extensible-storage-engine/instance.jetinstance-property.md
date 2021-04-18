---
description: 深入瞭解： JetInstance 屬性
title: JetInstance 屬性
TOCTitle: 'JetInstance property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Instance.JetInstance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.jetinstance(v=EXCHG.10)
ms:contentKeyID: 55103279
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.JetInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.JetInstance
- Microsoft.Isam.Esent.Interop.Instance.get_JetInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc1e330be27f25fe677410d5468e56eea7b26933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512329"
---
# <a name="instancejetinstance-property"></a>JetInstance 屬性

取得此實例包含的 JET_INSTANCE。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property JetInstance As JET_INSTANCE
    Get
'Usage
Dim instance As Instance
Dim value As JET_INSTANCE

value = instance.JetInstance
```

``` csharp
public JET_INSTANCE JetInstance { get; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Instance 類別](./instance-class.md)

[實例成員](./instance-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
