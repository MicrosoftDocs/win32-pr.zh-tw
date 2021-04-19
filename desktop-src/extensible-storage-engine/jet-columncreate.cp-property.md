---
description: 深入瞭解： JET_COLUMNCREATE 的 cp 屬性
title: JET_COLUMNCREATE cp 屬性
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.cp(v=EXCHG.10)
ms:contentKeyID: 55103400
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.get_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b39c47402a70778543f203777b6e2d0d3fc9ac29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984987"
---
# <a name="jet_columncreatecp-property"></a>JET_COLUMNCREATE cp 屬性

取得或設定資料行的字碼頁。 只有 [Text](./jet-coltyp-enumeration.md) 和 [LongText](./jet-coltyp-enumeration.md)類型的資料行才有意義。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Set
'Usage
Dim instance As JET_COLUMNCREATE
Dim value As JET_CP

value = instance.cp

instance.cp = value
```

``` csharp
public JET_CP cp { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COLUMNCREATE 類別](./jet-columncreate-class.md)

[JET_COLUMNCREATE 成員](./jet-columncreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
