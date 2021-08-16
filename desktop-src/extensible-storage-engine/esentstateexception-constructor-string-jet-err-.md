---
description: '深入瞭解： EsentStateException (字串的函式、JET_err) '
title: EsentStateException (字串 JET_err) 的函式
TOCTitle: EsentStateException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102995
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 99a5e381eb05b634f8eb76b18a9ba5bd477abaf5f796834635793538394bf11b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118490594"
---
# <a name="esentstateexception-constructor-string-jet_err"></a>EsentStateException (字串 JET_err) 的函式

初始化 EsentStateException 類別的新實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentStateException(description, _
    err)
```

``` csharp
protected EsentStateException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a>參數

  - description  
    類型： [system.string](/dotnet/api/system.string)  
    
    錯誤的描述。

<!-- end list -->

  - err  
    類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)  
    
    例外狀況的錯誤碼。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentStateException 類別](./esentstateexception-class.md)

[EsentStateException 成員](./esentstateexception-members.md)

[EsentStateException 多載](./esentstateexception-constructor.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
