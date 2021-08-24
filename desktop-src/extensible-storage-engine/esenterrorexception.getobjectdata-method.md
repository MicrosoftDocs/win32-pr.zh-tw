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
ms.openlocfilehash: 7a4388d9af4f7cc6dbc284296b121fb3366e210c0d174a3db8e2b726f748f23a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784358"
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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>例外狀況</th>
<th>條件</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a></td>
<td><p>info 參數是 null 參考 (在 Visual Basic 中為 Nothing)。</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentErrorException 類別](./esenterrorexception-class.md)

[EsentErrorException 成員](./esenterrorexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
