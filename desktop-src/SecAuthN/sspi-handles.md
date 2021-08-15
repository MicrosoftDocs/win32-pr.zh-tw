---
description: 列出 SSPI API 使用的控制碼。
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: SSPI 控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38fadebea7ff6b32f0058106595718a24d589854a662ef7b504ce6d7e8e5bc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916967"
---
# <a name="sspi-handles"></a>SSPI 控制碼

SSPI 會使用下列控制碼類型以及這些控制碼的指標：

-   **SecHandle** 和 **PSecHandle**
-   **CredHandle** 和 **PCredHandle**
-   **CtxtHandle** 和 **PCtxtHandle**

這些控制碼類型的控制碼型別和指標定義如下。


```C++
typedef struct _SecHandle {
  ULONG_PTR       dwLower;
  ULONG_PTR       dwUpper;
} SecHandle, * PSecHandle;

typedef SecHandle    CredHandle;
typedef PSecHandle   PCredHandle;

typedef SecHandle    CtxtHandle;
typedef PSecHandle   PCtxtHandle;
```



 

 



