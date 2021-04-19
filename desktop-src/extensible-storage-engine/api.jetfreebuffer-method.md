---
description: 深入瞭解： JetFreeBuffer 方法
title: JetFreeBuffer 方法
TOCTitle: 'JetFreeBuffer method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer(System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetfreebuffer(v=EXCHG.10)
ms:contentKeyID: 55100694
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a584caf0f7c59c77e7d3c4a058a03780043e0f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973820"
---
# <a name="apijetfreebuffer-method"></a>JetFreeBuffer 方法

釋出由 database engine 呼叫所配置的記憶體。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetFreeBuffer ( _
    buffer As IntPtr _
)
'Usage
Dim buffer As IntPtrApi.JetFreeBuffer(buffer)
```

``` csharp
public static void JetFreeBuffer(
    IntPtr buffer
)
```

#### <a name="parameters"></a>參數

  - 緩衝區  
    類型： [system.object](/dotnet/api/system.intptr)  
    
    由資料庫引擎的呼叫所配置的緩衝區。 [零](/dotnet/api/system.intptr.zero) 是可接受的，將會被忽略。

## <a name="remarks"></a>備註

這個方法是內部的，因為我們絕對不會將 ESENT 所配置的記憶體公開給呼叫者。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
