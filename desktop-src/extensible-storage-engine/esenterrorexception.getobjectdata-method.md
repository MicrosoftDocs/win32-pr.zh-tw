---
description: 深入瞭解： EsentErrorException. GetObjectData 方法
title: EsentErrorException. GetObjectData 方法
TOCTitle: 'GetObjectData method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.getobjectdata(v=EXCHG.10)
ms:contentKeyID: 55101432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ff4588429d5b45690763c3f4eefd3553f88f480
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476654"
---
# <a name="esenterrorexceptiongetobjectdata-method"></a>EsentErrorException. GetObjectData 方法

在衍生類別中覆寫時，使用例外狀況的相關資訊設定 [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Overrides Sub GetObjectData ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim instance As EsentErrorException
Dim info As SerializationInfo
Dim context As StreamingContext

instance.GetObjectData(info, context)
```

``` csharp
public override void GetObjectData(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>參數

  - info  
    類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。  
    
    [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) ，其中保存所擲回之例外狀況的相關序列化物件資料。

<!-- end list -->

  - 內容  
    類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。  
    
    [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) ，其中包含來源或目的地的相關內容資訊。

#### <a name="implements"></a>實作

[ISerializable GetObjectData (SerializationInfo、StreamingCoNtext) ](/dotnet/api/system.runtime.serialization.iserializable.getobjectdata#System_Runtime_Serialization_ISerializable_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  
[_Exception 的 GetObjectData (SerializationInfo、StreamingCoNtext) ](/dotnet/api/system.runtime.interopservices._exception.getobjectdata#System_Runtime_InteropServices__Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  

## <a name="exceptions"></a>例外狀況


| 例外狀況 | 條件 | 
|-----------|-----------|
| <a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a> | <p>info 參數是 null 參考 (在 Visual Basic 中為 Nothing)。</p> | 



## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentErrorException 類別](./esenterrorexception-class.md)

[EsentErrorException 成員](./esenterrorexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
