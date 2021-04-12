---
title: 建立視窗
description: .
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126f040d72fec423ad5b6f3ecb31bc780a3192b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375340"
---
# <a name="creating-a-window"></a><span data-ttu-id="61ced-103">建立視窗</span><span class="sxs-lookup"><span data-stu-id="61ced-103">Creating a Window</span></span>

## <a name="window-classes"></a><span data-ttu-id="61ced-104">視窗類別</span><span class="sxs-lookup"><span data-stu-id="61ced-104">Window Classes</span></span>

<span data-ttu-id="61ced-105">*視窗類別* 定義了幾個視窗可能共通的一組行為。</span><span class="sxs-lookup"><span data-stu-id="61ced-105">A *window class* defines a set of behaviors that several windows might have in common.</span></span> <span data-ttu-id="61ced-106">例如，在一組按鈕中，當使用者按一下按鈕時，每個按鈕都有類似的行為。</span><span class="sxs-lookup"><span data-stu-id="61ced-106">For example, in a group of buttons, each button has a similar behavior when the user clicks the button.</span></span> <span data-ttu-id="61ced-107">當然，按鈕並不完全相同;每個按鈕都會顯示自己的文字字串，且具有自己的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="61ced-107">Of course, buttons are not completely identical; each button displays its own text string and has its own screen coordinates.</span></span> <span data-ttu-id="61ced-108">每個視窗唯一的資料稱為 *實例資料*。</span><span class="sxs-lookup"><span data-stu-id="61ced-108">Data that is unique for each window is called *instance data*.</span></span>

<span data-ttu-id="61ced-109">每個視窗都必須與視窗類別產生關聯，即使您的程式只會建立該類別的一個實例也一樣。</span><span class="sxs-lookup"><span data-stu-id="61ced-109">Every window must be associated with a window class, even if your program only ever creates one instance of that class.</span></span> <span data-ttu-id="61ced-110">請務必瞭解，視窗類別不是 c + + 意義中的「類別」。</span><span class="sxs-lookup"><span data-stu-id="61ced-110">It is important to understand that a window class is not a "class" in the C++ sense.</span></span> <span data-ttu-id="61ced-111">相反地，它是作業系統內部使用的資料結構。</span><span class="sxs-lookup"><span data-stu-id="61ced-111">Rather, it is a data structure used internally by the operating system.</span></span> <span data-ttu-id="61ced-112">視窗類別會在執行時間向系統註冊。</span><span class="sxs-lookup"><span data-stu-id="61ced-112">Window classes are registered with the system at run time.</span></span> <span data-ttu-id="61ced-113">若要註冊新的視窗類別，請從填入 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) 結構開始：</span><span class="sxs-lookup"><span data-stu-id="61ced-113">To register a new window class, start by filling in a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure:</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

<span data-ttu-id="61ced-114">您必須設定下列結構成員：</span><span class="sxs-lookup"><span data-stu-id="61ced-114">You must set the following structure members:</span></span>

- <span data-ttu-id="61ced-115">**lpfnWndProc** 是應用程式定義函式的指標，稱為 *視窗* 程式或 "window proc"。</span><span class="sxs-lookup"><span data-stu-id="61ced-115">**lpfnWndProc** is a pointer to an application-defined function called the *window procedure* or "window proc."</span></span> <span data-ttu-id="61ced-116">視窗程式會定義視窗的大部分行為。</span><span class="sxs-lookup"><span data-stu-id="61ced-116">The window procedure defines most of the behavior of the window.</span></span> <span data-ttu-id="61ced-117">我們稍後將詳細檢查視窗程式。</span><span class="sxs-lookup"><span data-stu-id="61ced-117">We'll examine the window procedure in detail later.</span></span> <span data-ttu-id="61ced-118">現在，只要將它視為向前參考。</span><span class="sxs-lookup"><span data-stu-id="61ced-118">For now, just treat this as a forward reference.</span></span>
- <span data-ttu-id="61ced-119">**hInstance** 是應用程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="61ced-119">**hInstance** is the handle to the application instance.</span></span> <span data-ttu-id="61ced-120">從 **wWinMain** 的 *hInstance* 參數取得此值。</span><span class="sxs-lookup"><span data-stu-id="61ced-120">Get this value from the *hInstance* parameter of **wWinMain**.</span></span>
- <span data-ttu-id="61ced-121">**lpszClassName** 是可識別視窗類別的字串。</span><span class="sxs-lookup"><span data-stu-id="61ced-121">**lpszClassName** is a string that identifies the window class.</span></span>

