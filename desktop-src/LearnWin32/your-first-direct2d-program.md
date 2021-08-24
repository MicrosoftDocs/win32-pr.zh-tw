---
title: 您的第一個 Direct2D 計畫
description: 讓我們來建立我們的第一個 Direct2D 計畫。 此程式不會執行任何複雜的工作 \ 8212;它只會繪製一個會填滿視窗工作區的圓形。 但這個程式引進許多重要的 Direct2D 概念。
ms.assetid: 940cc5e4-2952-4714-bf32-c611a965f819
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb7b9b4a81b9e3767f9d53d0c5872b170772c1cb60b4a74c599401de342ee05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754388"
---
# <a name="your-first-direct2d-program"></a>您的第一個 Direct2D 計畫

讓我們來建立我們的第一個 Direct2D 計畫。 程式並不會執行任何複雜的工作，只是繪製一個會填滿視窗工作區的圓形。 但這個程式引進許多重要的 Direct2D 概念。

![圓形程式的螢幕擷取畫面。](images/graphics08.png)

以下是圓形程式的程式代碼清單。 此程式會重複使用 `BaseWindow` [管理應用程式狀態](managing-application-state-.md)主題中定義的類別。 稍後的主題將詳細檢查程式碼。


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





您可以從[Direct2D Circle 範例](direct2d-circle-sample.md)下載完整的 Visual Studio 專案。

## <a name="the-d2d1-namespace"></a>D2D1 命名空間

**D2D1** 命名空間包含 helper 函式和類別。 這些都不是 Direct2D API 的一部分，您可以在不使用的情況下編寫 Direct2D 的程式碼，但它們有助於簡化您的程式碼。 **D2D1** 命名空間包含：

-   用來建立色彩值的 [**ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) 類別。
-   用來建立轉換矩陣的 [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) 。
-   用來初始化 Direct2D 結構的一組函數。

您將在此課程模組中看到 **D2D1** 命名空間的範例。

## <a name="next"></a>下一個

[呈現目標、裝置和資源](render-targets--devices--and-resources.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 圓形範例](direct2d-circle-sample.md)
</dt> </dl>

 

 