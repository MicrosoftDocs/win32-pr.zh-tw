---
description: 若要將已經在執行中的處理常式，偵錯工具應該使用 DebugActiveProcess 搭配處理序識別碼。 若要取出進程識別碼的清單，請使用 EnumProcesses 或 Process32First 函式。
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: 正在執行進程的偵錯工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d184907bb66a651f04a5e144e40bf5955a672
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109992"
---
# <a name="debugging-a-running-process"></a>正在執行進程的偵錯工具

若要將已經在執行中的處理常式，偵錯工具應該使用 [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) 搭配處理序識別碼。 若要取出進程識別碼的清單，請使用 [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) 或 [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) 函式。

[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) 會將偵錯工具附加至使用中的進程。 在此情況下，只有使用中的進程可以進行調試;其子進程無法進行。 偵錯工具必須具有執行中進程的適當存取權，才能使用 **DebugActiveProcess**。 如需存取權限的詳細資訊，請參閱 [存取控制](../secauthz/access-control.md)。

當偵錯工具已建立或附加至它想要進行偵錯工具的程式之後，系統會將進程中發生之所有偵測事件的偵錯工具，以及在任何子進程中（如果有指定）通知偵錯工具。 如需有關偵錯工具事件的詳細資訊，請參閱 [偵錯工具事件](debugging-events.md)。

若要從正在進行調試的進程卸離，偵錯工具應該使用 [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) 函數。

 

 
