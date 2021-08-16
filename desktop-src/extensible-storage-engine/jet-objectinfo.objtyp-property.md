---
description: 深入瞭解： JET_OBJECTINFO objtyp 屬性
title: JET_OBJECTINFO objtyp 屬性
TOCTitle: 'objtyp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.objtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectinfo.objtyp(v=EXCHG.10)
ms:contentKeyID: 55103799
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.objtyp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.set_objtyp
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.get_objtyp
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.objtyp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f2abc54c2419b82ff6dc2469f46658bece41f39d4fe58a513abf5aef384e2eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979788"
---
# <a name="jet_objectinfoobjtyp-property"></a>JET_OBJECTINFO objtyp 屬性

取得資料表的 JET_OBJTYP。 目前只會傳回資料表， (也就是 [資料表](./jet-objtyp-enumeration.md)) 。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property objtyp As JET_objtyp
    Get
    Private Set
'Usage
Dim instance As JET_OBJECTINFO
Dim value As JET_objtyp

value = instance.objtyp
```

``` csharp
public JET_objtyp objtyp { get; private set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_OBJECTINFO 類別](./jet-objectinfo-class.md)

[JET_OBJECTINFO 成員](./jet-objectinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
