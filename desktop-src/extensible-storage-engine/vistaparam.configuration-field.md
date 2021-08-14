---
description: 深入瞭解： VistaParam.Configuration 欄位
title: 'VistaParam.Configuration 欄位 (的 Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2e3aeea82a74698243f9a9ba9114c6c91ac34984a505d70d58126daca65d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119356258"
---
# <a name="vistaparamconfiguration-field"></a>VistaParam.Configuration 欄位

此參數會針對整組系統參數公開多組預設值。 當此參數設定為特定設定時，所有系統參數值都會重設為該設定的預設值。 如果設定特定實例的設定，則全域系統參數將不會重設為其預設值。 Small Configuration (0) ：資料庫引擎已針對記憶體使用量優化。 舊版設定 (1) ：資料庫引擎有其傳統預設值。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[VistaParam 類別](./vistaparam-class.md)

[VistaParam 成員](./vistaparam-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
