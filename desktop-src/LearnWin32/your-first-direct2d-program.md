---
title: 您的第一個 Direct2D 計畫
description: 讓我們來建立我們的第一個 Direct2D 計畫。 此程式不會執行任何複雜的工作 \ 8212;它只會繪製一個會填滿視窗工作區的圓形。 但這個程式引進許多重要的 Direct2D 概念。
ms.assetid: 940cc5e4-2952-4714-bf32-c611a965f819
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d445f98c5dc6a6e5d1aa91d913010cb406a67992
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375092"
---
# <a name="your-first-direct2d-program"></a><span data-ttu-id="aa35b-105">您的第一個 Direct2D 計畫</span><span class="sxs-lookup"><span data-stu-id="aa35b-105">Your First Direct2D Program</span></span>

<span data-ttu-id="aa35b-106">讓我們來建立我們的第一個 Direct2D 計畫。</span><span class="sxs-lookup"><span data-stu-id="aa35b-106">Let's create our first Direct2D program.</span></span> <span data-ttu-id="aa35b-107">程式並不會執行任何複雜的工作，只是繪製一個會填滿視窗工作區的圓形。</span><span class="sxs-lookup"><span data-stu-id="aa35b-107">The program does not do anything fancy — it just draws a circle that fills the client area of the window.</span></span> <span data-ttu-id="aa35b-108">但這個程式引進許多重要的 Direct2D 概念。</span><span class="sxs-lookup"><span data-stu-id="aa35b-108">But this program introduces many essential Direct2D concepts.</span></span>

![圓形程式的螢幕擷取畫面。](images/graphics08.png)

<span data-ttu-id="aa35b-110">以下是圓形程式的程式代碼清單。</span><span class="sxs-lookup"><span data-stu-id="aa35b-110">Here is the code listing for the Circle program.</span></span> <span data-ttu-id="aa35b-111">此程式會重複使用 `BaseWindow` [管理應用程式狀態](managing-application-state-.md)主題中定義的類別。</span><span class="sxs-lookup"><span data-stu-id="aa35b-111">The program re-uses the `BaseWindow` class that was defined in the topic [Managing Application State](managing-application-state-.md).</span></span> <span data-ttu-id="aa35b-112">稍後的主題將詳細檢查程式碼。</span><span class="sxs-lookup"><span data-stu-id="aa35b-112">Later topics will examine the code in detail.</span></span>


```C++
#include <windows.h>
#include <d2d1.h>
#pragma comment(lib, "d2d1")

#include "basewin.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

class MainWindow : public BaseWindow<MainWindow>
{
    ID2D1Factory            *pFactory;
    ID2D1HwndRenderTarget   *pRenderTarget;
    ID2D1SolidColorBrush    *pBrush;
    D2D1_ELLIPSE            ellipse;

    void    CalculateLayout();
    HRESULT CreateGraphicsResources();
    void    DiscardGraphicsResources();
    void    OnPaint();
    void    Resize();

public:

    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL)
    {
    }

    PCWSTR  ClassName() const { return L"Circle Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};

// Recalculate drawing layout when the size of the window changes.

void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}

HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}

void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}

void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}

void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Circle", WS_OVERLAPPEDWINDOW))
    {
        return 0;
    }

    ShowWindow(win.Window(), nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}

LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;

    case WM_DESTROY:
        DiscardGraphicsResources();
        SafeRelease(&pFactory);
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        OnPaint();
        return 0;



    case WM_SIZE:
        Resize();
        return 0;
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```





<span data-ttu-id="aa35b-113">您可以從 [Direct2D Circle 範例](direct2d-circle-sample.md)下載完整的 Visual Studio 專案。</span><span class="sxs-lookup"><span data-stu-id="aa35b-113">You can download the complete Visual Studio project from [Direct2D Circle Sample](direct2d-circle-sample.md).</span></span>

## <a name="the-d2d1-namespace"></a><span data-ttu-id="aa35b-114">D2D1 命名空間</span><span class="sxs-lookup"><span data-stu-id="aa35b-114">The D2D1 Namespace</span></span>

<span data-ttu-id="aa35b-115">**D2D1** 命名空間包含 helper 函式和類別。</span><span class="sxs-lookup"><span data-stu-id="aa35b-115">The **D2D1** namespace contains helper functions and classes.</span></span> <span data-ttu-id="aa35b-116">這些都不是 Direct2D API 的一部分，您可以在不使用的情況下編寫 Direct2D 的程式碼，但它們有助於簡化您的程式碼。</span><span class="sxs-lookup"><span data-stu-id="aa35b-116">These are not strictly part of the Direct2D API — you can program Direct2D without using them — but they help simplify your code.</span></span> <span data-ttu-id="aa35b-117">**D2D1** 命名空間包含：</span><span class="sxs-lookup"><span data-stu-id="aa35b-117">The **D2D1** namespace contains:</span></span>

-   <span data-ttu-id="aa35b-118">用來建立色彩值的 [**ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) 類別。</span><span class="sxs-lookup"><span data-stu-id="aa35b-118">A [**ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) class for constructing color values.</span></span>
-   <span data-ttu-id="aa35b-119">用來建立轉換矩陣的 [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) 。</span><span class="sxs-lookup"><span data-stu-id="aa35b-119">A [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) for constructing transformation matrices.</span></span>
-   <span data-ttu-id="aa35b-120">用來初始化 Direct2D 結構的一組函數。</span><span class="sxs-lookup"><span data-stu-id="aa35b-120">A set of functions to initialize Direct2D structures.</span></span>

<span data-ttu-id="aa35b-121">您將在此課程模組中看到 **D2D1** 命名空間的範例。</span><span class="sxs-lookup"><span data-stu-id="aa35b-121">You will see examples of the **D2D1** namespace throughout this module.</span></span>

## <a name="next"></a><span data-ttu-id="aa35b-122">下一個</span><span class="sxs-lookup"><span data-stu-id="aa35b-122">Next</span></span>

[<span data-ttu-id="aa35b-123">呈現目標、裝置和資源</span><span class="sxs-lookup"><span data-stu-id="aa35b-123">Render Targets, Devices, and Resources</span></span>](render-targets--devices--and-resources.md)

## <a name="related-topics"></a><span data-ttu-id="aa35b-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa35b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa35b-125">Direct2D 圓形範例</span><span class="sxs-lookup"><span data-stu-id="aa35b-125">Direct2D Circle Sample</span></span>](direct2d-circle-sample.md)
</dt> </dl>

 

 