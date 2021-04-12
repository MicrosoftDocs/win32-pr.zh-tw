---
description: 當您呼叫 SymInitialize 函式，並將 fInvadeProcess 參數設為 TRUE，或當您呼叫 SymLoadModuleEx 函數來指定模組時，符號處理常式會載入符號。
ms.assetid: fae1895e-9fed-45e3-8ecf-4c6cc67a6094
title: 符號載入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705a7af3525c784b2bbcd512b267309a466a11c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385872"
---
# <a name="symbol-loading"></a>符號載入

當您呼叫 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 函式，並將 *fInvadeProcess* 參數設為 **TRUE** ，或當您呼叫 [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) 函數來指定模組時，符號處理常式會載入符號。 無論是哪一種情況，符號處理常式都會載入符號或延遲符號載入，直到要求符號為止，視 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) 函式所設定的選項而定。

符號處理常式可用來取出任何模組的符號資訊;它不需要與 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 呼叫中指定的進程相關聯。 若要使用任意模組，請在 *ImageName* 參數中指定模組映射的完整路徑。 您可以使用任何 ( .exe、.dll、winspool.drv、sys、.scr、cpl 或 .com) 的可執行模組的路徑。 使用 *BaseOfDll* 參數來指定任何載入位址，然後符號位址會以該位址為基礎。

您可能不需要在應用程式的持續時間內載入符號模組。 若要從符號處理常式的模組清單中釋放符號模組，請使用 [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule) 函數。 此函式會釋放配置給符號模組的記憶體。 若要再次使用該模組的符號，您必須呼叫 [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) 函式，即使已設定符號延後載入選項也一樣。

## <a name="diagnosing-symbol-load-problems"></a>診斷符號載入問題

若要查看所有載入符號的嘗試，請使用 SYMOPT DEBUG 來呼叫 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) \_ 。 這會導致 DbgHelp 使用符號搜尋的詳細資訊（例如搜尋的目錄和錯誤訊息）來呼叫 [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) 函數。 如果您的程式碼使用 [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)，DbgHelp 會呼叫您的回呼函式，而不是呼叫 **OutputDebugString**。 *ActionCode* 參數會設定為 CBA \_ DEBUG \_ INFO，而 *CallbackData* 參數是可顯示的字串。

若要讓此偵錯工具輸出顯示到主控台，而不變更您的原始程式碼，請將 DBGHELP \_ DBGOUT 環境變數設定為非 **Null** 值，然後再呼叫 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 函式。 若要將資訊記錄到檔案中，請將 DBGHELP \_ 記錄環境變數設定為要使用的記錄檔名稱。

請注意，只有在需要時才應該使用這些功能。 它們可能會讓包含許多符號的模組的符號載入變慢。

 

 
