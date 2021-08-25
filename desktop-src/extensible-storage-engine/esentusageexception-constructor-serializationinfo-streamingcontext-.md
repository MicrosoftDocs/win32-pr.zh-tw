---
description: '深入瞭解： EsentUsageException 的函式 (SerializationInfo、StreamingCoNtext) '
title: 'EsentUsageException 函式 (SerializationInfo、StreamingCoNtext) '
TOCTitle: EsentUsageException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103026
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a93c67f5bb8b324eaab04797f3a7d6bba6a5e4cf6867bd779e16057789503fcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781258"
---
# <a name="esentusageexception-constructor-serializationinfo-streamingcontext"></a>EsentUsageException 函式 (SerializationInfo、StreamingCoNtext) 

初始化 EsentUsageException 類別的新實例。 這個函式是用來將序列化的例外狀況還原序列化。

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

Dim instance As New EsentUsageException(info, context)
```

``` csharp
protected EsentUsageException(
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

[EsentUsageException 類別](./esentusageexception-class.md)

[EsentUsageException 成員](./esentusageexception-members.md)

[EsentUsageException 多載](./esentusageexception-constructor.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
