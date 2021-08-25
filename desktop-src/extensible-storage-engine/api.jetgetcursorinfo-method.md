---
description: 深入瞭解： JetGetCursorInfo 方法
title: JetGetCursorInfo 方法
TOCTitle: 'JetGetCursorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcursorinfo(v=EXCHG.10)
ms:contentKeyID: 55100707
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8203d541db2596f4d691c055aba83e3b6b76163f7b5949e3b62d6e46256d8b28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841038"
---
# <a name="apijetgetcursorinfo-method"></a>JetGetCursorInfo 方法

根據記錄目前的更新狀態，判斷資料指標的目前記錄更新是否會導致寫入衝突。 即使 JetGetCursorInfo 成功傳回，還是可能會傳回寫入衝突。 因為另一個會話可能會在目前的會話可以更新相同記錄之前更新記錄。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetGetCursorInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetGetCursorInfo(sesid, tableid)
```

``` csharp
public static void JetGetCursorInfo(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要檢查的資料指標。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
