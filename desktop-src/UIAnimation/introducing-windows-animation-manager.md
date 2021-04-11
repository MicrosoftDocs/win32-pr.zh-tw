---
title: 更新動畫管理員並繪製畫面格
description: 每次應用程式排程分鏡腳本時，應用程式都必須提供目前的時間給動畫管理員。
ms.assetid: c4f746c3-e47c-4b82-a41b-e2c0d177d097
keywords:
- 動畫管理員物件視窗動畫，更新
- 動畫計時器物件視窗動畫，連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9a48e8d6e273174e502c374727e69b61bc478d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023576"
---
# <a name="update-the-animation-manager-and-draw-frames"></a>更新動畫管理員並繪製畫面格

每次應用程式排程分鏡腳本時，應用程式都必須提供目前的時間給動畫管理員。 當您導向動畫管理員以更新其狀態，並將所有動畫變數設定為適當的插入值時，也需要目前的時間。

## <a name="overview"></a>概觀

Windows 動畫支援兩種設定：應用程式驅動的動畫和計時器驅動動畫。

若要在您的應用程式中使用應用程式驅動的動畫，您必須先更新動畫管理員，再繪製每個畫面格，並使用適當的機制，讓動畫的繪製頻率夠高。 使用應用程式驅動動畫的應用程式可以使用任何機制來判斷目前的時間，但是 Windows 動畫計時器物件會傳回動畫管理員所接受的單位精確的時間。 若要避免在沒有播放動畫時進行不必要的繪圖，您也應該提供管理員事件處理常式，以在動畫已排程時開始重繪，並在每個畫面格之後檢查是否可以暫停重繪。 如需詳細資訊，請參閱 [應用程式驅動的動畫](scenic-animation-api-overview.md)。

在應用程式驅動的設定中，應用程式可以呼叫 [**IUIAnimationManager：： GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) 方法來確認動畫目前已排程，並繼續繪製框架（如果有的話）。 因為重繪會在沒有排定動畫的情況下停止，所以在下一次排程動畫時必須重新開機。 應用程式可以註冊管理員事件處理常式，以在動畫管理員的狀態從閒置變更時通知 (沒有任何動畫目前已排程) 忙碌中。

若要在您的應用程式中使用計時器驅動動畫，您必須將動畫管理員連接至動畫計時器，並提供計時器事件處理常式。 當動畫管理員連接到計時器時，計時器會在動畫狀態應在時間進行時更新時告訴管理員。 應用程式應該繪製每個計時器刻度的畫面格。 動畫管理員可以接著在播放動畫時告訴計時器，讓計時器可以在不需要重繪時，于閒置期間關閉。 若要避免在沒有播放動畫時進行不必要的繪圖，您應該將計時器設定為自動停用。 如需詳細資訊，請參閱 [計時器驅動動畫](scenic-animation-api-overview.md)。

## <a name="example-code"></a>範例程式碼

