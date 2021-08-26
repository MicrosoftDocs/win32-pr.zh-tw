---
description: 深入瞭解： JET_RSTINFO pfnStatus 屬性
title: JET_RSTINFO pfnStatus 屬性
TOCTitle: 'pfnStatus property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstinfo.pfnstatus(v=EXCHG.10)
ms:contentKeyID: 55103829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.set_pfnStatus
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.get_pfnStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a4a74518b50358dc2e6317009684db356562d54927012c6af433f4172bd4f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967580"
---
# <a name="jet_rstinfopfnstatus-property"></a>JET_RSTINFO pfnStatus 屬性

取得或設定要取得或設定狀態函數的回呼。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pfnStatus As JET_PFNSTATUS
    Get
    Set
'Usage
Dim instance As JET_RSTINFO
Dim value As JET_PFNSTATUS

value = instance.pfnStatus

instance.pfnStatus = value
```

``` csharp
public JET_PFNSTATUS pfnStatus { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RSTINFO 類別](./jet-rstinfo-class.md)

[JET_RSTINFO 成員](./jet-rstinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
