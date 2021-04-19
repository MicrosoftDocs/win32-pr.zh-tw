---
description: 深入瞭解： Server2003Grbits. EnumerateIgnoreUserDefinedDefault 欄位
title: 'Server2003Grbits. EnumerateIgnoreUserDefinedDefault 欄位 (欄位，Server2003) '
TOCTitle: EnumerateIgnoreUserDefinedDefault field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.enumerateignoreuserdefineddefault(v=EXCHG.10)
ms:contentKeyID: 55104099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 508565c518b67d31b0299014817b669f9484f743
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992468"
---
# <a name="server2003grbitsenumerateignoreuserdefineddefault-field"></a>Server2003Grbits. EnumerateIgnoreUserDefinedDefault 欄位

如果指定的資料行不存在於記錄中，而且它具有使用者定義的預設值，則不會傳回任何資料行值。 此選項可防止在列舉該資料行的值時，計算資料行之使用者定義預設值的回呼。

**命名空間：**  [Microsoft Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Const EnumerateIgnoreUserDefinedDefault As EnumerateColumnsGrbit
'Usage
Dim value As EnumerateColumnsGrbit

value = Server2003Grbits.EnumerateIgnoreUserDefinedDefault
```

``` csharp
public const EnumerateColumnsGrbit EnumerateIgnoreUserDefinedDefault
```

## <a name="remarks"></a>備註

此選項僅適用于 Windows Server 2003 SP1 和更新版本的作業系統。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Server2003Grbits 類別](./server2003grbits-class.md)

[Server2003Grbits 成員](./server2003grbits-members.md)

[Server2003 命名空間。](./microsoft.isam.esent.interop.server2003-namespace.md)
