---
description: 視窗程式支援視窗類別。 您的應用程式可以使用 RegisterClassA 或 RegisterClassW 來註冊視窗類別。 新的應用程式通常應該使用 RegisterClassW。
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: 註冊視窗類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f508ebdbfa35f2551d723b3ef9a1ffd807917dfe71e503f9d77b2e8fdb136f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040448"
---
# <a name="registering-window-classes"></a>註冊視窗類別

視窗程式支援視窗類別。 您的應用程式可以使用 [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) 或 [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa)來註冊視窗類別。 新的應用程式通常應該使用 **RegisterClassW**。

如果應用程式使用 [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa)註冊視窗類別，此函式會通知作業系統，所建立類別的視窗會預期具有文字或字元參數的訊息使用 [Windows (ANSI) 字碼頁](code-pages.md)字元集。 使用 [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) 進行註冊可讓應用程式要求作業系統將訊息的文字參數傳遞為 [Unicode](unicode.md)。 [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode)函式可讓應用程式查詢每個視窗的本質。

下列範例示範如何註冊 Windows 字碼頁視窗類別和 Unicode 視窗類別，以及如何撰寫這兩種案例的視窗程式。 基於此範例的目的，所有函式和結構都會以特定的 "A" (ANSI) 或 "W" (寬、Unicode) 資料類型來顯示。 使用[泛型資料類型](using-generic-data-types.md)所說明的技巧，您也可以撰寫此範例來使用泛型資料類型，以便編譯成使用 Windows 字碼頁或 Unicode，取決於是否已定義 "unicode"。


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



下列範例顯示在 Windows 字碼頁視窗程式和 Unicode 視窗程式中處理 [**WM \_ 字元**](../inputdev/wm-char.md)訊息之間的差異。


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



**AnsiWndProc** 所接收之訊息中的所有文字都是由 Windows 字碼頁字元所組成。 **UniWndProc** 所接收之訊息中的所有文字都是由 Unicode 字元所組成。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Unicode 和字元集](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
