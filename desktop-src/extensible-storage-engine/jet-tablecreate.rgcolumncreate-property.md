---
description: 深入瞭解： JET_TABLECREATE rgcolumncreate 屬性
title: JET_TABLECREATE rgcolumncreate 屬性
TOCTitle: 'rgcolumncreate property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgcolumncreate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.rgcolumncreate(v=EXCHG.10)
ms:contentKeyID: 55103965
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgcolumncreate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_rgcolumncreate
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgcolumncreate
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_rgcolumncreate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbbdea76b79bf650009a7e667c4a5136697079569f6d43f9a93f11febba00369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472858"
---
# <a name="jet_tablecreatergcolumncreate-property"></a>JET_TABLECREATE rgcolumncreate 屬性

取得或設定資料行建立資訊的陣列，其類型為 [JET_COLUMNCREATE](./jet-columncreate-class.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property rgcolumncreate As JET_COLUMNCREATE()
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As JET_COLUMNCREATE()

value = instance.rgcolumncreate

instance.rgcolumncreate = value
```

``` csharp
public JET_COLUMNCREATE[] rgcolumncreate { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_TABLECREATE 類別](./jet-tablecreate-class.md)

[JET_TABLECREATE 成員](./jet-tablecreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
