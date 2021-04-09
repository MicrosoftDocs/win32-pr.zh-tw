---
description: 深入瞭解： JET_PFNREALLOC 委派
title: JET_PFNREALLOC 委派
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945361"
---
# <a name="jet_pfnrealloc-delegate"></a>JET_PFNREALLOC 委派

JetEnumerateColumns 用來為其輸出緩衝區配置記憶體的回呼。

此 API 不符合 CLS 規範。 

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a>參數

  - 內容  
    類型： [system.object](/dotnet/api/system.intptr)  
    
    提供給 JetEnumerateColumns 的內容。

<!-- end list -->

  - 記憶體  
    類型： [system.object](/dotnet/api/system.intptr)  
    
    如果非零，則為此回呼先前配置之記憶體區塊的指標。

<!-- end list -->

  - requestedSize  
    類型： [system.object](/dotnet/api/system.uint32)  
    
    記憶體區塊的新大小 (以位元組為單位) 。 如果這是0，而且指定了記憶體區塊，就會釋放該記憶體區塊。

#### <a name="return-value"></a>傳回值

類型： [system.object](/dotnet/api/system.intptr)  
新配置之記憶體的指標。 如果無法配置記憶體，則應該傳回 [零](/dotnet/api/system.intptr.zero) 。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
