---
description: 深入瞭解： JetEndExternalBackupInstance2 方法
title: JetEndExternalBackupInstance2 方法
TOCTitle: 'JetEndExternalBackupInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance2(v=EXCHG.10)
ms:contentKeyID: 55100692
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71a405c5e0ba3a398071cc317e0d42dd98c4953d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191249"
---
# <a name="apijetendexternalbackupinstance2-method"></a>JetEndExternalBackupInstance2 方法

結束外部備份會話。 此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As EndExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As EndExternalBackupGrbitApi.JetEndExternalBackupInstance2(instance, _
    grbit)
```

``` csharp
public static void JetEndExternalBackupInstance2(
    JET_INSTANCE instance,
    EndExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - instance  
    類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    要結束備份的實例。

<!-- end list -->

  - grbit  
    型別： [EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md) 。  
    
    指定備份如何結束的選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
