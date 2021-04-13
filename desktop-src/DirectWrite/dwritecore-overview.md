---
title: DWriteCore 總覽
description: DWriteCore 是 DirectWrite 的專案留尼旺島執行。
keywords:
- DirectWrite 核心
- DWriteCore
ms.topic: article
ms.date: 12/09/2020
ms.openlocfilehash: 605cab8d0cd0511b5ca3b0b14d517cdc3f290573
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321391"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="cc779-105">DWriteCore 總覽</span><span class="sxs-lookup"><span data-stu-id="cc779-105">DWriteCore overview</span></span>

<span data-ttu-id="cc779-106">DWriteCore 是[DirectWrite](./direct-write-portal.md)的[專案留尼旺島](/windows/apps/project-reunion/)執行。</span><span class="sxs-lookup"><span data-stu-id="cc779-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md).</span></span> <span data-ttu-id="cc779-107">DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。</span><span class="sxs-lookup"><span data-stu-id="cc779-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="cc779-108">本簡介主題說明 DWriteCore 是什麼，並示範如何將它安裝到您的開發環境和程式。</span><span class="sxs-lookup"><span data-stu-id="cc779-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="cc779-109">DWriteCore 的價值主張</span><span class="sxs-lookup"><span data-stu-id="cc779-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="cc779-110">[DirectWrite](./direct-write-portal.md) 本身支援豐富的功能陣列，讓它成為大部分應用程式（ &mdash; 無論是透過直接呼叫或透過 [Direct2D](../direct2d/direct2d-portal.md)）在 Windows 上選擇的字型呈現工具。</span><span class="sxs-lookup"><span data-stu-id="cc779-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="cc779-111">DirectWrite 包含與裝置無關的文字版面配置系統、高品質的子圖元 [Microsoft ClearType](/typography/cleartype/) 文字轉譯、硬體加速文字、多重格式文字、先進的 [OpenType®](/typography/opentype/) 印刷樣式功能、寬語言支援，以及與 [GDI](../gdi/windows-gdi.md)相容的版面配置和轉譯。</span><span class="sxs-lookup"><span data-stu-id="cc779-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="cc779-112">自 Windows Vista SP2 起，DirectWrite 已推出，其多年來加入更先進的功能，例如變數字型，可讓開發人員將樣式、權數和其他屬性套用至只有一個字型資源的字型。</span><span class="sxs-lookup"><span data-stu-id="cc779-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables developers to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="cc779-113">但由於 DirectWrite 的存留期較長，因此開發的進展比起讓舊版的 Windows 保持在幕後。</span><span class="sxs-lookup"><span data-stu-id="cc779-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="cc779-114">此外，DirectWrite 的狀態為頂級文字轉譯技術僅限於 Windows，讓跨平臺應用程式可以撰寫自己的文字呈現堆疊，或依賴協力廠商解決方案。</span><span class="sxs-lookup"><span data-stu-id="cc779-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="cc779-115">DWriteCore 可解決版本功能損壞和跨平臺相容性的基本問題，方法是從系統中移除程式庫，並將所有可能支援的端點設為目標。</span><span class="sxs-lookup"><span data-stu-id="cc779-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="cc779-116">為此，我們已將 DWriteCore 整合到專案中，並提供可在所有 Windows 端點下 Windows 8 支援的公用 API，並開啟可讓您跨平臺使用的門。</span><span class="sxs-lookup"><span data-stu-id="cc779-116">To that end, we've integrated DWriteCore into Project Reunion with a public API that's supported on all Windows endpoints down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="cc779-117">DWriteCore 可讓您以開發人員的身分，在 Project 留尼旺島中提供您的主要價值，就是可讓您以最下層的方式存取所有目前的 DirectWrite 功能，以 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="cc779-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to all current DirectWrite features all the way down-level to Windows 8.</span></span> <span data-ttu-id="cc779-118">DWriteCore 的所有功能在所有下層版本上的運作都相同;換句話說，所有目前的功能都可以在 Windows 8、8.1 和所有版本的 Windows 10 上運作，而不需要任何差異有關哪些功能可在哪些版本上運作。</span><span class="sxs-lookup"><span data-stu-id="cc779-118">All features of DWriteCore will function the same on all down-level versions; in other words, all current features will work on Windows 8, 8.1, and all versions of Windows 10, without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="cc779-119">DWriteCore 示範應用程式 &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="cc779-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="cc779-120">DWriteCore 會透過 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式來示範，您現在可以在此下載及研究。</span><span class="sxs-lookup"><span data-stu-id="cc779-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="cc779-121">DWriteCore 入門</span><span class="sxs-lookup"><span data-stu-id="cc779-121">Get started with DWriteCore</span></span>

