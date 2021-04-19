---
description: '深入瞭解： EsentQuotaException (字串的函式、JET_err) '
title: EsentQuotaException (字串 JET_err) 的函式
TOCTitle: EsentQuotaException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentQuotaException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102558
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f615cf2a46beb8c504de3dcc7d6fab1fc23da47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978982"
---
# <a name="esentquotaexception-constructor-string-jet_err"></a>EsentQuotaException (字串 JET_err) 的函式

初始化 EsentQuotaException 類別的新實例。

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

Dim instance As New EsentQuotaException(description, _
    err)
```

``` csharp
protected EsentQuotaException(
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

[EsentQuotaException 類別](./esentquotaexception-class.md)

[EsentQuotaException 成員](./esentquotaexception-members.md)

[EsentQuotaException 多載](./esentquotaexception-constructor.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
