---
description: 深入瞭解： JET_RECSIZE cbOverhead 屬性
title: 'JET_RECSIZE. cbOverhead 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cbOverhead property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cboverhead(v=EXCHG.10)
ms:contentKeyID: 39514763
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbOverhead
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e7318428ef4b50a08a05f5021d293ad1d8d78cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984160"
---
# <a name="jet_recsizecboverhead-property"></a>JET_RECSIZE cbOverhead 屬性

取得此記錄之 ESENT 記錄結構的額外負荷。 這包括記錄的金鑰大小。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbOverhead As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbOverhead
```

``` csharp
public long cbOverhead { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RECSIZE 結構](./jet-recsize-structure2.md)

[JET_RECSIZE 成員](./jet-recsize-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
