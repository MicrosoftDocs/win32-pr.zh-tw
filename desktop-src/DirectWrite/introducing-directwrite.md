---
title: DirectWrite 簡介
description: 人們會在每日生活中隨時與文字進行通訊。
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite，關於
- DirectWrite，印刷樣式功能
- 印刷樣式
- DirectWrite，國際文字
- DirectWrite，OpenType 字型
- OpenType 字型
- DirectWrite，ClearType
- ClearType
- DirectWrite，API 總覽
- DirectWrite、IDWriteFontFace
- IDWriteFontFace
- DirectWrite，文字轉譯
- DirectWrite，轉譯模式
- DirectWrite，GDI 交互操作
- DirectWrite，互通性
- 互通性，DirectWrite
- '互通性、圖形裝置介面 (GDI) '
- '圖形裝置介面 (GDI) '
- 'GDI (圖形裝置介面) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842679"
---
# <a name="introducing-directwrite"></a>DirectWrite 簡介

人們會在每日生活中隨時與文字進行通訊。 這是人們取用增加資訊量的主要方式。 過去，它是用來透過印刷的內容，主要是檔、報紙、書籍等等。 越來越多，它是 Windows 電腦上的線上內容。 一般的 Windows 使用者從電腦螢幕上花了很多時間來進行讀取。 他們可能會在網路上衝浪、掃描電子郵件、撰寫報表、填寫試算表或撰寫軟體，但他們其實正在閱讀。 雖然文字和字型幾乎穿透 Windows 中使用者體驗的每個部分，但對大部分的使用者而言，在螢幕上閱讀並不如閱讀列印輸出一樣愉快。

針對 Windows 應用程式開發人員，撰寫文字處理程式碼是一項挑戰，因為提高可讀性、精密的格式和版面配置控制項，以及支援應用程式必須顯示的多種語言都有更高的需求。 即使是最基本的文字處理系統，也必須允許文字輸入、版面配置、顯示、編輯和複製和貼上。 Windows 使用者通常會預期更多的基本功能，甚至需要簡單的編輯器來支援多種字型、各種段落樣式、內嵌影像、拼寫檢查，以及其他功能。 新式 UI 設計也不再局限于單一格式（純文字），但需要以豐富的字型和文字版面配置提供更好的體驗。

這是 [DirectWrite](direct-write-portal.md) 如何讓 Windows 應用程式增強 UI 和檔文字體驗的簡介。

## <a name="improving-the-text-experience"></a>改善文字體驗

新式 Windows 應用程式對於其 UI 和檔中的文字有精密的需求。 這些包括更好的可讀性、支援多種語言和腳本，以及出色的轉譯效能。 此外，大部分現有的應用程式都需要一種方法，在 WindowsWin32 程式碼基底中履行現有的投資。

[DirectWrite](direct-write-portal.md) 提供下列三項功能，可讓 Windows 應用程式開發人員改善其應用程式內的文字體驗：與轉譯系統的獨立性、高品質的印刷樣式，以及多層的功能。

## <a name="rendering-system-independence"></a>Rendering-System 獨立性

[DirectWrite](direct-write-portal.md) 與任何特定圖形技術無關。 應用程式可自由使用最適合其需求的轉譯技術。 如此一來，應用程式就可以透過 Direct3D 或 [Direct2D](../direct2d/direct2d-portal.md)，彈性地繼續透過 GDI 和其他部分來呈現應用程式的某些部分。 事實上，應用程式可以選擇透過專屬的轉譯堆疊來呈現 DirectWrite。

## <a name="high-quality-typography"></a>High-Quality 印刷樣式

[DirectWrite](direct-write-portal.md) 利用 [OpenType](../intl/opentype-font-format.md) 字型技術的進展，在 Windows 應用程式中啟用高品質的印刷功能。 DirectWrite 字型系統提供的服務可處理字型列舉、字型回復和字型快取，這些都是應用程式用來處理字型的必要項。

[DirectWrite](direct-write-portal.md)所提供的[OpenType](../intl/opentype-font-format.md)支援可讓開發人員加入其應用程式的先進印刷樣式功能和國際文字支援。

