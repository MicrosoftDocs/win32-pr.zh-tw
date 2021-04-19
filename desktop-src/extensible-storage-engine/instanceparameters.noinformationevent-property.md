---
description: 深入瞭解： InstanceParameters. NoInformationEvent 屬性
title: InstanceParameters. NoInformationEvent 屬性
TOCTitle: 'NoInformationEvent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.NoInformationEvent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.noinformationevent(v=EXCHG.10)
ms:contentKeyID: 55103564
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.NoInformationEvent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_NoInformationEvent
- Microsoft.Isam.Esent.Interop.InstanceParameters.NoInformationEvent
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_NoInformationEvent
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0e9b933dc477011c1835da5b95fc6ed11902827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990461"
---
# <a name="instanceparametersnoinformationevent-property"></a>InstanceParameters. NoInformationEvent 屬性

取得或設定值，這個值表示是否會隱藏資料庫引擎通常會產生的資訊事件記錄檔訊息。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property NoInformationEvent As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.NoInformationEvent

instance.NoInformationEvent = value
```

``` csharp
public bool NoInformationEvent { get; set; }
```

#### <a name="property-value"></a>屬性值

型別： [system.object](/dotnet/api/system.boolean)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
