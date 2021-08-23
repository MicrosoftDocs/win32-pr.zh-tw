---
description: 深入瞭解： BoolColumnValue. GetValueFromBytes 方法
title: BoolColumnValue. GetValueFromBytes 方法
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.BoolColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.boolcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55100913
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44fddd0e9eee1ce593b5ac8cb7cb2ca0efcabb2d48e7e614f1ed2d100ad38c8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670068"
---
# <a name="boolcolumnvaluegetvaluefrombytes-method"></a>BoolColumnValue. GetValueFromBytes 方法

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

[BoolColumnValue 類別](./boolcolumnvalue-class.md)

[BoolColumnValue 成員](./boolcolumnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
