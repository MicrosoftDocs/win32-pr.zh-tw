---
description: 深入瞭解：資料表類別
title: Table 類別
TOCTitle: Table class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table(v=EXCHG.10)
ms:contentKeyID: 55104053
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ea12d7bd59d946c7375150862cd8fa0c87ba6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973261"
---
# <a name="table-class"></a>Table 類別

封裝可處置物件中之 JET_TABLEID 的類別。 這會開啟現有的資料表。 若要建立資料表，請使用 JetCreateTable 方法。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [EsentResource （.）](./esentresource-class.md)  
    Microsoft. Esent. Interop. 資料表  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Class Table _
    Inherits EsentResource
'Usage
Dim instance As Table
```

``` csharp
public class Table : EsentResource
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[資料表成員](./table-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
