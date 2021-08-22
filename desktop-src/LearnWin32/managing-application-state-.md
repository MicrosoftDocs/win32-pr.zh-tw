---
title: 管理應用程式狀態
description: 視窗程式只是針對每個訊息叫用的函式，因此它原本就是無狀態的。 因此，您需要一種方式來追蹤應用程式的狀態，使其從一個函數呼叫到下一個。
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0cde27195ba0dfc16668da11beac243821902995a9d01daa337f8962944343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068060"
---
# <a name="managing-application-state"></a>管理應用程式狀態

視窗程式只是針對每個訊息叫用的函式，因此它原本就是無狀態的。 因此，您需要一種方式來追蹤應用程式的狀態，使其從一個函數呼叫到下一個。

最簡單的方法就是將所有專案都放在全域變數中。 這適用于小型程式，而許多 SDK 範例都使用這種方法。 不過，在大型程式中，它會導致全域變數激增。 此外，您可能會有數個視窗，每個視窗都有自己的視窗程式。 追蹤哪個視窗應該會存取哪些變數變得令人困惑，而且容易出錯。

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)函式提供將任何資料結構傳遞至視窗的方式。 呼叫此函式時，會將下列兩個訊息傳送至您的視窗程式：

- [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)
- [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)

這些訊息會以列出的順序傳送。  (這些都不是在 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)期間傳送的兩則訊息，但我們可以忽略其他的訊息來進行這項討論。 ) 

在視窗變成可見之前，會先傳送 [**wm \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) 和 [**wm \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息。 這讓它們成為初始化 UI 的絕佳位置，例如，用來判斷視窗的初始版面配置。

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的最後一個參數是 **void \** _ 類型的指標。 您可以在此參數中傳遞任何您想要的指標值。 當視窗程式處理 [_ *WM \_ NCCREATE* *](/windows/desktop/winmsg/wm-nccreate)或 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)訊息時，它可以從訊息資料中將此值解壓縮。

讓我們來看看如何使用此參數將應用程式資料傳遞至您的視窗。 首先，定義可保存狀態資訊的類別或結構。

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

當您呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)時，請將指標傳遞至最終 **void \*** 參數中的這個結構。

```C++
StateInfo *pState = new (std::nothrow) StateInfo;

if (pState == NULL)
{
    return 0;
}

// Initialize the structure members (not shown).

HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    pState      // Additional application data
    );
```

當您收到 [**wm \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) 和 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息時，每個訊息的 *lParam* 參數都是 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) 結構的指標。 **CREATESTRUCT** 結構接著會包含您傳遞至 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的指標。

![顯示 createstruct 結構的版面配置圖表](images/appstate01.png)

以下是您將指標解壓縮至資料結構的方式。 首先，藉由轉換 *lParam* 參數來取得 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構。

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構的 **lpCreateParams** 成員是您在 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)中指定的原始 void 指標。 藉由轉換 **lpCreateParams** 來取得您自己的資料結構指標。

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

接下來，呼叫 [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) 函式，並傳入資料結構的指標。

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

最後一個函式呼叫的目的是要將 *StateInfo* 指標儲存在視窗的實例資料中。 當您這樣做之後，就可以藉由呼叫 [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra)，從視窗中取回指標：

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

每個視窗都有自己的實例資料，因此您可以建立多個視窗，並為每個視窗提供自己的資料結構實例。 如果您定義 windows 的類別，並建立該類別的一個以上的視窗（例如，如果您建立自訂控制項類別的話），這個方法特別有用。 在小型 helper 函式中包裝 [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) 呼叫是很方便的。

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

現在您可以撰寫視窗程式，如下所示。

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;
    if (uMsg == WM_CREATE)
    {
        CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
        pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
        SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
    }
    else
    {
        pState = GetAppState(hwnd);
    }

    switch (uMsg)
    {


    // Remainder of the window procedure not shown ...

    }
    return TRUE;
}
```

## <a name="an-object-oriented-approach"></a>Object-Oriented 的方法

我們可以進一步擴充這種方法。 我們已經定義了資料結構來保存視窗的狀態資訊。 使用成員函式來提供此資料結構是很合理的， (可在資料上操作) 方法。 這自然會導致設計，其中結構 (或類別) 負責視窗上的所有作業。 視窗程式就會成為類別的一部分。

換句話說，我們想要從這個位置開始：

```C++
// pseudocode

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;

    /* Get pState from the HWND. */

    switch (uMsg)
    {
        case WM_SIZE:
            HandleResize(pState, ...);
            break;

        case WM_PAINT:
            HandlePaint(pState, ...);
            break;

       // And so forth.
    }
}
```

為此值：

```C++
// pseudocode

