---
description: 深入瞭解： JET_UNICODEINDEX。GetEffectiveLocaleName 方法
title: JET_UNICODEINDEX。GetEffectiveLocaleName 方法
TOCTitle: 'GetEffectiveLocaleName method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.geteffectivelocalename(v=EXCHG.10)
ms:contentKeyID: 55103988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10932398e022701b76be19c3ea7949ce4cfd45b5a159ae5362e7f0e6a0e427bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979078"
---
# <a name="jet_unicodeindexgeteffectivelocalename-method"></a>JET_UNICODEINDEX。GetEffectiveLocaleName 方法

為了因應沒有 LCID 支援之系統的因應措施，我們會將非常有限數目的 Lcid 轉換成地區設定名稱。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function GetEffectiveLocaleName As String
'Usage
Dim instance As JET_UNICODEINDEX
Dim returnValue As String

returnValue = instance.GetEffectiveLocaleName()
```

``` csharp
public string GetEffectiveLocaleName()
```

#### <a name="return-value"></a>傳回值

類型： [system.string](/dotnet/api/system.string)  
BCP-47 樣式的地區設定名稱。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_UNICODEINDEX 類別](./jet-unicodeindex-class.md)

[JET_UNICODEINDEX 成員](./jet-unicodeindex-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
