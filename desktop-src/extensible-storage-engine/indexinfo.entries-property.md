---
description: 深入瞭解： IndexInfo 專案屬性
title: IndexInfo 專案屬性
TOCTitle: 'Entries property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.IndexInfo.Entries
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo.entries(v=EXCHG.10)
ms:contentKeyID: 55103234
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexInfo.Entries
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexInfo.get_Entries
- Microsoft.Isam.Esent.Interop.IndexInfo.Entries
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f03d5db27e607e8a3c76249e70b78768887d86a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975466"
---
# <a name="indexinfoentries-property"></a>IndexInfo 專案屬性

取得索引中的專案數。 此值不是最新值，而且只會由 JetComputeStats 更新。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property Entries As Integer
    Get
'Usage
Dim instance As IndexInfo
Dim value As Integer

value = instance.Entries
```

``` csharp
public int Entries { get; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[IndexInfo 類別](./indexinfo-class.md)

[IndexInfo 成員](./indexinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
