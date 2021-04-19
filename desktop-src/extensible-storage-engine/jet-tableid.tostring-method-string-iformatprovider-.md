---
description: '深入瞭解： JET_TABLEID。ToString 方法 (字串，IFormatProvider) '
title: 'JET_TABLEID。ToString 方法 (字串，IFormatProvider) '
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.tostring(v=EXCHG.10)
ms:contentKeyID: 39510805
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e8d57d572a44f04c5b76ffb11f5243f7afb2b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980425"
---
# <a name="jet_tableidtostring-method-string-iformatprovider"></a>JET_TABLEID。ToString 方法 (字串，IFormatProvider) 

使用指定的格式，格式化目前執行個體的值。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_TABLEID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a>參數

  - format  
    類型： [system.string](/dotnet/api/system.string)  
    
    [字串](/dotnet/api/system.string)，指定要使用的格式;或者，null 會使用針對[>iformattable](/dotnet/api/system.iformattable)實作為型別所定義的預設格式。

<!-- end list -->

  - >formatprovider  
    類型： [System. IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    要用來格式化值的 [IFormatProvider](/dotnet/api/system.iformatprovider) ;或者，若要從作業系統的目前地區設定取得數值格式資訊，則為 null。

#### <a name="return-value"></a>傳回值

類型： [system.string](/dotnet/api/system.string)  
[字串](/dotnet/api/system.string)，包含指定格式之目前實例的值。  

#### <a name="implements"></a>實作

[>iformattable (字串，IFormatProvider) ](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_TABLEID 結構](./jet-tableid-structure.md)

[JET_TABLEID 成員](./jet-tableid-members.md)

[ToString 多載](./jet-tableid.tostring-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
