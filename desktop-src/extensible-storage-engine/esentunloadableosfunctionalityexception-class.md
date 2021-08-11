---
description: 深入瞭解： EsentUnloadableOSFunctionalityException 類別
title: EsentUnloadableOSFunctionalityException 類別
TOCTitle: EsentUnloadableOSFunctionalityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentunloadableosfunctionalityexception(v=EXCHG.10)
ms:contentKeyID: 55107333
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5ae24e5fd5867c847ef7f67d644e67e1be93f0d29d8bcc8a13b0fd05799f0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118256850"
---
# <a name="esentunloadableosfunctionalityexception-class"></a>EsentUnloadableOSFunctionalityException 類別

JET_err 的基類。UnloadableOSFunctionality 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentOperationException （.）](./esentoperationexception-class.md)  
          [EsentFatalException （.）](./esentfatalexception-class.md)  
            EsentUnloadableOSFunctionalityException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentUnloadableOSFunctionalityException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentUnloadableOSFunctionalityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentUnloadableOSFunctionalityException : EsentFatalException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentUnloadableOSFunctionalityException 成員](./esentunloadableosfunctionalityexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
