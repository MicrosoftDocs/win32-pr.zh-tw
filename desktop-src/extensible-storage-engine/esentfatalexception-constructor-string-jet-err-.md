---
description: '深入瞭解： EsentFatalException (字串的函式、JET_err) '
title: EsentFatalException (字串 JET_err) 的函式
TOCTitle: EsentFatalException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFatalException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101610
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f025b93e626c4b0f2ab6bb7729169aaff1d67707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192893"
---
# <a name="esentfatalexception-constructor-string-jet_err"></a>EsentFatalException (字串 JET_err) 的函式

初始化 EsentFatalException 類別的新實例。

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

Dim instance As New EsentFatalException(description, _
    err)
```

``` csharp
protected EsentFatalException(
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

[EsentFatalException 類別](./esentfatalexception-class.md)

[EsentFatalException 成員](./esentfatalexception-members.md)

[EsentFatalException 多載](./esentfatalexception-constructor.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
