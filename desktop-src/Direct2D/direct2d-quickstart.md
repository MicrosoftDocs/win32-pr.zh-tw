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
# <a name="creating-a-simple-direct2d-application"></a><span data-ttu-id="3efb1-108">建立簡單的 Direct2D 應用程式</span><span class="sxs-lookup"><span data-stu-id="3efb1-108">Creating a Simple Direct2D Application</span></span>

<span data-ttu-id="3efb1-109">本主題將逐步引導您完成建立 DemoApp 類別的程式，它會建立視窗並使用 Direct2D 來繪製方格和兩個矩形。</span><span class="sxs-lookup"><span data-stu-id="3efb1-109">This topic walks you through the process of creating the DemoApp class, which creates a window and uses Direct2D to draw a grid and two rectangles.</span></span> <span data-ttu-id="3efb1-110">在本教學課程中，您將瞭解如何建立 Direct2D 資源和繪製基本圖形。</span><span class="sxs-lookup"><span data-stu-id="3efb1-110">In this tutorial, you learn how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="3efb1-111">您也將瞭解如何建立應用程式的結構，藉由將資源建立降至最低來提高效能。</span><span class="sxs-lookup"><span data-stu-id="3efb1-111">You also learn how to structure your application to enhance performance by minimizing resource creation.</span></span>

<span data-ttu-id="3efb1-112">若要遵循本教學課程，您可以使用 Microsoft Visual Studio 2008 建立 Win32 專案，然後以本教學課程中所述的程式碼取代主要應用程式標頭和 .cpp 檔案中的程式碼。</span><span class="sxs-lookup"><span data-stu-id="3efb1-112">To follow the tutorial, you can use Microsoft Visual Studio 2008 to create a Win32 project and then replace the code in the main application header and cpp file with the code described in this tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="3efb1-113">如果您想要建立使用 Direct2D 的 Windows Store 應用程式，請參閱 [適用于 Windows 8 主題的 Direct2D 快速入門](direct2d-quickstart-with-device-context.md) 。</span><span class="sxs-lookup"><span data-stu-id="3efb1-113">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="3efb1-114">如需您可以用來建立 Direct2D 內容之介面的總覽，請參閱 [DIRECT2D API 總覽](the-direct2d-api.md)。</span><span class="sxs-lookup"><span data-stu-id="3efb1-114">For an overview of the interfaces you can use to create Direct2D content, see the [Direct2D API Overview](the-direct2d-api.md).</span></span>

