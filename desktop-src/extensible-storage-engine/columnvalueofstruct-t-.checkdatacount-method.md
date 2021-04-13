---
description: 深入瞭解： ColumnValueOfStruct <T> 。CheckDataCount 方法
title: ColumnValueOfStruct (T) 。CheckDataCount 方法
TOCTitle: 'CheckDataCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.CheckDataCount(System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334178(v=EXCHG.10)
ms:contentKeyID: 55100977
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.CheckDataCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.CheckDataCount
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fda3fcabe1bb8ff462c37f823d6441720e02c414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193437"
---
# <a name="columnvalueofstructtcheckdatacount-method"></a>ColumnValueOfStruct \<T\> 。CheckDataCount 方法

請確定已抓取的資料完全是結構所需的大小。 如果有不相符的，則會擲回例外狀況。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Protected Sub CheckDataCount ( _
    count As Integer _
)
'Usage
Dim count As Integer

Me.CheckDataCount(count)
```

``` csharp
protected void CheckDataCount(
    int count
)
```

#### <a name="parameters"></a>參數

  - count  
    類型： [system.object](/dotnet/api/system.int32)  
    
    抓取之資料的大小。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnValueOfStruct \<T\> 類別](./columnvalueofstruct-t-class.md)

[ColumnValueOfStruct \<T\> 成員](./columnvalueofstruct-t-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
