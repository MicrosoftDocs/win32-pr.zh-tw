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
ms.openlocfilehash: a9f70d2e26c8ee56e88f0405af19f17476612bd9a5f51ba624088ed9d58380d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120066938"
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
