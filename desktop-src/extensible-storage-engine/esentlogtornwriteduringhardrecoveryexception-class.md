---
description: 深入瞭解： EsentLogTornWriteDuringHardRecoveryException 類別
title: EsentLogTornWriteDuringHardRecoveryException 類別
TOCTitle: EsentLogTornWriteDuringHardRecoveryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogtornwriteduringhardrecoveryexception(v=EXCHG.10)
ms:contentKeyID: 55102218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd6f6342fcfec9961a34074e2ebb37be23bf0904e70cd856331e7918071a131c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119040906"
---
# <a name="esentlogtornwriteduringhardrecoveryexception-class"></a>EsentLogTornWriteDuringHardRecoveryException 類別

JET_err 的基類。LogTornWriteDuringHardRecovery 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          [EsentCorruptionException （.）](./esentcorruptionexception-class.md)  
            EsentLogTornWriteDuringHardRecoveryException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogTornWriteDuringHardRecoveryException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogTornWriteDuringHardRecoveryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogTornWriteDuringHardRecoveryException : EsentCorruptionException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentLogTornWriteDuringHardRecoveryException 成員](./esentlogtornwriteduringhardrecoveryexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
