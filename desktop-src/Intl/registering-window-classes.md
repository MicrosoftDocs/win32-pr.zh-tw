---
description: 視窗程式支援視窗類別。 您的應用程式可以使用 RegisterClassA 或 RegisterClassW 來註冊視窗類別。 新的應用程式通常應該使用 RegisterClassW。
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: 註冊視窗類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c82e9daead566e5bcb5419fccc234014005f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115925"
---
# <a name="registering-window-classes"></a><span data-ttu-id="05d07-105">註冊視窗類別</span><span class="sxs-lookup"><span data-stu-id="05d07-105">Registering Window Classes</span></span>

<span data-ttu-id="05d07-106">視窗程式支援視窗類別。</span><span class="sxs-lookup"><span data-stu-id="05d07-106">A window class is supported by a window procedure.</span></span> <span data-ttu-id="05d07-107">您的應用程式可以使用 [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) 或 [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa)來註冊視窗類別。</span><span class="sxs-lookup"><span data-stu-id="05d07-107">Your application can register a window class by using either [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) or [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="05d07-108">新的應用程式通常應該使用 **RegisterClassW**。</span><span class="sxs-lookup"><span data-stu-id="05d07-108">New applications should typically use **RegisterClassW**.</span></span>

<span data-ttu-id="05d07-109">如果應用程式使用 [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa)註冊視窗類別，此函式會通知作業系統，所建立類別的視窗會預期具有文字或字元參數的訊息，以使用 [windows (ANSI) 字碼頁](code-pages.md) 字元集。</span><span class="sxs-lookup"><span data-stu-id="05d07-109">If the application registers the window class using [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), the function informs the operating system that the windows of the created class expect messages with text or character parameters to use a [Windows (ANSI) code page](code-pages.md) character set.</span></span> <span data-ttu-id="05d07-110">使用 [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) 進行註冊可讓應用程式要求作業系統將訊息的文字參數傳遞為 [Unicode](unicode.md)。</span><span class="sxs-lookup"><span data-stu-id="05d07-110">Registration using [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) allows the application to request the operating system to pass text parameters of messages as [Unicode](unicode.md).</span></span> <span data-ttu-id="05d07-111">[**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode)函式可讓應用程式查詢每個視窗的本質。</span><span class="sxs-lookup"><span data-stu-id="05d07-111">The [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) function enables an application to query the nature of each window.</span></span>

<span data-ttu-id="05d07-112">下列範例示範如何註冊 Windows 字碼頁視窗類別和 Unicode 視窗類別，以及如何撰寫這兩種案例的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="05d07-112">The following example shows how to register a Windows code page window class and a Unicode window class and how to write the window procedures for both cases.</span></span> <span data-ttu-id="05d07-113">基於此範例的目的，所有函式和結構都會以特定的 "A" (ANSI) 或 "W" (寬、Unicode) 資料類型來顯示。</span><span class="sxs-lookup"><span data-stu-id="05d07-113">For the purposes of this example, all functions and structures are shown with the specific "A" (ANSI) or "W" (wide, Unicode) data types.</span></span> <span data-ttu-id="05d07-114">使用 [泛型資料類型](using-generic-data-types.md)中所述的技術，您也可以撰寫此範例以使用泛型資料類型，讓它可以編譯為使用 Windows 字碼頁或 Unicode，取決於是否已定義 "unicode"。</span><span class="sxs-lookup"><span data-stu-id="05d07-114">Using the techniques explained in [Using Generic Data Types](using-generic-data-types.md), you can alternatively write this example to use generic data types, so that it can be compiled to use either Windows code pages or Unicode, depending on whether "UNICODE" is defined.</span></span>


```C++
// Register a Windows code page window class.

WNDCLASSA AnsiWndCls;

AnsiWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
AnsiWndCls.lpfnWndProc   = (WNDPROC)AnsiWndProc;
AnsiWndCls.cbClsExtra    = 0;
AnsiWndCls.cbWndExtra    = 0;
AnsiWndCls.hInstance     = hInstance;
AnsiWndCls.hIcon         = NULL;
AnsiWndCls.hCursor       = LoadCursor(NULL, (LPTSTR)IDC_IBEAM);
AnsiWndCls.hbrBackground = NULL;
AnsiWndCls.lpszMenuName  = NULL;
AnsiWndCls.lpszClassName = "TestAnsi";

RegisterClassA(&AnsiWndCls);

// Register a Unicode window class.

WNDCLASSW UnicodeWndCls;

UnicodeWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
UnicodeWndCls.lpfnWndProc   = (WNDPROC)UniWndProc;
UnicodeWndCls.cbClsExtra    = 0;
UnicodeWndCls.cbWndExtra    = 0;
UnicodeWndCls.hInstance     = hInstance;
UnicodeWndCls.hIcon         = NULL;
UnicodeWndCls.hCursor       = LoadCursor(NULL,(LPTSTR)IDC_IBEAM);
UnicodeWndCls.hbrBackground = NULL;
UnicodeWndCls.lpszMenuName  = NULL;
UnicodeWndCls.lpszClassName = L"TestUnicode";

RegisterClassW(&UnicodeWndCls);
```



<span data-ttu-id="05d07-115">下列範例顯示在 Windows 字碼頁視窗程式和 Unicode 視窗程式中處理 [**WM \_ CHAR**](../inputdev/wm-char.md) 訊息之間的差異。</span><span class="sxs-lookup"><span data-stu-id="05d07-115">The following example shows the difference between handling the [**WM\_CHAR**](../inputdev/wm-char.md) message in a Windows code page window procedure and a Unicode window procedure.</span></span>


```C++
// "ANSI" Window Procedure

LRESULT CALLBACK AnsiWndProc(HWND hWnd, UINT message,
                             WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpA("Q", (LPCSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

// Unicode Window Procedure

LRESULT CALLBACK UniWndProc(HWND hWnd, UINT message,
                            WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpW(L"Q", (LPCWSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



<span data-ttu-id="05d07-116">**AnsiWndProc** 所接收之訊息中的所有文字都是由 Windows 字碼頁字元所組成。</span><span class="sxs-lookup"><span data-stu-id="05d07-116">All text in messages received by **AnsiWndProc** is composed of Windows code page characters.</span></span> <span data-ttu-id="05d07-117">**UniWndProc** 所接收之訊息中的所有文字都是由 Unicode 字元所組成。</span><span class="sxs-lookup"><span data-stu-id="05d07-117">All text in messages received by **UniWndProc** is composed of Unicode characters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05d07-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="05d07-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05d07-119">使用 Unicode 和字元集</span><span class="sxs-lookup"><span data-stu-id="05d07-119">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
