---
description: 深入瞭解： JET_CALLBACK 委派
title: JET_CALLBACK 委派
TOCTitle: JET_CALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_callback(v=EXCHG.10)
ms:contentKeyID: 39515752
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK..ctor
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.Invoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30ba54414bcc7043edb06300b7bda31e40b838cbc6f78f32171f26c1e37684c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487304"
---
# <a name="jet_callback-delegate"></a>JET_CALLBACK 委派

資料庫引擎使用的多用途回呼函式，用來通知應用程式涉及線上磁碟重組和資料指標狀態通知。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Delegate Function JET_CALLBACK ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    arg1 As Object, _
    arg2 As Object, _
    context As IntPtr, _
    unused As IntPtr _
) As JET_err
'Usage
Dim instance As New JET_CALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_CALLBACK(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    Object arg1,
    Object arg2,
    IntPtr context,
    IntPtr unused
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    正在進行回呼的會話。

<!-- end list -->

  - dbid  
    類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    正在進行回呼的資料庫。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    正在進行回呼的資料指標。

<!-- end list -->

  - cbtyp  
    類型： [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)  
    
    正在進行回呼的作業。

<!-- end list -->

  - arg1  
    類型： [system.object](/dotnet/api/system.object)  
    
    第一個回呼特定的引數。

<!-- end list -->

  - arg2  
    類型： [system.object](/dotnet/api/system.object)  
    
    第二個回呼特定的引數。

<!-- end list -->

  - 內容  
    類型： [system.object](/dotnet/api/system.intptr)  
    
    回呼內容。

<!-- end list -->

  - unused  
    類型： [system.object](/dotnet/api/system.intptr)  
    
    不使用這個參數。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
