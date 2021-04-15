---
description: 深入瞭解： SystemParameters. StopFlushThreshold 屬性
title: SystemParameters. StopFlushThreshold 屬性
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320163"
---
# <a name="systemparametersstopflushthreshold-property"></a>SystemParameters. StopFlushThreshold 屬性

取得或設定資料庫頁面快取結束從快取收回頁面的閾值，以騰出空間給未快取的頁面。 當快取中的頁面緩衝區數目超過此臨界值時，就會停止已開始補充該可用緩衝區集區的背景進程。 此臨界值一律相對於 JET_paramCacheSizeMax 所設定的最大快取大小。 此臨界值也必須大於 JET_paramStartFlushThreshold 所設定的 [開始] 閾值。 開始閾值和停止臨界值之間的距離，會影響背景進程清除資料庫頁面的效率。 較大的間距將可讓您更有可能合併對相鄰頁面的寫入。 不過，高停止閾值將會減少資料庫頁面快取的有效大小。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[SystemParameters 類別](./systemparameters-class.md)

[SystemParameters 成員](./systemparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
