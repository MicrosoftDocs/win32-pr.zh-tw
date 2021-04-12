---
description: '深入瞭解： EsentQuotaException 的函式 (SerializationInfo、StreamingCoNtext) '
title: 'EsentQuotaException 函式 (SerializationInfo、StreamingCoNtext) '
TOCTitle: EsentQuotaException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentQuotaException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102338
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36748053b8b9b48041c07ff51c99c0144093a9ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320307"
---
# <a name="esentquotaexception-constructor-serializationinfo-streamingcontext"></a>EsentQuotaException 函式 (SerializationInfo、StreamingCoNtext) 

初始化 EsentQuotaException 類別的新實例。 這個函式是用來將序列化的例外狀況還原序列化。

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

Dim instance As New EsentQuotaException(info, context)
```

``` csharp
protected EsentQuotaException(
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

[EsentQuotaException 類別](./esentquotaexception-class.md)

[EsentQuotaException 成員](./esentquotaexception-members.md)

[EsentQuotaException 多載](./esentquotaexception-constructor.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
