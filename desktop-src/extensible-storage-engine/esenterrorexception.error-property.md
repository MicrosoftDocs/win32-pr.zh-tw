---
description: 深入瞭解： EsentErrorException。 Error 屬性
title: EsentErrorException。 Error 屬性
TOCTitle: 'Error property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentErrorException.Error
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.error(v=EXCHG.10)
ms:contentKeyID: 55101646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.Error
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.get_Error
- Microsoft.Isam.Esent.Interop.EsentErrorException.Error
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: db54808d630ccbb976f36325a176a2da416bb236da25dc40ded2b029a3bb81a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118269959"
---
# <a name="esenterrorexceptionerror-property"></a>EsentErrorException。 Error 屬性

取得這個例外狀況的基礎 Esent 錯誤。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property Error As JET_err
    Get
'Usage
Dim instance As EsentErrorException
Dim value As JET_err

value = instance.Error
```

``` csharp
public JET_err Error { get; }
```

#### <a name="property-value"></a>屬性值

類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentErrorException 類別](./esenterrorexception-class.md)

[EsentErrorException 成員](./esenterrorexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
