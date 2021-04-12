---
description: '深入瞭解： EsentUsageException (字串的函式、JET_err) '
title: EsentUsageException (字串 JET_err) 的函式
TOCTitle: EsentUsageException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103223
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f9d38ebc5be25eb8f036583404d340a8882de6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321160"
---
# <a name="esentusageexception-constructor-string-jet_err"></a>EsentUsageException (字串 JET_err) 的函式

初始化 EsentUsageException 類別的新實例。

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

Dim instance As New EsentUsageException(description, _
    err)
```

``` csharp
protected EsentUsageException(
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

[EsentUsageException 類別](./esentusageexception-class.md)

[EsentUsageException 成員](./esentusageexception-members.md)

[EsentUsageException 多載](./esentusageexception-constructor.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
