---
title: 如何套用動畫
description: 本主題示範如何使用 Microsoft DirectComposition 以動畫顯示視覺效果的屬性。
ms.assetid: 932A3BCD-C290-47AE-80FB-94EE3E34837F
keywords:
- 製作 DirectComposition 視覺效果的動畫
- 如何套用 DirectComposition 動畫
- 套用 DirectComposition 動畫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecba1bde3c430acbb49f640dc7611452f0967746
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474224"
---
# <a name="how-to-apply-animations"></a>如何套用動畫

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 Windows 的撰寫 api，而不是 DirectComposition。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題示範如何使用 Microsoft DirectComposition 以動畫顯示視覺效果的屬性。 本主題中的範例會以動畫顯示視覺效果的效果屬性，使得視覺效果的透明度從零 (透明) 變更為一個 (完全不透明的) 在兩秒鐘的期間內。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [DirectComposition](directcomposition-portal.md)
-   [Direct3D 11 圖形](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [DirectX Graphic Infrastructure (DXGI) ](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Microsoft Win32
-   元件物件模型 (COM)

## <a name="instructions"></a>指示

### <a name="step-1-initialize-directcomposition-objects"></a>步驟1：初始化 DirectComposition 物件

1.  建立裝置物件和組合目標物件。
2.  建立視覺效果、設定其內容，並將它新增至視覺化樹狀結構。

如需詳細資訊，請參閱 [如何初始化 DirectComposition](initialize-directcomposition.md)。

### <a name="step-2-create-an-animation-object"></a>步驟2：建立動畫物件

使用 [**CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) 方法來建立動畫物件。


```C++
HRESULT hr = S_OK;


IDCompositionAnimation *m_pFadeInAnimation;
```






```C++
hr = m_pDevice->CreateAnimation(&m_pFadeInAnimation);
```



### <a name="step-3-define-the-animation-function"></a>步驟3：定義動畫函數

使用 [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) 物件的方法來定義動畫函數。 下列程式碼會定義簡單的動畫函數。 當套用至物件屬性時，動畫函式會在2秒的過程中，以累加方式將屬性值從0變更為1。


```C++
m_pFadeInAnimation->AddCubic(0.0f, 0.0f, 0.5f, 0.0f, 0.0f);
m_pFadeInAnimation->End(2.0f, 1.0f); 
```



### <a name="step-4-apply-the-animation-object-to-a-visual-property-or-to-a-property-of-a-directcomposition-object"></a>步驟4：將動畫物件套用至視覺屬性或 DirectComposition 物件的屬性

在 Microsoft DirectComposition 中，藉由將動畫物件設定為屬性值，即可以動畫顯示任何採用純量值的物件屬性。 下列範例會將動畫物件套用至效果群組物件的不透明度屬性。 然後，效果群組物件會套用至視覺效果的效果屬性。


```C++
IDCompositionEffectGroup *m_pEffectGroup;


hr = m_pDevice->CreateEffectGroup(&m_pEffectGroup);
```



<span codelanguage="ManagedCPlusPlus"></span>


| C++ | 
|-----|
| <pre><code>if (SUCCEEDED(hr)){    hr = m_pEffectGroup-&gt;SetOpacity(m_pFadeInAnimation);}</code></pre> | 


<span codelanguage="ManagedCPlusPlus"></span>


| C++ | 
|-----|
| <pre><code>hr = m_pVisual-&gt;SetEffect(m_pEffectGroup);</code></pre> | 




### <a name="step-5-commit-the-composition"></a>步驟5：認可組合

呼叫 [**IDCompositionDevice：： commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 方法，將視覺效果認可至 DirectComposition，以轉譯至目標視窗。 當視覺效果轉譯時，動畫會導致視覺效果的不透明度從透明變更為完全不透明，在兩秒鐘的期間內。


```C++
hr = m_pDevice->Commit();
```



### <a name="step-6-free-the-directcomposition-objects"></a>步驟6：釋放 DirectComposition 物件

當您不再需要時，請務必釋放動畫物件。


```C++
SafeRelease(&m_pFadeInAnimation);
```



也請記得在應用程式結束之前釋出其他 DirectComposition 物件，包括裝置物件、組合目標物件和視覺效果。 如需詳細資訊，請參閱 [如何初始化 DirectComposition](initialize-directcomposition.md)。

## <a name="complete-example"></a>完整範例


```C++
//
// ApplyAnimations.h
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

#pragma once
// Modify the following definitions if you need to target a platform prior to the ones specified below.
// Refer to MSDN for the latest info on corresponding values for different platforms.
#ifndef WINVER              // Allow use of features specific to Windows 7 or later.
#define WINVER 0x0700       // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT        // Allow use of features specific to Windows 7 or later.
#define _WIN32_WINNT 0x0700 // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN     // Exclude rarely-used items from Windows headers

// Windows Header Files:
#include <windows.h>
#include <objbase.h>
#include <Strsafe.h>
#include <wincodec.h>

// C RunTime Header Files
#include <math.h>

// DirectComposition Header File
#include <dcomp.h>

// Direct2D and Direct3D Header Files
#include <d2d1.h>
#include <d3d11.h>


/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT Initialize();

    void RunMessageLoop();
        
private:
    HRESULT InitializeDirectCompositionDevice();

    HRESULT OnPaint();
    HRESULT DemoApp::OnClick();

    HRESULT CreateDeviceIndependentResources();
    HRESULT CreateDeviceResources();
    void DiscardDeviceResources();

    HRESULT LoadJPEGImage(
        ID2D1RenderTarget *pRenderTarget,
        PCWSTR fileName,
        ID2D1Bitmap **ppBitmap
        );

    HRESULT GetImageFilenames(TCHAR szDir[MAX_PATH]);
    HRESULT SetVisualOpacity(IDCompositionVisual *pVisual, float opacity);

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

 private:
    HWND m_hwnd;
    ID2D1Bitmap *m_pBitmap;
    int m_bitmapWidth;
    int m_bitmapHeight;
    ID2D1Factory *m_pD2DFactory;
    ID2D1HwndRenderTarget *m_pRenderTarget;
    IWICImagingFactory *m_pWICFactory;
    ID3D11Device *m_pD3D11Device;
    IDCompositionDevice *m_pDevice;
    IDCompositionTarget *m_pCompTarget;
    IDCompositionVisual *m_pVisual;
    IDCompositionSurface *m_pSurface;
    IDCompositionAnimation *m_pFadeOutAnimation;
    IDCompositionAnimation *m_pFadeInAnimation;
    IDCompositionEffectGroup *m_pEffectGroup;
    LPCTSTR m_pImageFileNames[5]; 
    LPCTSTR m_pImageDir;
 };


//
// ApplyAnimations.cpp
//
// THIS CODE AND INFORMATION IS PROVIDED &quot;AS IS&quot; WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

// Instructions: Click the client area to view a &quot;slide&quot;. This creates
//     a visual and changes the visual&#39;s bitmap content with each click.
//   Animation is applied to the opacity to &quot;fade in&quot; each new bitmap.

//
// NOTE: This app is HARDCODED to look for images in C:\IMAGES.
//
#include &quot;ApplyAnimations.h&quot;

#define OFFSET_X 20
#define OFFSET_Y 20

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE /* hInstance */,
    HINSTANCE /* hPrevInstance */,
    LPSTR /* lpCmdLine */,
    int /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.Initialize()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                         *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL),
    m_pDevice(nullptr),
    m_pCompTarget(nullptr),
    m_pWICFactory(nullptr),
    m_pD3D11Device(nullptr),
    m_pD2DFactory(nullptr),
    m_pSurface(nullptr),
    m_pVisual(nullptr),
    m_pFadeInAnimation(nullptr),
    m_pFadeOutAnimation(nullptr),
    m_pEffectGroup(nullptr),
    m_bitmapHeight(0),
    m_bitmapWidth(0),
    m_pImageFileNames()
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()
{
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pWICFactory);
    SafeRelease(&m_pD2DFactory);
    SafeRelease(&m_pSurface);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pFadeOutAnimation);
    SafeRelease(&m_pFadeInAnimation);
    SafeRelease(&m_pEffectGroup);
}

/*******************************************************************
*                                                                  *
*  Create the application window.                                  *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Initialize device-independent resources, such 
    // as the Direct2D factory.
    hr = CreateDeviceIndependentResources();
    
    // Register the window class for the main application window
    // and create the window.
    if (SUCCEEDED(hr))
    {
        // Register the window class.
        WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
        wcex.style         = CS_HREDRAW | CS_VREDRAW;
        wcex.lpfnWndProc   = DemoApp::WndProc;
        wcex.cbClsExtra    = 0;
        wcex.cbWndExtra    = sizeof(LONG_PTR);
        wcex.hInstance     = HINST_THISCOMPONENT;
        wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
        wcex.lpszMenuName  = NULL;
        wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
        wcex.lpszClassName = L&quot;DirectCompDemoApp&quot;;

        RegisterClassEx(&wcex);

        // Create the application window.
        //
        // Because the CreateWindow function takes its size in pixels, we
        // obtain the system DPI and use it to scale the window size.
        int dpiX = 0;
        int dpiY = 0;
        HDC hdc = GetDC(NULL);
        if (hdc)
        {
            dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
            dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
            ReleaseDC(NULL, hdc);
        }

        m_hwnd = CreateWindow(
            L&quot;DirectCompDemoApp&quot;,
            L&quot;DirectComposition Demo Application&quot;,
            WS_OVERLAPPEDWINDOW,
            CW_USEDEFAULT,
            CW_USEDEFAULT,
            static_cast<UINT>(ceil(640.0f * dpiX / 96.0f)),
            static_cast<UINT>(ceil(480.0f * dpiY / 96.0f)),
            NULL,
            NULL,
            HINST_THISCOMPONENT,
            this
            );
    }

    hr = m_hwnd ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {   
        // Initialize DirectComposition resources, such as the
        // device object and composition target object.
        hr = InitializeDirectCompositionDevice();
    }

    if (SUCCEEDED(hr))
    {
        hr = CreateDeviceResources();
    }

    if (SUCCEEDED(hr))
    {
       ShowWindow(m_hwnd, SW_SHOWNORMAL);
       UpdateWindow(m_hwnd);
    }    

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the DirectComposition device object and    *
*  and the composition target object. These objects endure for    *
*  the lifetime of the application.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::InitializeDirectCompositionDevice()
{
    HRESULT hr = S_OK;

    D3D_FEATURE_LEVEL featureLevelSupported;

    // Create the D3D device object.
    D3D11CreateDevice(
        nullptr,
        D3D_DRIVER_TYPE_HARDWARE,
        NULL,
        D3D11_CREATE_DEVICE_BGRA_SUPPORT,
        NULL,
        0,
        D3D11_SDK_VERSION,
        &m_pD3D11Device,
        &featureLevelSupported,
        NULL);

    IDXGIDevice *pDXGIDevice = nullptr;

    hr = (m_pD3D11Device == nullptr) ? E_UNEXPECTED : S_OK;
    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = m_pD3D11Device->QueryInterface(&pDXGIDevice);
    }

    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, 
                __uuidof(IDCompositionDevice), 
                reinterpret_cast<void **>(&m_pDevice));
    }

    if (SUCCEEDED(hr))
    {
        // Create the composition target object.
        hr = m_pDevice->CreateTargetForHwnd(m_hwnd, TRUE, &m_pCompTarget);   
    }

    if (SUCCEEDED(hr))
    {
        // Create a visual object.          
        hr = m_pDevice->CreateVisual(&m_pVisual);  
    }

    if (SUCCEEDED(hr))
    {
        // Create a composition surface.
        hr = m_pDevice->CreateSurface(80, 80,//m_bitmapWidth, m_bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_PREMULTIPLIED, 
            &m_pSurface);
    }

    if (SUCCEEDED(hr))
    {
        hr = m_pVisual->SetContent(m_pSurface);
    }

    if (SUCCEEDED(hr))
    {
        hr = m_pCompTarget->SetRoot(m_pVisual);
    }

    if (SUCCEEDED(hr))
    {
        hr = m_pDevice->CreateAnimation(&m_pFadeInAnimation);
    }

    m_pFadeInAnimation->AddCubic(0.0f, 0.0f, 0.5f, 0.0f, 0.0f);
    m_pFadeInAnimation->End(2.0f, 1.0f); 

    if (SUCCEEDED(hr))
    {
        hr = m_pDevice->CreateAnimation(&m_pFadeOutAnimation);
    }

    if (SUCCEEDED(hr))
    {
        m_pFadeInAnimation->AddCubic(0.0f, 1.0f, 0.0f, 0.0f, 0.0f);
        m_pFadeInAnimation->End(2.0f, 0.0f); 
    }

    if (SUCCEEDED(hr))
    {
        hr = m_pDevice->CreateEffectGroup(&m_pEffectGroup);
    }

    if (SUCCEEDED(hr))
    {
        hr = m_pEffectGroup->SetOpacity(m_pFadeInAnimation);
    }

    SafeRelease(&pDXGIDevice);

    return hr;
}

/******************************************************************
*                                                                 *
*  This method is used to create resources which are not bound    *
*  to any device. Their lifetime effectively extends for the      *
*  duration of the app.                                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateDeviceIndependentResources()
{

    HRESULT hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pWICFactory)
        );


    if (SUCCEEDED(hr))
    {
        // Create a Direct2D factory.
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the D2D bitmap that the application gives  *
*  to DirectComposition to be composed.                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateDeviceResources()
{
    HRESULT hr = S_OK;

    RECT rc;
    GetClientRect(m_hwnd, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(
        rc.right - rc.left,
        rc.bottom - rc.top
        );

    // Create a Direct2D render target.
    hr = m_pD2DFactory->CreateHwndRenderTarget(
        D2D1::RenderTargetProperties(),
        D2D1::HwndRenderTargetProperties(m_hwnd, size),
        &m_pRenderTarget
        );
     
    // **********************************************
    // TODO: Remove hard coding. Enable the user to 
    //       select a directory.
    //***********************************************
    GetImageFilenames(L&quot;c:\\images\\*.jpg&quot;);

    return hr;
}


/******************************************************************
*                                                                 *
*  Discard device-specific resources.                             *
*                                                                 *
******************************************************************/

void DemoApp::DiscardDeviceResources()
{
    SafeRelease(&m_pRenderTarget);
    delete [] m_pImageFileNames;
}


/******************************************************************
*                                                                 *
*  The main window&#39;s message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}


HRESULT DemoApp::OnClick()
{
    HRESULT hr = S_OK;
    POINT offset = {0};
    IDXGISurface *pDXGISurface = nullptr;
    ID2D1RenderTarget* pRenderTarget = nullptr;
    ID2D1Bitmap *pBitmap = nullptr;
    LPCTSTR pbuf;
    static int i = 0;

    if (m_pEffectGroup == nullptr)
        return E_INVALIDARG;

    hr = m_pEffectGroup->SetOpacity(m_pFadeOutAnimation);

    if (SUCCEEDED(hr))
    {
        hr = m_pVisual->SetEffect(m_pEffectGroup);
    }

    if (SUCCEEDED(hr))
    {
        hr = m_pDevice->Commit();
    }


    hr = m_pSurface->BeginDraw(NULL, __uuidof(IDXGISurface), (void **)&pDXGISurface, &offset);

    if (pDXGISurface)
    {
        // Create a D2D render target which can draw into our off-screen D3D
        // surface. Given that we use a constant size for the texture, we
        // fix the DPI at 96.
        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_HARDWARE,
                D2D1::PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
                96.0,
                96.0
                );

        pbuf = new TCHAR[MAX_PATH];

        StringCbCopy((wchar_t *)pbuf, MAX_PATH,  L&quot;c:\\images\\&quot;);
        StringCchCat((wchar_t *)pbuf, MAX_PATH, m_pImageFileNames[i]);

        hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(pDXGISurface, &props, &pRenderTarget);

        pRenderTarget->BeginDraw();


        LoadJPEGImage(pRenderTarget, pbuf, &pBitmap);

        pRenderTarget->DrawBitmap(pBitmap, NULL, 1.0, 
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR, NULL);

        hr = pRenderTarget->EndDraw();
    }

    hr = m_pSurface->EndDraw();

    m_pEffectGroup->SetOpacity(m_pFadeInAnimation);
    m_pVisual->SetEffect(m_pEffectGroup);

    m_pDevice->Commit();

    i = (++i == 5) ? 0 : i;

    SafeRelease(&pRenderTarget);
    SafeRelease(&pDXGISurface);
    SafeRelease(&pBitmap);

    return hr;
}


/******************************************************************
*                                                                 *
*  Changes the opacity of a visual.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::SetVisualOpacity(IDCompositionVisual *pVisual, float opacity)
{
    HRESULT hr = S_OK;
    IDCompositionEffectGroup *pEffectGroup = nullptr;

    // Validate the input arguments.
    if (pVisual == NULL || (opacity > 1.0f || opacity < 0.0f))
        return E_INVALIDARG;

    // Create an effect group object.
    hr = m_pDevice->CreateEffectGroup(&pEffectGroup);

    if (SUCCEEDED(hr))
    {
        // Set the Opacity of the effect group object.
        hr = pEffectGroup->SetOpacity(opacity);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the effect group object to the Effect property of the visual.
        hr = m_pVisual->SetEffect(pEffectGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to DirectComposition.
        hr = m_pDevice->Commit();
    }

    // Free the effect group object.
    SafeRelease(&pEffectGroup);

    return hr;
}

/******************************************************************
*                                                                 *
*  The window&#39;s message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;
 
    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {
            case WM_PAINT:
                {
                    ValidateRect(hwnd, NULL);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_LBUTTONDOWN:
                {
                    pDemoApp->OnClick();
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                    pDemoApp->DiscardDeviceResources();
                }
                wasHandled = true;
                result = 1;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
}

/******************************************************************
*                                                                 *
*  This method will create a Direct2D bitmap from an application  *
*  resource.                                                      *
*                                                                 *
******************************************************************/

HRESULT DemoApp::LoadJPEGImage(
    ID2D1RenderTarget *pRenderTarget,
    PCWSTR fileName,
    ID2D1Bitmap **ppBitmap
    )
{
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pDecoder = nullptr;
    IWICBitmapFrameDecode *pDecoderFrame = nullptr;
    IWICFormatConverter *pConverter = nullptr;

    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pWICFactory)
        );

    hr = m_pWICFactory->CreateDecoderFromFilename(
        fileName,                       // Image to be decoded
        NULL,                           // Do not prefer a particular vendor
        GENERIC_READ,                   // Desired read access to the file
        WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
        &pDecoder                       // Pointer to the decoder
        );

    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
        hr = pDecoder->GetFrame(0, &pDecoderFrame);
    }

    if (SUCCEEDED(hr))
    {
        // Convert the image format to 32bppPBGRA
        // (DXGI_FORMAT_B8G8R8A8_UNORM + D2D1_ALPHA_MODE_PREMULTIPLIED).
        hr = m_pWICFactory->CreateFormatConverter(&pConverter);
    }

    if (SUCCEEDED(hr))
    {
        hr = pConverter->Initialize(
            pDecoderFrame,
            GUID_WICPixelFormat32bppPBGRA,
            WICBitmapDitherTypeNone,
            NULL,
            0.f,
            WICBitmapPaletteTypeMedianCut
            );
    }

    if (SUCCEEDED(hr))
    {
        // Create a Direct2D bitmap from the WIC bitmap.
        hr = pRenderTarget->CreateBitmapFromWicBitmap(
            pConverter,
            NULL,
            ppBitmap
            );
    }

    SafeRelease(&pDecoder);
    SafeRelease(&pDecoderFrame);
    SafeRelease(&pConverter);

    return hr;
}



HRESULT DemoApp::GetImageFilenames(TCHAR szDir[MAX_PATH])
{
    HRESULT hr = S_OK;
    HANDLE hFind = INVALID_HANDLE_VALUE;
    WIN32_FIND_DATA ffd;

    int fileCount = 0;

    hFind = FindFirstFile(szDir, &ffd);
    hr = (hFind == INVALID_HANDLE_VALUE) ? E_HANDLE : S_OK;

    if (SUCCEEDED(hr))
    {
        // Get a list of files in the directory.
        do
        {
            if (fileCount < 5)
            {
                m_pImageFileNames[fileCount] = new TCHAR[fileCount * MAX_PATH]; 
                StringCbCopy((wchar_t*)m_pImageFileNames[fileCount], 
                    MAX_PATH, ffd.cFileName);
                fileCount++;
            }
           
            else
            {
                break;
            }
        } 
        while (FindNextFile(hFind, &ffd) != 0);

        FindClose(hFind);
    }
    return hr;
}
```





## <a name="related-topics"></a>相關主題

<dl> <dt>

[動畫](animation.md)
</dt> </dl>

 

 