## <a name="support-for-advanced-typographic-features"></a>支援先進的印刷樣式功能

[DirectWrite](direct-write-portal.md) 可讓應用程式開發人員將無法在 WINFORMS 或 GDI 中使用的 OpenType 字型功能解除鎖定。 DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) 物件會公開許多 OpenType 字型的 advanced 功能，例如樣式的替換和花飾。 Microsoft Windows 軟體開發套件 (SDK) 提供一組以豐富功能（例如 Pericles 和 Pescadero 字型）設計的範例 [OpenType](../intl/opentype-font-format.md) 字型。 如需 OpenType 功能的詳細資訊，請參閱 [Opentype 字型功能](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85))。

## <a name="support-for-international-text"></a>支援國際文字

[DirectWrite](direct-write-portal.md) 使用 [OpenType](../intl/opentype-font-format.md) 字型來啟用廣泛的國際文字支援。 支援 Unicode 功能，例如代理程式、雙向、換行和 UVS。 語言導向的腳本明細、數位替換和圖像成形，可確保任何腳本中的文字都具有正確的版面配置和轉譯。

目前支援下列指令碼︰

> [!Note]  
> 針對以標記的腳本 \* ，沒有預設系統字型。 應用程式必須安裝支援這些腳本的字型。

 

-   阿拉伯文
-   亞美尼亞文
-   Bengala
-   符號
-   盲文\*
-   加拿大土著音節
-   卻洛奇文
-   中文 (簡化 & 傳統) 
-   古斯拉夫文
-   科普特文\*
-   梵文字母
-   文
-   喬治亞文
-   文\*
-   希臘文
-   古吉拉特文
-   古木基文
-   Hebrew
-   日文
-   坎那達文
-   高棉文
-   韓文
-   寮文
-   拉丁文
-   馬來亞拉姆文
-   蒙古文
-   緬甸
-   新傣文
-   豎\*
-   歐迪亞文
-   ' 八位 pa
-   符文\*
-   僧伽羅文
-   敘利亞文
-   泰 Le
-   坦米爾文
-   泰盧固文
-   塔安那文
-   泰文
-   西藏文
-   爨文

## <a name="multiple-layers-of-functionality"></a>多層功能

[DirectWrite](direct-write-portal.md) 提供一些要素的功能，每一層都能與下一層緊密互動。 API 設計可讓應用程式開發人員根據其需求和排程，自由且彈性地採用個別層。 下圖顯示這些圖層之間的關聯性。

![directwrite 圖層的圖表，以及它們如何與應用程式或 ui 架構和圖形 api 通訊](images/intro-01.png)

文字版面配置 API 提供可從 [DirectWrite](direct-write-portal.md)取得的最高層級功能。 它提供應用程式用來測量、顯示及與豐富格式化文字字串互動的服務。 此文字 API 可用於目前使用 Win32 DrawText 的應用程式，以豐富的格式化文字建立新式 UI。

需要大量文字的應用程式，這些應用程式會執行自己的版面配置引擎，可以使用下一個圖層：腳本處理器。 腳本處理器會將文字區塊細分為腳本區塊，並處理 Unicode 標記法與字型中適當圖像標記法之間的對應，讓腳本的文字可以正確地以正確的語言顯示。 文字版面配置 API 層所使用的版面配置系統是以字型和腳本處理系統為基礎。

圖像呈現圖層是最小的功能層，可為執行自己的文字配置引擎的應用程式提供圖像轉譯功能。 圖像轉譯層也適用于實作為自訂轉譯器的應用程式，透過 [DirectWrite](direct-write-portal.md) 文字格式 API 中的回呼函式修改圖像繪圖行為。

[DirectWrite](direct-write-portal.md)字型系統適用于所有 DirectWrite 功能層，並可讓應用程式存取字型和圖像資訊。 它是設計來處理常見的字型技術和資料格式。 DirectWrite 字型模型遵循在相同字型家族中支援任意數量的加權、樣式和伸展的一般印刷方式作法。 這個模型（也就是 WPF 和 CSS 的相同模型）會指定只有權數 (粗體、淺色等字型，以及) 、樣式 (垂直、斜體或傾斜) 或延展 (窄、緊縮、寬等等) 視為單一字型家族的成員。