<span data-ttu-id="cc779-122">針對專案的0.1 發行前版本，我們目前不支援將「專案留尼旺島」 NuGet 套件安裝到您自己的專案中。</span><span class="sxs-lookup"><span data-stu-id="cc779-122">For the Project Reunion 0.1 Prerelease, we currently don't support installing the Project Reunion NuGet package into your own projects.</span></span> <span data-ttu-id="cc779-123">相反地，使用 DWriteCore 進行程式設計的目前支援選項是從 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式專案開始，並以該專案為基礎進行開發。</span><span class="sxs-lookup"><span data-stu-id="cc779-123">Instead, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span>

<span data-ttu-id="cc779-124">然後您可以隨意移除任何現有的原始程式碼 (或從該範例專案) 的檔案，以及將任何新的原始程式碼 (或) 至專案的檔案中。</span><span class="sxs-lookup"><span data-stu-id="cc779-124">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span> <span data-ttu-id="cc779-125">如需使用 DWriteCore 進行程式設計的詳細資訊，請參閱本主題稍後的 [使用 DWriteCore 進行程式設計](#programming-with-dwritecore) 一節。</span><span class="sxs-lookup"><span data-stu-id="cc779-125">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="cc779-126">DWriteCore 的發行階段</span><span class="sxs-lookup"><span data-stu-id="cc779-126">The release phases of DWriteCore</span></span>

<span data-ttu-id="cc779-127">將 DirectWrite 移植到 DWriteCore 是一種夠大的專案，可跨越多個 Windows 發行週期。</span><span class="sxs-lookup"><span data-stu-id="cc779-127">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="cc779-128">該專案會分成幾個階段，每個階段都對應至一個發行中傳遞的功能區塊。</span><span class="sxs-lookup"><span data-stu-id="cc779-128">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="cc779-129">目前版本的 DWriteCore 功能</span><span class="sxs-lookup"><span data-stu-id="cc779-129">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="cc779-130">目前可用的 DWriteCore 版本包含您的開發人員需要使用 DWriteCore 的基本工具，包括下列功能。</span><span class="sxs-lookup"><span data-stu-id="cc779-130">The version of DWriteCore currently available contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="cc779-131">字型列舉。</span><span class="sxs-lookup"><span data-stu-id="cc779-131">Font enumeration.</span></span>
- <span data-ttu-id="cc779-132">字型 API。</span><span class="sxs-lookup"><span data-stu-id="cc779-132">Font API.</span></span>
- <span data-ttu-id="cc779-133">塑造。</span><span class="sxs-lookup"><span data-stu-id="cc779-133">Shaping.</span></span>
- <span data-ttu-id="cc779-134">低層級呈現 Api。</span><span class="sxs-lookup"><span data-stu-id="cc779-134">Low-level rendering APIs.</span></span> <span data-ttu-id="cc779-135">這是目前階段的部分 &mdash; DWriteCore 不會與 [Direct2D](../direct2d/direct2d-portal.md)交互操作，但您可以使用 [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) 和 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)。</span><span class="sxs-lookup"><span data-stu-id="cc779-135">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="cc779-136">基本文字版面配置功能。</span><span class="sxs-lookup"><span data-stu-id="cc779-136">Basic text layout functionality.</span></span>
- <span data-ttu-id="cc779-137">文字呈現 Api。</span><span class="sxs-lookup"><span data-stu-id="cc779-137">Text-rendering APIs.</span></span>
- <span data-ttu-id="cc779-138">點陣圖呈現目標。</span><span class="sxs-lookup"><span data-stu-id="cc779-138">Bitmap render target.</span></span>
- <span data-ttu-id="cc779-139">色彩字型。</span><span class="sxs-lookup"><span data-stu-id="cc779-139">Color fonts.</span></span>
- <span data-ttu-id="cc779-140">其他優化 (字型快取清除、記憶體內部字型載入器等) 。</span><span class="sxs-lookup"><span data-stu-id="cc779-140">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="cc779-141">此階段的橫幅功能為色彩字型。</span><span class="sxs-lookup"><span data-stu-id="cc779-141">The banner feature at this stage is color fonts.</span></span> <span data-ttu-id="cc779-142">色彩字型可讓您以更精密的色彩功能轉譯字型，而不只是簡單的單一色彩。</span><span class="sxs-lookup"><span data-stu-id="cc779-142">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="cc779-143">例如，色彩字型是能夠轉譯表情和工具列圖示字型 (後者會由 Office 使用，例如) 。</span><span class="sxs-lookup"><span data-stu-id="cc779-143">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="cc779-144">色彩字型是在 Windows 8.1 中首次引進，但此功能已在 Windows 10 的版本 1607 (年度更新) 中大幅擴充。</span><span class="sxs-lookup"><span data-stu-id="cc779-144">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="cc779-145">清除字型快取的工作，以及記憶體中的字型載入器，可讓您更快速地載入字型和記憶體改善。</span><span class="sxs-lookup"><span data-stu-id="cc779-145">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="cc779-146">有了這些功能，您就可以立即開始使用一些 DirectWrite 的新式核心功能， &mdash; 例如可變字型 &mdash; 下層至 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="cc779-146">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts&mdash;down-level to Windows 8.</span></span> <span data-ttu-id="cc779-147">此程式庫的反復專案也可以在 [Android](https://www.android.com/)和 **Linux** 上使用。</span><span class="sxs-lookup"><span data-stu-id="cc779-147">This iteration of the library can also be consumed on [Android](https://www.android.com/), and **Linux**.</span></span> <span data-ttu-id="cc779-148">變數字型是 DirectWrite 客戶最重要的功能之一;它們是在 Windows 10、1709版 (秋季建立者更新) 中引進，因此在舊版中進行存取是以開發人員身分 boon 給您。</span><span class="sxs-lookup"><span data-stu-id="cc779-148">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a massive boon to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="cc779-149">我們邀請您成為 DirectWrite 開發人員</span><span class="sxs-lookup"><span data-stu-id="cc779-149">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="cc779-150">DWriteCore 以及其他的 Project 留尼旺島元件，都將以開放性開發人員意見反應來開發。</span><span class="sxs-lookup"><span data-stu-id="cc779-150">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="cc779-151">我們邀請您開始探索 DWriteCore，並在我們的 [Project 留尼旺島 GitHub 存放庫](https://github.com/microsoft/ProjectReunion/)中提供深入解析或要求至功能的開發。</span><span class="sxs-lookup"><span data-stu-id="cc779-151">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="cc779-152">使用 DWriteCore 進行程式設計</span><span class="sxs-lookup"><span data-stu-id="cc779-152">Programming with DWriteCore</span></span>

<span data-ttu-id="cc779-153">如先前所述，針對專案留尼旺島0.1 發行前版本，您使用 DWriteCore 進行程式設計的目前支援選項是從 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式專案開始。</span><span class="sxs-lookup"><span data-stu-id="cc779-153">As already mentioned, for the Project Reunion 0.1 Prerelease, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project.</span></span>

<span data-ttu-id="cc779-154">就像使用 [DirectWrite](./direct-write-portal.md)，您可以透過 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) 介面，透過其 COM light API 來進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="cc779-154">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="cc779-155">**DWriteCoreGallery** 已包含 `dwrite_core.h` 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="cc779-155">**DWriteCoreGallery** already includes the `dwrite_core.h` header file.</span></span> <span data-ttu-id="cc779-156">該標頭會先定義權杖 *DWRITE_CORE*，然後包含 `dwrite_3.h` 。</span><span class="sxs-lookup"><span data-stu-id="cc779-156">That header first defines the token *DWRITE_CORE*, and then it includes `dwrite_3.h`.</span></span> <span data-ttu-id="cc779-157">*DWRITE_CORE* token 很重要，因為它會指示任何後續包含的標頭，讓所有 DirectWrite api 可供您使用。</span><span class="sxs-lookup"><span data-stu-id="cc779-157">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="cc779-158">一旦加入專案之後 `dwrite_core.h` ，您就可以繼續撰寫程式碼、建立和執行。</span><span class="sxs-lookup"><span data-stu-id="cc779-158">Once a project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