<span data-ttu-id="61ced-122">類別名稱是目前進程的本機名稱，因此名稱只需要在進程內是唯一的。</span><span class="sxs-lookup"><span data-stu-id="61ced-122">Class names are local to the current process, so the name only needs to be unique within the process.</span></span> <span data-ttu-id="61ced-123">不過，標準的 Windows 控制項也有類別。</span><span class="sxs-lookup"><span data-stu-id="61ced-123">However, the standard Windows controls also have classes.</span></span> <span data-ttu-id="61ced-124">如果您使用這些控制項中的任一個，則必須挑選與控制項類別名稱不衝突的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="61ced-124">If you use any of those controls, you must pick class names that do not conflict with the control class names.</span></span> <span data-ttu-id="61ced-125">例如，按鈕控制項的視窗類別會命名為 "Button"。</span><span class="sxs-lookup"><span data-stu-id="61ced-125">For example, the window class for the button control is named "Button".</span></span>

<span data-ttu-id="61ced-126">[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構具有此處未顯示的其他成員。</span><span class="sxs-lookup"><span data-stu-id="61ced-126">The [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure has other members not shown here.</span></span> <span data-ttu-id="61ced-127">您可以將它們設定為零（如本範例所示），或將其填入。</span><span class="sxs-lookup"><span data-stu-id="61ced-127">You can set them to zero, as shown in this example, or fill them in.</span></span> <span data-ttu-id="61ced-128">MSDN 檔會詳細說明此結構。</span><span class="sxs-lookup"><span data-stu-id="61ced-128">The MSDN documentation describes the structure in detail.</span></span>

<span data-ttu-id="61ced-129">接下來，將 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) 結構的位址傳遞給 [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) 函數。</span><span class="sxs-lookup"><span data-stu-id="61ced-129">Next, pass the address of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="61ced-130">此函式會向作業系統註冊視窗類別。</span><span class="sxs-lookup"><span data-stu-id="61ced-130">This function registers the window class with the operating system.</span></span>

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a><span data-ttu-id="61ced-131">建立視窗</span><span class="sxs-lookup"><span data-stu-id="61ced-131">Creating the Window</span></span>

<span data-ttu-id="61ced-132">若要建立視窗的新實例，請呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數：</span><span class="sxs-lookup"><span data-stu-id="61ced-132">To create a new instance of a window, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function:</span></span>

```C++
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
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}
```

<span data-ttu-id="61ced-133">您可以閱讀 MSDN 上的詳細參數描述，但以下是快速摘要：</span><span class="sxs-lookup"><span data-stu-id="61ced-133">You can read detailed parameter descriptions on MSDN, but here is a quick summary:</span></span>

- <span data-ttu-id="61ced-134">第一個參數可讓您為視窗指定一些選擇性的行為 (例如，透明的 windows) 。</span><span class="sxs-lookup"><span data-stu-id="61ced-134">The first parameter lets you specify some optional behaviors for the window (for example, transparent windows).</span></span> <span data-ttu-id="61ced-135">針對預設行為，將此參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="61ced-135">Set this parameter to zero for the default behaviors.</span></span>
- <span data-ttu-id="61ced-136">`CLASS_NAME` 這是視窗類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="61ced-136">`CLASS_NAME` is the name of the window class.</span></span> <span data-ttu-id="61ced-137">這會定義您正在建立的視窗類型。</span><span class="sxs-lookup"><span data-stu-id="61ced-137">This defines the type of window you are creating.</span></span>
- <span data-ttu-id="61ced-138">不同類型的視窗以不同的方式使用視窗文字。</span><span class="sxs-lookup"><span data-stu-id="61ced-138">The window text is used in different ways by different types of windows.</span></span> <span data-ttu-id="61ced-139">如果視窗具有標題列，則文字會顯示在標題列中。</span><span class="sxs-lookup"><span data-stu-id="61ced-139">If the window has a title bar, the text is displayed in the title bar.</span></span>
- <span data-ttu-id="61ced-140">視窗樣式是一組旗標，用來定義視窗的一些外觀和操作。</span><span class="sxs-lookup"><span data-stu-id="61ced-140">The window style is a set of flags that define some of the look and feel of a window.</span></span> <span data-ttu-id="61ced-141">常數 **WS \_ OVERLAPPEDWINDOW** 實際上是結合了位 **or** 的數個旗標。</span><span class="sxs-lookup"><span data-stu-id="61ced-141">The constant **WS\_OVERLAPPEDWINDOW** is actually several flags combined with a bitwise **OR**.</span></span> <span data-ttu-id="61ced-142">這些旗標一起為視窗提供標題列、框線、系統功能表，以及 **最小化** 和 **最大化** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="61ced-142">Together these flags give the window a title bar, a border, a system menu, and **Minimize** and **Maximize** buttons.</span></span> <span data-ttu-id="61ced-143">這組旗標是最常用於最上層應用程式視窗的樣式。</span><span class="sxs-lookup"><span data-stu-id="61ced-143">This set of flags is the most common style for a top-level application window.</span></span>
- <span data-ttu-id="61ced-144">針對位置和大小，常數的 **CW \_ USEDEFAULT** 表示使用預設值。</span><span class="sxs-lookup"><span data-stu-id="61ced-144">For position and size, the constant **CW\_USEDEFAULT** means to use default values.</span></span>
- <span data-ttu-id="61ced-145">下一個參數會設定新視窗的父視窗或擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="61ced-145">The next parameter sets a parent window or owner window for the new window.</span></span> <span data-ttu-id="61ced-146">如果您要建立子視窗，請設定父系。</span><span class="sxs-lookup"><span data-stu-id="61ced-146">Set the parent if you are creating a child window.</span></span> <span data-ttu-id="61ced-147">若為最上層視窗，請將此值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="61ced-147">For a top-level window, set this to **NULL**.</span></span>
- <span data-ttu-id="61ced-148">在應用程式視窗中，下一個參數會定義視窗的功能表。</span><span class="sxs-lookup"><span data-stu-id="61ced-148">For an application window, the next parameter defines the menu for the window.</span></span> <span data-ttu-id="61ced-149">此範例不使用功能表，因此值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="61ced-149">This example does not use a menu, so the value is **NULL**.</span></span>
- <span data-ttu-id="61ced-150">*hInstance* 是實例控制碼，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="61ced-150">*hInstance* is the instance handle, described previously.</span></span> <span data-ttu-id="61ced-151"> (參閱 [WinMain：應用程式進入點](winmain--the-application-entry-point.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="61ced-151">(See [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).)</span></span>
- <span data-ttu-id="61ced-152">最後一個參數是 **void \*** 類型之任意資料的指標。</span><span class="sxs-lookup"><span data-stu-id="61ced-152">The last parameter is a pointer to arbitrary data of type **void\***.</span></span> <span data-ttu-id="61ced-153">您可以使用此值，將資料結構傳遞至您的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="61ced-153">You can use this value to pass a data structure to your window procedure.</span></span> <span data-ttu-id="61ced-154">在 [管理應用程式狀態](managing-application-state-.md)的區段中，我們將示範一個可能使用此參數的方式。</span><span class="sxs-lookup"><span data-stu-id="61ced-154">We'll show one possible way to use this parameter in the section [Managing Application State](managing-application-state-.md).</span></span>

<span data-ttu-id="61ced-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 會傳回新視窗的控制碼，如果函式失敗，則傳回零。</span><span class="sxs-lookup"><span data-stu-id="61ced-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) returns a handle to the new window, or zero if the function fails.</span></span> <span data-ttu-id="61ced-156">若要顯示視窗，也就是讓視窗可見，請將視窗控制碼傳遞至 [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) 函式：</span><span class="sxs-lookup"><span data-stu-id="61ced-156">To show the window—that is, make the window visible —pass the window handle to the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function:</span></span>

```C++
ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="61ced-157">*Hwnd* 參數是 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)所傳回的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="61ced-157">The *hwnd* parameter is the window handle returned by [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="61ced-158">*NCmdShow* 參數可以用來將視窗最小化或最大化。</span><span class="sxs-lookup"><span data-stu-id="61ced-158">The *nCmdShow* parameter can be used to minimize or maximize a window.</span></span> <span data-ttu-id="61ced-159">作業系統會透過 **wWinMain** 函數將此值傳遞給程式。</span><span class="sxs-lookup"><span data-stu-id="61ced-159">The operating system passes this value to the program through the **wWinMain** function.</span></span>

<span data-ttu-id="61ced-160">以下是建立視窗的完整程式碼。</span><span class="sxs-lookup"><span data-stu-id="61ced-160">Here is the complete code to create the window.</span></span> <span data-ttu-id="61ced-161">請記住，仍然只是函式的 `WindowProc` 向前宣告。</span><span class="sxs-lookup"><span data-stu-id="61ced-161">Remember that `WindowProc` is still just a forward declaration of a function.</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;

RegisterClass(&wc);

// Create the window.

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
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}

ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="61ced-162">恭喜，您已建立視窗！</span><span class="sxs-lookup"><span data-stu-id="61ced-162">Congratulations, you've created a window!</span></span> <span data-ttu-id="61ced-163">現在，視窗不包含任何內容，也不會與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="61ced-163">Right now, the window does not contain any content or interact with the user.</span></span> <span data-ttu-id="61ced-164">在實際的 GUI 應用程式中，視窗會回應來自使用者和作業系統的事件。</span><span class="sxs-lookup"><span data-stu-id="61ced-164">In a real GUI application, the window would respond to events from the user and the operating system.</span></span> <span data-ttu-id="61ced-165">下一節將說明視窗訊息如何提供這類互動。</span><span class="sxs-lookup"><span data-stu-id="61ced-165">The next section describes how window messages provide this sort of interactivity.</span></span>

### <a name="next"></a><span data-ttu-id="61ced-166">下一個</span><span class="sxs-lookup"><span data-stu-id="61ced-166">Next</span></span>

[<span data-ttu-id="61ced-167">視窗訊息</span><span class="sxs-lookup"><span data-stu-id="61ced-167">Window Messages</span></span>](window-messages.md)