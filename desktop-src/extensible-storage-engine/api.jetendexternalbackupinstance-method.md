---
description: 深入瞭解： JetEndExternalBackupInstance 方法
title: JetEndExternalBackupInstance 方法
TOCTitle: 'JetEndExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100691
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4611962006d4edc70eb558ad84b6ee47e6fd290a4ed301794695efe9ce513f2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042696"
---
# <a name="apijetendexternalbackupinstance-method"></a>JetEndExternalBackupInstance 方法

結束外部備份會話。 此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetEndExternalBackupInstance(instance)
```

``` csharp
public static void JetEndExternalBackupInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a>參數

  - instance  
    類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    要結束備份的實例。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
