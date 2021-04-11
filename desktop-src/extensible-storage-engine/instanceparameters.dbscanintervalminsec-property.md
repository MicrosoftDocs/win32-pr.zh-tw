---
description: 深入瞭解： InstanceParameters. DbScanIntervalMinSec 屬性
title: InstanceParameters. DbScanIntervalMinSec 屬性
TOCTitle: 'DbScanIntervalMinSec property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.DbScanIntervalMinSec
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.dbscanintervalminsec(v=EXCHG.10)
ms:contentKeyID: 55107436
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbScanIntervalMinSec
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_DbScanIntervalMinSec
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbScanIntervalMinSec
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_DbScanIntervalMinSec
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6630f106675ac7ae7d5c82039d8321c0a78bee62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114437"
---
# <a name="instanceparametersdbscanintervalminsec-property"></a>InstanceParameters. DbScanIntervalMinSec 屬性

取得或設定重複資料庫掃描的最小間隔（以秒為單位）。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property DbScanIntervalMinSec As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.DbScanIntervalMinSec

instance.DbScanIntervalMinSec = value
```

``` csharp
public int DbScanIntervalMinSec { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
