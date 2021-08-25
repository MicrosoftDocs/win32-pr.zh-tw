---
title: 操作和慣性範例
description: 操作和慣性範例示範如何將 Windows Touch 支援新增至使用 Windows Touch API 的原生 Windows 應用程式。
ms.assetid: 6a6e2e39-026e-47a3-b936-16f6a740a3af
keywords:
- Windows觸控、程式碼範例
- Windows觸控，範例程式碼
- Windows觸控、操作
- Windows觸控、慣性
- Windows觸控、操作和慣性範例
- 操作和慣性範例
- Windows觸控、_IManipulationEventSink 介面
- WindowsTouch、IManipulationProcessor 介面
- WindowsTouch、IInertiaProcessor 介面
- 操作，範例程式碼
- 操作，程式碼範例
- 操作，_IManipulationEventSink 介面
- 操作，IManipulationProcessor 介面
- 慣性，範例程式碼
- 慣性，程式碼範例
- 慣性、IInertiaProcessor 介面
- _IManipulationEventSink 介面
- IManipulationProcessor 介面，程式碼範例
- IManipulationProcessor 介面，範例程式碼
- IInertiaProcessor 介面，程式碼範例
- IInertiaProcessor 介面，範例程式碼
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 8b6471362d30b6efc9dfa0c4f07df70f014c8cb72866c92bbb04c9eb33463410
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840590"
---
# <a name="manipulation-and-inertia-sample"></a>操作和慣性範例

操作和慣性範例示範如何將 Windows Touch 支援新增至使用 Windows Touch API 的原生 Windows 應用程式。 此範例會執行 API 的基本功能，以啟用物件的平移、旋轉和縮放，並將慣性屬性套用至它們。 此範例也會示範如何為您的 Windows Touch 應用程式提供基本的滑鼠支援。 下圖顯示範例在執行時的外觀。

![顯示操作和慣性範例中具有漸層之兩個方塊的螢幕擷取畫面](images/manip-inertia-sample.png)

當使用者從支援 Windows Touch 的電腦執行應用程式時，可以獨立操作具有漸層的方塊。

## <a name="register-the-touch-window"></a>註冊觸控視窗

您必須先藉由呼叫下列函式，通知系統您的應用程式是 Windows Touch 應用程式，才能接收觸控輸入：

```C++
   RegisterTouchWindow(g_hWnd, 0);
```

## <a name="implement-the-_imanipulationeventsink-interface"></a>執行 _IManipulationEventSink 介面

[**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)事件接收器包含三個函數： [**system.windows.uielement.manipulationstarted>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted)、 [**system.windows.uielement.manipulationdelta>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)和 [**system.windows.uielement.manipulationcompleted>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted)。 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)介面和 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)介面會使用這些回呼函式，以在叫用 [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)、 [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime)、 [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)和 [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime)函數之後，傳回由處理器計算的值。 下列程式碼範例顯示 **_IManipulationEvents** 介面的範例執行。

```C++
#include "cmanipulationeventsink.h"
#include <math.h>

CManipulationEventSink::CManipulationEventSink(HWND hWnd, CDrawingObject *dObj, int iTimerId, BOOL inertia) {
    // Manipulation & Inertia Processors
    m_manip = NULL;
    m_inert = NULL;

    // Connection points for COM.
    m_pConPointContainer = NULL;
    m_pConnPoint = NULL;

    // Reference to an object associated with this event sink.
    m_dObj = dObj;

    // Handle to the window used for computing boundaries.
    m_hWnd = hWnd;

    // The unique timer id for this manipulation event sink.
    m_iTimerId = iTimerId;

    m_bInertia = inertia;

    m_cRefCount = 1;
}


CManipulationEventSink::~CManipulationEventSink()
{

}


HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted(
    FLOAT x,
    FLOAT y)
{
    KillTimer(m_hWnd, m_iTimerId);

    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta(
    FLOAT x,
    FLOAT y,
    FLOAT translationDeltaX,
    FLOAT translationDeltaY,
    FLOAT scaleDelta,
    FLOAT expansionDelta,
    FLOAT rotationDelta,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    FLOAT pivot = 0.0f;

    // Apply transformation based on rotationDelta (in radians).
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta.
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta.
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    if(!m_bInertia)
    {
        // Set values for one-finger rotations.
        FLOAT fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->GetWidth()/2, 2)
                           + pow(m_dObj->GetHeight()/2, 2)))*0.4f;
        FLOAT fPivotPtX    = m_dObj->GetCenterX();
        FLOAT fPivotPtY    = m_dObj->GetCenterY();

        m_manip->put_PivotPointX(fPivotPtX);
        m_manip->put_PivotPointY(fPivotPtY);
        m_manip->put_PivotRadius(fPivotRadius);
    }
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted(
    FLOAT x,
    FLOAT y,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    if(!m_bInertia)
    {
        SetupInertia();

        // Kick off timer that handles inertia.
        SetTimer(m_hWnd, m_iTimerId, DESIRED_MILLISECONDS, NULL);
    }
    else
    {
        // Stop timer that handles inertia.
        KillTimer(m_hWnd, m_iTimerId);
    }

    return S_OK;
}
```

