---
description: 深入瞭解： IContentEquatable <T> 介面
title: IContentEquatable (T) 介面
TOCTitle: IContentEquatable(T) interface
ms:assetid: T:Microsoft.Isam.Esent.Interop.IContentEquatable`1
ms:mtpsurl: https://msdn.microsoft.com/library/Hh578046(v=EXCHG.10)
ms:contentKeyID: 39511318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02e237714f020f5bafa3ce8b7465f1c8e2615c01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974981"
---
# <a name="icontentequatablet-interface"></a>IContentEquatable \<T\> 介面

物件的介面，其內容可以彼此比較。 這應該用於覆寫 Equals () 的可變參考物件的相等比較，而 GetHashCode () 並不是個好主意。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Interface IContentEquatable(Of T)
'Usage
Dim instance As IContentEquatable(Of T)
```

``` csharp
public interface IContentEquatable<T>
```

#### <a name="type-parameters"></a>型別參數

  - T  
    要 comapre 的物件類型。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[IContentEquatable \<T\> 成員](./icontentequatable-t-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