LRESULT MyWindow::WindowProc(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_SIZE:
            this->HandleResize(...);
            break;

        case WM_PAINT:
            this->HandlePaint(...);
            break;
    }
}
```

唯一的問題是如何連結 `MyWindow::WindowProc` 方法。 [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa)函式預期視窗程式必須是函式指標。 您無法在此內容中將指標傳遞至 (的非靜態) 成員函式。 但是，您可以傳遞 *靜態* 成員函式的指標，然後委派給成員函式。 以下是顯示此方法的類別範本：

```C++
template <class DERIVED_TYPE> 
class BaseWindow
{
public:
    static LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
    {
        DERIVED_TYPE *pThis = NULL;

        if (uMsg == WM_NCCREATE)
        {
            CREATESTRUCT* pCreate = (CREATESTRUCT*)lParam;
            pThis = (DERIVED_TYPE*)pCreate->lpCreateParams;
            SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pThis);

            pThis->m_hwnd = hwnd;
        }
        else
        {
            pThis = (DERIVED_TYPE*)GetWindowLongPtr(hwnd, GWLP_USERDATA);
        }
        if (pThis)
        {
            return pThis->HandleMessage(uMsg, wParam, lParam);
        }
        else
        {
            return DefWindowProc(hwnd, uMsg, wParam, lParam);
        }
    }

    BaseWindow() : m_hwnd(NULL) { }

    BOOL Create(
        PCWSTR lpWindowName,
        DWORD dwStyle,
        DWORD dwExStyle = 0,
        int x = CW_USEDEFAULT,
        int y = CW_USEDEFAULT,
        int nWidth = CW_USEDEFAULT,
        int nHeight = CW_USEDEFAULT,
        HWND hWndParent = 0,
        HMENU hMenu = 0
        )
    {
        WNDCLASS wc = {0};

        wc.lpfnWndProc   = DERIVED_TYPE::WindowProc;
        wc.hInstance     = GetModuleHandle(NULL);
        wc.lpszClassName = ClassName();

        RegisterClass(&wc);

        m_hwnd = CreateWindowEx(
            dwExStyle, ClassName(), lpWindowName, dwStyle, x, y,
            nWidth, nHeight, hWndParent, hMenu, GetModuleHandle(NULL), this
            );

        return (m_hwnd ? TRUE : FALSE);
    }

    HWND Window() const { return m_hwnd; }

protected:

    virtual PCWSTR  ClassName() const = 0;
    virtual LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam) = 0;

    HWND m_hwnd;
};
```

`BaseWindow`類別是抽象基類，可從中衍生特定的視窗類別。 例如，以下是衍生自的簡單類別的宣告 `BaseWindow` ：

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

若要建立視窗，請呼叫 `BaseWindow::Create` ：

```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Learn to Program Windows", WS_OVERLAPPEDWINDOW))
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
```

純虛擬 `BaseWindow::HandleMessage` 方法是用來執行視窗程式。 例如，下列執行相當於 [模組 1](your-first-windows-program.md)開頭所顯示的視窗程式。

```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(m_hwnd, &ps);
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(m_hwnd, &ps);
        }
        return 0;

    default:
        return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
    }
    return TRUE;
}
```

請注意，視窗控制碼會儲存在成員變數 (*m \_ hwnd*) ，因此我們不需要將它當作參數傳遞至 `HandleMessage` 。

許多現有的 Windows 程式設計架構（例如 Microsoft Foundation class (MFC) 和 Active Template Library (ATL) ）都會使用基本上類似此處所示的方法。 當然，MFC 這類完全一般化的架構比這個相當簡單的範例更為複雜。

## <a name="next"></a>下一個

[模組2：在您的 Windows 程式中使用 COM](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a>相關主題

[BaseWindow 範例](basewindow-sample.md)