## <a name="create-com-objects-and-set-up-the-imanipulationprocessor-and-iinertiaprocessor-interfaces"></a>建立 COM 物件，並設定 IManipulationProcessor 和 IInertiaProcessor 介面

API 提供 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 和 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 介面的實作為。 您應建立的實例，並參考先前所執行之 [**IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) 事件接收器中的 COM 物件。

## <a name="handle-wm_touch-messages"></a>處理 WM_TOUCH 訊息

輸入資料必須從 [**WM_TOUCH**](wm-touchdown.md) 的訊息中解壓縮，之後必須處理，才能饋送正確的操作處理器。

```C++
switch (msg)
{
    case WM_TOUCH:

      iNumContacts = LOWORD(wParam);
      hInput       = (HTOUCHINPUT)lParam;
      pInputs      = new TOUCHINPUT[iNumContacts];

      // Get each touch input info and feed each
      // tagTOUCHINPUT into the process input handler.

      if(pInputs != NULL)
      {
          if(GetTouchInputInfo(hInput, iNumContacts,
               pInputs, sizeof(TOUCHINPUT)))
          {
              for(int i = 0; i < iNumContacts; i++)
              {
                  // Bring touch input info into client coordinates.
                  ptInputs.x = pInputs[i].x/100;
                  ptInputs.y = pInputs[i].y/100;
                  ScreenToClient(g_hWnd, &ptInputs);

                  pInputs[i].x = ptInputs.x;
                  pInputs[i].y = ptInputs.y;

                  g_ctDriver->ProcessInputEvent(pInputs[i]);
              }
          }
      }

      delete [] pInputs;
      break;
}
```

> [!Note]  
> 若要使用 [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) 函式，您的應用程式中必須有高 DPI 支援。 如需支援高 DPI 的詳細資訊，請造訪 MSDN 的 [高 DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) 區段。

## <a name="pass-touchinput-structures-to-the-appropriate-processor"></a>將 TOUCHINPUT 結構傳遞給適當的處理器

使用 [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)函式將資料從 [**WM_TOUCH**](wm-touchdown.md)的訊息中解壓縮之後，請叫用 [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime)、 [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)或 [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime)函式，將資料送入操作處理器，視 [**>dwflag**](/windows/win32/api/winuser/ns-winuser-touchinput)結構中所設定的 **TOUCHINPUT** 而定。

> [!Note]  
> 當支援多個操作時，如果必須使用 [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput)結構中定義的 **dwID** ，將資料傳送到正確的 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)物件，則必須建立新的操作處理器。

```C++
CoreObject* coCurrent = m_coHead;

while(coCurrent!=NULL && !bFoundObj)
{
    if(dwEvent & TOUCHEVENTF_DOWN)
    {
        DownEvent(coCurrent, inData, &bFoundObj);
    }
    else if(dwEvent & TOUCHEVENTF_MOVE)
    {
        MoveEvent(coCurrent, inData);
    }
    else if(dwEvent & TOUCHEVENTF_UP)
    {
        UpEvent(coCurrent, inData);
    }
    coCurrent = coCurrent->coNext;
}

VOID CComTouchDriver::DownEvent(CoreObject* coRef, tagTOUCHINPUT inData, BOOL* bFound) {
    DWORD dwPCursor = inData.dwID;
    DWORD dwPTime   = inData.dwTime;
    int x           = inData.x;
    int y           = inData.y;

    // Check that the user has touched within an object's region and fed to the object's manipulation processor.

    if(coRef->doDrawing->InRegion(x, y) &&
        !HasCursor(coRef, dwPCursor))
    {
        ...

        // Feed values to the Manipulation Processor.
        coRef->manipulationProc->ProcessDownWithTime(dwPCursor, (FLOAT)x, (FLOAT)y, dwPTime);

        ...
    }
}
```

