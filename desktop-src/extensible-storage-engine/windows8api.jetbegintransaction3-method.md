---
description: 深入瞭解： Windows8Api. JetBeginTransaction3 方法
title: 'Windows8Api. JetBeginTransaction3 方法 (Windows8 的) '
TOCTitle: 'JetBeginTransaction3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3(Microsoft.Isam.Esent.Interop.JET_SESID,System.Int64,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetbegintransaction3(v=EXCHG.10)
ms:contentKeyID: 55107825
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7605cdb44c66d929e6663caaad9e40d3c98737b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512473"
---
# <a name="windows8apijetbegintransaction3-method"></a>Windows8Api. JetBeginTransaction3 方法

導致會話進入交易，或在現有的交易中建立新的儲存點。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetBeginTransaction3 ( _
    sesid As JET_SESID, _
    userTransactionId As Long, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim userTransactionId As Long
Dim grbit As BeginTransactionGrbitWindows8Api.JetBeginTransaction3(sesid, _
    userTransactionId, grbit)
```

``` csharp
public static void JetBeginTransaction3(
    JET_SESID sesid,
    long userTransactionId,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    開始交易的會話。

<!-- end list -->

  - userTransactionId  
    類型： [Int64](/dotnet/api/system.int64)  
    
    使用者提供的選擇性識別碼，用來識別交易。

<!-- end list -->

  - grbit  
    型別： [BeginTransactionGrbit](./begintransactiongrbit-enumeration.md) 。  
    
    交易選項。

## <a name="remarks"></a>備註

Windows 8 引進。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows8Api 類別](./windows8api-class.md)

[Windows8Api 成員](./windows8api-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
