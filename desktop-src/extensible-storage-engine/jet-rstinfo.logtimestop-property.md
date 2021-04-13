---
description: 深入瞭解： JET_RSTINFO logtimeStop 屬性
title: JET_RSTINFO logtimeStop 屬性
TOCTitle: 'logtimeStop property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTINFO.logtimeStop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstinfo.logtimestop(v=EXCHG.10)
ms:contentKeyID: 55103905
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.logtimeStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.set_logtimeStop
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.logtimeStop
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.get_logtimeStop
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d4b5e770fafdded138224cd3e7868c24d42e13f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468836"
---
# <a name="jet_rstinfologtimestop-property"></a>JET_RSTINFO logtimeStop 屬性

取得或設定其停止的時間。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property logtimeStop As JET_LOGTIME
    Get
    Set
'Usage
Dim instance As JET_RSTINFO
Dim value As JET_LOGTIME

value = instance.logtimeStop

instance.logtimeStop = value
```

``` csharp
public JET_LOGTIME logtimeStop { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RSTINFO 類別](./jet-rstinfo-class.md)

[JET_RSTINFO 成員](./jet-rstinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
