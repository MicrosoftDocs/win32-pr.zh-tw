---
description: 深入瞭解： JET_TABLECREATE szTemplateTableName 屬性
title: JET_TABLECREATE szTemplateTableName 屬性
TOCTitle: 'szTemplateTableName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szTemplateTableName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.sztemplatetablename(v=EXCHG.10)
ms:contentKeyID: 55103961
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szTemplateTableName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szTemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_szTemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_szTemplateTableName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3820c514851569a5f846256f513a06d2ecf9610da02b3017c78d2c162560dad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729048"
---
# <a name="jet_tablecreatesztemplatetablename-property"></a>JET_TABLECREATE szTemplateTableName 屬性

取得或設定要繼承基底 DDL 之資料表的名稱。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szTemplateTableName As String
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As String

value = instance.szTemplateTableName

instance.szTemplateTableName = value
```

``` csharp
public string szTemplateTableName { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.string](/dotnet/api/system.string)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_TABLECREATE 類別](./jet-tablecreate-class.md)

[JET_TABLECREATE 成員](./jet-tablecreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
