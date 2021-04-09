---
description: '深入瞭解： EsentCorruptionException 的函式 (SerializationInfo、StreamingCoNtext) '
title: 'EsentCorruptionException 函式 (SerializationInfo、StreamingCoNtext) '
TOCTitle: EsentCorruptionException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101038
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0e80255d86ed6f953e4010541e98b794537f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945277"
---
# <a name="esentcorruptionexception-constructor-serializationinfo-streamingcontext"></a>EsentCorruptionException 函式 (SerializationInfo、StreamingCoNtext) 

初始化 EsentCorruptionException 類別的新實例。 這個函式是用來將序列化的例外狀況還原序列化。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentCorruptionException(info, context)
```

``` csharp
protected EsentCorruptionException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>參數

  - info  
    類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。  
    
    還原序列化物件所需的資料。

<!-- end list -->

  - 內容  
    類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。  
    
    還原序列化內容。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentCorruptionException 類別](./esentcorruptionexception-class.md)

[EsentCorruptionException 成員](./esentcorruptionexception-members.md)

[EsentCorruptionException 多載](./esentcorruptionexception-constructor.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
