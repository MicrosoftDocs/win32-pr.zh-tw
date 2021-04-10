---
title: 管理應用程式狀態
description: 視窗程式只是針對每個訊息叫用的函式，因此它原本就是無狀態的。 因此，您需要一種方式來追蹤應用程式的狀態，使其從一個函數呼叫到下一個。
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e275833c30c612b5b40ab29d089d07ed7794b429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023451"
---
# <a name="managing-application-state"></a><span data-ttu-id="425ef-104">管理應用程式狀態</span><span class="sxs-lookup"><span data-stu-id="425ef-104">Managing Application State</span></span>

<span data-ttu-id="425ef-105">視窗程式只是針對每個訊息叫用的函式，因此它原本就是無狀態的。</span><span class="sxs-lookup"><span data-stu-id="425ef-105">A window procedure is just a function that gets invoked for every message, so it is inherently stateless.</span></span> <span data-ttu-id="425ef-106">因此，您需要一種方式來追蹤應用程式的狀態，使其從一個函數呼叫到下一個。</span><span class="sxs-lookup"><span data-stu-id="425ef-106">Therefore, you need a way to track the state of your application from one function call to the next.</span></span>

<span data-ttu-id="425ef-107">最簡單的方法就是將所有專案都放在全域變數中。</span><span class="sxs-lookup"><span data-stu-id="425ef-107">The simplest approach is simply to put everything in global variables.</span></span> <span data-ttu-id="425ef-108">這適用于小型程式，而許多 SDK 範例都使用這種方法。</span><span class="sxs-lookup"><span data-stu-id="425ef-108">This works well enough for small programs, and many of the SDK samples use this approach.</span></span> <span data-ttu-id="425ef-109">不過，在大型程式中，它會導致全域變數激增。</span><span class="sxs-lookup"><span data-stu-id="425ef-109">In a large program, however, it leads to a proliferation of global variables.</span></span> <span data-ttu-id="425ef-110">此外，您可能會有數個視窗，每個視窗都有自己的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="425ef-110">Also, you might have several windows, each with its own window procedure.</span></span> <span data-ttu-id="425ef-111">追蹤哪個視窗應該會存取哪些變數變得令人困惑，而且容易出錯。</span><span class="sxs-lookup"><span data-stu-id="425ef-111">Keeping track of which window should access which variables becomes confusing and error-prone.</span></span>

<span data-ttu-id="425ef-112">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)函式提供將任何資料結構傳遞至視窗的方式。</span><span class="sxs-lookup"><span data-stu-id="425ef-112">The [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function provides a way to pass any data structure to a window.</span></span> <span data-ttu-id="425ef-113">呼叫此函式時，會將下列兩個訊息傳送至您的視窗程式：</span><span class="sxs-lookup"><span data-stu-id="425ef-113">When this function is called, it sends the following two messages to your window procedure:</span></span>

- [<span data-ttu-id="425ef-114">**WM \_ NCCREATE**</span><span class="sxs-lookup"><span data-stu-id="425ef-114">**WM\_NCCREATE**</span></span>](/windows/desktop/winmsg/wm-nccreate)
- [<span data-ttu-id="425ef-115">**WM \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="425ef-115">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)

<span data-ttu-id="425ef-116">這些訊息會以列出的順序傳送。</span><span class="sxs-lookup"><span data-stu-id="425ef-116">These messages are sent in the order listed.</span></span> <span data-ttu-id="425ef-117"> (這些都不是在 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)期間傳送的兩則訊息，但我們可以忽略其他的訊息來進行這項討論。 ) </span><span class="sxs-lookup"><span data-stu-id="425ef-117">(These are not the only two messages sent during [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), but we can ignore the others for this discussion.)</span></span>

