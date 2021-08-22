---
description: '深入瞭解： EsentResource 方法 (布林值) '
title: EsentResource (布林) 的 Dispose 方法
TOCTitle: Dispose method (Boolean)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResource.Dispose(System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource.dispose(v=EXCHG.10)
ms:contentKeyID: 55102624
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource.Dispose
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cc2f9fab375e2ae2b9a27611192c3db9e3bba4eb272de1dfca243d13bf7766f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119477328"
---
# <a name="esentresourcedispose-method-boolean"></a>EsentResource (布林) 的 Dispose 方法

由 Dispose 和完成項呼叫。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Protected Overridable Sub Dispose ( _
    isDisposing As Boolean _
)
'Usage
Dim isDisposing As Boolean

Me.Dispose(isDisposing)
```

``` csharp
protected virtual void Dispose(
    bool isDisposing
)
```

#### <a name="parameters"></a>參數

  - isDisposing  
    型別： [system.object](/dotnet/api/system.boolean)  
    
    如果從 Dispose 呼叫，則為 True。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentResource 類別](./esentresource-class.md)

[EsentResource 成員](./esentresource-members.md)

[Dispose 多載](./esentresource.dispose-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
