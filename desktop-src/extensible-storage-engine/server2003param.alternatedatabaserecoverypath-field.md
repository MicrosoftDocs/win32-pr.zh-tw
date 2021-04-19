---
description: 深入瞭解： Server2003Param. AlternateDatabaseRecoveryPath 欄位
title: 'Server2003Param. AlternateDatabaseRecoveryPath 欄位 (欄位，Server2003) '
TOCTitle: AlternateDatabaseRecoveryPath field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003param.alternatedatabaserecoverypath(v=EXCHG.10)
ms:contentKeyID: 55104217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 770ac27596b4385d0012cb65847754b4deb7e9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974144"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a>Server2003Param. AlternateDatabaseRecoveryPath 欄位

在執行時間，會將每個資料庫的完整路徑保存在交易記錄中。 一般來說，這些資料庫必須保留在原始位置，才能讓交易重新執行正常運作。 這個參數可以用來強制損毀復原或還原作業，以便在指定的資料夾中，尋找交易記錄中所參考的資料庫。

**命名空間：**  [Microsoft Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Const AlternateDatabaseRecoveryPath As JET_param
'Usage
Dim value As JET_param

value = Server2003Param.AlternateDatabaseRecoveryPath
```

``` csharp
public const JET_param AlternateDatabaseRecoveryPath
```

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Server2003Param 類別](./server2003param-class.md)

[Server2003Param 成員](./server2003param-members.md)

[Server2003 命名空間。](./microsoft.isam.esent.interop.server2003-namespace.md)
