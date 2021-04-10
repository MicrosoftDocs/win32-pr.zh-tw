---
title: 與桌面的執行緒連接
description: 在處理常式連接到視窗工作站之後，系統會將桌面指派給進行連接的執行緒。
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104185996"
---
# <a name="thread-connection-to-a-desktop"></a>與桌面的執行緒連接

在處理常式連接到視窗工作站之後，系統會將桌面指派給進行連接的執行緒。 系統會根據下列規則，決定要指派給執行緒的桌面：

1.  如果執行緒已呼叫 [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) 函式，它會連接到指定的桌面。
2.  如果執行緒未呼叫 [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)，它會連接到繼承自父進程的桌面。
3.  如果執行緒未呼叫 [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) ，且未繼承桌面，系統會嘗試開啟以取得允許的最大 \_ 存取權，並連接至桌面，如下所示：
    -   如果在建立進程時所使用之 [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa)結構的 **lpDesktop** 成員中指定了桌面名稱，執行緒就會連接到指定的桌面。
    -   否則，執行緒會連接到進程所連接之視窗工作站的預設桌面。

呼叫 [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) 函式時，無法關閉在此連接過程中指派的桌面。

當處理常式連接到桌面時，系統會在進程的控制碼資料表中搜尋繼承的控制碼。 系統會使用它所找到的第一個桌面控制碼。 如果您想要讓子進程連接到特定的繼承桌面，您必須確定只將所需的控制碼標示為可繼承。 如果子進程繼承多個桌面控制碼，則桌面連接的結果為未定義。

系統在將進程連接到桌面時開啟的桌面的控制碼，無法繼承。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[處理與視窗工作站的連接](process-connection-to-a-window-station.md)
</dt> </dl>

 

 