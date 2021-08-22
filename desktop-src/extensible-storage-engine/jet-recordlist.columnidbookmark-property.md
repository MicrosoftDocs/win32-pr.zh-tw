---
description: 深入瞭解： JET_RECORDLIST columnidBookmark 屬性
title: JET_RECORDLIST columnidBookmark 屬性
TOCTitle: 'columnidBookmark property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recordlist.columnidbookmark(v=EXCHG.10)
ms:contentKeyID: 55103827
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.get_columnidBookmark
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.set_columnidBookmark
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122462a3d809b59e4b3b17d5ecf82e342fac06267da7aae2875407b69b44deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730408"
---
# <a name="jet_recordlistcolumnidbookmark-property"></a>JET_RECORDLIST columnidBookmark 屬性

取得臨時表中的資料行 columnid，此資料行會儲存記錄的書簽。 資料行的類型為 JET_coltyp。文本。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property columnidBookmark As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_RECORDLIST
Dim value As JET_COLUMNID

value = instance.columnidBookmark
```

``` csharp
public JET_COLUMNID columnidBookmark { get; internal set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RECORDLIST 類別](./jet-recordlist-class.md)

[JET_RECORDLIST 成員](./jet-recordlist-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
