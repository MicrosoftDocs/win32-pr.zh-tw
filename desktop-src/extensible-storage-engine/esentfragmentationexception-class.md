---
description: 深入瞭解： EsentFragmentationException 類別
title: EsentFragmentationException 類別
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 081198a696be9982e1fd8a7e4f1468e6d63d1c97
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106997595"
---
# <a name="esentfragmentationexception-class"></a>EsentFragmentationException 類別

片段例外狀況的基類。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          EsentFragmentationException （.）  
            

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentFragmentationException 成員](./esentfragmentationexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>衍生類型

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          EsentFragmentationException （.）  
            [EsentLogSectorSizeMismatchException （.）](./esentlogsectorsizemismatchexception-class.md)  
            [EsentLogSequenceEndDatabasesConsistentException （.）](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [EsentLogSequenceEndException （.）](./esentlogsequenceendexception-class.md)  
            [EsentOutOfAutoincrementValuesException （.）](./esentoutofautoincrementvaluesexception-class.md)  
            [EsentOutOfDbtimeValuesException （.）](./esentoutofdbtimevaluesexception-class.md)  
            [EsentOutOfLongValueIDsException （.）](./esentoutoflongvalueidsexception-class.md)  
            [EsentOutOfObjectIDsException （.）](./esentoutofobjectidsexception-class.md)  
            [EsentOutOfSequentialIndexValuesException （.）](./esentoutofsequentialindexvaluesexception-class.md)