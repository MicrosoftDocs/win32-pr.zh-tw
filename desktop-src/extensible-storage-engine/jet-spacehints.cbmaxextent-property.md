---
description: 深入瞭解： JET_SPACEHINTS cbMaxExtent 屬性
title: JET_SPACEHINTS cbMaxExtent 屬性
TOCTitle: 'cbMaxExtent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.cbMaxExtent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints.cbmaxextent(v=EXCHG.10)
ms:contentKeyID: 55103979
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.cbMaxExtent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.get_cbMaxExtent
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.set_cbMaxExtent
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.cbMaxExtent
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8d95ada63fc6269dce6e21c4a7f3db04d1732a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689563"
---
# <a name="jet_spacehintscbmaxextent-property"></a>JET_SPACEHINTS cbMaxExtent 屬性

取得或設定值，這個值會設定 ulGrowth 的上限。 這個值是以位元組為單位。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbMaxExtent As Integer
    Get
    Set
'Usage
Dim instance As JET_SPACEHINTS
Dim value As Integer

value = instance.cbMaxExtent

instance.cbMaxExtent = value
```

``` csharp
public int cbMaxExtent { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SPACEHINTS 類別](./jet-spacehints-class.md)

[JET_SPACEHINTS 成員](./jet-spacehints-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
