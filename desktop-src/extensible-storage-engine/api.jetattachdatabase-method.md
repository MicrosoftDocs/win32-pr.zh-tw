---
description: 深入瞭解： JetAttachDatabase 方法
title: JetAttachDatabase 方法
TOCTitle: 'JetAttachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100652
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f81e70898165c2aa7882675620ed217efa79739aed12469685defd27c68a45d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983668"
---
# <a name="apijetattachdatabase-method"></a>JetAttachDatabase 方法

附加資料庫檔案以與資料庫實例搭配使用。 若要使用資料庫，就必須使用 [JetOpenDatabase (JET_SESID、string、string、JET_DBID、OpenDatabaseGrbit) ](./api.jetopendatabase-method.md)來開啟它。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Function JetAttachDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase(sesid, _
    database, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase(
    JET_SESID sesid,
    string database,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - [資料庫]  
    類型： [system.string](/dotnet/api/system.string)  
    
    要附加的資料庫。

<!-- end list -->

  - grbit  
    型別： [AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md) 。  
    
    附加選項。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
ESENT 警告碼。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
