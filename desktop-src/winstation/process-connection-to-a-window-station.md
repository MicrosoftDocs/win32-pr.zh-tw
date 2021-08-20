---
title: 處理與視窗工作站的連接
description: 程式會在第一次呼叫 USER32 或 GDI32 函式時，自動建立與視窗工作站和桌面的連接， (非視窗工作站和桌面函式) 。
ms.assetid: 280f69e7-5c99-41a7-94e3-da13deaac9f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c507546f57e16c4ac473baeaa1a82bfb8d8e6ed6a551ee2b70d8314b68112d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030692"
---
# <a name="process-connection-to-a-window-station"></a>處理與視窗工作站的連接

程式會在第一次呼叫 USER32 或 GDI32 函式時，自動建立與視窗工作站和桌面的連接， (非視窗工作站和桌面函式) 。 系統會根據下列規則，決定進程所要連接的視窗工作站：

1.  如果進程已呼叫 [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) 函式，它會連接到該呼叫中指定的視窗站。
2.  如果處理常式未呼叫 [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)，它會連接到繼承自父進程的視窗站。
3.  如果處理常式未呼叫 [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) ，且未繼承視窗工作站，系統會嘗試開啟以取得允許的最大 \_ 存取權，並連接到視窗工作站，如下所示：
    -   如果在建立進程時所使用之 [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa)結構的 **lpDesktop** 成員中指定了視窗工作站名稱，進程會連接到指定的視窗工作站。
    -   否則，如果處理常式是在互動式使用者的登入會話中執行，則此程式會連線到互動式視窗工作站。
    -   如果處理常式是在非互動式登入會話中執行，則會根據登入會話識別碼來形成視窗站名稱，並嘗試開啟該視窗工作站。 如果開啟作業失敗，因為此視窗工作站不存在，系統會嘗試建立視窗工作站和預設桌面。

呼叫 [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation) 函式時，無法關閉在此連接程式期間指派的視窗站。

當進程連接到視窗站時，系統會在進程的控制碼資料表中搜尋繼承的控制碼。 系統會使用它所找到的第一個視窗工作站控制碼。 如果您想要讓子進程連接到特定的繼承視窗工作站，您必須確定只將所需的控制碼標示為可繼承。 如果子進程繼承多個視窗工作站控制碼，則視窗站連接的結果會是未定義的。

系統在將進程連接到視窗工作站時開啟的視窗工作站的控制碼不是可繼承的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[與桌面的執行緒連接](thread-connection-to-a-desktop.md)
</dt> </dl>

 

 