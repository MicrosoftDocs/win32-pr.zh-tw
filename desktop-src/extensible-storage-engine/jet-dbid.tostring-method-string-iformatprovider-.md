---
description: '深入瞭解： JET_DBID。ToString 方法 (字串，IFormatProvider) '
title: 'JET_DBID。ToString 方法 (字串，IFormatProvider) '
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.tostring(v=EXCHG.10)
ms:contentKeyID: 39513106
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b6fca1494a31bc342d4f8ad2933968c58efacc5f5e115ff10fe92a8afbabca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017256"
---
# <a name="jet_dbidtostring-method-string-iformatprovider"></a>JET_DBID。ToString 方法 (字串，IFormatProvider) 

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
Dim instance As JET_DBID
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
    
    [字串](/dotnet/api/system.string)，指定要使用的格式。 -或-null 表示使用針對 [>iformattable](/dotnet/api/system.iformattable) 實作為型別所定義的預設格式。

<!-- end list -->

  - >formatprovider  
    類型： [System. IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    要用來格式化值的 [IFormatProvider](/dotnet/api/system.iformatprovider) 。 -或-null 可從作業系統的目前地區設定中取得數值格式資訊。

#### <a name="return-value"></a>傳回值

類型： [system.string](/dotnet/api/system.string)  
[字串](/dotnet/api/system.string)，包含指定格式之目前實例的值。  

#### <a name="implements"></a>實作

[>iformattable (字串，IFormatProvider) ](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBID 結構](./jet-dbid-structure.md)

[JET_DBID 成員](./jet-dbid-members.md)

[ToString 多載](./jet-dbid.tostring-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
