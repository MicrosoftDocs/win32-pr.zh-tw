---
description: '深入瞭解：實例的函式 (字串、字串、TermGrbit) '
title: '實例的函式 (字串、字串、TermGrbit) '
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691328"
---
# <a name="instance-constructor-string-string-termgrbit"></a>實例的函式 (字串、字串、TermGrbit) 

初始化實例類別的新實例。 已配置但未初始化基礎 JET_INSTANCE。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
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

<!-- end list -->

  - termGrbit  
    型別： [TermGrbit](./termgrbit-enumeration.md) 。  
    
    要在 JetTerm 階段使用的 TermGrbit。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Instance 類別](./instance-class.md)

[實例成員](./instance-members.md)

[實例多載](./instance-constructor.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