### <a name="improved-text-rendering-with-cleartype"></a>使用 ClearType 改進文字轉譯

在螢幕上提高可讀性是所有 Windows 應用程式的重要需求。 認知心理學研究中的辨識項表示我們必須能夠準確地辨識每個字母，而字母之間的間距甚至是快速處理的關鍵。 未對稱的字母和單字會被視為不美觀，而且會降低閱讀體驗。 Larson，Microsoft Advanced 閱讀技術群組，在以 IEEE 為範圍發行的主體上撰寫了一篇文章。 本文稱為「文字技術」 (https://www.spectrum.ieee.org/print/5049) 。

[DirectWrite](direct-write-portal.md)中的文字是使用 Microsoft ClearType 轉譯的，可增強文字的清晰和可讀性。 ClearType 利用新式 LCD 顯示器對每個可個別控制的圖元具有 RGB 條紋。 DirectWrite 使用最新的 ClearType 增強功能，第一次隨附于包含 Windows Presentation Foundation 的 Windows Vista，可讓它不只評估個別的字母，也可以評估字母之間的間距。 在這些 ClearType 增強功能之前，「讀取」大小為10或12點的文字難以顯示：我們可以在字母之間放置1圖元，這通常太小，或2個圖元，這通常太過多。 使用 subpixels 中的額外解析度可提供我們小數間距，以改善整個頁面的平均和對稱性。

下列兩個圖顯示使用子圖元定位時，如何在任何子圖元界限上開始使用符號。

下圖是使用「ClearType」版本的「ClearType 轉譯器」（不採用子圖元定位）來呈現。

![在不含子圖元定位的情況下呈現的「技術」圖例](images/intro-03.png)

下圖是使用 [DirectWrite](direct-write-portal.md) 版本的 ClearType 轉譯器轉譯，其使用子圖元定位。

![以子圖元定位呈現的「技術」圖例](images/intro-04.png)

請注意，字母 h 和 n 之間的間距甚至是第二個影像中的間距，而字母 o 會從字母 n 更進一步地分隔，甚至是使用字母 l。 另請注意，字母 l 的詞幹在自然的尋找方式。

子圖元 ClearType 定位可在螢幕上提供最精確的字元間距，尤其是子圖元與整個圖元之間的差異表示大量字元寬度的小型大小。 它可讓文字以理想的解析度空間來測量，並以其自然位置呈現于 LCD 色條紋，以及子圖元細微度。 使用這項技術測量和轉譯的文字是依定義、解析度無關，這表示完全相同的文字版面配置可跨各種顯示器解析度來達成。

不同于任何一種 GDI ClearType 轉譯，子圖元 ClearType 提供最精確的字元寬度。

文字字串 API 預設採用子圖元文字轉譯，這表示它會根據目前的顯示解析度來測量文字的理想解析度，並根據真正縮放的圖像前移寬度和定位位移來產生圖像定位結果。

針對大型文字， [DirectWrite](direct-write-portal.md) 也會啟用 y 軸的消除鋸齒，讓邊緣更平滑，並以字型設計工具的形式呈現字母。 下圖顯示 y 方向消除鋸齒。

![使用 y 方向消除鋸齒將 "cleartype" 轉譯為 gdi 文字和 directwrite 文字的圖例](images/intro-05.png)

雖然 [DirectWrite](direct-write-portal.md) 文字預設是使用子圖元 ClearType 來定位和轉譯，但仍有其他轉譯選項可用。 許多現有的應用程式都使用 GDI 來轉譯大部分的 UI，有些應用程式則使用系統編輯控制項，以繼續使用 GDI 進行文字轉譯。 將 DirectWrite 文字新增至這些應用程式時，可能需要犧牲子圖元 ClearType 提供的讀取體驗改進，讓文字在應用程式中具有一致的外觀。

為了符合這些需求， [DirectWrite](direct-write-portal.md) 也支援下列轉譯選項：

-   子圖元 ClearType (預設) 。
-   在水準和垂直維度中具有消除鋸齒的子圖元 ClearType。
-   別名文字。
-   Microsoft Word 閱讀檢視使用的 GDI 自然寬度 (，例如) 。
-   GDI 相容寬度 (包含東亞內嵌點陣圖) 。

您可以透過 DirectWrite API 和新的 Windows 7 收件匣 ClearType 調諧器來微調這些轉譯模式。

> [!Note]  
> 從 Windows 8 開始，在大部分情況下，您應該使用灰階文字消除鋸齒。 如需詳細資訊，請參閱下一節。

 

### <a name="support-for-natural-layout"></a>支援自然版面配置

自然配置與解析度無關，因此當您放大或縮小時，字元間距不會變更，或視顯示器的 DPI 而定。 第二個優點是，在字型的設計上，間距是 true。 自然配置是由 DirectWrite 對自然轉譯的支援所提供，這表示個別的字元可以定位至圖元的一部分。

雖然自然配置是預設值，但有些應用程式需要轉譯與 GDI 具有相同間距和外觀的文字。 針對這類應用程式，DirectWrite 提供 GDI 傳統和 GDI 自然測量模式和對應的轉譯模式。

上述任何轉譯模式都可以結合兩種消除鋸齒模式的其中一種： ClearType 或灰階。 ClearType 消除鋸齒會藉由個別操作每個圖元的紅色、綠色和藍色色彩值，模擬較高的解析度。 灰階消除鋸齒只會計算每個圖元的一個涵蓋範圍 (或 Alpha) 值。 ClearType 是預設值，但建議針對 Windows Store 應用程式使用灰階消除鋸齒，因為它比較快且與標準消除鋸齒相容，同時仍具有高度可讀性。

## <a name="api-overview"></a>API 概觀

[**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)介面是使用 DirectWrite 功能的起點。 Factory 是根物件，它會建立一組可一起使用的物件。

格式設定和版面配置作業是作業的必要條件，因為文字必須正確格式化並配置給一組指定的條件約束，才能進行繪製或點擊測試。 您可以使用 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) 來建立的兩個主要物件為此用途，例如 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 和 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)。 **IDWriteTextFormat** 物件代表文欄位落的格式資訊。 [**IDWriteFactory：： CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)函式會採用輸入字串、相關聯的條件約束（例如要填入的空間維度）和 **IDWriteTextFormat** 物件，並將經過完整分析和格式化的結果放入 **IDWriteTextLayout** 中，以用於後續作業。

