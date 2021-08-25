---
description: 深入瞭解： ColumnValueOfStruct <T> 。Length 屬性
title: ColumnValueOfStruct (T) 。Length 屬性
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Length
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334225(v=EXCHG.10)
ms:contentKeyID: 55101009
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.get_Length
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: adbd9a120fca578d2908ec1e98f467c6ce622dbcb16095653a08b81be35c4985
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120066928"
---
# <a name="columnvalueofstructtlength-property"></a>ColumnValueOfStruct \<T\> 。Length 屬性

取得資料行值的位元組長度，如果資料行是 null，則為零，否則會符合此固定大小資料行的大小。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValueOfStruct
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnValueOfStruct \<T\> 類別](./columnvalueofstruct-t-class.md)

[ColumnValueOfStruct \<T\> 成員](./columnvalueofstruct-t-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
