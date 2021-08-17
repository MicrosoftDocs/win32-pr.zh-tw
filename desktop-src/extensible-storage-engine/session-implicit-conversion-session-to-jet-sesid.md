---
description: '深入瞭解： (會話的會話隱含轉換至 JET_SESID) '
title: " (會話的會話隱含轉換 JET_SESID) "
TOCTitle: Implicit conversion (Session to JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.op_Implicit(Microsoft.Isam.Esent.Interop.Session)~Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104121
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.op_Implicit
- Microsoft.Isam.Esent.Interop.Session.Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be293636044e744ec02e3bdcddbc96b61373a35c9bddc04a03d282fcebe268d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485507"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a> (會話的會話隱含轉換 JET_SESID) 

從會話到 JET_SESID 的隱含轉換運算子。 這可讓會話與預期 JET_SESID 的 Api 搭配使用。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    session As Session _
) As JET_SESID
'Usage
Dim input As Session
Dim output As JET_SESID

output = CType(input, JET_SESID)
```

``` csharp
public static implicit operator JET_SESID (
    Session session
)
```

#### <a name="parameters"></a>參數

  - 工作階段 (session)  
    類型： [Microsoft. Isam](./session-class.md) 。  
    
    要轉換的會話。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
會話的 JET_SESID。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[工作階段類別](./session-class.md)

[會話成員](./session-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
