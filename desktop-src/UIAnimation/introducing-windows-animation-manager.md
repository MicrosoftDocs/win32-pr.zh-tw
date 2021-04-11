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
# <a name="update-the-animation-manager-and-draw-frames"></a><span data-ttu-id="c5f8d-105">更新動畫管理員並繪製畫面格</span><span class="sxs-lookup"><span data-stu-id="c5f8d-105">Update the Animation Manager and Draw Frames</span></span>

<span data-ttu-id="c5f8d-106">每次應用程式排程分鏡腳本時，應用程式都必須提供目前的時間給動畫管理員。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-106">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="c5f8d-107">當您導向動畫管理員以更新其狀態，並將所有動畫變數設定為適當的插入值時，也需要目前的時間。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-107">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span>

## <a name="overview"></a><span data-ttu-id="c5f8d-108">概觀</span><span class="sxs-lookup"><span data-stu-id="c5f8d-108">Overview</span></span>

<span data-ttu-id="c5f8d-109">Windows 動畫支援兩種設定：應用程式驅動的動畫和計時器驅動動畫。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-109">There are two configurations supported by Windows Animation: application-driven animation and timer-driven animation.</span></span>

<span data-ttu-id="c5f8d-110">若要在您的應用程式中使用應用程式驅動的動畫，您必須先更新動畫管理員，再繪製每個畫面格，並使用適當的機制，讓動畫的繪製頻率夠高。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-110">To use application-driven animation in your application, you must update the animation manager before drawing each frame and use an appropriate mechanism to draw frames frequently enough for animation.</span></span> <span data-ttu-id="c5f8d-111">使用應用程式驅動動畫的應用程式可以使用任何機制來判斷目前的時間，但是 Windows 動畫計時器物件會傳回動畫管理員所接受的單位精確的時間。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-111">An application using application-driven animation can use any mechanism to determine the current time, but the Windows Animation timer object returns a precise time in the units accepted by the animation manager.</span></span> <span data-ttu-id="c5f8d-112">若要避免在沒有播放動畫時進行不必要的繪圖，您也應該提供管理員事件處理常式，以在動畫已排程時開始重繪，並在每個畫面格之後檢查是否可以暫停重繪。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-112">To avoid unnecessary drawing when no animations are playing, you should also provide a manager event handler to start redrawing when animations are scheduled and check after each frame whether redrawing can be suspended.</span></span> <span data-ttu-id="c5f8d-113">如需詳細資訊，請參閱 [應用程式驅動的動畫](scenic-animation-api-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-113">For more information, see [Application-Driven Animation](scenic-animation-api-overview.md).</span></span>

<span data-ttu-id="c5f8d-114">在應用程式驅動的設定中，應用程式可以呼叫 [**IUIAnimationManager：： GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) 方法來確認動畫目前已排程，並繼續繪製框架（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-114">In the application-driven configuration, an application can call the [**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) method to verify that animations are currently scheduled and continue to draw frames if they are.</span></span> <span data-ttu-id="c5f8d-115">因為重繪會在沒有排定動畫的情況下停止，所以在下一次排程動畫時必須重新開機。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-115">Because redrawing stops when there are no animations scheduled, it is necessary to restart it the next time an animation is scheduled.</span></span> <span data-ttu-id="c5f8d-116">應用程式可以註冊管理員事件處理常式，以在動畫管理員的狀態從閒置變更時通知 (沒有任何動畫目前已排程) 忙碌中。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-116">An application can register a manager event handler to be notified when the status of the animation manager changes from idle (no animations are currently scheduled) to busy.</span></span>

