---
description: 深入瞭解： IndexInfo 的索引鍵屬性
title: IndexInfo 索引鍵屬性
TOCTitle: 'Keys property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.IndexInfo.Keys
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo.keys(v=EXCHG.10)
ms:contentKeyID: 55103265
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexInfo.Keys
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexInfo.Keys
- Microsoft.Isam.Esent.Interop.IndexInfo.get_Keys
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d96f9a6e92aeba02bf29ff53fff5f9f4a6c13b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980717"
---
# <a name="indexinfokeys-property"></a>IndexInfo 索引鍵屬性

取得索引中的唯一索引鍵數目。 此值不是最新值，而且只會由 JetComputeStats 更新。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property Keys As Integer
    Get
'Usage
Dim instance As IndexInfo
Dim value As Integer

value = instance.Keys
```

``` csharp
public int Keys { get; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[IndexInfo 類別](./indexinfo-class.md)

[IndexInfo 成員](./indexinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
