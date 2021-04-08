---
description: 深入瞭解： EsentMemoryException 類別
title: EsentMemoryException 類別
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a7090fdedee2969e5dd3658b7068fd8739e9365
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103853259"
---
# <a name="esentmemoryexception-class"></a>EsentMemoryException 類別

記憶體例外狀況的基類。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentOperationException （.）](./esentoperationexception-class.md)  
          [EsentResourceException （.）](./esentresourceexception-class.md)  
            EsentMemoryException （.）  
              

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentMemoryException 成員](./esentmemoryexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>衍生類型

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentOperationException （.）](./esentoperationexception-class.md)  
          [EsentResourceException （.）](./esentresourceexception-class.md)  
            EsentMemoryException （.）  
              [EsentOutOfBuffersException （.）](./esentoutofbuffersexception-class.md)  
              [EsentOutOfCursorsException （.）](./esentoutofcursorsexception-class.md)  
              [EsentOutOfFileHandlesException （.）](./esentoutoffilehandlesexception-class.md)  
              [EsentOutOfMemoryException （.）](./esentoutofmemoryexception-class.md)  
              [EsentOutOfSessionsException （.）](./esentoutofsessionsexception-class.md)  
              [EsentOutOfThreadsException （.）](./esentoutofthreadsexception-class.md)  
              [EsentTooManyMempoolEntriesException （.）](./esenttoomanymempoolentriesexception-class.md)  
              [EsentTooManyOpenIndexesException （.）](./esenttoomanyopenindexesexception-class.md)  
              [EsentTooManySortsException （.）](./esenttoomanysortsexception-class.md)