<span data-ttu-id="c5f8d-117">若要在您的應用程式中使用計時器驅動動畫，您必須將動畫管理員連接至動畫計時器，並提供計時器事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-117">To use timer-driven animation in your application, you must connect the animation manager to an animation timer and provide a timer event handler.</span></span> <span data-ttu-id="c5f8d-118">當動畫管理員連接到計時器時，計時器會在動畫狀態應在時間進行時更新時告訴管理員。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-118">When the animation manager is connected to a timer, the timer can tell the manager when the animation state should be updated as time progresses.</span></span> <span data-ttu-id="c5f8d-119">應用程式應該繪製每個計時器刻度的畫面格。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-119">The application should draw a frame for each timer tick.</span></span> <span data-ttu-id="c5f8d-120">動畫管理員可以接著在播放動畫時告訴計時器，讓計時器可以在不需要重繪時，于閒置期間關閉。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-120">The animation manager can in turn tell the timer when there are animations playing, so the timer can shut itself off during idle periods when redrawing is unnecessary.</span></span> <span data-ttu-id="c5f8d-121">若要避免在沒有播放動畫時進行不必要的繪圖，您應該將計時器設定為自動停用。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-121">To avoid unnecessary drawing when no animations are playing, you should configure the timer to disable itself automatically.</span></span> <span data-ttu-id="c5f8d-122">如需詳細資訊，請參閱 [計時器驅動動畫](scenic-animation-api-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-122">For more information, see [Timer-Driven Animation](scenic-animation-api-overview.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="c5f8d-123">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="c5f8d-123">Example Code</span></span>

-   [<span data-ttu-id="c5f8d-124">應用程式驅動的動畫</span><span class="sxs-lookup"><span data-stu-id="c5f8d-124">Application-Driven Animation</span></span>](#application-driven-animation)
-   [<span data-ttu-id="c5f8d-125">計時器驅動動畫</span><span class="sxs-lookup"><span data-stu-id="c5f8d-125">Timer-Driven Animation</span></span>](#timer-driven-animation)

### <a name="application-driven-animation"></a><span data-ttu-id="c5f8d-126">Application-Driven 動畫</span><span class="sxs-lookup"><span data-stu-id="c5f8d-126">Application-Driven Animation</span></span>

<span data-ttu-id="c5f8d-127">下列範例程式碼是從 Windows 動畫範例 [應用程式驅動的動畫](application-driven-animation-sample.md) 和 [方格](/windows/desktop/UIAnimation/grid-layout-sample)配置中的 ManagerEventHandler 取得。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-127">The following example code is taken from ManagerEventHandler.h from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample).</span></span> <span data-ttu-id="c5f8d-128">它會定義管理員事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-128">It defines the manager event handler.</span></span>


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



<span data-ttu-id="c5f8d-129">下列範例程式碼是從 Windows 動畫範例 [應用程式驅動動畫](application-driven-animation-sample.md)的 MainWindow 取得;請參閱 CMainWindow：： InitializeAnimation。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-129">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="c5f8d-130">此範例會使用 [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) 方法建立管理員事件處理常式的實例，並使用 [**IUIAnimationManager：： SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) 方法將其傳遞至動畫管理員。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-130">This example creates an instance of the manager event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the animation manager using the [**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) method.</span></span>


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



<span data-ttu-id="c5f8d-131">因為管理員事件處理常式會保留主視窗物件的參考，所以 (藉由將 **Null** 傳遞給 [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) 來清除管理員事件處理常式，否則動畫管理員應該在主視窗損毀之前完全釋放。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-131">Because the manager event handler retains a reference to the main window object, the manager event handler should be cleared (by passing **NULL** to [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) or the animation manager should be completely released before the main window is destroyed.</span></span>

<span data-ttu-id="c5f8d-132">下列範例程式碼取自 Windows 動畫範例 [應用程式驅動動畫](application-driven-animation-sample.md)中的 MainWindow。請參閱 CMainWindow：： OnPaint 方法。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-132">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="c5f8d-133">它會呼叫 [**IUIAnimationManager：： GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) 方法，以 [**IUIAnimationManager：： Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) 方法所需的單位來取得時間。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-133">It calls the [**IUIAnimationManager::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) method to retrieve the time in the units required by the [**IUIAnimationManager::Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) method.</span></span>


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



<span data-ttu-id="c5f8d-134">下列範例程式碼取自從 MainWindow 的 Windows 動畫範例 [應用程式驅動的動畫](application-driven-animation-sample.md) 和 [方格](/windows/desktop/UIAnimation/grid-layout-sample)配置;請參閱 CMainWindow：： OnPaint 方法。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-134">The following example code is taken from MainWindow.cpp from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="c5f8d-135">它會假設應用程式使用的圖形 API 會自動同步處理至監視器重新整理頻率 (例如 Direct2D 及其預設設定) ，在此情況下， [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) 函式的呼叫就足以確保在繪製下一個畫面格時，會再次呼叫繪製程式碼。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-135">It assumes that the application is using a graphics API that automatically synchronizes to the monitor refresh rate (such as Direct2D with its default settings), in which case a call to the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function is enough to ensure that the painting code will be called again when it is time to draw the next frame.</span></span> <span data-ttu-id="c5f8d-136">並不是無條件地呼叫 **InvalidateRect** ，最好是檢查是否仍有任何使用 [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)排程的動畫。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-136">Rather than call **InvalidateRect** unconditionally, it is better to check if there are still any animations scheduled using [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span></span>


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



### <a name="timer-driven-animation"></a><span data-ttu-id="c5f8d-137">Timer-Driven 動畫</span><span class="sxs-lookup"><span data-stu-id="c5f8d-137">Timer-Driven Animation</span></span>

<span data-ttu-id="c5f8d-138">下列範例程式碼是從 Windows 動畫範例 [計時器驅動動畫](timer-driven-animation-sample.md)的 TimerEventHandler 取得。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-138">The following example code is taken from TimerEventHandler.h from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="c5f8d-139">範例程式碼會定義計時器事件處理常式，此處理程式會使視窗的工作區失效，以在每次更新動畫狀態之後重新繪製。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-139">The example code defines the timer event handler, which invalidates the window's client area to cause a repaint after each update of the animation state.</span></span>


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



<span data-ttu-id="c5f8d-140">下列範例程式碼是從 Windows 動畫範例 [計時器驅動動畫](timer-driven-animation-sample.md)的 MainWindow 取得;請參閱 CMainWindow：： InitializeAnimation。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-140">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="c5f8d-141">這個範例會使用 [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) 方法建立計時器事件處理常式的實例，並使用 [**IUIAnimationTimer：： SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) 方法將它傳遞給計時器。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-141">This example creates an instance of the timer event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the timer using the [**IUIAnimationTimer::SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) method.</span></span> <span data-ttu-id="c5f8d-142">由於計時器事件處理常式會保留主視窗物件的參考，因此 (藉由將 **Null** 傳遞給 **SetTimerEventHandler**) ，或在主視窗終結之前完全釋放的計時器，來清除計時器事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-142">Because the timer event handler retains a reference to the main window object, the timer event handler should be cleared (by passing **NULL** to **SetTimerEventHandler**) or the timer completely released before the main window is destroyed.</span></span>


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



<span data-ttu-id="c5f8d-143">下列範例程式碼取自 Windows 動畫範例 [計時器驅動動畫](timer-driven-animation-sample.md)中的 MainWindow。請參閱 CMainWindow：： InitializeAnimation 方法。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-143">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::InitializeAnimation method.</span></span> <span data-ttu-id="c5f8d-144">它會呼叫動畫管理員物件上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法，以取得 [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler)的指標，然後使用 [**IUIAnimationTimer：： SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)方法將動畫管理員設定為計時器的更新處理常式，以連接 [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))和 [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))物件。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-144">It calls the [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the animation manager object to get a pointer to [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), then connects the [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) and [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) objects by setting the animation manager as the timer's update handler using the [**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) method.</span></span> <span data-ttu-id="c5f8d-145">請注意，您不需要明確地清除此連接;此連接會在應用程式釋放動畫管理員和動畫計時器之後安全地清除。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-145">Note that it is not necessary to explicitly clear this connection; the connection is cleared safely after the application releases both the animation manager and the animation timer.</span></span>


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



<span data-ttu-id="c5f8d-146">如果未使用 **UI \_ 動畫 \_ 閒置 \_ 行為 \_ 停** 用，則也必須啟用計時器以開始計時。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-146">If **UI\_ANIMATION\_IDLE\_BEHAVIOR\_DISABLE** is not used, it is also necessary to enable the timer to start it ticking.</span></span>

## <a name="previous-step"></a><span data-ttu-id="c5f8d-147">上一個步驟</span><span class="sxs-lookup"><span data-stu-id="c5f8d-147">Previous Step</span></span>

<span data-ttu-id="c5f8d-148">開始此步驟之前，您應該已完成此步驟： [建立動畫變數](create-animation-variables.md)。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-148">Before starting this step, you should have completed this step: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="c5f8d-149">後續步驟</span><span class="sxs-lookup"><span data-stu-id="c5f8d-149">Next Step</span></span>

<span data-ttu-id="c5f8d-150">完成此步驟之後，下一步是： [讀取動畫變數值](updating---application-driven-animation.md)。</span><span class="sxs-lookup"><span data-stu-id="c5f8d-150">After completing this step, the next step is: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5f8d-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5f8d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5f8d-152">**IUIAnimationManager：： GetStatus**</span><span class="sxs-lookup"><span data-stu-id="c5f8d-152">**IUIAnimationManager::GetStatus**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[<span data-ttu-id="c5f8d-153">**IUIAnimationManager::SetManagerEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c5f8d-153">**IUIAnimationManager::SetManagerEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[<span data-ttu-id="c5f8d-154">**IUIAnimationManager：： Update**</span><span class="sxs-lookup"><span data-stu-id="c5f8d-154">**IUIAnimationManager::Update**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[<span data-ttu-id="c5f8d-155">**IUIAnimationTimer：： GetTime**</span><span class="sxs-lookup"><span data-stu-id="c5f8d-155">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="c5f8d-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span><span class="sxs-lookup"><span data-stu-id="c5f8d-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

<span data-ttu-id="c5f8d-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5f8d-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c5f8d-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5f8d-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c5f8d-159">Windows 動畫總覽</span><span class="sxs-lookup"><span data-stu-id="c5f8d-159">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 