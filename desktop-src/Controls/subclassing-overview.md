---
title: 子類別化控制項
description: 如果控制項幾乎會執行您想要的所有專案，但您需要更多的功能，您可以將功能子類別化來變更或加入原始控制項。
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2e338deca61c4aac07fca431e77492f53f168540cfbbcf7596b8540ba5369f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168578"
---
# <a name="subclassing-controls"></a>子類別化控制項

如果控制項幾乎會執行您想要的所有專案，但您需要更多的功能，您可以將功能子類別化來變更或加入原始控制項。 子類別可以擁有現有類別的所有功能，以及您想要提供給它的任何其他功能。

本檔討論如何建立子類別，並包含下列主題。

-   [ComCtl32.dll 第6版之前的子類別化控制項](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [儲存使用者資料](#storing-user-data)
    -   [舊子類別化方法的缺點](#disadvantages-of-the-old-subclassing-approach)
-   [使用 ComCtl32.dll 第6版將控制項子類別化](#subclassing-controls-using-comctl32dll-version-6)
    -   [SetWindowSubclass](#setwindowsubclass)
    -   [GetWindowSubclass](#getwindowsubclass)
    -   [RemoveWindowSubclass](#removewindowsubclass)
    -   [DefSubclassProc](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a>ComCtl32.dll 第6版之前的子類別化控制項

您可以將控制項放在子類別中，並將使用者資料儲存在控制項內。 當您使用版本6之前的 ComCtl32.dll 版本時，請執行此動作。 使用舊版 ComCtl32.dll 建立子類別有一些缺點。

若要建立新的控制項，最好是從其中一個 Windows 的通用控制項開始，並加以擴充以符合特定需求。 若要擴充控制項，請建立控制項，並將其現有的視窗程式取代為新的視窗程式。 新程式會攔截控制項的訊息，並對其採取動作，或將它們傳遞至原始程式進行預設處理。 使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 或 [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) 函式來取代控制項的 WNDPROC。 下列程式碼範例顯示如何取代 WNDPROC。


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a>儲存使用者資料

您可能會想要將使用者資料儲存在個別的視窗中。 這項資料可供新的視窗程式用來判斷如何繪製控制項，或是要將特定訊息傳送至何處。 例如，您可以使用資料將 c + + 類別指標儲存至代表控制項的類別。 下列程式碼範例示範如何使用 [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) ，以視窗儲存資料。


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a>舊子類別化方法的缺點

下列清單指出使用先前所述方法將控制項子類別化的一些缺點。

-   視窗程式只能取代一次。
-   建立子類別之後，很難將它移除。
-   建立私用資料與視窗的關聯效率不佳。
-   若要呼叫子類別鏈中的下一個程式，您無法轉換舊的視窗程式並呼叫它，您必須使用 [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) 函數來呼叫它。

## <a name="subclassing-controls-using-comctl32dll-version-6"></a>使用 ComCtl32.dll 第6版將控制項子類別化

> [!Note]  
> ComCtl32.dll 第6版僅限 Unicode。 ComCtl32.dll 第6版所支援的通用控制項，不應使用 ANSI 視窗程式 (或 superclass) 進行子類別化。

 

ComCtl32.dll 第6版包含四個功能，可讓您更輕鬆地建立子類別，並消除先前所討論的缺點。 新的函式會封裝與多組參考資料相關的管理，因此開發人員可以專注于程式設計功能，而不是管理子類別。 子類別化函數包括：

-   [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a>SetWindowSubclass

這個函式是用來一開始將視窗子類別化。 每個子類別都是由 *pfnSubclass* 和其 *uIdSubclass* 的位址唯一識別。 這兩個都是 [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) 函式的參數。 數個子類別可以共用相同的子類別程式，且識別碼可以識別每個呼叫。 若要變更參考資料，您可以對 **SetWindowSubclass** 進行後續的呼叫。 重要的優點是每個子類別實例都有自己的參考資料。

子類別程式的宣告與一般視窗程式稍有不同，因為它有兩個額外的資料片段：子類別識別碼和參考資料。 下列函式宣告的最後兩個參數顯示此。


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



每次新的視窗程式收到訊息時，就會包含子類別識別碼和參考資料。

> [!Note]  
> 傳遞至程式的所有字串都是 Unicode 字串，即使 Unicode 未指定為預處理器定義。

 

下列範例顯示子類別化控制項之視窗程式的基本架構執行。


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



視窗程式可以附加至對話程式之 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 處理常式中的控制項，如下列範例所示。


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a>GetWindowSubclass

此函數會抓取子類別的相關資訊。 例如，您可以使用 [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) 來存取參考資料。

### <a name="removewindowsubclass"></a>RemoveWindowSubclass

此函數會移除子類別。 結合 [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)的 [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)可讓您以動態方式新增和移除子類別。

### <a name="defsubclassproc"></a>DefSubclassProc

[**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)函式會呼叫子類別鏈中的下一個處理常式。 函數也會抓取適當的識別碼和參考資料，並將資訊傳遞至下一個視窗程式。

 

 