然後，應用程式可以使用 [Direct2D](../direct2d/direct2d-portal.md)所提供的 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)函式，或執行可使用 GDI、Direct2D 或其他圖形系統轉譯圖像的回呼函式，以轉譯文字。 針對單一格式文字，Direct2D 上的 [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 函式提供較簡單的方式來繪製文字，而不需要先建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件。

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a>使用 DirectWrite 格式化和繪製 "Hello World"

下列程式碼範例會示範應用程式如何使用 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 來格式化單一段落，並使用 [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 函式加以繪製。


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a>存取字型系統

除了使用上述範例中的 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 介面來指定文字字串的字型系列名稱之外， [DirectWrite](direct-write-portal.md) 還可讓應用程式透過字型列舉來更充分掌控字型選取，以及根據內嵌檔字型建立自訂字型集合的能力。

[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)物件是字型系列的集合。 DirectWrite 可讓您透過稱為系統字型集合的特殊字型集合，存取系統上安裝的字型集。 這是藉由呼叫 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)物件的 [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection)方法來取得。 應用程式也可以從應用程式定義的回呼所列舉的一組字型建立自訂字型集合，也就是應用程式所安裝的私用字型，或內嵌在檔中的字型。

然後，應用程式可以呼叫 [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) 來取得集合內的特定 FontFamily 物件，然後呼叫 [**IDWriteFontFamily：： GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) 來取得特定的 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) 物件。 **IDWriteFont** 物件代表字型集合中的字型，並公開屬性和一些基本字型度量。

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)是另一個代表字型的物件，會在字型上公開一組完整的度量。 您可以直接從字型名稱建立 **IDWriteFontFace** ;應用程式不需要取得字型集合即可存取它。 它適用于需要查詢特定字型詳細資料的文字版面配置應用程式（例如 Microsoft Word）。