-   [應用程式驅動的動畫](#application-driven-animation)
-   [計時器驅動動畫](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven 動畫

下列範例程式碼是從 Windows 動畫範例 [應用程式驅動的動畫](application-driven-animation-sample.md) 和 [方格](/windows/desktop/UIAnimation/grid-layout-sample)配置中的 ManagerEventHandler 取得。 它會定義管理員事件處理常式。


```C++
#include "UIAnimationHelper.h"

// Event handler object for manager status changes

class CManagerEventHandler :
    public CUIAnimationManagerEventHandlerBase<CManagerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationManagerEventHandler **ppManagerEventHandler
    ) throw()
    {
        CManagerEventHandler *pManagerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppManagerEventHandler,
            &pManagerEventHandler
            );
        if (SUCCEEDED(hr))
        {
            pManagerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationManagerEventHandler

    IFACEMETHODIMP
    OnManagerStatusChanged
    (
        UI_ANIMATION_MANAGER_STATUS newStatus,
        UI_ANIMATION_MANAGER_STATUS previousStatus
    )
    {
        HRESULT hr = S_OK;

        if (newStatus == UI_ANIMATION_MANAGER_BUSY)
        {
            hr = m_pMainWindow->Invalidate();
        }

        return hr;
    }

    ...

};
```



下列範例程式碼是從 Windows 動畫範例 [應用程式驅動動畫](application-driven-animation-sample.md)的 MainWindow 取得;請參閱 CMainWindow：： InitializeAnimation。 此範例會使用 [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) 方法建立管理員事件處理常式的實例，並使用 [**IUIAnimationManager：： SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) 方法將其傳遞至動畫管理員。


```C++
// Create and set the ManagerEventHandler to start updating when animations are scheduled

IUIAnimationManagerEventHandler *pManagerEventHandler;
HRESULT hr = CManagerEventHandler::CreateInstance(
    this,
    &pManagerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->SetManagerEventHandler(
        pManagerEventHandler
        );
    pManagerEventHandler->Release();
}
```



因為管理員事件處理常式會保留主視窗物件的參考，所以 (藉由將 **Null** 傳遞給 [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) 來清除管理員事件處理常式，否則動畫管理員應該在主視窗損毀之前完全釋放。

下列範例程式碼取自 Windows 動畫範例 [應用程式驅動動畫](application-driven-animation-sample.md)中的 MainWindow。請參閱 CMainWindow：： OnPaint 方法。 它會呼叫 [**IUIAnimationManager：： GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) 方法，以 [**IUIAnimationManager：： Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) 方法所需的單位來取得時間。


```C++
// Update the animation manager with the current time

UI_ANIMATION_SECONDS secondsNow;
HRESULT hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->Update(
        secondsNow
        );

    ...

}
```



下列範例程式碼取自從 MainWindow 的 Windows 動畫範例 [應用程式驅動的動畫](application-driven-animation-sample.md) 和 [方格](/windows/desktop/UIAnimation/grid-layout-sample)配置;請參閱 CMainWindow：： OnPaint 方法。 它會假設應用程式使用的圖形 API 會自動同步處理至監視器重新整理頻率 (例如 Direct2D 及其預設設定) ，在此情況下， [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) 函式的呼叫就足以確保在繪製下一個畫面格時，會再次呼叫繪製程式碼。 並不是無條件地呼叫 **InvalidateRect** ，最好是檢查是否仍有任何使用 [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)排程的動畫。


```C++
// Read the values of the animation variables and draw the client area

hr = DrawClientArea();
if (SUCCEEDED(hr))
{          
    // Continue redrawing the client area as long as there are animations scheduled
    UI_ANIMATION_MANAGER_STATUS status;
    hr = m_pAnimationManager->GetStatus(
        &status
        );
    if (SUCCEEDED(hr))
    {
        if (status == UI_ANIMATION_MANAGER_BUSY)
        {
            InvalidateRect(
                m_hwnd,
                NULL,
                FALSE
                );
        }
    }
}
```



### <a name="timer-driven-animation"></a>Timer-Driven 動畫

下列範例程式碼是從 Windows 動畫範例 [計時器驅動動畫](timer-driven-animation-sample.md)的 TimerEventHandler 取得。 範例程式碼會定義計時器事件處理常式，此處理程式會使視窗的工作區失效，以在每次更新動畫狀態之後重新繪製。


```C++
#include "UIAnimationHelper.h"

// Event handler object for timer events

class CTimerEventHandler :
    public CUIAnimationTimerEventHandlerBase<CTimerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationTimerEventHandler **ppTimerEventHandler
    ) throw()
    {
        CTimerEventHandler *pTimerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppTimerEventHandler,
            &pTimerEventHandler
            );

        if (SUCCEEDED(hr))
        {
            pTimerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationTimerEventHandler

    IFACEMETHODIMP
    OnPreUpdate()
    {
        return S_OK;
    }

    IFACEMETHODIMP
    OnPostUpdate()
    {
        HRESULT hr = m_pMainWindow->Invalidate();

        return hr;
    }

    IFACEMETHODIMP
    OnRenderingTooSlow
    (
        UINT32 /* fps */
    )
    {
        return S_OK;
    }

    ...

};
```



下列範例程式碼是從 Windows 動畫範例 [計時器驅動動畫](timer-driven-animation-sample.md)的 MainWindow 取得;請參閱 CMainWindow：： InitializeAnimation。 這個範例會使用 [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) 方法建立計時器事件處理常式的實例，並使用 [**IUIAnimationTimer：： SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) 方法將它傳遞給計時器。 由於計時器事件處理常式會保留主視窗物件的參考，因此 (藉由將 **Null** 傳遞給 **SetTimerEventHandler**) ，或在主視窗終結之前完全釋放的計時器，來清除計時器事件處理常式。


```C++
// Create and set the timer event handler

IUIAnimationTimerEventHandler *pTimerEventHandler;
hr = CTimerEventHandler::CreateInstance(
    this,
    &pTimerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerEventHandler(
        pTimerEventHandler
        );
    pTimerEventHandler->Release();
}
```



下列範例程式碼取自 Windows 動畫範例 [計時器驅動動畫](timer-driven-animation-sample.md)中的 MainWindow。請參閱 CMainWindow：： InitializeAnimation 方法。 它會呼叫動畫管理員物件上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法，以取得 [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler)的指標，然後使用 [**IUIAnimationTimer：： SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)方法將動畫管理員設定為計時器的更新處理常式，以連接 [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))和 [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))物件。 請注意，您不需要明確地清除此連接;此連接會在應用程式釋放動畫管理員和動畫計時器之後安全地清除。


```C++
// Connect the animation manager to the timer

IUIAnimationTimerUpdateHandler *pTimerUpdateHandler;
hr = m_pAnimationManager->QueryInterface(
    IID_PPV_ARGS(&pTimerUpdateHandler)
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerUpdateHandler(
        pTimerUpdateHandler
        UI_ANIMATION_IDLE_BEHAVIOR_DISABLE  // timer will shut itself off when there are no animations playing
        );
    pTimerUpdateHandler->Release();
    if (SUCCEEDED(hr))
    {
        // Create and set the timer event handler

        ...

    }
}
```



如果未使用 **UI \_ 動畫 \_ 閒置 \_ 行為 \_ 停** 用，則也必須啟用計時器以開始計時。

## <a name="previous-step"></a>上一個步驟

開始此步驟之前，您應該已完成此步驟： [建立動畫變數](create-animation-variables.md)。

## <a name="next-step"></a>後續步驟

完成此步驟之後，下一步是： [讀取動畫變數值](updating---application-driven-animation.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IUIAnimationManager：： GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[**IUIAnimationManager：： Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[**IUIAnimationTimer：： GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))
</dt> <dt>

[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))
</dt> <dt>

[Windows 動畫總覽](scenic-animation-api-overview.md)
</dt> </dl>

 

 