---
description: 深入瞭解： InstanceParameters. TempDirectory 屬性
title: InstanceParameters. TempDirectory 屬性
TOCTitle: 'TempDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.tempdirectory(v=EXCHG.10)
ms:contentKeyID: 55103324
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_TempDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_TempDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bbe31b7f437f045f601b18daf92877784d58512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945367"
---
# <a name="instanceparameterstempdirectory-property"></a>InstanceParameters. TempDirectory 屬性

取得或設定資料夾的相對或絕對檔案系統路徑，其中將包含實例的暫存資料庫。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property TempDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.TempDirectory

instance.TempDirectory = value
```

``` csharp
public string TempDirectory { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.string](/dotnet/api/system.string)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
