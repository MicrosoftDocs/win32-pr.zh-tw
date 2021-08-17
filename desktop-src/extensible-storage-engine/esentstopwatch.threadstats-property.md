---
description: 深入瞭解： EsentStopwatch. ThreadStats 屬性
title: EsentStopwatch. ThreadStats 屬性
TOCTitle: 'ThreadStats property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch.threadstats(v=EXCHG.10)
ms:contentKeyID: 55102996
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.get_ThreadStats
- Microsoft.Isam.Esent.Interop.EsentStopwatch.set_ThreadStats
- Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13cfe4ac7f318530e7fee60d0b0020c94602f5ad1a1dd1ba4f262a25380b7409
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119273098"
---
# <a name="esentstopwatchthreadstats-property"></a>EsentStopwatch. ThreadStats 屬性

取得目前實例所測量的總 ESENT 工作統計資料。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ThreadStats As JET_THREADSTATS
    Get
    Private Set
'Usage
Dim instance As EsentStopwatch
Dim value As JET_THREADSTATS

value = instance.ThreadStats
```

``` csharp
public JET_THREADSTATS ThreadStats { get; private set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentStopwatch 類別](./esentstopwatch-class.md)

[EsentStopwatch 成員](./esentstopwatch-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
