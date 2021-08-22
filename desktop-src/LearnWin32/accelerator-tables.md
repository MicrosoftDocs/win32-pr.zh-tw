---
title: 快速鍵對應表
description: 快速鍵對應表
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504749b6fad794f5f587e035f0dbc81662aa8b5faaf9b9eb13de365dd9a8d312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146441"
---
# <a name="accelerator-tables"></a>快速鍵對應表

應用程式通常會定義鍵盤快速鍵，例如 [開啟檔案] 命令的 CTRL + O。 您可以藉由處理個別的 [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息來執行鍵盤快速鍵，但快速鍵對應表提供了更好的解決方案：

-   需要較少的編碼。
-   將您所有的快捷方式合併成一個資料檔案。
-   支援其他語言的當地語系化。
-   啟用快速鍵和功能表命令以使用相同的應用程式邏輯。

*快速鍵對應表* 是將鍵盤組合（例如 CTRL + O）對應到應用程式命令的資料資源。 在瞭解如何使用快速鍵對應表之前，我們需要資源的快速簡介。 *資源* 是在應用程式二進位 (EXE 或 DLL) 內建的資料 blob。 資源會儲存應用程式所需的資料，例如功能表、資料指標、圖示、影像、文字字串或任何自訂應用程式資料。 應用程式會在執行時間從二進位檔載入資源資料。 若要將資源包含在二進位檔中，請執行下列動作：

1.   ( .rc) 檔案建立資源定義。 此檔案會定義資源類型及其識別碼。 資源定義檔可能包含其他檔案的參考。 例如，在 .rc 檔中宣告圖示資源，但圖示影像會儲存在不同的檔案中。
2.  使用 Microsoft Windows 資源編譯器 (RC) 將資源定義檔編譯成已編譯的資源 ( .res) 檔。 RC 編譯器隨附 Visual Studio 以及 Windows SDK。
3.  將已編譯的資源檔連結至二進位檔案。

這些步驟大致上等同于程式碼檔案的編譯/連結程式。 Visual Studio 提供一組資源編輯器，可讓您輕鬆地建立及修改資源。  (這些工具不適用於 Visual Studio 的 Express 版本。 ) 但 .rc 檔只是文字檔，而語法記載于 MSDN 上，因此可以使用任何文字編輯器建立 .rc 檔。 如需詳細資訊，請參閱 [關於資源檔](/windows/desktop/menurc/about-resource-files)。

## <a name="defining-an-accelerator-table"></a>定義快速鍵對應表

快速鍵對應表是鍵盤快速鍵的表格。 每個快捷方式的定義方式如下：

-   數值識別碼。 這個數位會識別要由快捷方式叫用的應用程式命令。
-   快速鍵的 ASCII 字元或虛擬按鍵碼。
-   選擇性輔助按鍵： ALT、SHIFT 或 CTRL。

快速鍵對應表本身具有數值識別碼，可識別應用程式資源清單中的資料表。 讓我們建立簡單繪圖程式的快速鍵對應表。 此程式將會有兩種模式：繪圖模式和選取模式。 在繪製模式中，使用者可以繪製圖形。 在選取模式中，使用者可以選取 [圖形]。 在這個程式中，我們想要定義下列鍵盤快速鍵。



| 快速鍵 | 命令                   |
|----------|---------------------------|
| CTRL+M   | 切換模式。     |
| F1       | 切換至繪圖模式。      |
| F2       | 切換至選取模式。 |



 

首先，定義資料表和應用程式命令的數值識別碼。 這些值是任意的。 您可以在標頭檔中定義識別碼以指派其符號常數。 例如：


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



在此範例中，值會 `IDR_ACCEL1` 識別快速鍵對應表，接下來的三個常數則會定義應用程式命令。 依照慣例，定義資源常數的標頭檔通常名為 resource .h。 下一個清單顯示資源定義檔。


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



快速鍵會定義在大括弧內。 每個快捷方式都包含下列專案。

-   叫用快捷方式的虛擬金鑰程式碼或 ASCII 字元。
-   應用程式命令。 請注意，此範例中會使用符號常數。 資源定義檔包含資源 .h，其中定義了這些常數。
-   關鍵字 **VIRTKEY** 表示第一個專案是虛擬金鑰程式碼。 另一個選項是使用 ASCII 字元。
-   選擇性修飾詞： ALT、CONTROL 或 SHIFT。

如果您將 ASCII 字元用於快速鍵，則小寫字元將會是與大寫字元不同的快捷方式。  (例如，輸入 ' a ' 可能會叫用不同于輸入 ' A ' 的命令。 ) 可能會讓使用者混淆，因此通常最好是使用虛擬機器碼（而非 ASCII 字元）的快捷方式。

## <a name="loading-the-accelerator-table"></a>載入快速鍵對應表

必須先載入快速鍵對應表的資源，程式才能使用它。 若要載入快速鍵對應表，請呼叫 [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) 函數。


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



請在輸入訊息迴圈之前呼叫這個函數。 第一個參數是模組的控制碼。  (此參數會傳遞至您的 [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) 函數。 如需詳細資訊，請參閱 [WinMain：應用程式進入點](winmain--the-application-entry-point.md)。 ) 第二個參數是資源識別碼。 函數會傳回資源的控制碼。 回想一下，控制碼是一種不透明的類型，參考系統所管理的物件。 如果函式失敗，則會傳回 **Null**。

您可以藉由呼叫 [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable)來釋放快速鍵對應表。 不過，系統會在程式結束時自動釋出資料表，因此，如果您要以另一個資料表取代某個資料表，則只需要呼叫此函數。 在 [建立使用者可編輯加速器](/windows/desktop/menurc/using-keyboard-accelerators)的主題中，有一個有趣的範例。

## <a name="translating-key-strokes-into-commands"></a>將按鍵筆劃轉譯成命令

快速鍵轉換表的運作方式是將按鍵筆劃轉譯成 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。 **WM \_ 命令** 的 *wParam* 參數包含命令的數值識別碼。 例如，使用先前顯示的表格，按鍵筆觸 CTRL + M 會轉譯為具有值的 **WM \_ 命令** 訊息 `ID_TOGGLE_MODE` 。 若要這樣做，請將您的訊息迴圈變更為下列內容：


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



這段程式碼會將呼叫新增至訊息迴圈內的 [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) 函式。 **TranslateAccelerator** 函式會檢查每個視窗訊息，以尋找重要的訊息。 如果使用者按下快速鍵對應表中所列的其中一個按鍵組合， **TranslateAccelerator** 會將 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息傳送至視窗。 函數會直接叫用視窗程式來傳送 **WM \_ 命令** 。 當 **TranslateAccelerator** 成功轉譯按鍵筆劃時，此函式會傳回非零的值，這表示您應該略過訊息的正常處理。 否則， **TranslateAccelerator** 會傳回零。 在這種情況下，請將視窗訊息傳遞給 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 和 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)，如往常一般。

繪圖程式可能處理 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的方式如下：


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



這段程式碼假設 `SetMode` 是應用程式所定義的函式，可在這兩種模式之間切換。 您要如何處理每個命令的詳細資料，顯然取決於您的程式。

## <a name="next"></a>下一個

[設定游標影像](setting-the-cursor-image.md)

 

 
