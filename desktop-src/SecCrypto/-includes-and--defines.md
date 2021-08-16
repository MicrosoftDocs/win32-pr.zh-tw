---
description: 加密 SDK 檔中的所有範例都假設有下列 \# 包含和定義編譯器指示詞 \# 。
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#包含和 #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dbab2a3c33b510df99c9d2e0fa292af53c96fcc471dfe8180d9d4be06b3a5b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774273"
---
# <a name="includes-and-defines"></a>\#包含和 \# 定義

加密 SDK 檔中的所有範例都假設有下列 **\# 包含** 和 **\# 定義** 編譯器指示詞。


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



此外， **\_ WIN32 \_ WINNT** 常數必須適當地定義。 如需 **\_ WIN32 \_ WINNT** 的詳細資訊，請參閱 [使用 Windows 標頭](../winprog/using-the-windows-headers.md)。

 

 
