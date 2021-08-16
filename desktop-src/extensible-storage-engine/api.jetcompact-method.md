---
description: 深入瞭解： JetCompact 方法
title: JetCompact 方法
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8aecd3ec6120a93edb19b06d1f86c9573c1404f8dc1feb95c1acfec2d0077bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983458"
---
# <a name="apijetcompact-method"></a>JetCompact 方法

建立現有資料庫的複本。 複本會壓縮為使用狀態的最佳狀態。 複製的資料中的資料將會根據在索引建立時為索引選擇的量值進行壓縮。 如此一來，壓縮的資料可能會盡可能儲存為密集。 或者，壓縮的資料可能會保留空間，以便後續記錄成長或插入索引。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要用於呼叫的會話。

<!-- end list -->

  - sourceDatabase  
    類型： [system.string](/dotnet/api/system.string)  
    
    將壓縮的源資料庫。

<!-- end list -->

  - destinationDatabase  
    類型： [system.string](/dotnet/api/system.string)  
    
    要用於壓縮資料庫的名稱。

<!-- end list -->

  - statusCallback  
    類型： [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    可透過資料庫 compact 作業定期呼叫以報告進度的回呼函數。

<!-- end list -->

  - 忽略  
    類型： [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)  
    
    此參數會被忽略，而且應該是 null。

<!-- end list -->

  - grbit  
    型別： [CompactGrbit](./compactgrbit-enumeration.md) 。  
    
    壓縮選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
