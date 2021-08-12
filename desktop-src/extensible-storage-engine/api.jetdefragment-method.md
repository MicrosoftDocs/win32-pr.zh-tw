---
description: 深入瞭解： JetDefragment 方法
title: JetDefragment 方法
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9761782e2c6522752d6a05f69005a4db6844542c700cbc5c942ea80d96bf4c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272652"
---
# <a name="apijetdefragment-method"></a>JetDefragment 方法

啟動和停止資料庫重組工作，以改善資料庫中的資料組織。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要用於呼叫的會話。

<!-- end list -->

  - dbid  
    類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    要進行磁碟重組的資料庫。

<!-- end list -->

  - tableName  
    類型： [system.string](/dotnet/api/system.string)  
    
    未使用的參數。 針對指定資料庫識別碼所描述的整個資料庫執行磁碟重組。

<!-- end list -->

  - 通過  
    類型： [system.object](/dotnet/api/system.int32)  
    
    開始進行線上磁碟重組工作時，此參數會設定磁碟重組傳遞的最大數目。 停止線上磁碟重組工作時，此參數會設定為所執行的行程數目。

<!-- end list -->

  - seconds  
    類型： [system.object](/dotnet/api/system.int32)  
    
    開始進行線上磁碟重組工作時，此參數會設定磁碟重組的最長時間。 停止線上磁碟重組工作時，此輸出緩衝區會設定為用於重組的時間長度。

<!-- end list -->

  - grbit  
    型別： [DefragGrbit](./defraggrbit-enumeration.md) 。  
    
    磁碟重組選項。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
警告碼。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
