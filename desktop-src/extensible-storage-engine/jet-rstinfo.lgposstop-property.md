---
description: 深入瞭解： JET_RSTINFO lgposStop 屬性
title: JET_RSTINFO lgposStop 屬性
TOCTitle: 'lgposStop property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTINFO.lgposStop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstinfo.lgposstop(v=EXCHG.10)
ms:contentKeyID: 55103830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.lgposStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.get_lgposStop
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.set_lgposStop
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.lgposStop
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08823de30cfe13497a4bd42073688bc739d80acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511122"
---
# <a name="jet_rstinfolgposstop-property"></a>JET_RSTINFO lgposStop 屬性

取得或設定要停止復原的記錄位置。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property lgposStop As JET_LGPOS
    Get
    Set
'Usage
Dim instance As JET_RSTINFO
Dim value As JET_LGPOS

value = instance.lgposStop

instance.lgposStop = value
```

``` csharp
public JET_LGPOS lgposStop { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RSTINFO 類別](./jet-rstinfo-class.md)

[JET_RSTINFO 成員](./jet-rstinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
