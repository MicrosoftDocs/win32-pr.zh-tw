---
description: 深入瞭解： EsentPageNotInitializedException 類別
title: EsentPageNotInitializedException 類別
TOCTitle: EsentPageNotInitializedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpagenotinitializedexception(v=EXCHG.10)
ms:contentKeyID: 55107308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c349560498993d0920f344ef716835afa8fb62c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320015"
---
# <a name="esentpagenotinitializedexception-class"></a>EsentPageNotInitializedException 類別

JET_err 的基類。PageNotInitialized 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          [EsentCorruptionException （.）](./esentcorruptionexception-class.md)  
            EsentPageNotInitializedException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPageNotInitializedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentPageNotInitializedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPageNotInitializedException : EsentCorruptionException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentPageNotInitializedException 成員](./esentpagenotinitializedexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
