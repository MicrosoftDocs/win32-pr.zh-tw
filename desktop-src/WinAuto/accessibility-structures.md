---
title: 協助工具結構
description: 本節說明用來執行 Windows 協助工具功能的結構。Microsoft Win32 協助工具功能。
ms.assetid: 0ff480ae-18e3-413d-b208-a67fbae28c25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576b398769a2cf1dc88d9f7ade8c995988c346e04f1c7becf7aef31cded50e91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994388"
---
# <a name="accessibility-structures"></a>協助工具結構

本節說明用來執行 Windows 協助工具功能的結構。

## <a name="in-this-section"></a>本節內容



| 結構                                         | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACCESSTIMEOUT**](/windows/win32/api/winuser/ns-winuser-accesstimeout)<br/> | 包含與 Microsoft Win32 協助工具功能相關聯的超時時間的相關資訊。 <br/> 存取範圍超時期限是在作業系統自動關閉協助工具功能之前，必須經過鍵盤和滑鼠輸入才能傳遞的時間長度。 存取範圍超時是針對由多位使用者共用的電腦所設計，讓一位使用者選取的選項不會造成後續使用者的不便。<br/> 受超時影響的協助工具功能是 (SlowKeys、BounceKeys 和 RepeatKeys) 、滑鼠鍵、切換器和相黏鍵的篩選器功能。 存取範圍超時也會影響高對比模式設定。<br/> |
| [**L**](/windows/win32/api/winuser/ns-winuser-filterkeys)<br/>       | 包含 [篩選] 存取範圍功能的相關資訊，可讓殘障使用者將鍵盤的重複速度設定 (RepeatKeys) 、接受延遲 (SlowKeys) 和跳動率 (BounceKeys) 。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**SYSTEMINFORMATION.HIGHCONTRAST**](/windows/win32/api/winuser/ns-winuser-highcontrasta)<br/>   | 包含高對比協助工具功能的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**方向鍵**](/windows/win32/api/winuser/ns-winuser-mousekeys)<br/>         | 包含滑鼠鍵協助工具功能的相關資訊。 當 [滑鼠鍵] 功能為作用中時，使用者可以使用數位鍵台控制滑鼠指標，然後按一下、按兩下、拖放。 藉由按下 [NUMLOCK]，使用者可以在滑鼠控制模式與正常操作之間切換數位鍵台。 <br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**R**](/windows/win32/api/winuser/ns-winuser-serialkeysa)<br/>       | 包含有關 [輸入串列] 協助工具的資訊，它會從連接到序列埠的通訊協助工具，將資料解讀為導致系統模擬鍵盤和滑鼠輸入的命令。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**衛士**](/windows/win32/api/winuser/ns-winuser-soundsentrya)<br/>     | 包含 [聲音感測協助工具] 功能的相關資訊。 當聲段功能開啟時，只有在產生音效時，電腦才會顯示視覺指示。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**粘連**](/windows/win32/api/winuser/ns-winuser-stickykeys)<br/>       | 包含相黏鍵協助工具功能的相關資訊。 當相黏鍵功能為開啟時，使用者可以按下輔助按鍵， (SHIFT、CTRL 或 ALT) ，然後按順序（而不是同時）輸入另一個按鍵，以輸入 (修改) 字元和其他按鍵組合的移動。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**$**](/windows/win32/api/winuser/ns-winuser-togglekeys)<br/>       | 包含 [切換鍵] 協助工具功能的相關資訊。 當開啟切換器功能時，電腦會在使用者開啟 CAPS LOCK、NUM LOCK 或 SCROLL LOCK 鍵時發出高音調的色調，而當使用者關閉其中一個按鍵時，則會發出一個低音調的色調。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows協助工具功能](../accessibility/accessibility.md)
</dt> </dl>

 

