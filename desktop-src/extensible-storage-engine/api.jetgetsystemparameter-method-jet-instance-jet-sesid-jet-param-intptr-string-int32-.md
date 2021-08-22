---
description: '深入瞭解： JetGetSystemParameter 方法 (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String、Int32) '
title: 'JetGetSystemParameter 方法 (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String、Int32) '
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100731
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6188db63795513d0fb207621a15ca9dd11798e619c5d9c5b7bb0d915e59ace77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983288"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string-int32"></a>JetGetSystemParameter 方法 (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String、Int32) 

取得資料庫設定選項。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As IntPtr, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref IntPtr paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a>參數

  - instance  
    類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    要從中取出選項的實例。

<!-- end list -->

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - paramid  
    類型： [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)  
    
    要取得的參數。

<!-- end list -->

  - paramValue  
    類型： [system.object](/dotnet/api/system.intptr)  
    
    如果值是整數，則傳回參數的值。

<!-- end list -->

  - paramString  
    類型： [system.string](/dotnet/api/system.string)  
    
    如果值為字串，則傳回參數的值。

<!-- end list -->

  - maxParam  
    類型： [system.object](/dotnet/api/system.int32)  
    
    參數字串的大小上限。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
ESENT 警告碼。  

## <a name="remarks"></a>備註

[ErrorToString](./jet-param-enumeration.md) 會傳入 paramValue 中的錯誤號碼，這就是為什麼它是 ref 參數，而不是 out 參數。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[JetGetSystemParameter 多載](./api.jetgetsystemparameter-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
