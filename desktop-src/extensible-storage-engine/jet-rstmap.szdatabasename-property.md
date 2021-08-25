---
description: 深入瞭解： JET_RSTMAP szDatabaseName 屬性
title: JET_RSTMAP szDatabaseName 屬性
TOCTitle: 'szDatabaseName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTMAP.szDatabaseName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstmap.szdatabasename(v=EXCHG.10)
ms:contentKeyID: 55103894
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.szDatabaseName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.get_szDatabaseName
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.set_szDatabaseName
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.szDatabaseName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a66be5a854abee395a910596686dbc0a7f16b588fe4567e574da3efcae38d53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850048"
---
# <a name="jet_rstmapszdatabasename-property"></a>JET_RSTMAP szDatabaseName 屬性

取得或設定資料庫的舊名稱/路徑。 如果未變更，則可以是 null。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szDatabaseName As String
    Get
    Set
'Usage
Dim instance As JET_RSTMAP
Dim value As String

value = instance.szDatabaseName

instance.szDatabaseName = value
```

``` csharp
public string szDatabaseName { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.string](/dotnet/api/system.string)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RSTMAP 類別](./jet-rstmap-class.md)

[JET_RSTMAP 成員](./jet-rstmap-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
