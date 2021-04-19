---
description: 深入瞭解： JET_UNICODEINDEX dwMapFlags 屬性
title: JET_UNICODEINDEX dwMapFlags 屬性
TOCTitle: 'dwMapFlags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.dwmapflags(v=EXCHG.10)
ms:contentKeyID: 55103990
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.set_dwMapFlags
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.get_dwMapFlags
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a625da5f80271b52f6eff74a2427e749219e46a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990341"
---
# <a name="jet_unicodeindexdwmapflags-property"></a>JET_UNICODEINDEX dwMapFlags 屬性

取得或設定正規化 unicode 資料時，要與 LCMapString 搭配使用的旗標。

此 API 不符合 CLS 規範。 

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Property dwMapFlags As UInteger
    Get
    Set
'Usage
Dim instance As JET_UNICODEINDEX
Dim value As UInteger

value = instance.dwMapFlags

instance.dwMapFlags = value
```

``` csharp
[CLSCompliantAttribute(false)]
public uint dwMapFlags { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.uint32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_UNICODEINDEX 類別](./jet-unicodeindex-class.md)

[JET_UNICODEINDEX 成員](./jet-unicodeindex-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
