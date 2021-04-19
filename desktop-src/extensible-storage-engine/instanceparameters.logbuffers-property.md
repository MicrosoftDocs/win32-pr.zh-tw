---
description: 深入瞭解： InstanceParameters. LogBuffers 屬性
title: InstanceParameters. LogBuffers 屬性
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994456"
---
# <a name="instanceparameterslogbuffers-property"></a>InstanceParameters. LogBuffers 屬性

取得或設定在將記錄寫入交易記錄檔之前，用來快取記錄檔記錄的記憶體數量。 此參數的單位是保存交易記錄檔之磁片區的磁區大小。 磁區大小幾乎一律為512個位元組，因此可以安全地假設該單位的大小。 此參數會對效能造成影響。 當資料庫引擎處於大量更新負載時，此緩衝區可能會非常快速地完成。 交易記錄檔較大的快取大小，對於在這種高負載狀況下的良好更新效能來說非常重要。 在此情況下，已知的預設值太小。 請勿將此參數設定為大於交易記錄檔大小一半的緩衝區數 (以位元組為單位) 。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[InstanceParameters 成員](./instanceparameters-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
