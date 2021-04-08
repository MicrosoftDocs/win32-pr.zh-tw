---
description: 深入瞭解： ByteColumnValue. GetValueFromBytes 方法
title: ByteColumnValue. GetValueFromBytes 方法
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ByteColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytecolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55100909
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ByteColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ByteColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf88d98460ab3766c7f354275a9c77571ff24da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852875"
---
# <a name="bytecolumnvaluegetvaluefrombytes-method"></a>ByteColumnValue. GetValueFromBytes 方法

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

  - value  
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

[ByteColumnValue 類別](./bytecolumnvalue-class.md)

[ByteColumnValue 成員](./bytecolumnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
