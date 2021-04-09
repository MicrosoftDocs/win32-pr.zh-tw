---
description: 符號處理常式是設計來追蹤各種不同的符號檔集合。
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: 符號處理常式初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110201"
---
# <a name="symbol-handler-initialization"></a>符號處理常式初始化

符號處理常式是設計來追蹤各種不同的符號檔集合。

若要初始化符號處理常式，請呼叫 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 函數。 *HProcess* 參數可以是唯一的任一數字、 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)函數所傳回的值，或任何執行中進程的識別碼。 *FInvadeProcess* 參數會指出符號處理常式是否應該列舉進程載入的模組，並且載入其每個模組的符號。 如果 *fInvadeProcess* 為 **TRUE**， *HProcess* 參數必須是從 **GetCurrentProcess** 傳回的值或現有進程的識別碼。 若要重新整理此清單，請使用 [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) 函數。

使用 *fInvadeProcess* 是載入進程之所有符號檔的簡單方法。 不過，符號處理常式將不會嘗試載入 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式後續載入之模組的符號。 在此情況下，您必須使用 [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) 函數。

 

 
