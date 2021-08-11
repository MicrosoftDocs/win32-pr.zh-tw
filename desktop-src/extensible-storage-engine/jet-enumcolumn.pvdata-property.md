---
description: 深入瞭解： JET_ENUMCOLUMN pvData 屬性
title: JET_ENUMCOLUMN pvData 屬性
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103500
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df79d838277a849c99ea49af2a8ca12e77cb3667d4750b141f0b9247b46b9232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254690"
---
# <a name="jet_enumcolumnpvdata-property"></a>JET_ENUMCOLUMN pvData 屬性

取得為數據行列舉的值。 只有當 [err](./jet-enumcolumn.err-property.md) 等於 [ColumnSingleValue](./jet-wrn-enumeration.md)時，才會使用這個成員。 這會指向傳遞給[JetEnumerateColumns (JET_SESID、JET_TABLEID、Int32、 \[ \] 、int32、 \[ \] 、JET_PFNREALLOC、IntPtr、int32、EnumerateColumnsGrbit) ](./api.jetenumeratecolumns-method.md)的[JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)配置器回呼所配置的記憶體。 請記得在完成時釋放記憶體。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pvData As IntPtr
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
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

[JET_ENUMCOLUMN 類別](./jet-enumcolumn-class.md)

[JET_ENUMCOLUMN 成員](./jet-enumcolumn-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
