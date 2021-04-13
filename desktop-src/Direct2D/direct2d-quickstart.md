---
title: 建立簡單的 Direct2D 應用程式
description: 引導您完成建立視窗以轉譯 Direct2D 內容的程式。
ms.assetid: a627523e-417a-40cd-82c0-4f0380a3a0b1
keywords:
- Direct2D，教學課程
- Direct2D，逐步解說
- Direct2D，建立應用程式
- Direct2D，應用程式
- 適用于 Direct2D 的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d023e348e30b4e421ffe177f30c0c55a344fba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104564482"
---
# <a name="creating-a-simple-direct2d-application"></a>建立簡單的 Direct2D 應用程式

本主題將逐步引導您完成建立 DemoApp 類別的程式，它會建立視窗並使用 Direct2D 來繪製方格和兩個矩形。 在本教學課程中，您將瞭解如何建立 Direct2D 資源和繪製基本圖形。 您也將瞭解如何建立應用程式的結構，藉由將資源建立降至最低來提高效能。

若要遵循本教學課程，您可以使用 Microsoft Visual Studio 2008 建立 Win32 專案，然後以本教學課程中所述的程式碼取代主要應用程式標頭和 .cpp 檔案中的程式碼。

> [!Note]  
> 如果您想要建立使用 Direct2D 的 Windows Store 應用程式，請參閱 [適用于 Windows 8 主題的 Direct2D 快速入門](direct2d-quickstart-with-device-context.md) 。

 

如需您可以用來建立 Direct2D 內容之介面的總覽，請參閱 [DIRECT2D API 總覽](the-direct2d-api.md)。

本教學課程包含下列部分：