<span data-ttu-id="425ef-118">在視窗變成可見之前，會先傳送 [**wm \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) 和 [**wm \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息。</span><span class="sxs-lookup"><span data-stu-id="425ef-118">The [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message are sent before the window becomes visible.</span></span> <span data-ttu-id="425ef-119">這讓它們成為初始化 UI 的絕佳位置，例如，用來判斷視窗的初始版面配置。</span><span class="sxs-lookup"><span data-stu-id="425ef-119">That makes them a good place to initialize your UI—for example, to determine the initial layout of the window.</span></span>

<span data-ttu-id="425ef-120">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的最後一個參數是 **void \*** 類型的指標。</span><span class="sxs-lookup"><span data-stu-id="425ef-120">The last parameter of [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) is a pointer of type **void\***.</span></span> <span data-ttu-id="425ef-121">您可以在此參數中傳遞任何您想要的指標值。</span><span class="sxs-lookup"><span data-stu-id="425ef-121">You can pass any pointer value that you want in this parameter.</span></span> <span data-ttu-id="425ef-122">當視窗程式處理 [**wm \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) 或 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息時，它可以從訊息資料中將此值解壓縮。</span><span class="sxs-lookup"><span data-stu-id="425ef-122">When the window procedure handles the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) or [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, it can extract this value from the message data.</span></span>

<span data-ttu-id="425ef-123">讓我們來看看如何使用此參數將應用程式資料傳遞至您的視窗。</span><span class="sxs-lookup"><span data-stu-id="425ef-123">Let's see how you would use this parameter to pass application data to your window.</span></span> <span data-ttu-id="425ef-124">首先，定義可保存狀態資訊的類別或結構。</span><span class="sxs-lookup"><span data-stu-id="425ef-124">First, define a class or structure that holds state information.</span></span>

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

<span data-ttu-id="425ef-125">當您呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)時，請將指標傳遞至最終 **void \*** 參數中的這個結構。</span><span class="sxs-lookup"><span data-stu-id="425ef-125">When you call [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), pass a pointer to this structure in the final **void\*** parameter.</span></span>

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

<span data-ttu-id="425ef-126">當您收到 [**wm \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) 和 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息時，每個訊息的 *lParam* 參數都是 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="425ef-126">When you receive the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) messages, the *lParam* parameter of each message is a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="425ef-127">**CREATESTRUCT** 結構接著會包含您傳遞至 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的指標。</span><span class="sxs-lookup"><span data-stu-id="425ef-127">The **CREATESTRUCT** structure, in turn, contains the pointer that you passed into [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>

![顯示 createstruct 結構的版面配置圖表](images/appstate01.png)

<span data-ttu-id="425ef-129">以下是您將指標解壓縮至資料結構的方式。</span><span class="sxs-lookup"><span data-stu-id="425ef-129">Here is how you extract the pointer to your data structure.</span></span> <span data-ttu-id="425ef-130">首先，藉由轉換 *lParam* 參數來取得 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構。</span><span class="sxs-lookup"><span data-stu-id="425ef-130">First, get the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure by casting the *lParam* parameter.</span></span>

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

<span data-ttu-id="425ef-131">[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構的 **lpCreateParams** 成員是您在 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)中指定的原始 void 指標。</span><span class="sxs-lookup"><span data-stu-id="425ef-131">The **lpCreateParams** member of the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure is the original void pointer that you specified in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="425ef-132">藉由轉換 **lpCreateParams** 來取得您自己的資料結構指標。</span><span class="sxs-lookup"><span data-stu-id="425ef-132">Get a pointer to your own data structure by casting **lpCreateParams**.</span></span>

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

<span data-ttu-id="425ef-133">接下來，呼叫 [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) 函式，並傳入資料結構的指標。</span><span class="sxs-lookup"><span data-stu-id="425ef-133">Next, call the [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function and pass in the pointer to your data structure.</span></span>

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

<span data-ttu-id="425ef-134">最後一個函式呼叫的目的是要將 *StateInfo* 指標儲存在視窗的實例資料中。</span><span class="sxs-lookup"><span data-stu-id="425ef-134">The purpose of this last function call is to store the *StateInfo* pointer in the instance data for the window.</span></span> <span data-ttu-id="425ef-135">當您這樣做之後，就可以藉由呼叫 [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra)，從視窗中取回指標：</span><span class="sxs-lookup"><span data-stu-id="425ef-135">Once you do this, you can always get the pointer back from the window by calling [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span></span>

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

<span data-ttu-id="425ef-136">每個視窗都有自己的實例資料，因此您可以建立多個視窗，並為每個視窗提供自己的資料結構實例。</span><span class="sxs-lookup"><span data-stu-id="425ef-136">Each window has its own instance data, so you can create multiple windows and give each window its own instance of the data structure.</span></span> <span data-ttu-id="425ef-137">如果您定義 windows 的類別，並建立該類別的一個以上的視窗（例如，如果您建立自訂控制項類別的話），這個方法特別有用。</span><span class="sxs-lookup"><span data-stu-id="425ef-137">This approach is especially useful if you define a class of windows and create more than one window of that class—for example, if you create a custom control class.</span></span> <span data-ttu-id="425ef-138">在小型 helper 函式中包裝 [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) 呼叫是很方便的。</span><span class="sxs-lookup"><span data-stu-id="425ef-138">It is convenient to wrap the [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) call in a small helper function.</span></span>

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

<span data-ttu-id="425ef-139">現在您可以撰寫視窗程式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="425ef-139">Now you can write your window procedure as follows.</span></span>

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

## <a name="an-object-oriented-approach"></a><span data-ttu-id="425ef-140">Object-Oriented 的方法</span><span class="sxs-lookup"><span data-stu-id="425ef-140">An Object-Oriented Approach</span></span>

<span data-ttu-id="425ef-141">我們可以進一步擴充這種方法。</span><span class="sxs-lookup"><span data-stu-id="425ef-141">We can extend this approach further.</span></span> <span data-ttu-id="425ef-142">我們已經定義了資料結構來保存視窗的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="425ef-142">We have already defined a data structure to hold state information about the window.</span></span> <span data-ttu-id="425ef-143">使用成員函式來提供此資料結構是很合理的， (可在資料上操作) 方法。</span><span class="sxs-lookup"><span data-stu-id="425ef-143">It makes sense to provide this data structure with member functions (methods) that operate on the data.</span></span> <span data-ttu-id="425ef-144">這自然會導致設計，其中結構 (或類別) 負責視窗上的所有作業。</span><span class="sxs-lookup"><span data-stu-id="425ef-144">This naturally leads to a design where the structure (or class) is responsible for all of the operations on the window.</span></span> <span data-ttu-id="425ef-145">視窗程式就會成為類別的一部分。</span><span class="sxs-lookup"><span data-stu-id="425ef-145">The window procedure would then become part of the class.</span></span>

<span data-ttu-id="425ef-146">換句話說，我們想要從這個位置開始：</span><span class="sxs-lookup"><span data-stu-id="425ef-146">In other words, we would like to go from this:</span></span>

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

<span data-ttu-id="425ef-147">為此值：</span><span class="sxs-lookup"><span data-stu-id="425ef-147">To this:</span></span>

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

<span data-ttu-id="425ef-148">唯一的問題是如何連結 `MyWindow::WindowProc` 方法。</span><span class="sxs-lookup"><span data-stu-id="425ef-148">The only problem is how to hook up the `MyWindow::WindowProc` method.</span></span> <span data-ttu-id="425ef-149">[**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa)函式預期視窗程式必須是函式指標。</span><span class="sxs-lookup"><span data-stu-id="425ef-149">The [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function expects the window procedure to be a function pointer.</span></span> <span data-ttu-id="425ef-150">您無法在此內容中將指標傳遞至 (的非靜態) 成員函式。</span><span class="sxs-lookup"><span data-stu-id="425ef-150">You can't pass a pointer to a (non-static) member function in this context.</span></span> <span data-ttu-id="425ef-151">但是，您可以傳遞 *靜態* 成員函式的指標，然後委派給成員函式。</span><span class="sxs-lookup"><span data-stu-id="425ef-151">However, you can pass a pointer to a *static* member function and then delegate to the member function.</span></span> <span data-ttu-id="425ef-152">以下是顯示此方法的類別範本：</span><span class="sxs-lookup"><span data-stu-id="425ef-152">Here is a class template that shows this approach:</span></span>

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

<span data-ttu-id="425ef-153">`BaseWindow`類別是抽象基類，可從中衍生特定的視窗類別。</span><span class="sxs-lookup"><span data-stu-id="425ef-153">The `BaseWindow` class is an abstract base class, from which specific window classes are derived.</span></span> <span data-ttu-id="425ef-154">例如，以下是衍生自的簡單類別的宣告 `BaseWindow` ：</span><span class="sxs-lookup"><span data-stu-id="425ef-154">For example, here is the declaration of a simple class derived from `BaseWindow`:</span></span>

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

<span data-ttu-id="425ef-155">若要建立視窗，請呼叫 `BaseWindow::Create` ：</span><span class="sxs-lookup"><span data-stu-id="425ef-155">To create the window, call `BaseWindow::Create`:</span></span>

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

<span data-ttu-id="425ef-156">純虛擬 `BaseWindow::HandleMessage` 方法是用來執行視窗程式。</span><span class="sxs-lookup"><span data-stu-id="425ef-156">The pure-virtual `BaseWindow::HandleMessage` method is used to implement the window procedure.</span></span> <span data-ttu-id="425ef-157">例如，下列執行相當於 [模組 1](your-first-windows-program.md)開頭所顯示的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="425ef-157">For example, the following implementation is equivalent to the window procedure shown at the start of [Module 1](your-first-windows-program.md).</span></span>

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

<span data-ttu-id="425ef-158">請注意，視窗控制碼會儲存在成員變數 (*m \_ hwnd*) ，因此我們不需要將它當作參數傳遞至 `HandleMessage` 。</span><span class="sxs-lookup"><span data-stu-id="425ef-158">Notice that the window handle is stored in a member variable (*m\_hwnd*), so we do not need to pass it as a parameter to `HandleMessage`.</span></span>

<span data-ttu-id="425ef-159">許多現有的 Windows 程式設計架構（例如，Microsoft Foundation class (MFC) 和 Active Template Library (ATL) ）使用基本上類似此處所示的方法。</span><span class="sxs-lookup"><span data-stu-id="425ef-159">Many of the existing Windows programming frameworks, such as Microsoft Foundation Classes (MFC) and Active Template Library (ATL), use approaches that are basically similar to the one shown here.</span></span> <span data-ttu-id="425ef-160">當然，MFC 這類完全一般化的架構比這個相當簡單的範例更為複雜。</span><span class="sxs-lookup"><span data-stu-id="425ef-160">Of course, a fully generalized framework such as MFC is more complex than this relatively simplistic example.</span></span>

## <a name="next"></a><span data-ttu-id="425ef-161">下一個</span><span class="sxs-lookup"><span data-stu-id="425ef-161">Next</span></span>

[<span data-ttu-id="425ef-162">模組2：在您的 Windows 程式中使用 COM</span><span class="sxs-lookup"><span data-stu-id="425ef-162">Module 2: Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a><span data-ttu-id="425ef-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="425ef-163">Related topics</span></span>

[<span data-ttu-id="425ef-164">BaseWindow 範例</span><span class="sxs-lookup"><span data-stu-id="425ef-164">BaseWindow Sample</span></span>](basewindow-sample.md)