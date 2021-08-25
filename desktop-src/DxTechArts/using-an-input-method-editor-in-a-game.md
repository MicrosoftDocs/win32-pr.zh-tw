---
title: 在遊戲中使用輸入法編輯器
description: 本文說明如何在全螢幕 Microsoft DirectX 應用程式中，執行基本的 IME 編輯控制項。
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8cb5869579da97aeea465b572082a23a963e9db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471964"
---
# <a name="using-an-input-method-editor-in-a-game"></a>在遊戲中使用輸入法編輯器

> [!Note]  
> 本文詳細說明如何使用 Windows XP 輸入法編輯器 (IME) 。 針對 Windows Vista 的 IME 進行的變更，在本文中未完全詳述。 如需 Windows vista 之 ime 變更的詳細資訊，請參閱 Windows Vista 中的[輸入法編輯器 (ime) ](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) -Microsoft 全球開發和運算入口網站上[的國際化 Ever-Expanding 觀點](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx)。

 

輸入法編輯器 (IME) 是一種程式，可讓您使用標準鍵盤（例如中文、日文、韓文及其他語言的複雜字元）輕鬆地輸入文字。 例如，在使用者輸入 Ime 的情況下，使用者可以在文字處理器中輸入複雜字元，或大量多人遊戲線上遊戲的玩家可以用複雜的字元與朋友聊天。

本文說明如何在全螢幕 Microsoft DirectX 應用程式中，執行基本的 IME 編輯控制項。 利用 DXUT 的應用程式會自動取得輸入法功能。 針對未使用架構的應用程式，本文將說明如何在編輯控制項中新增 IME 支援。

內容: 

