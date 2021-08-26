---
title: DWriteCore 總覽
description: DWriteCore 是 DirectWrite 的 Windows App SDK 執行。
keywords:
- DirectWrite核心
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: bfa23ef41ac2de77901f8601fa0a68f650730403e4dc0bee2f9bbf69d6e1bc9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902871"
---
# <a name="dwritecore-overview"></a>DWriteCore 總覽

DWriteCore 是[DirectWrite](./direct-write-portal.md) (的[Windows App SDK](/windows/apps/windows-app-sdk/) DirectWrite 是適用于高品質文字轉譯的 DirectX API、與解析度無關的大綱字型，以及) 的完整 Unicode 文字和版面配置支援。 DWriteCore 是一種 DirectWrite 形式，可在 Windows 向下執行以 Windows 10 版本 1809 (10.0;組建 17763) ，並開啟可讓您跨平臺使用的門。

本簡介主題說明 DWriteCore 是什麼，並示範如何將它安裝到您的開發環境和程式。

> [!TIP]
> 如需有效開發中 DirectX 元件的說明和連結，請參閱 blog post [頁面（Directx 登陸頁面](https://devblogs.microsoft.com/directx/landing-page/)）。

## <a name="the-value-proposition-of-dwritecore"></a>DWriteCore 的價值主張

[DirectWrite](./direct-write-portal.md)本身支援豐富的功能陣列，讓它成為大部分應用程式（ &mdash; 無論是透過直接呼叫或透過[Direct2D](../direct2d/direct2d-portal.md)） Windows 的字型轉譯工具。 DirectWrite 包含與裝置無關的文字版面配置系統、高品質的子圖元[Microsoft ClearType](/typography/cleartype/)文字轉譯、硬體加速文字、多重格式文字、先進的[OpenType®](/typography/opentype/)印刷樣式功能、寬語言支援，以及與[GDI](../gdi/windows-gdi.md)相容的版面配置和轉譯。 自 Windows Vista SP2 起，DirectWrite 已可供使用，而且已多年來加入更先進的功能，例如變數字型，可讓您將樣式、權數和其他屬性套用至只有一個字型資源的字型。

不過，由於 DirectWrite 的存留期很長，因此開發的進展比起將舊版的 Windows 遺留下來。 此外，DirectWrite 的狀態，因為 premier text 轉譯技術僅限於 Windows，因此跨平臺應用程式可以撰寫自己的文字呈現堆疊，或依賴協力廠商解決方案。

DWriteCore 可解決版本功能損壞和跨平臺相容性的基本問題，方法是從系統中移除程式庫，並將所有可能支援的端點設為目標。 為此，我們已將 DWriteCore 整合到 Windows App SDK。

DWriteCore 可讓您以開發人員身分在 Windows App SDK 中提供您的主要價值，就是它可提供許多 (的存取權，以及最終所有) DirectWrite 功能。 DWriteCore 的所有功能在所有下層版本上的運作都相同，而不需要任何差異有關哪些功能可在哪些版本上運作。

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>DWriteCore 示範應用程式 &mdash; DWriteCoreGallery

DWriteCore 會透過 [DWriteCoreGallery](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) 範例應用程式來示範，您現在可以在此下載及研究。

## <a name="get-started-with-dwritecore"></a>DWriteCore 入門

DWriteCore 是[Windows App SDK 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0)的一部分。 本節說明如何設定您的開發環境，以使用 DWriteCore 進行程式設計。

### <a name="install-the-windows-app-sdk-08-vsix"></a>安裝 Windows App SDK 0.8 VSIX

在 Visual Studio 中，按一下 [**擴充** 功能  >  **管理延伸** 模組]，搜尋 *Windows App sdk*]，然後下載 Windows App sdk 擴充功能。 關閉並重新開啟 Visual Studio，並遵循提示來安裝擴充功能。

