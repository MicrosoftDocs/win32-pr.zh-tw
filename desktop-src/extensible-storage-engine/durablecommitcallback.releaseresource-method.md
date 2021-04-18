---
description: 深入瞭解： DurableCommitCallback. ReleaseResource 方法
title: 'DurableCommitCallback. ReleaseResource 方法 (Windows8 的) '
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 634dd081513e576c7aabaac17cc5f9d207a8769f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195201"
---
# <a name="durablecommitcallbackreleaseresource-method"></a>DurableCommitCallback. ReleaseResource 方法

釋出持久的認可會話。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="remarks"></a>備註

請勿嘗試將 instance 參數設定為 null，因為在 JetTerm 之後會處置回呼，而且無法在 JetTerm 之後設定回呼。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[DurableCommitCallback 類別](./durablecommitcallback-class.md)

[DurableCommitCallback 成員](./durablecommitcallback-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
