---
description: 深入瞭解： EsentStopwatch. 經過的屬性
title: EsentStopwatch. 經過的屬性
TOCTitle: 'Elapsed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentStopwatch.Elapsed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch.elapsed(v=EXCHG.10)
ms:contentKeyID: 55102997
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.Elapsed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.Elapsed
- Microsoft.Isam.Esent.Interop.EsentStopwatch.set_Elapsed
- Microsoft.Isam.Esent.Interop.EsentStopwatch.get_Elapsed
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02d60a19f799d5470711e9479b7ce0b28e190cdc63a23f853aa45a02d60aa70d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118490495"
---
# <a name="esentstopwatchelapsed-property"></a>EsentStopwatch. 經過的屬性

取得目前執行個體所測量的已耗用時間總和。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property Elapsed As TimeSpan
    Get
    Private Set
'Usage
Dim instance As EsentStopwatch
Dim value As TimeSpan

value = instance.Elapsed
```

``` csharp
public TimeSpan Elapsed { get; private set; }
```

#### <a name="property-value"></a>屬性值

類型： [TimeSpan](/dotnet/api/system.timespan)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentStopwatch 類別](./esentstopwatch-class.md)

[EsentStopwatch 成員](./esentstopwatch-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