如需詳細資訊，請參閱[Windows App SDK 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0)並[設定您的開發環境](/windows/apps/windows-app-sdk/set-up-your-development-environment#3-install-the-windows-app-sdk-extension-for-visual-studio)。

### <a name="create-a-new-project"></a>建立新專案

在 Visual Studio 中，從空白應用程式建立新的專案 **，並在桌面) 專案範本中封裝 (WinUI 3** 。 您可以選擇 [language： *c + +*;] 來尋找該專案範本。平臺： *Windows App SDK*;專案類型： *Desktop*。

如需詳細資訊，請參閱[WinUI 3 的 Project 範本](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3)。

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a>安裝 ProjectReunion. DWrite NuGet 套件

在 Visual Studio 中，按一下 [ **Project** \> **管理 NuGet 套件** \> **]**，然後在 [搜尋] 方塊中輸入或貼上 **ProjectReunion** ，在搜尋結果中選取專案，然後按一下 [**安裝**] 以安裝該專案的套件。

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a>或者，從 DWriteCoreGallery 範例應用程式開始

或者，您可以從 [DWriteCoreGallery](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) 範例應用程式專案開始使用 DWriteCore 進行程式設計，並以該專案為基礎進行開發。 然後您可以隨意移除任何現有的原始程式碼 (或從該範例專案) 的檔案，以及將任何新的原始程式碼 (或) 至專案的檔案中。

### <a name="use-dwritecore-in-your-project"></a>在您的專案中使用 DWriteCore

如需使用 DWriteCore 進行程式設計的詳細資訊，請參閱本主題稍後的 [使用 DWriteCore 進行程式設計](#programming-with-dwritecore) 一節。

## <a name="the-release-phases-of-dwritecore"></a>DWriteCore 的發行階段

將 DirectWrite 移植至 DWriteCore 是一項夠大的專案，以跨越多個 Windows 的發行週期。 該專案會分成幾個階段，每個階段都對應至一個發行中傳遞的功能區塊。

### <a name="features-in-the-current-release-of-dwritecore"></a>目前版本的 DWriteCore 功能

目前可用的 DWriteCore 版本是[Windows App SDK 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0)的一部分。 它包含您以開發人員身分使用 DWriteCore 所需的基本工具，包含下列功能。

- 字型列舉。
- 字型 API。
- 塑造。
- 低層級呈現 Api。 這是目前階段的部分 &mdash; DWriteCore 不會與 [Direct2D](../direct2d/direct2d-portal.md)交互操作，但您可以使用 [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) 和 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)。
- 基本文字版面配置功能。
- 文字呈現 Api。
- 點陣圖呈現目標。
- 色彩字型。
- 其他優化 (字型快取清除、記憶體內部字型載入器等) 。
- 支援底線 &mdash; ，請參閱 [**IDWriteTextLayout：： GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) 和 [**IDWriteTextLayout：： SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline)。
- 支援刪除線的詳細內容 &mdash; ，請參閱 [**IDWriteTextLayout：： GetStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getstrikethrough) 和 [**IDWriteTextLayout：： SetStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setstrikethrough)。
- 透過 IDWriteTextLayout 支援垂直文字[](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) &mdash; 請參閱[垂直文字](/windows/win32/directwrite/vertical-text)。
- [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)和 [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)介面的所有方法都是實作為。

橫幅功能為色彩字型。 色彩字型可讓您以更精密的色彩功能轉譯字型，而不只是簡單的單一色彩。 例如，色彩字型是可轉譯表情和工具列圖示字型 (後者會由 Office 使用的功能，例如) 。 色彩字型是在 Windows 8.1 中首次引進，但此功能已在 Windows 10 的版本 1607 (年度更新) 中大幅擴充。

清除字型快取的工作，以及記憶體中的字型載入器，可讓您更快速地載入字型和記憶體改善。

有了這些功能，您就可以立即開始使用一些 DirectWrite 的新式核心功能， &mdash; 例如變數字型。 變數字型是 DirectWrite 客戶最重要的功能之一。

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>我們邀請您成為 DirectWrite 開發人員

DWriteCore 以及其他 Windows App SDK 元件，將會以開放性開發人員意見反應來開發。 我們邀請您開始探索 DWriteCore，並在我們的[Windows App SDK GitHub 存放庫](https://github.com/microsoft/ProjectReunion/)上提供見解或要求至功能開發。

## <a name="programming-with-dwritecore"></a>使用 DWriteCore 進行程式設計

就像 [DirectWrite](./direct-write-portal.md)一樣，您也可以透過 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)介面，透過其 DWriteCore 的 COM light API 來進行程式設計。

若要使用 DWriteCore，必須包含 `dwrite_core.h` 標頭檔。

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

`dwrite_core.h`標頭檔會先定義權杖 *DWRITE_CORE*，然後再包含 `dwrite_3.h` 標頭檔。 *DWRITE_CORE* token 很重要，因為它會指示任何後續包含的標頭，讓所有 DirectWrite 的 api 都可供您使用。 當您的專案包含之後 `dwrite_core.h` ，您就可以繼續撰寫程式碼、建立和執行。

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>適用于 DWriteCore 的新或不同 Api

DWriteCore API 表面與[DirectWrite](/windows/win32/api/_directwrite/)的方式大致相同。 但目前只有 DWriteCore 有少量的新 Api。

#### <a name="create-a-factory-object"></a>建立 factory 物件

[**DWriteCoreCreateFactory**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free 函式會建立用於後續建立個別 DWriteCore 物件的 factory 物件。

**DWriteCoreCreateFactory** 的功能與系統版 DirectWrite 所匯出的 [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory)函式相同。 DWriteCore 函式有不同的名稱，以避免混淆。

#### <a name="create-a-restricted-factory-object"></a>建立受限制的 factory 物件

[**DWRITE_FACTORY_TYPE**](/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type)列舉具有新的常數 &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**，表示受限的 FACTORY。 受限制的處理站比隔離處理站更受鎖定。 它不會以任何方式與跨進程或持續性的字型快取互動。 此外，從這個 factory 傳回的系統字型集合只包含已知字型。 以下是當您呼叫 [**DWriteCoreCreateFactory**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free 函式時，如何使用 **DWRITE_FACTORY_TYPE_ISOLATED2** 來建立受限制的 FACTORY 物件。

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

如果您將 **DWRITE_FACTORY_TYPE_ISOLATED2** 傳遞至不支援的舊版 DirectWrite，則 **DWriteCreateFactory** 會傳回 **E_INVALIDARG**。

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>將圖像繪製至系統記憶體點陣圖

DirectWrite 具有點陣圖轉譯目標介面，可支援將圖像轉譯成系統記憶體中的點陣圖。 不過，目前取得基礎圖元資料存取權的唯一方法是透過 GDI，因此 API 無法跨平臺使用。 您可以藉由新增方法來取出圖元資料，輕鬆地解決此情況。

因此，DWriteCore 引進了 [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata) 介面，以及其方法 [**IDWriteBitmapRenderTarget2：： GetBitmapData**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata)。 該方法會接受 (指標的參數，以) 類型 [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32)，也就是新的結構。

您的應用程式會藉由呼叫 [IDWriteGdiInterop：： CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)來建立點陣圖呈現目標。 在 Windows 上，點陣圖轉譯目標會封裝 gdi 記憶體 DC，並在其中選取與 gdi 裝置無關的點陣圖 (DIB) 。 [IDWriteBitmapRenderTarget：:D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 會將圖像轉譯為 DIB。 DirectWrite 直接轉譯圖像本身，而不需要透過 GDI。 然後，您的應用程式可以從點陣圖轉譯目標取得 **HDC** ，然後使用 [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) 將圖元複製到視窗 **HDC**。

在非 Windows 的平臺上，您的應用程式仍然可以建立點陣圖轉譯目標，但它只會封裝沒有 **HDC** 和 DIB 的系統記憶體陣列。 如果沒有使用 **HDC**，您的應用程式就必須有另一種方式來取得點陣圖圖元，讓它可以複製或使用它們。 即使在 Windows 上，取得實際的圖元資料有時也會很有用，而且我們會在下面的程式碼範例中，示範目前的做法。

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a>DWriteCore 與 DirectWrite 之間的其他 API 差異

有幾個僅限存根的 api，或它們在非 Windows 平臺上的行為稍有不同。 例如， [IDWriteGdiInterop：： CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)會在非 Windows 的平臺上傳回 **E_NOTIMPL** ，因為沒有 [GDI](../gdi/windows-gdi.md)的 **HDC** 沒有任何這類內容。

最後，還有一些其他 Windows 的 api，通常會與 DirectWrite 一起使用， (Direct2D 是值得注意的範例) 。 但是，Direct2D 和 DWriteCore 目前無法互通。 例如，如果您使用 DWriteCore 建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ，並將它傳遞至 [**D2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)，則該呼叫會失敗。