下圖說明這些物件之間的關聯性。

![字型集合、字型系列與字型字型之間關聯性的圖表](images/fontcollection.png)

### <a name="idwritefontface"></a>IDWriteFontFace

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)物件代表字型，並提供比 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)物件更詳細的字型資訊。 **IDWriteFontFace** 中的字型和字元度量適用于執行文字配置的應用程式。

大部分的主流應用程式不會直接使用這些 Api，而是會直接使用 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) 或指定字型系列名稱。

下表摘要說明這兩個物件的使用案例。



| 類別                                                                                                         | [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| 支援使用者互動的 Api，例如字型選擇器使用者介面：描述和其他資訊 Api | 是                                        | 否                                                 |
| 支援字型對應的 Api：系列、樣式、粗細、延展、字元涵蓋範圍                                 | 是                                        | 否                                                 |
| DrawText API                                                                                                     | 是                                        | 否                                                 |
| 用於呈現的 Api                                                                                          | 否                                         | 是                                                |
| 用於文字版面配置的 Api：圖像度量等                                                              | 否                                         | 是                                                |
| UI 控制項和文字版面配置的 Api：全字型計量                                                           | 是                                        | 是                                                |



 

下列範例應用程式會列舉系統字型集合中的字型。


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a>文字轉譯

文字轉譯 Api 可讓 [DirectWrite](direct-write-portal.md) 字型中的字元轉譯成 [DIRECT2D](../direct2d/direct2d-portal.md) 表面或 GDI 裝置獨立點陣圖，或是轉換成大綱或點陣圖。 相較于 Windows 先前的執行版本，DirectWrite 中的 ClearType 轉譯支援以改良的清晰度和對比來進行子圖元定位。 DirectWrite 也支援將黑白文字加上別名，以支援與內嵌點陣圖相關的東亞字型，或使用者已停用任何類型之字型平滑處理的案例。

所有的選項都可透過 [DirectWrite](direct-write-portal.md) api 存取的所有可用 ClearType 旋鈕進行調整，也可以透過新的 Windows 7 ClearType 調諧器控制台小程式來公開。

有兩個 Api 可用於轉譯圖像，一個可透過 [Direct2D](../direct2d/direct2d-portal.md) 提供硬體加速轉譯，另一個則提供軟體轉譯至 GDI 點陣圖。 使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 和執行 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 回呼的應用程式可以呼叫這些函式，以回應 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) 回呼。 此外，執行自己配置或處理圖像層級資料的應用程式可以使用這些 Api。

1.  [**ID2DRenderTarget：:D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    應用程式可以使用 [Direct2D](../direct2d/direct2d-portal.md) API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) 來提供硬體加速，以使用 GPU 進行文字轉譯。 硬體加速會影響文字轉譯管線的所有階段，包括將字元合併為圖像執行，以及篩選圖像執行點陣圖，以將 ClearType 混合演算法套用至最終顯示的輸出。 這是取得最佳轉譯效能的建議 API。

