---
description: 深入瞭解： JET_DBINFOMISC genMinRequired 屬性
title: JET_DBINFOMISC genMinRequired 屬性
TOCTitle: 'genMinRequired property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genMinRequired
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.genminrequired(v=EXCHG.10)
ms:contentKeyID: 39514817
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genMinRequired
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_genMinRequired
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_genMinRequired
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genMinRequired
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55a202e171e82f85511b30c1f0a590a846b02a57e88289d5cd7a2852c5c5f917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017228"
---
# <a name="jet_dbinfomiscgenminrequired-property"></a>JET_DBINFOMISC genMinRequired 屬性

取得重新執行記錄所需的最小記錄檔產生。 通常是檢查點產生。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property genMinRequired As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Integer

value = instance.genMinRequired
```

``` csharp
public int genMinRequired { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
