---
description: 深入瞭解： JET_RECSIZE cbLongValueDataCompressed 屬性
title: 'JET_RECSIZE. cbLongValueDataCompressed 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cbLongValueDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cblongvaluedatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbLongValueDataCompressed
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e7ea71f705c14ef7c62244fde691e1a1174216fd07fa06b49e97d2fd124c592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038846"
---
# <a name="jet_recsizecblongvaluedatacompressed-property"></a>JET_RECSIZE cbLongValueDataCompressed 屬性

取得完整值樹狀結構中使用者資料的壓縮大小。 如果沒有壓縮分隔的 long 值，就會與 [cbLongValueData](./jet-recsize.cblongvaluedata-property.md) 相同。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbLongValueDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbLongValueDataCompressed
```

``` csharp
public long cbLongValueDataCompressed { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RECSIZE 結構](./jet-recsize-structure2.md)

[JET_RECSIZE 成員](./jet-recsize-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
