---
description: 深入瞭解： EsentStopwatch 類別
title: EsentStopwatch 類別
TOCTitle: EsentStopwatch class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch(v=EXCHG.10)
ms:contentKeyID: 55102933
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStopwatch
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStopwatch
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1250b10763aca6155ef7ac12bc64adbb95ac77a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851967"
---
# <a name="esentstopwatch-class"></a>EsentStopwatch 類別

提供一組方法和屬性，您可以使用這些方法和屬性來測量執行緒的 ESENT 工作統計資料。 如果最新版本的 ESENT 不支援 [JetGetThreadStats (JET_THREADSTATS) ](./vistaapi.jetgetthreadstats-method.md) 那麼所有 ESENT 統計資料都會是0。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  EsentStopwatch （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Class EsentStopwatch
'Usage
Dim instance As EsentStopwatch
```

``` csharp
public class EsentStopwatch
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentStopwatch 成員](./esentstopwatch-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
