---
description: 深入瞭解： JET_OPENTEMPORARYTABLE pidxunicode 屬性
title: 'JET_OPENTEMPORARYTABLE. pidxunicode 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98e5beb4f4523f5e6a6da37a999b6c0a2ab7b4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978377"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a>JET_OPENTEMPORARYTABLE pidxunicode 屬性

取得或設定要用來比較臨時表中任何 Unicode 索引鍵資料行資料的地區設定識別碼和正規化旗標。 當此參數為 null 時，預設的 LCID 將用來比較臨時表中的任何 Unicode 索引鍵資料行。 預設的 LCID 是美國英文地區設定。 當此參數為 null 時，將會使用預設正規化旗標來比較臨時表中的任何 Unicode 索引鍵資料行資料。 預設正規化旗標為： NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_OPENTEMPORARYTABLE 類別](./jet-opentemporarytable-class.md)

[JET_OPENTEMPORARYTABLE 成員](./jet-opentemporarytable-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
