---
description: 深入瞭解： JetSesid 屬性
title: JetSesid 屬性
TOCTitle: 'JetSesid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Session.JetSesid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.jetsesid(v=EXCHG.10)
ms:contentKeyID: 55104125
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.JetSesid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.JetSesid
- Microsoft.Isam.Esent.Interop.Session.get_JetSesid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71f8742b5b0166681b0f20007d27b6d8797498f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193027"
---
# <a name="sessionjetsesid-property"></a>JetSesid 屬性

取得此會話包含的 JET_SESID。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property JetSesid As JET_SESID
    Get
'Usage
Dim instance As Session
Dim value As JET_SESID

value = instance.JetSesid
```

``` csharp
public JET_SESID JetSesid { get; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[工作階段類別](./session-class.md)

[會話成員](./session-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
