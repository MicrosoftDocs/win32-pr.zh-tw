---
description: 深入瞭解： EsentSectorSizeNotSupportedException 類別
title: EsentSectorSizeNotSupportedException 類別
TOCTitle: EsentSectorSizeNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsectorsizenotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55107328
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d281083093c52c0aa6119f7790d002e3a4fceb4a008a58f123bf1752319feef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781733"
---
# <a name="esentsectorsizenotsupportedexception-class"></a>EsentSectorSizeNotSupportedException 類別

JET_err 的基類。SectorSizeNotSupported 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentOperationException （.）](./esentoperationexception-class.md)  
          [EsentFatalException （.）](./esentfatalexception-class.md)  
            EsentSectorSizeNotSupportedException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSectorSizeNotSupportedException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentSectorSizeNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSectorSizeNotSupportedException : EsentFatalException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentSectorSizeNotSupportedException 成員](./esentsectorsizenotsupportedexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
