---
description: 深入瞭解： InstanceParameters. DbScanIntervalMaxSec 屬性
title: InstanceParameters. DbScanIntervalMaxSec 屬性
TOCTitle: 'DbScanIntervalMaxSec property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.DbScanIntervalMaxSec
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.dbscanintervalmaxsec(v=EXCHG.10)
ms:contentKeyID: 55103552
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbScanIntervalMaxSec
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbScanIntervalMaxSec
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_DbScanIntervalMaxSec
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_DbScanIntervalMaxSec
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c76aed86c138c846b27e5b5ba13ea0ec5be563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114440"
---
# <a name="instanceparametersdbscanintervalmaxsec-property"></a>InstanceParameters. DbScanIntervalMaxSec 屬性

取得或設定允許資料庫掃描完成的最大間隔（以秒為單位）。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property DbScanIntervalMaxSec As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.DbScanIntervalMaxSec

instance.DbScanIntervalMaxSec = value
```

``` csharp
public int DbScanIntervalMaxSec { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
