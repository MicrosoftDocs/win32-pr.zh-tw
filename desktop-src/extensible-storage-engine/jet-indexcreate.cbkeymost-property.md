---
description: 深入瞭解： JET_INDEXCREATE cbKeyMost 屬性
title: JET_INDEXCREATE cbKeyMost 屬性
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17908b19cba3ed047b98f4532982001019516d9b32e2799c29a6671cbd862fe7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119232678"
---
# <a name="jet_indexcreatecbkeymost-property"></a>JET_INDEXCREATE cbKeyMost 屬性

取得或設定索引中索引鍵允許的大小上限（以位元組為單位）。 最小支援的金鑰大小為 JET_cbKeyMostMin (255) 這是舊版的最大金鑰大小。 最大索引鍵大小取決於資料庫頁面大小 [DatabasePageSize](./jet-param-enumeration.md)。 您可以使用 [KeyMost](./systemparameters.keymost-property.md)抓取最大的索引鍵大小。 Windows XP 和 Windows Server 2003 會忽略此參數。 不同于非受控 API，不需要 **IndexKeyMost ()** (JET_bitIndexKeyMost) ，它會自動加入。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXCREATE 類別](./jet-indexcreate-class.md)

[JET_INDEXCREATE 成員](./jet-indexcreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
