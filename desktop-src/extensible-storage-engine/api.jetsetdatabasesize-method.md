---
description: 深入瞭解： JetSetDatabaseSize 方法
title: JetSetDatabaseSize 方法
TOCTitle: 'JetSetDatabaseSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetdatabasesize(v=EXCHG.10)
ms:contentKeyID: 55100807
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04134cec24888a7ed6d046fddf2380f6483ed0d2d8c59c3ce33f51f6e64fcaa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118084812"
---
# <a name="apijetsetdatabasesize-method"></a>JetSetDatabaseSize 方法

設定未開啟之資料庫檔案的大小。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetSetDatabaseSize ( _
    sesid As JET_SESID, _
    database As String, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetSetDatabaseSize(sesid, database, _
    desiredPages, actualPages)
```

``` csharp
public static void JetSetDatabaseSize(
    JET_SESID sesid,
    string database,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - [資料庫]  
    類型： [system.string](/dotnet/api/system.string)  
    
    資料庫的名稱。

<!-- end list -->

  - desiredPages  
    類型： [system.object](/dotnet/api/system.int32)  
    
    所需的資料庫大小（以頁面為限）。

<!-- end list -->

  - actualPages  
    類型： [system.object](/dotnet/api/system.int32)  
    
    在呼叫之後，資料庫的大小（以頁面為限）。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
