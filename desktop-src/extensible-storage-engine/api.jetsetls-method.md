---
description: 深入瞭解： JetSetLS 方法
title: JetSetLS 方法
TOCTitle: 'JetSetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetls(v=EXCHG.10)
ms:contentKeyID: 55100808
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d11d0790bb1d9340c427fd1b836d927527c6ca63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194482"
---
# <a name="apijetsetls-method"></a>JetSetLS 方法

讓應用程式將稱為本機儲存的內容控制碼與資料指標或與該資料指標相關聯的資料表產生關聯。 應用程式可以使用此內容控制碼來儲存與資料指標或資料表相關聯的輔助資料。 當內容控制碼必須釋放時，應用程式稍後會使用執行時間回呼來通知。 這樣就可以將動態配置的狀態與資料指標或資料表產生關聯。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetSetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetSetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetSetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要使用的資料指標。

<!-- end list -->

  - ls  
    類型： [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)  
    
    要與會話或資料指標相關聯的內容控制碼。

<!-- end list -->

  - grbit  
    型別： [LsGrbit](./lsgrbit-enumeration.md) 。  
    
    設定選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
