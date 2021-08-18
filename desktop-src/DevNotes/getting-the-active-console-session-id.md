---
description: 下列 Winternl 定義是作用中終端機服務主控台會話識別碼的靜態記憶體位址。 此使用中的主控台會話識別碼未在 Windows XP 之前的 Microsoft Windows 作業系統版本中定義。
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: 取得使用中的主控台會話識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f7b23669240f0cd109a48f454ee6f6329f6839221a1677e81b75712430cb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002298"
---
# <a name="getting-the-active-console-session-id"></a>取得使用中的主控台會話識別碼

下列 Winternl 定義是作用中終端機服務主控台會話識別碼的靜態記憶體位址。 此使用中的主控台會話識別碼未在 Windows XP 之前的 Microsoft Windows 作業系統版本中定義。

> [!Note]  
> Windows 的未來版本中，此定義可能會變更。 為確保您的應用程式會在未來繼續正常執行，您的應用程式必須呼叫 [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid)。

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
