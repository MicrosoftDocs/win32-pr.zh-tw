---
description: 深入瞭解： IJET_LOGTIME。ToDateTime 方法
title: IJET_LOGTIME。ToDateTime 方法
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.IJET_LOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.ijet_logtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39510507
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IJET_LOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IJET_LOGTIME.ToDateTime
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78226731ef945025aef0609cfeb905fe9b42101d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981463"
---
# <a name="ijet_logtimetodatetime-method"></a>IJET_LOGTIME。ToDateTime 方法

產生此 IJET_LOGTIME 的日期時程表示。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As IJET_LOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a>傳回值

類型： [可為 null](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
代表 IJET_LOGTIME 的日期時間。 如果 IJET_LOGTIME 為 null，則會傳回 null。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[IJET_LOGTIME 介面](./ijet-logtime-interface.md)

[IJET_LOGTIME 成員](./ijet-logtime-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
