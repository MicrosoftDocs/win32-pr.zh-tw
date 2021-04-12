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
# <a name="creating-a-window"></a>建立視窗

## <a name="window-classes"></a>視窗類別

*視窗類別* 定義了幾個視窗可能共通的一組行為。 例如，在一組按鈕中，當使用者按一下按鈕時，每個按鈕都有類似的行為。 當然，按鈕並不完全相同;每個按鈕都會顯示自己的文字字串，且具有自己的螢幕座標。 每個視窗唯一的資料稱為 *實例資料*。

每個視窗都必須與視窗類別產生關聯，即使您的程式只會建立該類別的一個實例也一樣。 請務必瞭解，視窗類別不是 c + + 意義中的「類別」。 相反地，它是作業系統內部使用的資料結構。 視窗類別會在執行時間向系統註冊。 若要註冊新的視窗類別，請從填入 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) 結構開始：

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

您必須設定下列結構成員：

- **lpfnWndProc** 是應用程式定義函式的指標，稱為 *視窗* 程式或 "window proc"。 視窗程式會定義視窗的大部分行為。 我們稍後將詳細檢查視窗程式。 現在，只要將它視為向前參考。
- **hInstance** 是應用程式實例的控制碼。 從 **wWinMain** 的 *hInstance* 參數取得此值。
- **lpszClassName** 是可識別視窗類別的字串。

類別名稱是目前進程的本機名稱，因此名稱只需要在進程內是唯一的。 不過，標準的 Windows 控制項也有類別。 如果您使用這些控制項中的任一個，則必須挑選與控制項類別名稱不衝突的類別名稱。 例如，按鈕控制項的視窗類別會命名為 "Button"。

[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構具有此處未顯示的其他成員。 您可以將它們設定為零（如本範例所示），或將其填入。 MSDN 檔會詳細說明此結構。

接下來，將 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) 結構的位址傳遞給 [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) 函數。 此函式會向作業系統註冊視窗類別。

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a>建立視窗

若要建立視窗的新實例，請呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數：

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

您可以閱讀 MSDN 上的詳細參數描述，但以下是快速摘要：

- 第一個參數可讓您為視窗指定一些選擇性的行為 (例如，透明的 windows) 。 針對預設行為，將此參數設定為零。
- `CLASS_NAME` 這是視窗類別的名稱。 這會定義您正在建立的視窗類型。
- 不同類型的視窗以不同的方式使用視窗文字。 如果視窗具有標題列，則文字會顯示在標題列中。
- 視窗樣式是一組旗標，用來定義視窗的一些外觀和操作。 常數 **WS \_ OVERLAPPEDWINDOW** 實際上是結合了位 **or** 的數個旗標。 這些旗標一起為視窗提供標題列、框線、系統功能表，以及 **最小化** 和 **最大化** 按鈕。 這組旗標是最常用於最上層應用程式視窗的樣式。
- 針對位置和大小，常數的 **CW \_ USEDEFAULT** 表示使用預設值。
- 下一個參數會設定新視窗的父視窗或擁有者視窗。 如果您要建立子視窗，請設定父系。 若為最上層視窗，請將此值設定為 **Null**。
- 在應用程式視窗中，下一個參數會定義視窗的功能表。 此範例不使用功能表，因此值為 **Null**。
- *hInstance* 是實例控制碼，如先前所述。  (參閱 [WinMain：應用程式進入點](winmain--the-application-entry-point.md)。 ) 
- 最後一個參數是 **void \*** 類型之任意資料的指標。 您可以使用此值，將資料結構傳遞至您的視窗程式。 在 [管理應用程式狀態](managing-application-state-.md)的區段中，我們將示範一個可能使用此參數的方式。

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 會傳回新視窗的控制碼，如果函式失敗，則傳回零。 若要顯示視窗，也就是讓視窗可見，請將視窗控制碼傳遞至 [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) 函式：

```C++
ShowWindow(hwnd, nCmdShow);
```

*Hwnd* 參數是 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)所傳回的視窗控制碼。 *NCmdShow* 參數可以用來將視窗最小化或最大化。 作業系統會透過 **wWinMain** 函數將此值傳遞給程式。

以下是建立視窗的完整程式碼。 請記住，仍然只是函式的 `WindowProc` 向前宣告。

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

恭喜，您已建立視窗！ 現在，視窗不包含任何內容，也不會與使用者互動。 在實際的 GUI 應用程式中，視窗會回應來自使用者和作業系統的事件。 下一節將說明視窗訊息如何提供這類互動。

### <a name="next"></a>下一個

[視窗訊息](window-messages.md)