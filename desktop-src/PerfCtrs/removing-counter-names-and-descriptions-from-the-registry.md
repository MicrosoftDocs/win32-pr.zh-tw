---
description: Unlodctr 工具會移除 lodctr 所建立的登錄專案。
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: 從登錄中移除計數器名稱和描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ea8c0a8efbe9a798f980a061c6cfc65745b89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977319"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>從登錄中移除計數器名稱和描述

**Unlodctr** 工具會移除 **lodctr** 所建立的登錄專案。 您傳遞給 **unlodctr** 的應用程式名稱必須與您在 **服務** 金鑰下建立的 [應用程式金鑰名稱](creating-the-applications-performance-key.md)相符。 如需執行 **unlodctr** 的詳細資訊，請參閱說明及支援中心。

## <a name="using-unlodctr"></a>使用 unlodctr

**Unlodctr** 工具會查閱第一個和最後一個計數器，並在您的應用程式 **效能** 金鑰下使用類似的命名登錄值來協助索引值。 **Unlodctr** 工具會使用索引值的範圍來移除 **計數器** 的文字 **，以及每** 個語言識別項的說明值。

**Unlodctr** 會使用索引值對登錄進行下列變更。

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

**Unlodctr** 工具也會從應用程式的 **效能** 索引鍵中移除 **第一個計數器**、**最後一個計數器**、**第一個** 說明、**最後** 一個說明和 **物件清單** 值，其位於 **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ *應用程式名稱* \\ **效能**。

> [!Note]  
> **Unlodctr**， [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)的卸載函式是在 Loadperf 中宣告，並且從 Loadperf.dll 匯出。 這可讓您直接從卸載程式呼叫此函式。

 

 

 



