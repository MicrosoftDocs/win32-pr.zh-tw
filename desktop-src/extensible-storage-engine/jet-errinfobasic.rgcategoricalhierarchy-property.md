---
description: 深入瞭解： JET_ERRINFOBASIC rgCategoricalHierarchy 屬性
title: RgCategoricalHierarchy 屬性 (Windows8) 的 JET_ERRINFOBASIC。
TOCTitle: 'rgCategoricalHierarchy property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errinfobasic.rgcategoricalhierarchy(v=EXCHG.10)
ms:contentKeyID: 55104314
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.set_rgCategoricalHierarchy
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.get_rgCategoricalHierarchy
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a64c043ccd63cfc8c60bd89e38b1b2bfa4c3cbb3f300144c4a6d436e7c67f2fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119232748"
---
# <a name="jet_errinfobasicrgcategoricalhierarchy-property"></a>JET_ERRINFOBASIC rgCategoricalHierarchy 屬性

取得或設定錯誤的階層。 位置0是階層中最高的層級，而其餘的則是 JET_errcatUnknown。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property rgCategoricalHierarchy As JET_ERRCAT()
    Get
    Set
'Usage
Dim instance As JET_ERRINFOBASIC
Dim value As JET_ERRCAT()

value = instance.rgCategoricalHierarchy

instance.rgCategoricalHierarchy = value
```

``` csharp
public JET_ERRCAT[] rgCategoricalHierarchy { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_ERRINFOBASIC 類別](./jet-errinfobasic-class.md)

[JET_ERRINFOBASIC 成員](./jet-errinfobasic-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
