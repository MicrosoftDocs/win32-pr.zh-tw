---
description: 深入瞭解： InstanceParameters. DbScanThrottle 屬性
title: InstanceParameters. DbScanThrottle 屬性
TOCTitle: 'DbScanThrottle property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.DbScanThrottle
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.dbscanthrottle(v=EXCHG.10)
ms:contentKeyID: 55103556
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbScanThrottle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbScanThrottle
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_DbScanThrottle
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_DbScanThrottle
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b2293df80cdf4d5b19407d2719ba2d3252e87c2673f4ac2e011b66067a0dd7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834408"
---
# <a name="instanceparametersdbscanthrottle-property"></a>InstanceParameters. DbScanThrottle 屬性

取得或設定資料庫掃描的節流（以毫秒為單位）。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property DbScanThrottle As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.DbScanThrottle

instance.DbScanThrottle = value
```

``` csharp
public int DbScanThrottle { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
