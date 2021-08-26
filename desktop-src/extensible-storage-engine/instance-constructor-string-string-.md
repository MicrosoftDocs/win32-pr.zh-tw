---
description: '深入瞭解：實例的函式 (字串、字串) '
title: '實例的函式 (字串，字串) '
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d93a5799a646a90688261bdd55bc9dfe929ef6bd074a51e15cabdcee768ffa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116438"
---
# <a name="instance-constructor-string-string"></a>實例的函式 (字串，字串) 

初始化實例類別的新實例。 已配置但未初始化基礎 JET_INSTANCE。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a>參數

  - NAME  
    類型： [system.string](/dotnet/api/system.string)  
    
    執行個體的名稱。 這個字串在主控資料庫引擎的指定進程內必須是唯一的。

<!-- end list -->

  - displayName  
    類型： [system.string](/dotnet/api/system.string)  
    
    實例的顯示名稱。 這將用於 eventlog 專案中。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Instance 類別](./instance-class.md)

[實例成員](./instance-members.md)

[實例多載](./instance-constructor.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
