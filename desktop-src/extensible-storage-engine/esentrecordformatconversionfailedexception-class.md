---
description: 深入瞭解： EsentRecordFormatConversionFailedException 類別
title: EsentRecordFormatConversionFailedException 類別
TOCTitle: EsentRecordFormatConversionFailedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordformatconversionfailedexception(v=EXCHG.10)
ms:contentKeyID: 55102564
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d83997a7f0a92a1df929322f55223dc3600a4a193f235cccfb3e11751b35c77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781958"
---
# <a name="esentrecordformatconversionfailedexception-class"></a>EsentRecordFormatConversionFailedException 類別

JET_err 的基類。RecordFormatConversionFailed 例外狀況。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          [EsentCorruptionException （.）](./esentcorruptionexception-class.md)  
            EsentRecordFormatConversionFailedException （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordFormatConversionFailedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentRecordFormatConversionFailedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordFormatConversionFailedException : EsentCorruptionException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentRecordFormatConversionFailedException 成員](./esentrecordformatconversionfailedexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
