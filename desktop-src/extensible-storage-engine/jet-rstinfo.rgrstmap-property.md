---
description: 深入瞭解： JET_RSTINFO rgrstmap 屬性
title: JET_RSTINFO rgrstmap 屬性
TOCTitle: 'rgrstmap property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTINFO.rgrstmap
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstinfo.rgrstmap(v=EXCHG.10)
ms:contentKeyID: 55103890
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.rgrstmap
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.get_rgrstmap
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.set_rgrstmap
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.rgrstmap
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5ed9a44b4f38fc5b468db20a8f7657d625ef13a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972612"
---
# <a name="jet_rstinforgrstmap-property"></a>JET_RSTINFO rgrstmap 屬性

取得或設定 [JET_RSTMAP](./jet-rstmap-class.md) 結構的陣列。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property rgrstmap As JET_RSTMAP()
    Get
    Set
'Usage
Dim instance As JET_RSTINFO
Dim value As JET_RSTMAP()

value = instance.rgrstmap

instance.rgrstmap = value
```

``` csharp
public JET_RSTMAP[] rgrstmap { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RSTINFO 類別](./jet-rstinfo-class.md)

[JET_RSTINFO 成員](./jet-rstinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
