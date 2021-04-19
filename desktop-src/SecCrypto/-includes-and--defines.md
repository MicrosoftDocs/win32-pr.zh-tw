---
description: 加密 SDK 檔中的所有範例都假設有下列 \# 包含和定義編譯器指示詞 \# 。
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#包含和 #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9834fd8103b9fd28a01e416bd1df8b03fb7ad680
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "107000521"
---
# <a name="includes-and-defines"></a><span data-ttu-id="981a2-103">\#包含和 \# 定義</span><span class="sxs-lookup"><span data-stu-id="981a2-103">\#includes and \#defines</span></span>

<span data-ttu-id="981a2-104">加密 SDK 檔中的所有範例都假設有下列 **\# 包含** 和 **\# 定義** 編譯器指示詞。</span><span class="sxs-lookup"><span data-stu-id="981a2-104">All of the examples in the Cryptography SDK documentation are assumed to have the following **\#include** and **\#define** compiler directives.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



<span data-ttu-id="981a2-105">此外， **\_ WIN32 \_ WINNT** 常數必須適當地定義。</span><span class="sxs-lookup"><span data-stu-id="981a2-105">Additionally, the **\_WIN32\_WINNT** constant must be appropriately defined.</span></span> <span data-ttu-id="981a2-106">如需 **\_ WIN32 \_ WINNT** 的詳細資訊，請參閱 [使用 Windows 標頭](../winprog/using-the-windows-headers.md)。</span><span class="sxs-lookup"><span data-stu-id="981a2-106">For more information about **\_WIN32\_WINNT**, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

 

 
