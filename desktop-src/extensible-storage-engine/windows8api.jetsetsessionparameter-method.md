---
description: 深入瞭解： Windows8Api. JetSetSessionParameter 方法
title: 'Windows8Api. JetSetSessionParameter 方法 (Windows8 的) '
TOCTitle: 'JetSetSessionParameter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetsessionparameter(v=EXCHG.10)
ms:contentKeyID: 55104461
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b73331c765e1f8026b39c28dde5268417601663c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848381"
---
# <a name="windows8apijetsetsessionparameter-method"></a>Windows8Api. JetSetSessionParameter 方法

在提供的會話狀態上設定參數，用於此會話的存留期，或在重設之前使用。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetSetSessionParameter ( _
    sesid As JET_SESID, _
    sesparamid As JET_sesparam, _
    data As Byte(), _
    dataSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim sesparamid As JET_sesparam
Dim data As Byte()
Dim dataSize As IntegerWindows8Api.JetSetSessionParameter(sesid, _
    sesparamid, data, dataSize)
```

``` csharp
public static void JetSetSessionParameter(
    JET_SESID sesid,
    JET_sesparam sesparamid,
    byte[] data,
    int dataSize
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要在其上設定參數的會話。

<!-- end list -->

  - sesparamid  
    類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)  
    
    要設定之會話參數的識別碼。

<!-- end list -->

  - data  
    類型： \[\]  
    
    要在此會話參數中設定的資料。

<!-- end list -->

  - dataSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    所提供資料的大小。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows8Api 類別](./windows8api-class.md)

[Windows8Api 成員](./windows8api-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
