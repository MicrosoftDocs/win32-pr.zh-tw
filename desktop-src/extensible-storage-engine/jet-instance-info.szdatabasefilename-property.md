---
description: 深入瞭解： JET_INSTANCE_INFO szDatabaseFileName 屬性
title: JET_INSTANCE_INFO szDatabaseFileName 屬性
TOCTitle: 'szDatabaseFileName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.szdatabasefilename(v=EXCHG.10)
ms:contentKeyID: 55103711
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_szDatabaseFileName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bcf0360ea2c901c1fc68c97c8b29f222c1df2e9a65dacf87297e3b560ece0d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119272428"
---
# <a name="jet_instance_infoszdatabasefilename-property"></a>JET_INSTANCE_INFO szDatabaseFileName 屬性

取得字串的集合，每個字串都包含附加至資料庫實例的資料庫檔案名。 陣列具有 cDatabases 元素。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property szDatabaseFileName As IList(Of String)
    Get
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As IList(Of String)

value = instance.szDatabaseFileName
```

``` csharp
public IList<string> szDatabaseFileName { get; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.collections.generic.ilist-1) 。\<[String](/dotnet/api/system.string)\>  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INSTANCE_INFO 類別](./jet-instance-info-class.md)

[JET_INSTANCE_INFO 成員](./jet-instance-info-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
