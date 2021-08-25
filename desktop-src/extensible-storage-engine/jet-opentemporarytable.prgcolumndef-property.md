---
description: 深入瞭解： JET_OPENTEMPORARYTABLE prgcolumndef 屬性
title: 'JET_OPENTEMPORARYTABLE. prgcolumndef 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'prgcolumndef property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumndef
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.prgcolumndef(v=EXCHG.10)
ms:contentKeyID: 55104129
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumndef
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_prgcolumndef
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_prgcolumndef
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumndef
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8a0889e35d35c7296755fae3a6772f30546d3937b4c0f2c840f796d66c8a2aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945728"
---
# <a name="jet_opentemporarytableprgcolumndef-property"></a>JET_OPENTEMPORARYTABLE prgcolumndef 屬性

取得或設定在臨時表中建立之資料行的資料行定義。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property prgcolumndef As JET_COLUMNDEF()
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_COLUMNDEF()

value = instance.prgcolumndef

instance.prgcolumndef = value
```

``` csharp
public JET_COLUMNDEF[] prgcolumndef { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_OPENTEMPORARYTABLE 類別](./jet-opentemporarytable-class.md)

[JET_OPENTEMPORARYTABLE 成員](./jet-opentemporarytable-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
