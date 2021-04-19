---
description: 深入瞭解： JET_COLUMNCREATE pvDefault 屬性
title: JET_COLUMNCREATE pvDefault 屬性
TOCTitle: 'pvDefault property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.pvDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.pvdefault(v=EXCHG.10)
ms:contentKeyID: 55103402
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.pvDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.get_pvDefault
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.set_pvDefault
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.pvDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9011d08e015c7a0ad374647a4d2863056f2be689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984688"
---
# <a name="jet_columncreatepvdefault-property"></a>JET_COLUMNCREATE pvDefault 屬性

取得或設定預設值 (Null （若無) ）。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pvDefault As Byte()
    Get
    Set
'Usage
Dim instance As JET_COLUMNCREATE
Dim value As Byte()

value = instance.pvDefault

instance.pvDefault = value
```

``` csharp
public byte[] pvDefault { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COLUMNCREATE 類別](./jet-columncreate-class.md)

[JET_COLUMNCREATE 成員](./jet-columncreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