-   [第1部分：建立 DemoApp 標頭](#part-1-create-the-demoapp-header)
-   [第2部分：執行類別基礎結構](#part-2-implement-the-class-infrastructure)
-   [第3部分：建立 Direct2D 資源](#part-3-create-direct2d-resources)
-   [第4部分：轉譯 Direct2D 內容](#part-4-render-direct2d-content)
-   [總結](#summary)
-   [相關主題](#related-topics)

完成時，DemoApp 類別會產生下圖中顯示的輸出。

![格線背景上兩個矩形的圖例](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a>第1部分：建立 DemoApp 標頭

在此步驟中，您會藉由新增必要的標頭和宏，將應用程式設定為使用 Direct2D。 您也會宣告您將在本教學課程的後續部分中使用的方法和資料成員。

1.  在您的應用程式標頭檔中，包含下列常用的標頭。
```C++
    // Windows Header Files:
    #include <windows.h>

    // C RunTime Header Files:
    #include <stdlib.h>
    #include <malloc.h>
    #include <memory.h>
    #include <wchar.h>
    #include <math.h>

    #include <d2d1.h>
    #include <d2d1helper.h>
    #include <dwrite.h>
    #include <wincodec.h>
```

    

2.  宣告用來釋出介面和宏的其他函式，以處理錯誤，以及取得模組的基底位址。
```C++
    template<class Interface>
    inline void SafeRelease(
        Interface **ppInterfaceToRelease
        )
    {
        if (*ppInterfaceToRelease != NULL)
        {
            (*ppInterfaceToRelease)->Release();

            (*ppInterfaceToRelease) = NULL;
        }
    }


    #ifndef Assert
    #if defined( DEBUG ) || defined( _DEBUG )
    #define Assert(b) do {if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}} while(0)
    #else
    #define Assert(b)
    #endif //DEBUG || _DEBUG
    #endif



    #ifndef HINST_THISCOMPONENT
    EXTERN_C IMAGE_DOS_HEADER __ImageBase;
    #define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
    #endif
```

    

3.  宣告方法來初始化類別、建立和捨棄資源、處理訊息迴圈、轉譯內容，以及 windows 程式。
```C++
    class DemoApp
    {
    public:
        DemoApp();
        ~DemoApp();

        // Register the window class and call methods for instantiating drawing resources
        HRESULT Initialize();

        // Process and dispatch messages
        void RunMessageLoop();

    private:
        // Initialize device-independent resources.
        HRESULT CreateDeviceIndependentResources();

        // Initialize device-dependent resources.
        HRESULT CreateDeviceResources();

        // Release device-dependent resource.
        void DiscardDeviceResources();

        // Draw content.
        HRESULT OnRender();

        // Resize the render target.
        void OnResize(
            UINT width,
            UINT height
            );

        // The windows procedure.
        static LRESULT CALLBACK WndProc(
            HWND hWnd,
            UINT message,
            WPARAM wParam,
            LPARAM lParam
            );

    
};
```



    

4.  宣告 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 物件的指標、 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 物件，以及兩個 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 物件做為類別成員。
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a>第2部分：執行類別基礎結構

在此部分中，您會執行 DemoApp 的函式和函式、其初始化和訊息迴圈方法，以及 WinMain 函數。 大部分的方法與在其他任何 Win32 應用程式中所找到的方法相同。 唯一的例外狀況是 Initialize 方法，它會呼叫 CreateDeviceIndependentResources 方法 (您在下一個部分中定義的) 會建立數個 Direct2D 資源。

1.  在類別實檔案中，執行類別的函式和函式。 此函式應該將其成員初始化為 **Null**。 此函式應該釋放任何儲存為類別成員的介面。
```C++
    DemoApp::DemoApp() :
        m_hwnd(NULL),
        m_pDirect2dFactory(NULL),
        m_pRenderTarget(NULL),
        m_pLightSlateGrayBrush(NULL),
        m_pCornflowerBlueBrush(NULL)
    {
    }

    
DemoApp::~DemoApp()
    {
        SafeRelease(&m_pDirect2dFactory);
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);

    }
```



    

2.  執行可轉譯和分派訊息的 DemoApp：： RunMessageLoop 方法。
```C++
    void DemoApp::RunMessageLoop()
    {
        MSG msg;

        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```

    

3.  執行初始化方法來建立視窗、顯示它，並呼叫 DemoApp：： CreateDeviceIndependentResources 方法。 您將在下一節中執行 CreateDeviceIndependentResources 方法。
```C++
    HRESULT DemoApp::Initialize()
    {
        HRESULT hr;

        // Initialize device-indpendent resources, such
        // as the Direct2D factory.
        hr = CreateDeviceIndependentResources();

        if (SUCCEEDED(hr))
        {
            // Register the window class.
            WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
            wcex.style         = CS_HREDRAW | CS_VREDRAW;
            wcex.lpfnWndProc   = DemoApp::WndProc;
            wcex.cbClsExtra    = 0;
            wcex.cbWndExtra    = sizeof(LONG_PTR);
            wcex.hInstance     = HINST_THISCOMPONENT;
            wcex.hbrBackground = NULL;
            wcex.lpszMenuName  = NULL;
            wcex.hCursor       = LoadCursor(NULL, IDI_APPLICATION);
            wcex.lpszClassName = L"D2DDemoApp";

            RegisterClassEx(&wcex);


            // Because the CreateWindow function takes its size in pixels,
            // obtain the system DPI and use it to scale the window size.
            FLOAT dpiX, dpiY;

            // The factory returns the current system DPI. This is also the value it will use
            // to create its own windows.
            m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


            // Create the window.
            m_hwnd = CreateWindow(
                L"D2DDemoApp",
                L"Direct2D Demo App",
                WS_OVERLAPPEDWINDOW,
                CW_USEDEFAULT,
                CW_USEDEFAULT,
                static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
                static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
                NULL,
                NULL,
                HINST_THISCOMPONENT,
                this
                );
            hr = m_hwnd ? S_OK : E_FAIL;
            if (SUCCEEDED(hr))
            {
                ShowWindow(m_hwnd, SW_SHOWNORMAL);
                UpdateWindow(m_hwnd);
            }
        }

        return hr;
    }
```

    

4.  建立作為應用程式進入點的 WinMain 方法。 初始化 DemoApp 類別的實例，並開始它的訊息迴圈。
```C++
    int WINAPI WinMain(
        HINSTANCE /* hInstance */,
        HINSTANCE /* hPrevInstance */,
        LPSTR /* lpCmdLine */,
        int /* nCmdShow */
        )
    {
        // Use HeapSetInformation to specify that the process should
        // terminate if the heap manager detects an error in any heap used
        // by the process.
        // The return value is ignored, because we want to continue running in the
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
```

    

## <a name="part-3-create-direct2d-resources"></a>第3部分：建立 Direct2D 資源

在此部分中，您會建立用來繪製的 Direct2D 資源。 Direct2D 提供兩種類型的資源：與裝置無關的資源，這些資源可在應用程式持續時間和裝置相依的資源上持續進行。 與裝置相關的資源會與特定的轉譯裝置相關聯，而且如果移除該裝置，將會停止運作。

1.  執行 DemoApp：： CreateDeviceIndependentResources 方法。 在方法中，建立 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)，這是與裝置無關的資源，用來建立其他 Direct2D 資源。 使用 **m \_ pDirect2DdFactory** 類別成員來儲存 factory。
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  執行 DemoApp：： CreateDeviceResources 方法。 這個方法會建立視窗的裝置相依資源、轉譯目標和兩筆筆刷。 取得工作區的大小，並建立與轉譯至視窗 **HWND** 相同大小的 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 。 將轉譯目標儲存在 **m \_ pRenderTarget** 類別成員中。
```C++
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );
    
```

    

3.  使用轉譯目標來建立灰色 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 和矢菊花 blue **ID2D1SolidColorBrush**。
```C++
            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
```

    

4.  因為此方法會重複呼叫，所以請加入 if 語句來檢查轉譯目標 (**m \_ pRenderTarget** ) 是否已存在。 下列程式碼顯示完整的 CreateDeviceResources 方法。
```C++
    HRESULT DemoApp::CreateDeviceResources()
    {
        HRESULT hr = S_OK;

        if (!m_pRenderTarget)
        {
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );


            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
        }

        return hr;
    }
```

    

5.  執行 DemoApp：:D iscardDeviceResources 方法。 在這個方法中，釋放轉譯目標和您在 DemoApp：： CreateDeviceResources 方法中建立的兩筆筆刷。
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a>第4部分：轉譯 Direct2D 內容

在這個部分中，您會執行 windows 程式、繪製內容的 OnRender 方法，以及調整視窗大小時調整轉譯目標大小的 OnResize 方法。

1.  執行 DemoApp：： WndProc 方法來處理視窗訊息。 若為 [**WM \_ 大小**](../winmsg/wm-size.md) 的訊息，請呼叫 DemoApp：： OnResize 方法，並將新的寬度和高度傳遞給它。 若為 [**wm \_ 油漆**](/windows/desktop/gdi/wm-paint) 和 [**wm \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) 訊息，請呼叫 DemoApp：： OnRender 方法來繪製視窗。 您會在後續步驟中執行 OnRender 和 OnResize 方法。
```C++
    LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
    {
        LRESULT result = 0;

        if (message == WM_CREATE)
        {
            LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
            DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

            ::SetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA,
                reinterpret_cast<LONG_PTR>(pDemoApp)
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
                case WM_SIZE:
                    {
                        UINT width = LOWORD(lParam);
                        UINT height = HIWORD(lParam);
                        pDemoApp->OnResize(width, height);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DISPLAYCHANGE:
                    {
                        InvalidateRect(hwnd, NULL, FALSE);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_PAINT:
                    {
                        pDemoApp->OnRender();
                        ValidateRect(hwnd, NULL);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DESTROY:
                    {
                        PostQuitMessage(0);
                    }
                    result = 1;
                    wasHandled = true;
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
    
```

    

2.  執行 DemoApp：： OnRender 方法。 首先，建立 **HRESULT**。 然後呼叫 CreateDeviceResource 方法。 每次繪製視窗時，就會呼叫這個方法。 回想一下，在第3部分的步驟4中，您已加入 **if** 語句，以防止方法在轉譯目標已存在時執行任何工作。
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  確認 CreateDeviceResource 方法成功。 如果沒有，請不要執行任何繪製。
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  在您剛剛建立的 **if** 語句內，藉由呼叫轉譯目標的 BeginDraw 方法來起始繪製。 將轉譯目標的轉換設定為識別矩陣，並清除視窗。
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  取出繪圖區域的大小。
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  使用 **for** 迴圈和轉譯目標的 [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) 方法繪製一系列的線條，以繪製格線背景。
```C++
            // Draw a grid background.
            int width = static_cast<int>(rtSize.width);
            int height = static_cast<int>(rtSize.height);

            for (int x = 0; x < width; x += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                    D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }

            for (int y = 0; y < height; y += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                    D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }
```

    

7.  建立兩個在螢幕上置中的矩形基本物件。
```C++
            // Draw two rectangles.
            D2D1_RECT_F rectangle1 = D2D1::RectF(
                rtSize.width/2 - 50.0f,
                rtSize.height/2 - 50.0f,
                rtSize.width/2 + 50.0f,
                rtSize.height/2 + 50.0f
                );

            D2D1_RECT_F rectangle2 = D2D1::RectF(
                rtSize.width/2 - 100.0f,
                rtSize.height/2 - 100.0f,
                rtSize.width/2 + 100.0f,
                rtSize.height/2 + 100.0f
                );
    
```

    

8.  使用呈現目標的 [**graphicswindow.fillrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) 方法，以灰色筆刷繪製第一個矩形的內部。
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  使用呈現目標的 [**graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) 方法，以矢菊花藍色筆刷繪製第二個矩形的外框。
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. 呼叫呈現目標的 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。 **EndDraw** 方法會傳回 **HRESULT** ，指出繪圖作業是否成功。 關閉您在步驟3中開始的 **if** 語句。
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. 檢查 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)所傳回的 **HRESULT** 。 如果它指出需要重新建立轉譯目標，請呼叫 DemoApp：:D iscardDeviceResources 方法來釋放它;它會在下一次視窗收到 [**wm \_ 油漆**](/windows/desktop/gdi/wm-paint) 或 [**wm \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) 訊息時重新建立。
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. 傳回 **HRESULT** 並關閉方法。
```C++
        return hr;
    }
```

    

13. 執行 DemoApp：： OnResize 方法，讓它將轉譯目標調整為視窗的新大小。
```C++
    void DemoApp::OnResize(UINT width, UINT height)
    {
        if (m_pRenderTarget)
        {
            // Note: This method can fail, but it's okay to ignore the
            // error here, because the error will be returned again
            // the next time EndDraw is called.
            m_pRenderTarget->Resize(D2D1::SizeU(width, height));
        }
    }
```

    

您已完成教學課程。

> [!Note]  
> 若要使用 Direct2D，請確定您的應用程式包含 d2d1 .h 標頭檔案，並針對 d2d1 .lib 程式庫進行編譯。 您可以在 [適用于 Windows 7 的 Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx)中找到 d2d1 .h 和 d2d1。

 

## <a name="summary"></a>總結

在本教學課程中，您已瞭解如何建立 Direct2D 資源和繪製基本圖形。 您也已瞭解如何建立應用程式的結構，藉由將資源建立降至最低來提高效能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D API 概觀](the-direct2d-api.md)
</dt> <dt>

[改善 Direct2D 的效能](improving-direct2d-performance.md)
</dt> </dl>

 

 