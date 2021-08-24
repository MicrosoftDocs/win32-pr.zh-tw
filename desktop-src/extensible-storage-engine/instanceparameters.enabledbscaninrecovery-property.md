---
description: 深入瞭解： InstanceParameters. EnableDbScanInRecovery 屬性
title: InstanceParameters. EnableDbScanInRecovery 屬性
TOCTitle: 'EnableDbScanInRecovery property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enabledbscaninrecovery(v=EXCHG.10)
ms:contentKeyID: 55107448
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableDbScanInRecovery
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableDbScanInRecovery
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eeb1fc7b9e9cab89f25f5b17d72b36c95bb73bf7ae2f15a11bee64ece8fbb4cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834388"
---
# <a name="instanceparametersenabledbscaninrecovery-property"></a>InstanceParameters. EnableDbScanInRecovery 屬性

取得或設定值，指出是否應在復原期間執行資料庫維護。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property EnableDbScanInRecovery As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.EnableDbScanInRecovery

instance.EnableDbScanInRecovery = value
```

``` csharp
public int EnableDbScanInRecovery { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
