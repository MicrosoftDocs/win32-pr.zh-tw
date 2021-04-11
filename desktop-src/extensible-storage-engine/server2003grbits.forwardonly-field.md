---
description: 深入瞭解： Server2003Grbits. ForwardOnly 欄位
title: 'Server2003Grbits. ForwardOnly 欄位 (欄位，Server2003) '
TOCTitle: ForwardOnly field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.forwardonly(v=EXCHG.10)
ms:contentKeyID: 55104214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec4427628e8d6bfee427fa91c15ed6aee3887314
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114041"
---
# <a name="server2003grbitsforwardonly-field"></a>Server2003Grbits. ForwardOnly 欄位

如果臨時表管理員可以使用針對中繼查詢結果優化的執行，此選項會要求只建立臨時表。 如果臨時表的任何特性會防止使用這項優化，則作業會失敗並 JET_errCannotMaterializeForwardOnlySort。 此選項的副作用是允許臨時表包含具有重複索引鍵的記錄。 如需詳細資訊，請參閱 [唯一](./temptablegrbit-enumeration.md) 的。

**命名空間：**  [Microsoft Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Const ForwardOnly As TempTableGrbit
'Usage
Dim value As TempTableGrbit

value = Server2003Grbits.ForwardOnly
```

``` csharp
public const TempTableGrbit ForwardOnly
```

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Server2003Grbits 類別](./server2003grbits-class.md)

[Server2003Grbits 成員](./server2003grbits-members.md)

[Server2003 命名空間。](./microsoft.isam.esent.interop.server2003-namespace.md)
