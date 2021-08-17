---
description: 深入瞭解： DateTimeColumnValue. GetValueFromBytes 方法
title: DateTimeColumnValue. GetValueFromBytes 方法
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.DateTimeColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.datetimecolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55101200
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88ab0291e21839ccb666a3d9343a79787a5dad48c8ab8debbd1aafd17a8ab573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117528"
---
# <a name="datetimecolumnvaluegetvaluefrombytes-method"></a>DateTimeColumnValue. GetValueFromBytes 方法

從 ESENT 取出資料，將資料解碼，並設定 ColumnValue 物件中的值。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a>參數

  - 值  
    類型： \[\]  
    
    位元組陣列。

<!-- end list -->

  - startIndex  
    類型： [system.object](/dotnet/api/system.int32)  
    
    位元組內的開始位置。

<!-- end list -->

  - count  
    類型： [system.object](/dotnet/api/system.int32)  
    
    要解碼的位元組數。

<!-- end list -->

  - err  
    類型： [system.object](/dotnet/api/system.int32)  
    
    從 ESENT 傳回的錯誤。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[DateTimeColumnValue 類別](./datetimecolumnvalue-class.md)

[DateTimeColumnValue 成員](./datetimecolumnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
