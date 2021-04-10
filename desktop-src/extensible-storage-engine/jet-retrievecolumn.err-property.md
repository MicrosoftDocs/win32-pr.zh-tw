---
description: 深入瞭解： JET_RETRIEVECOLUMN err 屬性
title: JET_RETRIEVECOLUMN err 屬性
TOCTitle: 'err property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.err
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.err(v=EXCHG.10)
ms:contentKeyID: 55103814
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.err
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.err
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_err
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_err
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a4d0a66a93485ba6e5ff70540182ef07588d3aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026846"
---
# <a name="jet_retrievecolumnerr-property"></a>JET_RETRIEVECOLUMN err 屬性

取得從資料行抓取傳回的警告。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property err As JET_wrn
    Get
    Private Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As JET_wrn

value = instance.err
```

``` csharp
public JET_wrn err { get; private set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RETRIEVECOLUMN 類別](./jet-retrievecolumn-class.md)

[JET_RETRIEVECOLUMN 成員](./jet-retrievecolumn-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
