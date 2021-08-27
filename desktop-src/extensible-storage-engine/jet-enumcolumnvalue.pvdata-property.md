---
description: 深入瞭解： JET_ENUMCOLUMNVALUE pvData 屬性
title: JET_ENUMCOLUMNVALUE pvData 屬性
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103630
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.set_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.get_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d8278a9611a95792cd18529228692999382ec4a3dd7f3759330023ea7449cab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116108"
---
# <a name="jet_enumcolumnvaluepvdata-property"></a>JET_ENUMCOLUMNVALUE pvData 屬性

取得為數據行列舉的值。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pvData As IntPtr
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
Dim value As IntPtr

value = instance.pvData
```

``` csharp
public IntPtr pvData { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.intptr)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_ENUMCOLUMNVALUE 類別](./jet-enumcolumnvalue-class.md)

[JET_ENUMCOLUMNVALUE 成員](./jet-enumcolumnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
