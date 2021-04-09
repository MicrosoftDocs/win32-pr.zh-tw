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
# <a name="handling-dvd-event-notifications"></a><span data-ttu-id="d30cb-103">處理 DVD 事件通知</span><span class="sxs-lookup"><span data-stu-id="d30cb-103">Handling DVD Event Notifications</span></span>

<span data-ttu-id="d30cb-104">當發生特定事件時，DVD 瀏覽器會將通知傳送至應用程式指定的視窗，例如，當 DVD 網域變更、遇到新的家長監護時，以及當 DVD 導覽器即將進入角度區塊時。</span><span class="sxs-lookup"><span data-stu-id="d30cb-104">The DVD Navigator sends notifications to an application-specified window when certain events take place, such as when the DVD domain changes, when a new parental management level is encountered, and when the DVD Navigator is about to enter an angle block.</span></span> <span data-ttu-id="d30cb-105">事件參數可以包含事件的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d30cb-105">The event parameters can contain additional information related to the event.</span></span> <span data-ttu-id="d30cb-106">也會以這種方式傳送錯誤訊息和警告。</span><span class="sxs-lookup"><span data-stu-id="d30cb-106">Error messages and warnings are also sent in this way.</span></span> <span data-ttu-id="d30cb-107">應用程式會使用 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 指標呼叫 [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)，指定將處理事件通知的視窗，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d30cb-107">The application specifies the window that will handle the event notifications by using the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer to call [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), as follows:</span></span>


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



<span data-ttu-id="d30cb-108">在上述範例中，m \_ hWnd 是接收訊息之視窗的 hwnd，而 wm \_ DVD \_ 事件則是應用程式定義的訊息 (大於 WM 的 \_ 使用者) ，會指出已發生 DVD 事件。</span><span class="sxs-lookup"><span data-stu-id="d30cb-108">In the preceding example, m\_hWnd is the HWND of the window to receive the messages and WM\_DVD\_EVENT is the application-defined message (greater than WM\_USER) that will signal that a DVD event has taken place.</span></span> <span data-ttu-id="d30cb-109">應用程式會透過呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)來抓取事件本身。</span><span class="sxs-lookup"><span data-stu-id="d30cb-109">The event itself is retrieved by the application through a call to [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="d30cb-110">由於事件佇列中有一個以上的事件可能在任何指定時間，因此應用程式必須在重複的迴圈中呼叫 **GetEvent** ，直到所有已排入佇列的事件都被抓取為止，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="d30cb-110">Because more than one event might be in the event queue at any given time, the application must call **GetEvent** within a loop that repeats until all queued events have been retrieved, as shown in the following code example.</span></span>


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



<span data-ttu-id="d30cb-111">DVD 事件可能會在 *lParam1* 或 *lParam2* 參數中包含其他資訊，如上所示，目前時間包含在 *lParam1* 中。</span><span class="sxs-lookup"><span data-stu-id="d30cb-111">DVD events might contain additional information in the *lParam1* or *lParam2* parameters, as illustrated above where the current time is contained in *lParam1*.</span></span> <span data-ttu-id="d30cb-112">上述程式碼範例是來自 Dvdcore 中的 DVD 範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="d30cb-112">The preceding code example is from the DVD sample application in Dvdcore.cpp.</span></span> <span data-ttu-id="d30cb-113">如需所有 DVD 事件及其參數的完整清單，請參閱 [Dvd 事件通知碼](dvd-notification-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="d30cb-113">For a complete list of all DVD events and their parameters, see [DVD Event Notification Codes](dvd-notification-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d30cb-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="d30cb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d30cb-115">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="d30cb-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



