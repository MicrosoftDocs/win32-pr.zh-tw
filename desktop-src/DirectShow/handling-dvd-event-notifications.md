---
description: 處理 DVD 事件通知
ms.assetid: 7a12aa36-f709-4ee2-aac6-45ab273ad3f9
title: 處理 DVD 事件通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212f3eb9f868c494aa008602713c1750a6c6dc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935975"
---
# <a name="handling-dvd-event-notifications"></a>處理 DVD 事件通知

當發生特定事件時，DVD 瀏覽器會將通知傳送至應用程式指定的視窗，例如，當 DVD 網域變更、遇到新的家長監護時，以及當 DVD 導覽器即將進入角度區塊時。 事件參數可以包含事件的其他相關資訊。 也會以這種方式傳送錯誤訊息和警告。 應用程式會使用 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 指標呼叫 [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)，指定將處理事件通知的視窗，如下所示：


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



在上述範例中，m \_ hWnd 是接收訊息之視窗的 hwnd，而 wm \_ DVD \_ 事件則是應用程式定義的訊息 (大於 WM 的 \_ 使用者) ，會指出已發生 DVD 事件。 應用程式會透過呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)來抓取事件本身。 由於事件佇列中有一個以上的事件可能在任何指定時間，因此應用程式必須在重複的迴圈中呼叫 **GetEvent** ，直到所有已排入佇列的事件都被抓取為止，如下列程式碼範例所示。


```C++
while (SUCCEEDED(m_pIME->GetEvent(&lEvent, &lParam1, &lParam2, lTimeOut)))
{
    HRESULT hr;
    switch (lEvent)
    {

    case EC_DVD_CURRENT_HMSF_TIME:
        {
            DVD_HMSF_TIMECODE *pTC = reinterpret_cast<DVD_HMSF_TIMECODE *>(&lParam1);
            m_CurTime = *pTC;
            ...
        }
        break;
        ...
    } // switch
}
```



DVD 事件可能會在 *lParam1* 或 *lParam2* 參數中包含其他資訊，如上所示，目前時間包含在 *lParam1* 中。 上述程式碼範例是來自 Dvdcore 中的 DVD 範例應用程式。 如需所有 DVD 事件及其參數的完整清單，請參閱 [Dvd 事件通知碼](dvd-notification-codes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 