2.  [**IDWriteBitmapRenderTarget：:D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    應用程式可以使用 [**IDWriteBitmapRenderTarget：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 方法，執行將字元執行到 32-bpp 點陣圖的軟體呈現。 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)物件會封裝可用於呈現圖像的點陣圖和記憶體裝置內容。 如果您想要繼續使用 GDI，這個 API 會很有用，因為您有以 GDI 轉譯的現有程式碼基底。

如果您的應用程式具有使用 GDI 的現有文字版面配置程式碼，而且您想要保留其現有的版面配置程式碼，但只在轉譯圖像的最後一個步驟使用 [DirectWrite](direct-write-portal.md) ， [**IDWriteGdiInterop：： CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) 會在這兩個 api 之間提供橋樑。 在呼叫此函式之前，應用程式會使用 **IDWriteGdiInterop：： CreateFontFaceFromHdc** 函數，從裝置內容取得字型臉部參考。

> [!Note]  
> 在大部分的情況下，應用程式可能不需要使用這些圖像呈現 Api。 在應用程式建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件之後，就可以使用 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法來呈現文字。

 

## <a name="custom-rendering-modes"></a>自訂呈現模式

許多參數會影響文字轉譯，例如 gamma、ClearType 層級、圖元幾何和增強對比。 轉譯參數是由物件封裝，該物件會實作為公用 [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) 介面。 系統會根據 Windows 7 中的 ClearType 控制台小程式所指定的硬體內容和/或使用者喜好設定，自動初始化轉譯參數物件。 一般而言，如果用戶端使用 [DirectWrite](direct-write-portal.md) 版面配置 API，DirectWrite 將會自動選取對應至指定之測量模式的轉譯模式。

需要更多控制權的應用程式可以使用 [**IDWriteFactory：： CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) 來執行不同的轉譯選項。 這個函數也可以用來設定 gamma、圖元幾何和增強對比。

可用的各種呈現選項如下：

-   子圖元消除鋸齒

    應用程式會將 *renderingMode* 參數設定為 DWRITE 轉譯模式，使 \_ \_ \_ 其只以水準維度中的消除鋸齒來指定轉譯。

-   水準和垂直維度中的子圖元消除鋸齒。

    應用程式會將 *renderingMode* 參數設定為 DWRITE 轉譯 \_ \_ 模式 \_ 自然 \_ 對稱式，以指定以水準和垂直維度的消除鋸齒呈現。 如此一來，曲線和對角線線看起來會比某些柔和的成本更平滑，而且通常會用在 16 ppem 以上的大小。

-   別名文字

    應用程式會將 *renderingMode* 參數設定為 DWRITE \_ 呈現 \_ 模式 \_ ，以指定別名文字。

-   灰階文字

    應用程式會將 *pixelGeometry* 參數設定為 \_ 平面 DWRITE 圖元 \_ 幾何 \_ ，以指定灰階文字。

-   GDI 相容寬度 (包含東亞內嵌點陣圖) 

    應用程式會將 *renderingMode* 參數設定為 DWRITE 轉譯 \_ \_ 模式 \_ GDI \_ 傳統，以指定 gdi 相容寬度的消除鋸齒。

-   GDI 自然寬度

    應用程式會將 *renderingMode* 參數設定為 DWRITE 轉譯 \_ \_ 模式 \_ GDI \_ 自然，以指定 gdi 自然寬度相容的消除鋸齒。

-   大綱文字

    若要以大尺寸轉譯，應用程式開發人員可能會想要使用字型外框來轉譯，而不是藉由將它柵格化到點陣圖中。 應用程式會將 *renderingMode* 參數設定為 **DWRITE 轉譯 \_ \_ 模式 \_ 大綱** ，以指定轉譯應略過轉譯器並直接使用大綱。

## <a name="gdi-interoperability"></a>GDI 互通性

[**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop)介面提供與 GDI 的互通性。 這可讓應用程式繼續其在 GDI 程式碼基底中的現有投資，並選擇性地使用 [DirectWrite](direct-write-portal.md) 來呈現或配置。

下列 Api 可讓應用程式在 GDI 字型系統中進行遷移：

-   [**CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    建立符合 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構所指定之屬性的 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)物件。

-   [**ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    根據指定之 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)的 GDI 相容屬性，初始化 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構。

-   [**ConvertFontFaceToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    根據指定之 [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)的 GDI 相容屬性，初始化 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構。

-   [**CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    建立 [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) 物件，該物件會對應至目前選取的 **HFONT**。

## <a name="conclusion"></a>結論

改善閱讀體驗對於使用者是否在螢幕上或在紙張上很有價值。 [DirectWrite](direct-write-portal.md) 可為應用程式開發人員提供簡單易用和分層式程式設計模型，以改善其 Windows 應用程式的文字體驗。 應用程式可以使用 DirectWrite，以版面配置 API 呈現其 UI 和檔的豐富格式化文字。 在更複雜的案例中，應用程式可以直接使用圖像、存取字型等等，並利用 DirectWrite 的強大功能來提供高品質的印刷樣式。

[DirectWrite](direct-write-portal.md)的互通性功能可讓應用程式開發人員執行其現有的 Win32 程式碼基底，並選擇性地在其應用程式中採用 DirectWrite。

 

 