## <a name="set-up-inertia-within-manipulationcompleted"></a>設定 System.windows.uielement.manipulationcompleted> 中的慣性

叫用 [**system.windows.uielement.manipulationcompleted>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted)方法之後， [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)物件必須設定連結至 **IManipulationProcessor** 的 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)物件值，以叫用慣性。 下列程式碼範例顯示如何從 **IManipulationProcessor** 方法 **system.windows.uielement.manipulationcompleted>** 設定 **IInertiaProcessor** 物件。

```C++
    int iVWidth       = GetSystemMetrics(SM_CXVIRTUALSCREEN);
    int iVHeight      = GetSystemMetrics(SM_CYVIRTUALSCREEN);

    RECT rc;
    GetClientRect(m_hWnd, &rc);
    FLOAT lCWidth     = (FLOAT)rc.right;
    FLOAT lCHeight    = (FLOAT)rc.bottom;

    // Set properties for inertia events.

    // Deceleration for tranlations in pixel / msec^2.
    m_inert->put_DesiredDeceleration(0.001f);

    // Deceleration for rotations in radians / msec^2.
    m_inert->put_DesiredAngularDeceleration(0.00001f);

    // Calculate borders and elastic margin to be set.
    // They are relative to the width and height of the object.

    FLOAT fHOffset = m_dObj->GetWidth()  * 0.5f;
    FLOAT fVOffset = m_dObj->GetHeight() * 0.5f;

    // Elastic margin is in pixels - note that it offsets the boundary.

    FLOAT fHElasticMargin = 25.0f;
    FLOAT fVElasticMargin = 25.0f;

    FLOAT fBoundaryLeft   = fHOffset + fHElasticMargin;
    FLOAT fBoundaryTop    = fVOffset + fVElasticMargin;
    FLOAT fBoundaryRight  = lCWidth - fHOffset - fHElasticMargin;
    FLOAT fBoundaryBottom = lCHeight - fVOffset - fVElasticMargin;

    // Set borders and elastic margin.

    m_inert->put_BoundaryLeft(fBoundaryLeft);
    m_inert->put_BoundaryTop(fBoundaryTop);
    m_inert->put_BoundaryRight(fBoundaryRight);
    m_inert->put_BoundaryBottom(fBoundaryBottom);

    m_inert->put_ElasticMarginLeft(fHElasticMargin);
    m_inert->put_ElasticMarginTop(fVElasticMargin);
    m_inert->put_ElasticMarginRight(fHElasticMargin);
    m_inert->put_ElasticMarginBottom(fVElasticMargin);

    // Set initial origins.

    m_inert->put_InitialOriginX(m_dObj->GetCenterX());
    m_inert->put_InitialOriginY(m_dObj->GetCenterY());

    FLOAT fVX;
    FLOAT fVY;
    FLOAT fVR;

    m_manip->GetVelocityX(&fVX);
    m_manip->GetVelocityY(&fVY);
    m_manip->GetAngularVelocity(&fVR);

    // Set initial velocities for inertia processor.

    m_inert->put_InitialVelocityX(fVX);
    m_inert->put_InitialVelocityY(fVY);
    m_inert->put_InitialAngularVelocity(fVR);
```

## <a name="clean-up-your-com-objects"></a>清除您的 COM 物件

當您的應用程式關閉時，您必須清除 COM 物件。 下列程式碼說明如何釋放範例中所配置的資源。

```C++
CComTouchDriver::~CComTouchDriver(VOID) {
    CoreObject* coCurrent = m_coHead;

    // Clean up COM objects.

    while(coCurrent!=NULL)
    {
        coCurrent->inertiaEventSink->Release();
        coCurrent->manipulationEventSink->Release();
        coCurrent->inertiaProc->Release();
        coCurrent->manipulationProc->Release();
        coCurrent = coCurrent->coNext;
    }
}
```

## <a name="related-topics"></a>相關主題

[多點觸控操作應用程式](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp)、[操作和慣性範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp)、 [Windows Touch 範例](windows-touch-samples.md)