---
description: 深入瞭解： JetRestoreInstance 方法
title: JetRestoreInstance 方法
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973030"
---
# <a name="apijetrestoreinstance-method"></a>JetRestoreInstance 方法

還原和復原實例（包括所有附加的資料庫）的資料流程備份。 它是設計來搭配使用 [JetBackupInstance (JET_INSTANCE、String、BackupGrbit JET_PFNSTATUS) ](./api.jetbackupinstance-method.md) 函數所建立的備份。 這是最簡單且最具封裝的還原功能。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a>參數

  - instance  
    類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    要使用的實例。 不應初始化實例。 還原檔案將會初始化實例。

<!-- end list -->

  - source  
    類型： [system.string](/dotnet/api/system.string)  
    
    備份的位置。 應使用 [JetBackupInstance (JET_INSTANCE、String、BackupGrbit JET_PFNSTATUS) ](./api.jetbackupinstance-method.md)建立備份。

<!-- end list -->

  - 目的地  
    類型： [system.string](/dotnet/api/system.string)  
    
    將從備份組複製和復原資料庫檔案的資料夾名稱。 如果設定為 null，則會將資料庫檔案複製並復原到原始位置。

<!-- end list -->

  - statusCallback  
    類型： [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    選擇性狀態通知回呼。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
