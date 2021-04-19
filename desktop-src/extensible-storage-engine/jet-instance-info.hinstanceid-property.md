---
description: 深入瞭解： JET_INSTANCE_INFO hInstanceId 屬性
title: JET_INSTANCE_INFO hInstanceId 屬性
TOCTitle: 'hInstanceId property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.hInstanceId
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.hinstanceid(v=EXCHG.10)
ms:contentKeyID: 55103700
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.hInstanceId
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.set_hInstanceId
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.hInstanceId
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_hInstanceId
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9fb86352ac2975022b9bc29c9c02a5940f5071d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988331"
---
# <a name="jet_instance_infohinstanceid-property"></a>JET_INSTANCE_INFO hInstanceId 屬性

取得指定實例的 JET_INSTANCE。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property hInstanceId As JET_INSTANCE
    Get
    Private Set
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As JET_INSTANCE

value = instance.hInstanceId
```

``` csharp
public JET_INSTANCE hInstanceId { get; private set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INSTANCE_INFO 類別](./jet-instance-info-class.md)

[JET_INSTANCE_INFO 成員](./jet-instance-info-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
