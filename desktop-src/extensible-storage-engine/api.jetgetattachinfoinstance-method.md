---
description: 深入瞭解： JetGetAttachInfoInstance 方法
title: JetGetAttachInfoInstance 方法
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29796919302b19b708878feb31e1fd53151700694a67bd1f6943bfa9d82d419c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272454"
---
# <a name="apijetgetattachinfoinstance-method"></a>JetGetAttachInfoInstance 方法

在 JetBeginExternalBackupInstance (JET_INSTANCE 所起始的備份期間使用 [，BeginExternalBackupGrbit) ](./api.jetbeginexternalbackupinstance-method.md) 來查詢實例，以取得應該成為備份檔案集一部分的資料庫檔案名。 系統只會考慮目前使用 [JetAttachDatabase (JET_SESID、String、AttachDatabaseGrbit) ](./api.jetattachdatabase-method.md) 連接到實例的資料庫。 之後可能會使用[JetOpenFileInstance (JET_INSTANCE、字串、JET_HANDLE、int64、int64) ](./api.jetopenfileinstance-method.md)和使用[JetReadFileInstance (JET_INSTANCE、JET_HANDLE、 \[ \] 、int32、int32) ](./api.jetreadfileinstance-method.md)來開啟這些檔案。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a>參數

  - instance  
    類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    要取得資訊的實例。

<!-- end list -->

  - files  
    類型： [system.string](/dotnet/api/system.string)  
    
    傳回 null 結束字串的清單，這些字串會描述應該是備份檔案集一部分的資料庫檔案集。 此緩衝區中傳回的字串清單，與登錄所用的多重字串格式相同。 每個以 null 終止的字串會依序傳回，後面接著最後一個 null 結束字元。

<!-- end list -->

  - maxChars  
    類型： [system.object](/dotnet/api/system.int32)  
    
    要取出的最大字元數。

<!-- end list -->

  - actualChars  
    類型： [system.object](/dotnet/api/system.int32)  
    
    檔案清單的實際大小。 如果大於 maxChars，表示清單已被截斷。

## <a name="remarks"></a>備註

請務必注意，如果輸出緩衝區太小而無法接受備份檔案集中應包含的完整檔案清單，則此 API 不會傳回錯誤或警告。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
