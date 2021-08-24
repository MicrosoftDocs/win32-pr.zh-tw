---
description: '深入瞭解： Instance.Init 方法 (JET_RSTINFO、InitGrbit) '
title: 'Instance.Init 方法 (JET_RSTINFO、InitGrbit) '
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e2a9975c42383c4ba0d58fb1a41dfeb1df07f81cebfd9b028bd54240bfb6b47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834438"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a>Instance.Init 方法 (JET_RSTINFO、InitGrbit) 

初始化 JET_INSTANCE。 此 API 至少需要 Vista 版本的 ESENT。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - recoveryOptions  
    類型： [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)  
    
    在復原期間重新對應資料庫的其他修復參數、放置停止復原的位置，或復原狀態。

<!-- end list -->

  - grbit  
    類型： [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)  
    
    初始化選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Instance 類別](./instance-class.md)

[實例成員](./instance-members.md)

[Init 多載](./instance.init-method2.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
