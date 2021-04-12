---
title: 端點
description: 設定 COM 應用程式使用指定的 TCP 通訊埠編號進行 DCOM 通訊。
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- 端點登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0addcd6c09b409629bb4a7157241d57476cafe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372033"
---
# <a name="endpoints"></a>端點

設定 COM 應用程式使用指定的 TCP 通訊埠編號進行 DCOM 通訊。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>備註

這是 **REG \_ 多重 \_ SZ** 值。

*埠* 值為介於1024到65535之間的數位，指定 COM 應用程式將用於 DCOM 通訊的 TCP 埠號碼。 如果您未指定此登錄機碼，則會動態指派 DCOM 通訊的埠號碼。 在大部分的情況下，您可能會想要讓此登錄機碼保持未定義狀態，並允許 DCOM 動態指派埠號碼。

 

 




