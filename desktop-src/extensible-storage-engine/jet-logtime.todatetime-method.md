---
description: 深入瞭解： JET_LOGTIME。ToDateTime 方法
title: JET_LOGTIME。ToDateTime 方法
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39512964
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14d427d1c7e4a6f37c27677ed9617d92eb8ff644
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695671"
---
# <a name="jet_logtimetodatetime-method"></a>JET_LOGTIME。ToDateTime 方法

產生此 JET_LOGTIME 的日期時程表示。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As JET_LOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
public Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a>傳回值

類型： [可為 null](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
代表 JET_LOGTIME 的日期時間。 如果 JET_LOGTIME 為 null，則會傳回 null。  

#### <a name="implements"></a>實作

[IJET_LOGTIME。ToDateTime () ](./ijet-logtime.todatetime-method.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_LOGTIME 結構](./jet-logtime-structure2.md)

[JET_LOGTIME 成員](./jet-logtime-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