-   [預設 IME 行為](#default-ime-behavior)
-   [搭配使用 Ime 與 DXUT](#using-imes-with-dxut)
-   [覆寫預設的 IME 行為](#overriding-the-default-ime-behavior)
-   [函數](#functions)
-   [訊息](#ime-messages)
-   [範例](#examples)
    -   [CHT IME 4.2、4.3 和4.4 版](#cht-ime-version-42-43-and-44)
    -   [CHT IME 5.0 版](#cht-ime-version-50)
    -   [CHT IME 5.1、5.2 和 CHS IME 版本5。3](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [CHS IME 4.1 版](#chs-ime-version-41)
    -   [CHS IME 4.2 版](#chs-ime-version-42)
-   [輸入法訊息](#ime-messages)
    -   [WM \_ INPUTLANGCHANGE](#wm_inputlangchange)
    -   [WM \_ IME \_ STARTCOMPOSITION](/windows)
    -   [WM \_ IME \_ 組合](/windows)
    -   [WM \_ IME \_ ENDCOMPOSITION](/windows)
    -   [WM \_ 輸入法 \_ 通知](/windows)
-   [轉譯](#rendering)
    -   [輸入地區設定指標](#input-locale-indicator)
    -   [撰寫視窗](#composition-window)
    -   [讀取和候選 Windows](#reading-and-candidate-windows)
-   [限制](#limitations)
-   [登錄資訊](#registry-information)
-   [附錄 A：每個作業系統的 CHT 版本](#appendix-a-cht-versions-per-operating-system)
-   [詳細資訊](#further-information)
-   [GetReadingString](#getreadingstring)
-   [ShowReadingWindow](#showreadingwindow)

## <a name="default-ime-behavior"></a>預設 IME 行為

Ime 會將鍵盤輸入對應至所選語言特定的語音元件或其他語言元素。 在一般案例中，使用者會輸入代表複雜字元發音的按鍵。 如果 IME 將發音辨識為有效，則會向使用者顯示一份單字或片語候選人清單，讓使用者可以從中選取最後的選項。 選擇的單字接著會透過一系列 Microsoft Windows [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)訊息傳送至應用程式。 因為 IME 會在應用程式下方的某個層級上運作，藉由攔截鍵盤輸入，因此，IME 是否存在於應用程式中是透明的。 幾乎所有的 Windows 應用程式都可以在不知道是否存在且不需要特殊編碼的情況下，隨時利用 ime。

一般的 IME 會顯示數個視窗，以引導使用者完成字元輸入，如下列範例所示。

![ime 會顯示數個視窗](images/ime-elements.png)

| 視窗類型                                       | Description                                                                                                                                                                                                                                                                                                                 | IME 輸出                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| A. 讀取視窗                                 | 包含鍵盤的按鍵;通常會在每次擊鍵之後變更。                                                                                                                                                                                                                                              | 讀取字串                               |
| B. 撰寫視窗                             | 包含使用者使用 IME 所撰寫的字元集合。 這些字元是由應用程式頂端的 IME 所繪製。 當使用者將組合字元串通知給 IME 時，IME 接著會透過一系列的 WM 字元訊息，將撰寫字串傳送給應用程式 \_ 。 | 組合字元串                           |
| C. 候選視窗                               | 當使用者輸入有效的發音時，IME 會顯示所有符合指定發音的候選字元清單。 然後，使用者從這份清單中選取想要的字元，並將此字元加入至組合視窗顯示中。                                                    | 組合字元串中的下一個字元 |
| D. [輸入地區](/windows/desktop/Intl/nls-terminology) 設定指標 | 顯示使用者為鍵盤輸入選取的語言。 此指標內嵌于 Windows 工作列中。 開啟 [地區及語言選項] 主控台然後按一下 [語言] 索引標籤上的 [詳細資料]，即可選取輸入語言。                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a>搭配使用 Ime 與 DXUT

在 DXUT 中，CDXUTIMEEditBox 類別會實作為 IME 功能。 這個類別衍生自 CDXUTEditBox 類別，此為架構所提供的基本編輯控制項。 CDXUTIMEEditBox 會藉由覆寫 CDXUTIMEEditBox 方法，擴充該編輯控制項以支援 Ime。 這些類別是以這種方式設計，可協助開發人員瞭解他們需要從架構中取得的內容，以在自己的編輯控制項中執行 IME 支援。 本主題的其餘部分將說明架構和 CDXUTIMEEditBox 如何覆寫基本編輯控制項以執行 IME 功能。

CDXUTIMEEditBox 中大部分的輸入法特定變數都會宣告為靜態，因為許多輸入的緩衝區和狀態都是進程特有的。 比方說，進程的組合字元串只有一個緩衝區。 即使進程有十個編輯控制項，它們全都會共用相同的組合字元串緩衝區。 因此，CDXUTIMEEditBox 的組合字元串緩衝區是靜態的，可防止應用程式佔用不必要的記憶體空間。

CDXUTIMEEditBox 會在下列 DXUT 程式碼中執行：

 (SDK 根) \\ 範例 \\ c + + \\ Common \\ DXUTgui .cpp

## <a name="overriding-the-default-ime-behavior"></a>覆寫預設的 IME 行為

IME 通常會使用標準 Windows 程式來建立視窗 (請參閱[使用 Windows](/windows/desktop/winmsg/using-windows)) 。 在正常情況下，這會產生令人滿意的結果。 不過，當應用程式在全螢幕模式下呈現時（如同遊戲的常見），標準 windows 將不再運作，而且可能不會顯示在應用程式的最上層。 若要解決這個問題，應用程式必須繪製 IME 視窗本身，而不是依賴 Windows 來執行這項工作。

當預設的 IME 視窗建立行為未提供應用程式所需的行為時，應用程式可以覆寫 IME 視窗處理。 應用程式可以藉由處理輸入法相關的訊息，並呼叫 [輸入方法管理員](/windows/desktop/Intl/input-method-manager) (IMM) API 來達到此目的。

當使用者與 IME 互動以輸入複雜字元時，輸出會將訊息傳送至應用程式，以通知它有重要事件，例如開始撰寫或顯示候選視窗。 應用程式通常會忽略這些訊息，並將它們傳遞至預設的訊息處理常式，以使 IME 處理這些訊息。 當應用程式（而不是預設處理常式）處理訊息時，它會完全控制每個 IME 事件所發生的情況。 訊息處理常式通常會呼叫 IMM API 來抓取各種 IME 視窗的內容。 一旦應用程式擁有這種資訊之後，它就可以在需要呈現給顯示器時，適當地繪製 IME 視窗本身。

## <a name="functions"></a>函式

輸入法需要取得讀取字串、隱藏讀取視窗，以及取得閱讀視窗的方向。 下表顯示每個 IME 版本的功能：



|                    | 取得讀取字串                                                | 隱藏讀取視窗                       | 讀取視窗的方向                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| **在6.0 版之前** | A. 直接讀取視窗存取 IME 私用資料。 請參閱「4結構」 | 陷阱 IME 私用訊息。 請參閱「3個訊息」 | 檢查登錄資訊。 請參閱 "5 Registry Information" |
| **6.0 版之後**  | [GetReadingString](#getreadingstring)                                 | [ShowReadingWindow](#showreadingwindow)     | [GetReadingString](#getreadingstring)                      |



 

## <a name="messages"></a>訊息

下列訊息不需要針對執行 [ShowReadingWindow](#showreadingwindow) () 的較新 IME 進行處理。

下列訊息是由應用程式訊息處理常式所攔截 (也就是它們不會傳遞至 DefWindowProc) 以防止讀取視窗顯示。

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a>範例

下列範例說明如何從沒有 GetReadingString () 的舊版輸入法讀取字串資訊。 此程式碼會產生下列輸出：



| 輸出              | 描述                                                                                      |
|--------------|---------------------------------------------------------------------------------------|
| DWORD dwlen  | 讀取字串的長度。                                                          |
| DWORD dwerr  | 錯誤字元的索引。                                                                   |
| LPWSTR wstr  | 讀取字串的指標。                                                         |
| BOOL unicode | 若為 true，則表示讀取字串採用 Unicode 格式。 否則會是多位元組格式。 |



 

### <a name="cht-ime-version-42-43-and-44"></a>CHT IME 4.2、4.3 和4.4 版

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a>CHT IME 5.0 版

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a>CHT IME 5.1、5.2 和 CHS IME 版本5。3

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a>CHS IME 4.1 版

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a>CHS IME 4.2 版

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a>輸入法訊息

全螢幕應用程式必須適當地處理下列與 IME 相關的訊息：

### <a name="wm_inputlangchange"></a>WM \_ INPUTLANGCHANGE

\_當使用者以按鍵組合變更輸入地區設定之後，輸出會將 WM INPUTLANGCHANGE 訊息傳送至應用程式的使用中視窗， (通常是 ALT + SHIFT) ，或使用工作列或語言列上的輸入地區設定指標。 語言列是螢幕上的控制項，使用者可以用它來設定文字服務。  (參閱 [如何顯示語言](/windows/desktop/TSF/how-to-set-up-tsf)列。 ) 下列螢幕擷取畫面顯示當使用者按一下地區設定指標時所顯示的語言挑選清單。

![當使用者按一下地區設定指標時所顯示的語言挑選清單](images/ime-langselection.png)

當 IMM 傳送 WM \_ INPUTLANGCHANGE 訊息時，CDXUTIMEEditBox 必須執行幾項重要工作：

1.  呼叫 GetKeyboardLayout 方法，以傳回應用程式執行緒 (識別碼) 的輸入地區設定識別碼。 CDXUTIMEEditBox 類別會將此識別碼儲存在其靜態成員變數 s \_ hklCurrent 中，以供稍後使用。 應用程式必須知道目前的輸入地區設定是很重要的，因為每種語言的 IME 都有自己的獨特行為。 開發人員可能需要針對不同的輸入地區設定提供不同的程式碼。
2.  CDXUTIMEEditBox 會初始化要顯示在編輯方塊語言指標中的字串。 當應用程式在全螢幕模式下執行，而且沒有看到工作列或語言列時，此指標可以顯示作用中的輸入語言。
3.  呼叫 ImmGetConversionStatus 方法，以指出輸入地區設定是否為原生或非原生轉換模式。 原生轉換模式可讓使用者以選擇的語言輸入文字。 非原生轉換模式讓鍵盤成為標準的英文鍵盤。 請務必為使用者提供視覺提示，指出輸入法在何種類型的轉換模式中，如此一來，使用者就能在叫用按鍵時輕鬆知道預期的字元。 CDXUTIMEEditBox 會以語言指標色彩提供此視覺提示。 當輸入地區設定使用具有原生轉換模式的輸入法時，CDXUTIMEEditBox 類別會使用 m IndicatorImeColor 參數所定義的色彩來繪製指標文字 \_ 。 當 IME 處於非原生轉換模式，或完全沒有使用任何輸入法時，類別會使用 m IndicatorEngColor 參數所定義的色彩來繪製指標文字 \_ 。
4.  CDXUTIMEEditBox 會檢查輸入地區設定，並將韓文的靜態成員變數 s bInsertOnType 設定為 TRUE，並將 \_ 所有其他語言設定為 FALSE。 因為韓文 Ime 和所有其他 Ime 的行為不同，所以需要此旗標。 以韓文以外的語言輸入字元時，使用者輸入的文字會顯示在組合視窗中，使用者可以自由變更組合字元串的內容。 當您滿意組合字元串時，使用者按下 ENTER 鍵，然後將組合字元串以一系列的 WM 字元訊息傳送至應用程式 \_ 。 不過，在韓文 Ime 中，當使用者按下按鍵來輸入文字時，會立即將字元傳送至應用程式。 當使用者後續按更多按鍵來修改該初始字元時，編輯方塊中的字元會變更，以反映使用者的其他輸入。 基本上，使用者是在編輯方塊中撰寫字元。 這兩種行為不同，CDXUTIMEEditBox 必須特別為每個行為編寫程式碼。
5.  呼叫靜態成員方法 SetupImeApi 時，會從 IME 模組取得兩個函式的位址： GetReadingString 和 ShowReadingWindow。 如果這些函式存在，則會呼叫 ShowReadingWindow 來隱藏此 IME 的預設讀取視窗。 由於應用程式會轉譯讀取視窗本身，因此它會通知 IME 停用繪製預設的讀取視窗，使其不會干擾全螢幕呈現。

\_ \_ 當應用程式的視窗啟用時，IMM 會傳送 WM IME SETCONTEXT 訊息。 此訊息的 lParam 參數所包含的旗標，會向 IME 指出應該繪製的視窗，以及不應該使用的參數。 因為應用程式會處理所有繪圖，所以不需要 IME 來繪製任何 IME 視窗。 因此，應用程式的訊息處理常式只會將 lParam 設定為0，並傳回。

為了讓應用程式支援 IME，IME 相關訊息 WM ime SETCONTEXT 需要進行特殊處理 \_ \_ 。 因為 Windows 通常會在呼叫 PanoramaInitialize () 方法之前將此訊息傳送至應用程式，所以全景沒有機會處理 UI 來顯示候選清單視窗。

下列程式碼片段會指定 Windows 應用程式不會顯示任何與候選清單視窗相關聯的 UI，讓全景可以明確地處理這個 ui。

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a>WM \_ IME \_ STARTCOMPOSITION

\_ \_ 當 IME 組合即將從使用者擊鍵的結果開始時，輸出會將 WM ime STARTCOMPOSITION 訊息傳送至應用程式。 如果 IME 使用撰寫視窗，則會在組合視窗中顯示目前的組合字元串。 CDXUTIMEEditBox 會執行兩個工作來處理此訊息：

1.  CDXUTIMEEditBox 會清除組合字元串緩衝區和屬性緩衝區。 這些緩衝區是 CDXUTIMEEditBox 的靜態成員。
2.  CDXUTIMEEditBox 會將 s \_ bHideCaret 靜態成員變數設為 TRUE。 這個成員定義在基底 CDXUTEditBox 類別中，可控制是否要在編輯方塊時繪製編輯方塊中的游標。 組合視窗的功能類似于具有文字和游標的編輯方塊。 為了避免在組合視窗可見時產生混淆，編輯方塊會隱藏其資料指標，因此一次只會顯示一個資料指標。

### <a name="wm_ime_composition"></a>WM \_ IME \_ 組合

\_ \_ 當使用者輸入按鍵來變更組合字元串時，IMM 會將 WM IME 組合訊息傳送至應用程式。 LParam 的值表示應用程式可以從輸入方法管理員 (的 IMM) 中取出的資訊類型。 應用程式應該藉由呼叫 [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) 來取得可用的資訊，然後應該將資訊儲存在其私用緩衝區中，以便稍後可以轉譯 IME 元素。

CDXUTIMEEditBox 會檢查並抓取下列組合字元串資料：



| [**WM \_IME \_ 組合**](/windows/desktop/Intl/wm-ime-composition) lParam 旗標值 | 資料                           | 描述                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GC \_ COMPATTR                                                         | 組合屬性          | 這個屬性所包含的資訊，像是組合字元串中每個字元的狀態 (例如，已轉換或非轉換的) 。 這項資訊是必要的，因為 CDXUTIMEEditBox 會根據其屬性，以不同的方式來色彩撰寫字串字元。                                                                                   |
| GC \_ COMPCLAUSE                                                       | 撰寫子句資訊 | 當日文 IME 為使用中時，會使用這個子句資訊。 轉換日文組合字元串時，可以將字元群組在一起，成為轉換成單一實體的子句。 當使用者移動游標時，CDXUTIMEEditBox 會使用這項資訊來反白顯示整個子句，而不只是子句內的單一字元。 |
| GC \_ COMPSTR                                                          | 組合字元串             | 這個字串是由使用者組成的最新字串。 這也是顯示在組合視窗中的字串。                                                                                                                                                                                                                                        |
| GC \_ CURSORPOS                                                        | 組合游標位置    | 組合視窗會實作為游標，類似于編輯方塊中的游標。 應用程式可以在處理 WM IME 組合訊息時取出游標位置，以便 \_ \_ 適當地繪製資料指標。                                                                                                                                            |
| GC \_ RESULTSTR                                                        | 結果字串                  | 當使用者即將完成撰寫程式時，就可以使用結果字串。 應抓取這個字串，並將字元傳送至編輯方塊。                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a>WM \_ IME \_ ENDCOMPOSITION

\_ \_ 當 IME 組合作業結束時，IMM 會將 WM ime ENDCOMPOSITION 訊息傳送至應用程式。 當使用者按下 ENTER 鍵核准組合字元串，或是按 ESC 鍵取消群組時，就會發生這種情況。 CDXUTIMEEditBox 會藉由將組合字元串緩衝區設定為空白來處理此訊息。 然後，它會將 \_ bHideCaret 設定為 FALSE，因為組合視窗已關閉，而編輯方塊中的游標應該會再次顯示。

CDXUTIMEEditBox 訊息處理常式也會將 \_ bShowReadingWindow 設定為 FALSE。 此旗標會控制當編輯方塊本身呈現時，類別是否繪製讀取視窗，因此在組合結束時必須將它設定為 FALSE。

### <a name="wm_ime_notify"></a>WM \_ 輸入法 \_ 通知

\_ \_ 每當輸入法視窗變更時，IMM 都會將 WM ime 通知訊息傳送至應用程式。 處理 IME 視窗繪圖的應用程式應該處理此訊息，讓它知道視窗內容的任何更新。 WParam 指出正在進行的命令或變更。 CDXUTIMEEditBox 會處理下列命令：




| IME 命令 | Description | 
|-------------|-------------|
| <a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a> | 這個屬性所包含的資訊，像是組合字元串中每個字元的狀態 (例如，已轉換或非轉換的) 。 這項資訊是必要的，因為 CDXUTIMEEditBox 會根據其屬性，以不同的方式來色彩撰寫字串字元。 | 
| <a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  / <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a> | 在即將開啟或更新候選視窗時，傳送至應用程式。 當使用者想要變更轉換的文字選擇時，就會開啟候選視窗。 當使用者移動選取指標或變更頁面時，會更新視窗。 CDXUTIMEEditBox 會針對這兩個命令使用一個訊息處理常式，因為所需的工作完全相同：<br /><ol><li>CDXUTIMEEditBox 會將候選清單結構的 bShowWindow 成員 s_CandList 設定為 TRUE，表示需要在畫面格轉譯期間繪製候選視窗。</li><li>CDXUTIMEEditBox 會藉由呼叫 <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>，先取得所需的緩衝區大小，然後再取得實際的資料，以抓取候選清單。</li><li>私用候選清單結構 s_CandList 會以抓取的候選資料進行初始化。</li><li>候選字串會儲存為字串陣列。</li><li>所選取專案的索引和頁面索引都會儲存起來。</li><li>CDXUTIMEEditBox 會檢查候選視窗樣式是垂直或水準。 如果視窗樣式是水準的，則額外的字串緩衝區（s_CandList 的 HoriCand 成員）必須使用所有的候選字串來初始化，並在所有相鄰字串之間插入空白字元。 轉譯垂直候選視窗時，會一次繪製一個候選字串，其中每個字串的 y 座標都會遞增。 不過，轉譯水準候選視窗時應該使用這個 HoriCand 字串，因為空白字元是在同一行上分隔兩個相鄰字串的最佳方式。</li></ol> | 
| <a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a> | 當候選視窗即將關閉時，傳送至應用程式。 當使用者從候選清單進行選取時，就會發生這種情況。 CDXUTIMEEditBox 會藉由將候選視窗的可見旗標設定為 FALSE，然後清除候選字串緩衝區，來處理此命令。 | 
| IMN_PRI加值稅E | 當 IME 將其讀取字串更新為使用者鍵入或移除字元的結果時，傳送至應用程式。 應用程式應該取出讀取字串，並加以儲存以供呈現。 CDXUTIMEEditBox 有兩個方法可根據 IME 中的讀取字串支援方式來取出讀取字串： <br /><ul><li>如果 IME 支援 GetReadingString 函式，就會呼叫 GetReadingString 來取出讀取字串。</li><li>如果 IME 未執行 GetReadingString，CDXUTIMEEditBox 會從輸入內容內容中抓取讀取字串。</li></ul> | 




 

## <a name="rendering"></a>轉譯

IME 元素和視窗的轉譯很簡單。 CDXUTIMEEditBox 可讓基類先轉譯，因為 IME 視窗應該會出現在編輯控制項的上方。 在基底編輯方塊呈現之後，CDXUTIMEEditBox 會檢查每個輸入視窗的可見度旗標 (指標、撰寫、候選和讀取視窗) 並繪製視窗（如果應該顯示的話）。 如需不同 IME 視窗類型的說明，請參閱預設的輸入法行為。

### <a name="input-locale-indicator"></a>輸入地區設定指標

輸入地區設定指標會在任何其他 IME 視窗之前轉譯，因為它是永遠顯示的元素。 因此，它應該會出現在其他的 IME 視窗底下。 CDXUTIMEEditBox 會藉由呼叫 RenderIndicator 方法來轉譯指標，其中指標字型色彩是藉由檢查 s \_ ImeState 靜態變數（反映目前的 IME 轉換模式）來決定。 啟用 IME 且原生轉換為使用中時，此方法會使用 m \_ IndicatorImeColor 做為指標色彩。 如果 IME 已停用或處於非原生轉換模式， \_ 則會使用 m IndicatorImeColor 來繪製指標文字。 根據預設，指標視窗本身會繪製在編輯方塊的右邊。 應用程式可以藉由覆寫 RenderIndicator 方法來變更此行為。

下圖顯示英文的輸入地區設定指標的不同外觀、英數位元轉換模式的日文，以及日文的原生轉換模式：

![英文和日文輸入地區設定指標的不同外觀](images/ime-indicator.png)

### <a name="composition-window"></a>撰寫視窗

撰寫視窗的繪圖是在 CDXUTIMEEditBox 的 RenderComposition 方法中處理。 撰寫視窗會浮動在編輯方塊上方。 它應該繪製在基礎編輯控制項的游標位置。 CDXUTIMEEditBox 會處理轉譯，如下所示：

1.  整個組合字元串是使用預設的組合字元串色彩來繪製。
2.  具有特定特殊屬性的字元應以不同的色彩繪製，因此 CDXUTIMEEditBox 會審核組合字元串的字元，並檢查字串屬性。 如果屬性呼叫不同的色彩，則會使用適當的色彩再次繪製該字元。
3.  繪製組合視窗的游標以完成轉譯。

資料指標應針對韓文 Ime 閃爍，但不應該用於其他 Ime。 RenderComposition 會根據使用韓文 IME 時的計時器值，決定是否要顯示資料指標。

### <a name="reading-and-candidate-windows"></a>讀取和候選 Windows

讀取和候選視窗都是由相同的 CDXUTIMEEditBox 方法 RenderCandidateReadingWindow 所呈現。 這兩個視窗都包含垂直配置的字串陣列，或是水準配置時的單一字串。 RenderCandidateReadingWindow 中的大部分程式碼都是用來放置視窗，讓視窗中的部分不會落在應用程式視窗之外，而且會被裁剪。

## <a name="limitations"></a>限制

Ime 有時包含增強的功能，可改善輸入文字的便利性。 下圖顯示一些在較新的 Ime 中找到的功能。 這些 advanced 功能不存在於 DXUT 中。 由於未定義介面可從 Ime 取得必要的資訊，因此針對這些先進的功能執行支援可能會很困難。

先進的繁體中文 IME 與擴充的候選清單：

![具有展開候選清單的 advanced 繁體中文 ime](images/ime-advanced1.png)

具有一些候選項目的 Advanced 日文 IME，其中包含可描述其意義的其他文字：

![具有某些候選項目的 advanced 日文 ime，其中包含用來描述其意義的其他文字](images/ime-advanced2.png)

包含手寫辨識系統的 Advanced 韓文 IME：

![包含手寫辨識系統的 advanced 韓文 ime](images/ime-advanced3.png)

## <a name="registry-information"></a>登錄資訊

當目前的 IME 較舊 CHT 不會執行 GetReadingString () 的新語音時，會檢查下列登錄資訊以決定閱讀視窗的方向。



| Key                                                           | 值            |
|---------------------------------------------------------------|------------------|
| HKCU \\ software \\ microsoft \\ windows \\ currentversion \\ IME \_ 名稱 | 鍵盤對應 |



 

其中： \_ 如果 ime 檔案版本是5.1 或更新版本，則會 MSTCIPH ime 名稱; 否則輸入 \_ 名稱為 TINTLGNT。

讀取視窗的方向是水準的，如果其中一個：

-   IME 是版本5.0，而鍵盤對應值為0x22 或0x23
-   IME 是版本5.1 或5.2 版，而鍵盤對應值為0x22、0x23 或0x24。

如果兩個條件都不符合，讀取視窗會垂直。

## <a name="appendix-a-cht-versions-per-operating-system"></a>附錄 A：每個作業系統的 CHT 版本



| 作業系統           | CHT IME 版本 |
|----------------------------|-----------------|
| Windows 98                 | 4.2             |
| Windows 2000               | 4.3             |
| 未知                    | 4.4             |
| Windows我                 | 5.0             |
| Office XP                  | 5.1             |
| Windows XP                 | 5.2             |
| 獨立 web 可下載檔案 | 6.0             |



 

## <a name="further-information"></a>詳細資訊

如需相關資訊，請參閱：

-   [安裝和使用輸入法編輯器](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [國際文字顯示](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [Unicode 協會](https://www.unicode.org/)
-   開發國際軟體。 Dr. 國際化。 第 2 ed。 華盛頓州 Redmond，WA： Microsoft 按下，2003。

## <a name="getreadingstring"></a>GetReadingString

取得讀取字串資訊。

**參數**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[在 [ \] 輸入內容] 中。

</dd> <dt>

<span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*
</dt> <dd>

\[在 \] WCHAR 中的 lpwReadingBuf 長度。 如果是零，則表示查詢讀取緩衝區長度。

</dd> <dt>

<span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf* 
</dt> <dd>

\[out 傳回 \] 讀取字串 (不是零的結束) 。

</dd> <dt>

<span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex* 
</dt> <dd>

\[\]如果有的話，會傳回讀取字串中錯誤字元的索引。

</dd> <dt>

<span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical* 
</dt> <dd>

\[\]如果是 TRUE，則讀取 UI 是垂直的。 否則，水準 puMaxReadingLen。

</dd> <dt>

<span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen* 
</dt> <dd>

\[\]讀取 UI 長度。 最大讀取長度不是固定的;它不僅取決於鍵盤配置，也取決於輸入模式 (例如，內部程式碼、代理輸入) 。

</dd> </dl>

**傳回值**

讀取字串長度。

**備註**

如果傳回值大於 uReadingBufLen 的值，則所有輸出參數都是未定義的。

此函式會在 CHT IME 6.0 或更新版本中執行，並可在輸入法模組控制碼上以 GetProcAddress 方式取得。ImmGetIMEFileName 和 LoadLibrary 可以取得輸入法模組控制碼。

**需求**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**頭**
</dt> <dd>

宣告于 Imm. h 中。

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**匯入程式庫**
</dt> <dd>

使用 Imm。

</dd> </dl>

## <a name="showreadingwindow"></a>ShowReadingWindow

顯示 (或隱藏讀取視窗) 。

**參數**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[在 [ \] 輸入內容] 中。

</dd> <dt>

<span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow* 
</dt> <dd>

\[\]將設定為 TRUE 以顯示閱讀視窗 (或 FALSE，將它隱藏) 。

</dd> </dl>

**傳回值**

**備註**

如果成功則傳回 TRUE，否則傳回 FALSE。

**需求**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**頭**
</dt> <dd>

宣告于 Imm. h 中。

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**匯入程式庫**
</dt> <dd>

使用 Imm。

</dd> </dl>
