---
description: 深入瞭解： JET_SETINFO itagSequence 屬性
title: JET_SETINFO itagSequence 屬性
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c409903f90633f15daa8d289c72530db943f1c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112525"
---
# <a name="jet_setinfoitagsequence-property"></a>JET_SETINFO itagSequence 屬性

取得或設定要設定之多重值資料行中的值順序。 值的陣列是以一為基礎。 第一個值是 sequence 1，而不是 0 (零) 。 如果 [記錄] 資料行只有一個值，則如果要取代該值，則應將1當作 itagSequence 傳遞。 值為 0 (零) 表示將新的資料行值實例加入至資料行值序列的結尾。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SETINFO 類別](./jet-setinfo-class.md)

[JET_SETINFO 成員](./jet-setinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
