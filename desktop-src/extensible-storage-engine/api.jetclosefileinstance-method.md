---
description: 深入瞭解： JetCloseFileInstance 方法
title: JetCloseFileInstance 方法
TOCTitle: 'JetCloseFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosefileinstance(v=EXCHG.10)
ms:contentKeyID: 55100663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04ca76f5c96a34c6cd552eefc6ff383e6ca31634b03f33637674fa7b347b22d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983518"
---
# <a name="apijetclosefileinstance-method"></a>JetCloseFileInstance 方法

當使用 JetReadFileInstance 解壓縮該檔案中的資料之後，關閉以 JetOpenFileInstance 開啟的檔案。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetCloseFileInstance ( _
    instance As JET_INSTANCE, _
    handle As JET_HANDLE _
)
'Usage
Dim instance As JET_INSTANCE
Dim handle As JET_HANDLEApi.JetCloseFileInstance(instance, _
    handle)
```

``` csharp
public static void JetCloseFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE handle
)
```

#### <a name="parameters"></a>參數

  - instance  
    類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    要使用的實例。

<!-- end list -->

  - 處理  
    類型： [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    要關閉的控制碼。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