```cppwinrt
// pch.h
...
#include <dwrite_core.h>
```

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="cc779-159">適用于 DWriteCore 的新或不同 Api</span><span class="sxs-lookup"><span data-stu-id="cc779-159">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="cc779-160">DWriteCore API 表面與 [DirectWrite](/windows/win32/api/_directwrite/)的方式大致相同。</span><span class="sxs-lookup"><span data-stu-id="cc779-160">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="cc779-161">但目前只有 DWriteCore 有少量的新 Api。</span><span class="sxs-lookup"><span data-stu-id="cc779-161">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="cc779-162">建立受限制的 factory 物件</span><span class="sxs-lookup"><span data-stu-id="cc779-162">Create a restricted factory object</span></span>

<span data-ttu-id="cc779-163">[**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md)列舉具有新的常數 &mdash; **DWRITE_FACTORY_TYPE_RESTRICTED**。</span><span class="sxs-lookup"><span data-stu-id="cc779-163">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_RESTRICTED**.</span></span> <span data-ttu-id="cc779-164">受限制的處理站比隔離處理站更受鎖定。</span><span class="sxs-lookup"><span data-stu-id="cc779-164">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="cc779-165">它不會以任何方式與跨進程或持續性的字型快取互動。</span><span class="sxs-lookup"><span data-stu-id="cc779-165">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="cc779-166">此外，從這個 factory 傳回的系統字型集合只包含已知字型。</span><span class="sxs-lookup"><span data-stu-id="cc779-166">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="cc779-167">以下是當您呼叫 [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) free 函式時，如何使用 **DWRITE_FACTORY_TYPE_RESTRICTED** 來建立受限制的 FACTORY 物件。</span><span class="sxs-lookup"><span data-stu-id="cc779-167">Here's how you can use **DWRITE_FACTORY_TYPE_RESTRICTED** to create a restricted factory object when you call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCreateFactory(
    DWRITE_FACTORY_TYPE_RESTRICTED,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="cc779-168">如果您將 **DWRITE_FACTORY_TYPE_RESTRICTED** 傳遞至不支援的舊版 DirectWrite，則 **DWriteCreateFactory** 會傳回 **E_INVALIDARG**。</span><span class="sxs-lookup"><span data-stu-id="cc779-168">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="cc779-169">將圖像繪製至系統記憶體點陣圖</span><span class="sxs-lookup"><span data-stu-id="cc779-169">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="cc779-170">DirectWrite 具有點陣圖轉譯目標介面，可支援將圖像轉譯成系統記憶體中的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="cc779-170">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="cc779-171">不過，目前取得基礎圖元資料存取權的唯一方法是透過 GDI，因此 API 無法跨平臺使用。</span><span class="sxs-lookup"><span data-stu-id="cc779-171">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="cc779-172">您可以藉由新增方法來取出圖元資料，輕鬆地解決此情況。</span><span class="sxs-lookup"><span data-stu-id="cc779-172">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="cc779-173">因此，DWriteCore 引進了 [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) 介面，以及其方法 [**IDWriteBitmapRenderTarget2：： GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md)。</span><span class="sxs-lookup"><span data-stu-id="cc779-173">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="cc779-174">該方法會接受 (指標的參數，以) 類型 [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md)，也就是新的結構。</span><span class="sxs-lookup"><span data-stu-id="cc779-174">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="cc779-175">您的應用程式會藉由呼叫 [IDWriteGdiInterop：： CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)來建立點陣圖呈現目標。</span><span class="sxs-lookup"><span data-stu-id="cc779-175">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="cc779-176">在 Windows 上，點陣圖轉譯目標會封裝 GDI 記憶體 DC，其中含有與 GDI 裝置無關的點陣圖 (DIB) 選取。</span><span class="sxs-lookup"><span data-stu-id="cc779-176">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="cc779-177">[IDWriteBitmapRenderTarget：:D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 會將圖像轉譯為 DIB。</span><span class="sxs-lookup"><span data-stu-id="cc779-177">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="cc779-178">DirectWrite 會呈現圖像本身，而不會透過 GDI。</span><span class="sxs-lookup"><span data-stu-id="cc779-178">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="cc779-179">然後，您的應用程式可以從點陣圖轉譯目標取得 **HDC** ，然後使用 [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) 將圖元複製到視窗 **HDC**。</span><span class="sxs-lookup"><span data-stu-id="cc779-179">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="cc779-180">在非 Windows 平臺上，您的應用程式仍然可以建立點陣圖轉譯目標，但它只會封裝沒有 **HDC** 和 DIB 的系統記憶體陣列。</span><span class="sxs-lookup"><span data-stu-id="cc779-180">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="cc779-181">如果沒有使用 **HDC**，您的應用程式就必須有另一種方式來取得點陣圖圖元，讓它可以複製或使用它們。</span><span class="sxs-lookup"><span data-stu-id="cc779-181">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="cc779-182">即使是在 Windows 上，取得實際的圖元資料有時也會很有用，而且我們會在下面的程式碼範例中，示範目前的做法。</span><span class="sxs-lookup"><span data-stu-id="cc779-182">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="cc779-183">DWriteCore 和 DirectWrite 之間的其他 API 差異</span><span class="sxs-lookup"><span data-stu-id="cc779-183">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="cc779-184">有一些僅限存根的 Api，或在非 Windows 平臺上的行為稍有不同。</span><span class="sxs-lookup"><span data-stu-id="cc779-184">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="cc779-185">例如， [IDWriteGdiInterop：： CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)會傳回非 Windows 平臺上的 **E_NOTIMPL** ，因為沒有 [GDI](../gdi/windows-gdi.md)的 **HDC** 沒有任何這類內容。</span><span class="sxs-lookup"><span data-stu-id="cc779-185">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="cc779-186">最後，還有一些其他 Windows Api 通常會與 DirectWrite 一起使用 (Direct2D 是值得注意的範例) 。</span><span class="sxs-lookup"><span data-stu-id="cc779-186">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="cc779-187">但是，Direct2D 和 DWriteCore 目前無法互通。</span><span class="sxs-lookup"><span data-stu-id="cc779-187">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="cc779-188">例如，如果您使用 DWriteCore 建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ，並將它傳遞至 [**D2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)，則該呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="cc779-188">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>