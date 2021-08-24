---
description: 深入瞭解： JET_RSTMAP szNewDatabaseName 屬性
title: JET_RSTMAP szNewDatabaseName 屬性
TOCTitle: 'szNewDatabaseName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTMAP.szNewDatabaseName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstmap.sznewdatabasename(v=EXCHG.10)
ms:contentKeyID: 55103885
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.szNewDatabaseName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.set_szNewDatabaseName
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.szNewDatabaseName
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.get_szNewDatabaseName
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84a4e51129458479be28d9d1f04740bf211259945ca80a5c8648320b9c71cc96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833508"
---
# <a name="jet_rstmapsznewdatabasename-property"></a>JET_RSTMAP szNewDatabaseName 屬性

取得或設定資料庫的目前名稱/路徑。 不得為 null。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szNewDatabaseName As String
    Get
    Set
'Usage
Dim instance As JET_RSTMAP
Dim value As String

value = instance.szNewDatabaseName

instance.szNewDatabaseName = value
```

``` csharp
public string szNewDatabaseName { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.string](/dotnet/api/system.string)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RSTMAP 類別](./jet-rstmap-class.md)

[JET_RSTMAP 成員](./jet-rstmap-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
