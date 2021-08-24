---
description: 深入瞭解： JET_THREADSTATS cPageDirtied 屬性
title: 'JET_THREADSTATS. cPageDirtied 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cPageDirtied property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpagedirtied(v=EXCHG.10)
ms:contentKeyID: 39512428
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageDirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageDirtied
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d633ab829c510d6e44e72d6500da422663f9df17b145e23cb7df51b8d3c7523
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719508"
---
# <a name="jet_threadstatscpagedirtied-property"></a>JET_THREADSTATS cPageDirtied 屬性

取得目前線程上的資料庫引擎已修改的資料庫頁面總數（沒有不成文變更）。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cPageDirtied As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageDirtied
```

``` csharp
public int cPageDirtied { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_THREADSTATS 結構](./jet-threadstats-structure2.md)

[JET_THREADSTATS 成員](./jet-threadstats-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
