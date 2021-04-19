---
description: 深入瞭解： JET_INDEX_COLUMN pvData 屬性
title: PvData 屬性 (Windows8) 的 JET_INDEX_COLUMN。
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_index_column.pvdata(v=EXCHG.10)
ms:contentKeyID: 55104449
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN.pvData
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN.set_pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9eadb6b13798af0d18d56d0141cd3a7997106dc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993181"
---
# <a name="jet_index_columnpvdata-property"></a>JET_INDEX_COLUMN pvData 屬性

取得或設定要用來 comparte 資料行的值。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pvData As Byte()
    Get
    Set
'Usage
Dim instance As JET_INDEX_COLUMN
Dim value As Byte()

value = instance.pvData

instance.pvData = value
```

``` csharp
public byte[] pvData { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： \[\]  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEX_COLUMN 類別](./jet-index-column-class.md)

[JET_INDEX_COLUMN 成員](./jet-index-column-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
