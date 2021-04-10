---
description: OutputDebugString 函式會藉由產生輸出 \_ DEBUG \_ 字串事件的偵錯工具，從正在調試的進程傳送字串至偵錯工具 \_ 。 進程可以藉由呼叫 IsDebuggerPresent 函式來偵測是否正在進行調試。
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: 與偵錯工具通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846948"
---
# <a name="communicating-with-the-debugger"></a>與偵錯工具通訊

[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)函式會藉由產生輸出 \_ DEBUG \_ 字串事件的偵錯工具，從正在調試的進程傳送字串至偵錯工具 \_ 。 進程可以藉由呼叫 [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) 函式來偵測是否正在進行調試。

[**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)函式會在目前的進程中造成中斷點例外狀況。 中斷點是程式中停止執行的位置，可讓開發人員檢查程式的程式碼、變數和暫存器值，並視需要進行變更、繼續執行或終止執行。

[**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)函式會終止目前的進程，並提供偵錯工具的執行控制權，但與 [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)不同的是，它不會產生例外狀況。 這個函式只能用來做為最後的手段，因為它不一定會釋放進程的記憶體或關閉其檔案。

 

 
