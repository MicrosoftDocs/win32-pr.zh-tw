---
description: 深入瞭解： EsentDTCCallbackUnexpectedErrorException 類別
title: EsentDTCCallbackUnexpectedErrorException 類別
TOCTitle: EsentDTCCallbackUnexpectedErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdtccallbackunexpectederrorexception(v=EXCHG.10)
ms:contentKeyID: 55107266
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ec2d5c2e204d0babeaf1e671d6096b8c52a9b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851995"
---
# <a name="esentdtccallbackunexpectederrorexception-class"></a>EsentDTCCallbackUnexpectedErrorException 類別

JET_err 的基類。DTCCallbackUnexpectedError 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          [EsentObsoleteException （.）](./esentobsoleteexception-class.md)  
            EsentDTCCallbackUnexpectedErrorException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDTCCallbackUnexpectedErrorException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDTCCallbackUnexpectedErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDTCCallbackUnexpectedErrorException : EsentObsoleteException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentDTCCallbackUnexpectedErrorException 成員](./esentdtccallbackunexpectederrorexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
