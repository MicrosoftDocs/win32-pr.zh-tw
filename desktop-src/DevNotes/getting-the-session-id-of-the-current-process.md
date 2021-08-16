---
description: 下列範例 x86 元件程式碼會取得與目前進程相關聯的終端機服務會話識別碼。
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: 取得目前進程的會話識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4326020f145c98544132703611fbd783edac9ae9eb89a5c69f44b67dc997ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955977"
---
# <a name="getting-the-session-id-of-the-current-process"></a>取得目前進程的會話識別碼

\[此範例程式碼所指定的記憶體位址，在 Windows 的未來版本中可能會變更。 為確保您的應用程式會在未來繼續正常執行，您的應用程式必須呼叫 [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) ，然後 [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) ，而不是下列範例程式碼。\]

下列範例 x86 元件程式碼會取得與目前進程相關聯的終端機服務會話識別碼。

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