<span data-ttu-id="3efb1-115">本教學課程包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="3efb1-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="3efb1-116">第1部分：建立 DemoApp 標頭</span><span class="sxs-lookup"><span data-stu-id="3efb1-116">Part 1: Create the DemoApp Header</span></span>](#part-1-create-the-demoapp-header)
-   [<span data-ttu-id="3efb1-117">第2部分：執行類別基礎結構</span><span class="sxs-lookup"><span data-stu-id="3efb1-117">Part 2: Implement the Class Infrastructure</span></span>](#part-2-implement-the-class-infrastructure)
-   [<span data-ttu-id="3efb1-118">第3部分：建立 Direct2D 資源</span><span class="sxs-lookup"><span data-stu-id="3efb1-118">Part 3: Create Direct2D Resources</span></span>](#part-3-create-direct2d-resources)
-   [<span data-ttu-id="3efb1-119">第4部分：轉譯 Direct2D 內容</span><span class="sxs-lookup"><span data-stu-id="3efb1-119">Part 4: Render Direct2D Content</span></span>](#part-4-render-direct2d-content)
-   [<span data-ttu-id="3efb1-120">總結</span><span class="sxs-lookup"><span data-stu-id="3efb1-120">Summary</span></span>](#summary)
-   [<span data-ttu-id="3efb1-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="3efb1-121">Related topics</span></span>](#related-topics)

<span data-ttu-id="3efb1-122">完成時，DemoApp 類別會產生下圖中顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="3efb1-122">Upon completion, the DemoApp class produces the output shown in the following illustration.</span></span>

![格線背景上兩個矩形的圖例](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a><span data-ttu-id="3efb1-124">第1部分：建立 DemoApp 標頭</span><span class="sxs-lookup"><span data-stu-id="3efb1-124">Part 1: Create the DemoApp Header</span></span>

<span data-ttu-id="3efb1-125">在此步驟中，您會藉由新增必要的標頭和宏，將應用程式設定為使用 Direct2D。</span><span class="sxs-lookup"><span data-stu-id="3efb1-125">In this step, you set up your application to use Direct2D by adding the necessary headers and macros.</span></span> <span data-ttu-id="3efb1-126">您也會宣告您將在本教學課程的後續部分中使用的方法和資料成員。</span><span class="sxs-lookup"><span data-stu-id="3efb1-126">You also declare the methods and data members you'll use in later parts of this tutorial.</span></span>

1.  <span data-ttu-id="3efb1-127">在您的應用程式標頭檔中，包含下列常用的標頭。</span><span class="sxs-lookup"><span data-stu-id="3efb1-127">In your application header file, include the following frequently used headers.</span></span>
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

    

2.  <span data-ttu-id="3efb1-128">宣告用來釋出介面和宏的其他函式，以處理錯誤，以及取得模組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="3efb1-128">Declare additional functions for releasing interfaces and macros for error handling and retrieving the module's base address.</span></span>
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

    

3.  <span data-ttu-id="3efb1-129">宣告方法來初始化類別、建立和捨棄資源、處理訊息迴圈、轉譯內容，以及 windows 程式。</span><span class="sxs-lookup"><span data-stu-id="3efb1-129">Declare methods for initializing the class, creating and discarding resources, handling the message loop, rendering content, and the windows procedure.</span></span>
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



    

4.  <span data-ttu-id="3efb1-130">宣告 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 物件的指標、 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 物件，以及兩個 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 物件做為類別成員。</span><span class="sxs-lookup"><span data-stu-id="3efb1-130">Declare pointers for an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object, and two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) objects as class members.</span></span>
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a><span data-ttu-id="3efb1-131">第2部分：執行類別基礎結構</span><span class="sxs-lookup"><span data-stu-id="3efb1-131">Part 2: Implement the Class Infrastructure</span></span>

<span data-ttu-id="3efb1-132">在此部分中，您會執行 DemoApp 的函式和函式、其初始化和訊息迴圈方法，以及 WinMain 函數。</span><span class="sxs-lookup"><span data-stu-id="3efb1-132">In this part, you implement the DemoApp constructor and destructor, its initialization and message looping methods, and the WinMain function.</span></span> <span data-ttu-id="3efb1-133">大部分的方法與在其他任何 Win32 應用程式中所找到的方法相同。</span><span class="sxs-lookup"><span data-stu-id="3efb1-133">Most of these methods look the same as those found in any other Win32 application.</span></span> <span data-ttu-id="3efb1-134">唯一的例外狀況是 Initialize 方法，它會呼叫 CreateDeviceIndependentResources 方法 (您在下一個部分中定義的) 會建立數個 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="3efb1-134">The only exception is the Initialize method, which calls the CreateDeviceIndependentResources method (which you define in the next part) that creates several Direct2D resources.</span></span>

1.  <span data-ttu-id="3efb1-135">在類別實檔案中，執行類別的函式和函式。</span><span class="sxs-lookup"><span data-stu-id="3efb1-135">In the class implementation file, implement the class constructor and destructor.</span></span> <span data-ttu-id="3efb1-136">此函式應該將其成員初始化為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3efb1-136">The constructor should initialize its members to **NULL**.</span></span> <span data-ttu-id="3efb1-137">此函式應該釋放任何儲存為類別成員的介面。</span><span class="sxs-lookup"><span data-stu-id="3efb1-137">The destructor should release any interfaces stored as class members.</span></span>
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



    

2.  <span data-ttu-id="3efb1-138">執行可轉譯和分派訊息的 DemoApp：： RunMessageLoop 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-138">Implement the DemoApp::RunMessageLoop method that translates and dispatches messages.</span></span>
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

    

3.  <span data-ttu-id="3efb1-139">執行初始化方法來建立視窗、顯示它，並呼叫 DemoApp：： CreateDeviceIndependentResources 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-139">Implement the Initialize method that creates the window, shows it, and calls the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="3efb1-140">您將在下一節中執行 CreateDeviceIndependentResources 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-140">You implement the CreateDeviceIndependentResources method in the next section.</span></span>
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

    

4.  <span data-ttu-id="3efb1-141">建立作為應用程式進入點的 WinMain 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-141">Create the WinMain method that serves as the application entry point.</span></span> <span data-ttu-id="3efb1-142">初始化 DemoApp 類別的實例，並開始它的訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="3efb1-142">Initialize an instance of the DemoApp class and begin its message loop.</span></span>
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

    

## <a name="part-3-create-direct2d-resources"></a><span data-ttu-id="3efb1-143">第3部分：建立 Direct2D 資源</span><span class="sxs-lookup"><span data-stu-id="3efb1-143">Part 3: Create Direct2D Resources</span></span>

<span data-ttu-id="3efb1-144">在此部分中，您會建立用來繪製的 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="3efb1-144">In this part, you create the Direct2D resources that you use to draw.</span></span> <span data-ttu-id="3efb1-145">Direct2D 提供兩種類型的資源：與裝置無關的資源，這些資源可在應用程式持續時間和裝置相依的資源上持續進行。</span><span class="sxs-lookup"><span data-stu-id="3efb1-145">Direct2D provides two types of resources: device-independent resources that can last for the duration of the application, and device-dependent resources.</span></span> <span data-ttu-id="3efb1-146">與裝置相關的資源會與特定的轉譯裝置相關聯，而且如果移除該裝置，將會停止運作。</span><span class="sxs-lookup"><span data-stu-id="3efb1-146">Device-dependent resources are associated with a particular rendering device and will cease to function if that device is removed.</span></span>

1.  <span data-ttu-id="3efb1-147">執行 DemoApp：： CreateDeviceIndependentResources 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-147">Implement the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="3efb1-148">在方法中，建立 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)，這是與裝置無關的資源，用來建立其他 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="3efb1-148">In the method, create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), a device-independent resource, for creating other Direct2D resources.</span></span> <span data-ttu-id="3efb1-149">使用 **m \_ pDirect2DdFactory** 類別成員來儲存 factory。</span><span class="sxs-lookup"><span data-stu-id="3efb1-149">Use the **m\_pDirect2DdFactory** class member to store the factory.</span></span>
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  <span data-ttu-id="3efb1-150">執行 DemoApp：： CreateDeviceResources 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-150">Implement the DemoApp::CreateDeviceResources method.</span></span> <span data-ttu-id="3efb1-151">這個方法會建立視窗的裝置相依資源、轉譯目標和兩筆筆刷。</span><span class="sxs-lookup"><span data-stu-id="3efb1-151">This method creates the window's device-dependent resources, a render target, and two brushes.</span></span> <span data-ttu-id="3efb1-152">取得工作區的大小，並建立與轉譯至視窗 **HWND** 相同大小的 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 。</span><span class="sxs-lookup"><span data-stu-id="3efb1-152">Retrieve the size of the client area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of the same size that renders to the window's **HWND**.</span></span> <span data-ttu-id="3efb1-153">將轉譯目標儲存在 **m \_ pRenderTarget** 類別成員中。</span><span class="sxs-lookup"><span data-stu-id="3efb1-153">Store the render target in the **m\_pRenderTarget** class member.</span></span>
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

    

3.  <span data-ttu-id="3efb1-154">使用轉譯目標來建立灰色 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 和矢菊花 blue **ID2D1SolidColorBrush**。</span><span class="sxs-lookup"><span data-stu-id="3efb1-154">Use the render target to create a gray [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) and a cornflower blue **ID2D1SolidColorBrush**.</span></span>
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

    

4.  <span data-ttu-id="3efb1-155">因為此方法會重複呼叫，所以請加入 if 語句來檢查轉譯目標 (**m \_ pRenderTarget** ) 是否已存在。</span><span class="sxs-lookup"><span data-stu-id="3efb1-155">Because this method will be called repeatedly, add an if statement to check whether the render target (**m\_pRenderTarget** ) already exists.</span></span> <span data-ttu-id="3efb1-156">下列程式碼顯示完整的 CreateDeviceResources 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-156">The following code shows the complete CreateDeviceResources method.</span></span>
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

    

5.  <span data-ttu-id="3efb1-157">執行 DemoApp：:D iscardDeviceResources 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-157">Implement the DemoApp::DiscardDeviceResources method.</span></span> <span data-ttu-id="3efb1-158">在這個方法中，釋放轉譯目標和您在 DemoApp：： CreateDeviceResources 方法中建立的兩筆筆刷。</span><span class="sxs-lookup"><span data-stu-id="3efb1-158">In this method, release the render target and the two brushes you created in the DemoApp::CreateDeviceResources method.</span></span>
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a><span data-ttu-id="3efb1-159">第4部分：轉譯 Direct2D 內容</span><span class="sxs-lookup"><span data-stu-id="3efb1-159">Part 4: Render Direct2D Content</span></span>

<span data-ttu-id="3efb1-160">在這個部分中，您會執行 windows 程式、繪製內容的 OnRender 方法，以及調整視窗大小時調整轉譯目標大小的 OnResize 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-160">In this part, you implement the windows procedure, the OnRender method that paints content, and the OnResize method that adjusts the size of the render target when the window is resized.</span></span>

1.  <span data-ttu-id="3efb1-161">執行 DemoApp：： WndProc 方法來處理視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="3efb1-161">Implement the DemoApp::WndProc method to handle window messages.</span></span> <span data-ttu-id="3efb1-162">若為 [**WM \_ 大小**](../winmsg/wm-size.md) 的訊息，請呼叫 DemoApp：： OnResize 方法，並將新的寬度和高度傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="3efb1-162">For the [**WM\_SIZE**](../winmsg/wm-size.md) message, call the DemoApp::OnResize method and pass it the new width and height.</span></span> <span data-ttu-id="3efb1-163">若為 [**wm \_ 油漆**](/windows/desktop/gdi/wm-paint) 和 [**wm \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) 訊息，請呼叫 DemoApp：： OnRender 方法來繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="3efb1-163">For the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) messages, call the DemoApp::OnRender method to paint the window.</span></span> <span data-ttu-id="3efb1-164">您會在後續步驟中執行 OnRender 和 OnResize 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-164">You implement the OnRender and OnResize methods in the steps that follow.</span></span>
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

    

2.  <span data-ttu-id="3efb1-165">執行 DemoApp：： OnRender 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-165">Implement the DemoApp::OnRender method.</span></span> <span data-ttu-id="3efb1-166">首先，建立 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="3efb1-166">First, create an **HRESULT**.</span></span> <span data-ttu-id="3efb1-167">然後呼叫 CreateDeviceResource 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-167">Then call the CreateDeviceResource method.</span></span> <span data-ttu-id="3efb1-168">每次繪製視窗時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-168">This method is called every time the window is painted.</span></span> <span data-ttu-id="3efb1-169">回想一下，在第3部分的步驟4中，您已加入 **if** 語句，以防止方法在轉譯目標已存在時執行任何工作。</span><span class="sxs-lookup"><span data-stu-id="3efb1-169">Recall that, in step 4 of Part 3, you added an **if** statement to prevent the method from doing any work if the render target already exists.</span></span>
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  <span data-ttu-id="3efb1-170">確認 CreateDeviceResource 方法成功。</span><span class="sxs-lookup"><span data-stu-id="3efb1-170">Verify that the CreateDeviceResource method succeeded.</span></span> <span data-ttu-id="3efb1-171">如果沒有，請不要執行任何繪製。</span><span class="sxs-lookup"><span data-stu-id="3efb1-171">If it didn't, don't perform any drawing.</span></span>
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  <span data-ttu-id="3efb1-172">在您剛剛建立的 **if** 語句內，藉由呼叫轉譯目標的 BeginDraw 方法來起始繪製。</span><span class="sxs-lookup"><span data-stu-id="3efb1-172">Inside the **if** statement you just created, initiate drawing by calling the render target's BeginDraw method.</span></span> <span data-ttu-id="3efb1-173">將轉譯目標的轉換設定為識別矩陣，並清除視窗。</span><span class="sxs-lookup"><span data-stu-id="3efb1-173">Set the render target's transform to the identity matrix, and clear the window.</span></span>
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  <span data-ttu-id="3efb1-174">取出繪圖區域的大小。</span><span class="sxs-lookup"><span data-stu-id="3efb1-174">Retrieve the size of the drawing area.</span></span>
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  <span data-ttu-id="3efb1-175">使用 **for** 迴圈和轉譯目標的 [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) 方法繪製一系列的線條，以繪製格線背景。</span><span class="sxs-lookup"><span data-stu-id="3efb1-175">Draw a grid background by using a **for** loop and the render target's [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) method to draw a series of lines.</span></span>
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

    

7.  <span data-ttu-id="3efb1-176">建立兩個在螢幕上置中的矩形基本物件。</span><span class="sxs-lookup"><span data-stu-id="3efb1-176">Create two rectangle primitives that are centered on the screen.</span></span>
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

    

8.  <span data-ttu-id="3efb1-177">使用呈現目標的 [**graphicswindow.fillrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) 方法，以灰色筆刷繪製第一個矩形的內部。</span><span class="sxs-lookup"><span data-stu-id="3efb1-177">Use the render target's [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the first rectangle with the gray brush.</span></span>
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  <span data-ttu-id="3efb1-178">使用呈現目標的 [**graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) 方法，以矢菊花藍色筆刷繪製第二個矩形的外框。</span><span class="sxs-lookup"><span data-stu-id="3efb1-178">Use the render target's [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the second rectangle with the cornflower blue brush.</span></span>
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. <span data-ttu-id="3efb1-179">呼叫呈現目標的 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-179">Call the render target's [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="3efb1-180">**EndDraw** 方法會傳回 **HRESULT** ，指出繪圖作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="3efb1-180">The **EndDraw** method returns an **HRESULT** to indicate whether the drawing operations were successful.</span></span> <span data-ttu-id="3efb1-181">關閉您在步驟3中開始的 **if** 語句。</span><span class="sxs-lookup"><span data-stu-id="3efb1-181">Close the **if** statement you began in Step 3.</span></span>
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. <span data-ttu-id="3efb1-182">檢查 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)所傳回的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="3efb1-182">Check the **HRESULT** returned by [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span> <span data-ttu-id="3efb1-183">如果它指出需要重新建立轉譯目標，請呼叫 DemoApp：:D iscardDeviceResources 方法來釋放它;它會在下一次視窗收到 [**wm \_ 油漆**](/windows/desktop/gdi/wm-paint) 或 [**wm \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) 訊息時重新建立。</span><span class="sxs-lookup"><span data-stu-id="3efb1-183">If it indicates that the render target needs to be recreated, call the DemoApp::DiscardDeviceResources method to release it; it will be recreated the next time the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) or [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span>
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. <span data-ttu-id="3efb1-184">傳回 **HRESULT** 並關閉方法。</span><span class="sxs-lookup"><span data-stu-id="3efb1-184">Return the **HRESULT** and close the method.</span></span>
```C++
        return hr;
    }
```

    

13. <span data-ttu-id="3efb1-185">執行 DemoApp：： OnResize 方法，讓它將轉譯目標調整為視窗的新大小。</span><span class="sxs-lookup"><span data-stu-id="3efb1-185">Implement the DemoApp::OnResize method so that it resizes the render target to the new size of the window.</span></span>
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

    

<span data-ttu-id="3efb1-186">您已完成教學課程。</span><span class="sxs-lookup"><span data-stu-id="3efb1-186">You've completed the tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="3efb1-187">若要使用 Direct2D，請確定您的應用程式包含 d2d1 .h 標頭檔案，並針對 d2d1 .lib 程式庫進行編譯。</span><span class="sxs-lookup"><span data-stu-id="3efb1-187">To use Direct2D, ensure that your application includes the d2d1.h header file and compiles against the d2d1.lib library.</span></span> <span data-ttu-id="3efb1-188">您可以在 [適用于 Windows 7 的 Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx)中找到 d2d1 .h 和 d2d1。</span><span class="sxs-lookup"><span data-stu-id="3efb1-188">You can find d2d1.h and d2d1.lib in [Windows Software Development Kit (SDK) for Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

 

## <a name="summary"></a><span data-ttu-id="3efb1-189">總結</span><span class="sxs-lookup"><span data-stu-id="3efb1-189">Summary</span></span>

<span data-ttu-id="3efb1-190">在本教學課程中，您已瞭解如何建立 Direct2D 資源和繪製基本圖形。</span><span class="sxs-lookup"><span data-stu-id="3efb1-190">In this tutorial, you learned how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="3efb1-191">您也已瞭解如何建立應用程式的結構，藉由將資源建立降至最低來提高效能。</span><span class="sxs-lookup"><span data-stu-id="3efb1-191">You also learned how to structure your application to enhance performance by minimizing resource creation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3efb1-192">相關主題</span><span class="sxs-lookup"><span data-stu-id="3efb1-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3efb1-193">Direct2D API 概觀</span><span class="sxs-lookup"><span data-stu-id="3efb1-193">Direct2D API Overview</span></span>](the-direct2d-api.md)
</dt> <dt>

[<span data-ttu-id="3efb1-194">改善 Direct2D 的效能</span><span class="sxs-lookup"><span data-stu-id="3efb1-194">Improving the Performance of Direct2D</span></span>](improving-direct2d-performance.md)
</dt> </dl>

 

 