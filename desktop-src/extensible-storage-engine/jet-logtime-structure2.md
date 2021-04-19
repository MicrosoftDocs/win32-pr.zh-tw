---
description: 深入瞭解： JET_LOGTIME 結構
title: JET_LOGTIME 結構
TOCTitle: JET_LOGTIME structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LOGTIME
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime(v=EXCHG.10)
ms:contentKeyID: 39510198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617911c8f9f0246a836de11d9530536bf9c6e6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982091"
---
# <a name="jet_logtime-structure"></a>JET_LOGTIME 結構

描述日期/時間。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_LOGTIME _
    Implements IEquatable(Of JET_LOGTIME), IJET_LOGTIME,  _
    INullableJetStruct
'Usage
Dim instance As JET_LOGTIME
```

``` csharp
[SerializableAttribute]
public struct JET_LOGTIME : IEquatable<JET_LOGTIME>, 
    IJET_LOGTIME, INullableJetStruct
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_LOGTIME 成員](./jet-logtime-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
