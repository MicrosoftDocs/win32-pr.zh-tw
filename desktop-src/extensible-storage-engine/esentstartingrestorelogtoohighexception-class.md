---
description: 深入瞭解： EsentStartingRestoreLogTooHighException 類別
title: EsentStartingRestoreLogTooHighException 類別
TOCTitle: EsentStartingRestoreLogTooHighException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstartingrestorelogtoohighexception(v=EXCHG.10)
ms:contentKeyID: 55102926
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a886142e5b99546ba01ce941c9a24a116e43adf8011ba938098c4baeca6fac15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018008"
---
# <a name="esentstartingrestorelogtoohighexception-class"></a>EsentStartingRestoreLogTooHighException 類別

JET_err 的基類。StartingRestoreLogTooHigh 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          [EsentInconsistentException （.）](./esentinconsistentexception-class.md)  
            EsentStartingRestoreLogTooHighException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentStartingRestoreLogTooHighException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentStartingRestoreLogTooHighException
```

``` csharp
[SerializableAttribute]
public sealed class EsentStartingRestoreLogTooHighException : EsentInconsistentException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentStartingRestoreLogTooHighException 成員](./esentstartingrestorelogtoohighexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
