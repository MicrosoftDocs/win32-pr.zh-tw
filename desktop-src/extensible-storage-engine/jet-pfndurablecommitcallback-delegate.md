---
description: 深入瞭解： JET_PFNDURABLECOMMITCALLBACK 委派
title: 'JET_PFNDURABLECOMMITCALLBACK 委派 (Windows8) '
TOCTitle: JET_PFNDURABLECOMMITCALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_pfndurablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104327
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.Invoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK..ctor
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.BeginInvoke
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4cba4c3e1db919634bff701855a75ab51fdd50aeef28c1d5d2e01e4a519446a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107657"
---
# <a name="jet_pfndurablecommitcallback-delegate"></a>JET_PFNDURABLECOMMITCALLBACK 委派

JET_paramDurableCommitCallback 的回呼。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Delegate Function JET_PFNDURABLECOMMITCALLBACK ( _
    instance As JET_INSTANCE, _
    pCommitIdSeen As JET_COMMIT_ID, _
    grbit As DurableCommitCallbackGrbit _
) As JET_err
'Usage
Dim instance As New JET_PFNDURABLECOMMITCALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNDURABLECOMMITCALLBACK(
    JET_INSTANCE instance,
    JET_COMMIT_ID pCommitIdSeen,
    DurableCommitCallbackGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - instance  
    類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    要使用的實例。

<!-- end list -->

  - pCommitIdSeen  
    類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    剛排清的認可識別碼。

<!-- end list -->

  - grbit  
    型別： [Windows8. DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)  
    
    目前已保留。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
