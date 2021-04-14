---
title: 自訂字型集
description: 本主題說明您可以在應用程式中使用自訂字型的各種方式。
ms.assetid: 50842838-d150-df9a-f1b7-67ce5ea2bc80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a79f1ccfcb1dadd355c5f582417aacb5041ecf8b
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383238"
---
# <a name="custom-font-sets"></a><span data-ttu-id="c7ba8-103">自訂字型集</span><span class="sxs-lookup"><span data-stu-id="c7ba8-103">Custom Font Sets</span></span>

<span data-ttu-id="c7ba8-104">本主題說明您可以在應用程式中使用自訂字型的各種方式。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-104">This topic describes various ways in which you can use custom fonts in your app.</span></span>

-   [<span data-ttu-id="c7ba8-105">介紹 </span><span class="sxs-lookup"><span data-stu-id="c7ba8-105">Introduction </span></span>](#introduction)
-   [<span data-ttu-id="c7ba8-106">API 的摘要</span><span class="sxs-lookup"><span data-stu-id="c7ba8-106">Summary of APIs</span></span>](#summary-of-apis)
-   [<span data-ttu-id="c7ba8-107">重要概念</span><span class="sxs-lookup"><span data-stu-id="c7ba8-107">Key concepts</span></span>](#key-concepts)
-   [<span data-ttu-id="c7ba8-108">字型和字型檔案格式</span><span class="sxs-lookup"><span data-stu-id="c7ba8-108">Fonts and font file formats</span></span>](#fonts-and-font-file-formats)
-   [<span data-ttu-id="c7ba8-109">字型組和字型集合</span><span class="sxs-lookup"><span data-stu-id="c7ba8-109">Font sets and font collections</span></span>](#font-sets-and-font-collections)
-   [<span data-ttu-id="c7ba8-110">常見案例</span><span class="sxs-lookup"><span data-stu-id="c7ba8-110">Common scenarios</span></span>](#common-scenarios)
    -   [<span data-ttu-id="c7ba8-111">使用本機檔案系統中的任意字型建立字型組</span><span class="sxs-lookup"><span data-stu-id="c7ba8-111">Creating a font set using arbitrary fonts in the local file system</span></span>](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [<span data-ttu-id="c7ba8-112">使用本機檔案系統中的已知字型建立字型組</span><span class="sxs-lookup"><span data-stu-id="c7ba8-112">Creating a font set using known fonts in the local file system</span></span>](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [<span data-ttu-id="c7ba8-113">在 Web 上使用已知的遠端字型來建立自訂字型組</span><span class="sxs-lookup"><span data-stu-id="c7ba8-113">Creating a custom font set using known, remote fonts on the Web</span></span>](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [<span data-ttu-id="c7ba8-114">使用載入至記憶體的字型資料來建立自訂字型組</span><span class="sxs-lookup"><span data-stu-id="c7ba8-114">Creating a custom font set using font data loaded into memory</span></span>](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [<span data-ttu-id="c7ba8-115">進階案例</span><span class="sxs-lookup"><span data-stu-id="c7ba8-115">Advanced scenarios</span></span>](#advanced-scenarios)
    -   [<span data-ttu-id="c7ba8-116">組合字型組</span><span class="sxs-lookup"><span data-stu-id="c7ba8-116">Combining font sets</span></span>](#combining-font-sets)
    -   [<span data-ttu-id="c7ba8-117">使用本機 WOFF 或 WOFF2 字型資料 </span><span class="sxs-lookup"><span data-stu-id="c7ba8-117">Using local WOFF or WOFF2 font data </span></span>](#using-local-woff-or-woff2-font-data)
    -   [<span data-ttu-id="c7ba8-118">使用 DirectWrite 遠端字型機制搭配自訂的低層級網路執行 </span><span class="sxs-lookup"><span data-stu-id="c7ba8-118">Using DirectWrite remote font mechanisms with custom low-level network implementation </span></span>](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [<span data-ttu-id="c7ba8-119">舊版 Windows 上的支援案例 </span><span class="sxs-lookup"><span data-stu-id="c7ba8-119">Supporting scenarios on earlier Windows versions </span></span>](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a><span data-ttu-id="c7ba8-120">簡介</span><span class="sxs-lookup"><span data-stu-id="c7ba8-120">Introduction</span></span>

<span data-ttu-id="c7ba8-121">大部分的情況下，應用程式會使用安裝在本機系統上的字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-121">Most of the time, apps use the fonts that are installed locally on the system.</span></span> <span data-ttu-id="c7ba8-122">DirectWrite 可讓您使用 [**IDWriteFactory3：： GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) 或 [**IDWriteFactory：： GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) 方法存取這些字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-122">DirectWrite provides access to these fonts using the [**IDWriteFactory3::GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) or [**IDWriteFactory::GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) methods.</span></span> <span data-ttu-id="c7ba8-123">在某些情況下，應用程式可能也會想要使用包含在 Windows 10 中的字型，但目前系統並未安裝該字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-123">In some cases, apps may also want to use fonts that are included as part of Windows 10 but that are not currently installed on the current system.</span></span> <span data-ttu-id="c7ba8-124">您可以使用 **GetSystemFontSet** 方法，或藉由呼叫 [**IDWriteFactory3：： GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) （includeDownloadableFonts 設定為 TRUE），從 Windows 字型服務存取這類字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-124">Such fonts can be accessed from the Windows font service by using the **GetSystemFontSet** method, or by calling [**IDWriteFactory3::GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) with includeDownloadableFonts set to TRUE.</span></span> 

<span data-ttu-id="c7ba8-125">不過，在某些應用程式案例中，應用程式需要使用未安裝在系統中且不是由 Windows 字型服務提供的字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-125">In some application scenarios, however, apps need to use fonts that are not installed in the system and are not provided by the Windows Font Service.</span></span> <span data-ttu-id="c7ba8-126">以下是這類案例的範例：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-126">The following are examples of such scenarios:</span></span>

-   <span data-ttu-id="c7ba8-127">字型會內嵌為應用程式二進位檔內的資源。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-127">Fonts are embedded as resources within an app binary.</span></span>
-   <span data-ttu-id="c7ba8-128">字型檔案會在應用程式套件中配套，並儲存在應用程式安裝資料夾下的磁片上。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-128">Font files are bundled within an app package and stored on disk under the app’s installation folder.</span></span>
-   <span data-ttu-id="c7ba8-129">應用程式是需要載入使用者指定字型檔案的字型開發工具。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-129">The app is a font-development tool that needs to load user-specified font files.</span></span> 
-   <span data-ttu-id="c7ba8-130">字型內嵌于可在應用程式中查看或編輯的檔檔案。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-130">Fonts are embedded in document files that can be viewed or edited in the app.</span></span> 
-   <span data-ttu-id="c7ba8-131">應用程式會使用從公用 Web 字型服務取得的字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-131">The app uses fonts obtained from a public Web font service.</span></span> 
-   <span data-ttu-id="c7ba8-132">應用程式會使用透過私人網路協定進行資料流程處理的字型資料。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-132">The app uses font data streamed via a private network protocol.</span></span> 

<span data-ttu-id="c7ba8-133">DirectWrite 提供 Api，可在這些和其他類似的案例中使用自訂字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-133">DirectWrite provides APIs for working with custom fonts in these and other similar scenarios.</span></span> <span data-ttu-id="c7ba8-134">自訂字型資料可能來自本機檔案系統中的檔案;從使用 HTTP 存取的遠端雲端式來源;或從任意來源載入至記憶體緩衝區之後。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-134">The custom font data might come from files in the local file system; from remote, cloud-based sources accessed using HTTP; or from arbitrary sources after having been loaded into a memory buffer.</span></span> 

> [!Note]  
> <span data-ttu-id="c7ba8-135">雖然 DirectWrite 提供了自 Windows 7 之後使用自訂字型的 Api，但新的 Api 已新增至 Windows 10，並同樣在 Windows 10 Creators Update (preview 組建15021或更新版本) 中，可讓您更輕鬆地執行所述的數個案例。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-135">While DirectWrite has provided APIs for working with custom fonts since Windows 7, newer APIs were added in Windows 10 and again in the Windows 10 Creators Update (preview build 15021 or later) that make it easier to implement several of the scenarios mentioned.</span></span> <span data-ttu-id="c7ba8-136">本主題著重于 Windows 10 中提供的 Api。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-136">This topic focuses on APIs available in Window 10.</span></span> <span data-ttu-id="c7ba8-137">對於需要在舊版 Windows 上運作的應用程式，請參閱 [ (Windows 7/8) 的自訂字型集合 ](custom-font-collections.md)。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-137">For applications that need to work on earlier Windows versions, see [Custom Font Collections (Windows 7/8)](custom-font-collections.md).</span></span> 

 

## <a name="summary-of-apis"></a><span data-ttu-id="c7ba8-138">API 的摘要</span><span class="sxs-lookup"><span data-stu-id="c7ba8-138">Summary of APIs</span></span>

<span data-ttu-id="c7ba8-139">本主題著重于下列 Api 所提供的功能：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-139">This topic focuses on functionality provided by the following APIs:</span></span> 

-   <span data-ttu-id="c7ba8-140">[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-140">[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) interface</span></span>
-   <span data-ttu-id="c7ba8-141">[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-141">[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) interface</span></span>
-   <span data-ttu-id="c7ba8-142">[**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-142">[**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) interface</span></span> 
-   <span data-ttu-id="c7ba8-143">[**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-143">[**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) interface</span></span>
-   <span data-ttu-id="c7ba8-144">[**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-144">[**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) interface</span></span>
-   <span data-ttu-id="c7ba8-145">[**IDWriteFactory：： CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 方法</span><span class="sxs-lookup"><span data-stu-id="c7ba8-145">[**IDWriteFactory::CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) method</span></span> 
-   <span data-ttu-id="c7ba8-146">[**IDWriteFactory：： CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) 方法</span><span class="sxs-lookup"><span data-stu-id="c7ba8-146">[**IDWriteFactory::CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) method</span></span> 
-   <span data-ttu-id="c7ba8-147">[**IDWriteFactory3：： CreateFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) 方法</span><span class="sxs-lookup"><span data-stu-id="c7ba8-147">[**IDWriteFactory3::CreateFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) methods</span></span> 
-   <span data-ttu-id="c7ba8-148">[**DWRITE \_字型 \_ 屬性**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 結構</span><span class="sxs-lookup"><span data-stu-id="c7ba8-148">[**DWRITE\_FONT\_PROPERTY**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) structure</span></span> 
-   <span data-ttu-id="c7ba8-149">[**DWRITE \_字型 \_ 屬性 \_ 識別碼**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) 列舉</span><span class="sxs-lookup"><span data-stu-id="c7ba8-149">[**DWRITE\_FONT\_PROPERTY\_ID**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) enumeration</span></span> 
-   <span data-ttu-id="c7ba8-150">[**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-150">[**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) interface</span></span> 
-   <span data-ttu-id="c7ba8-151">[**IDWriteFactory：： RegisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) 方法</span><span class="sxs-lookup"><span data-stu-id="c7ba8-151">[**IDWriteFactory::RegisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) method</span></span> 
-   <span data-ttu-id="c7ba8-152">[**IDWriteFactory：： UnregisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) 方法</span><span class="sxs-lookup"><span data-stu-id="c7ba8-152">[**IDWriteFactory::UnregisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) method</span></span> 
-   <span data-ttu-id="c7ba8-153">[**IDWriteFactory5：： CreateInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) 方法</span><span class="sxs-lookup"><span data-stu-id="c7ba8-153">[**IDWriteFactory5::CreateInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) method</span></span> 
-   <span data-ttu-id="c7ba8-154">[**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-154">[**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) interface</span></span> 
-   <span data-ttu-id="c7ba8-155">[**IDWriteFactory5：： CreateHttpFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) 方法</span><span class="sxs-lookup"><span data-stu-id="c7ba8-155">[**IDWriteFactory5::CreateHttpFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) method</span></span> 
-   <span data-ttu-id="c7ba8-156">[**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-156">[**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) interface</span></span> 
-   <span data-ttu-id="c7ba8-157">[**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-157">[**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) interface</span></span> 
-   <span data-ttu-id="c7ba8-158">[**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-158">[**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) interface</span></span> 
-   <span data-ttu-id="c7ba8-159">[**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-159">[**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) interface</span></span> 
-   <span data-ttu-id="c7ba8-160">[**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-160">[**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) interface</span></span> 
-   <span data-ttu-id="c7ba8-161">[**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 介面</span><span class="sxs-lookup"><span data-stu-id="c7ba8-161">[**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) interface</span></span> 
-   <span data-ttu-id="c7ba8-162">[**IDWriteFactory5：： AnalyzeContainerType**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) 方法</span><span class="sxs-lookup"><span data-stu-id="c7ba8-162">[**IDWriteFactory5::AnalyzeContainerType**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) method</span></span> 
-   <span data-ttu-id="c7ba8-163">[**IDWriteFactory5：： UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) 方法</span><span class="sxs-lookup"><span data-stu-id="c7ba8-163">[**IDWriteFactory5::UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) method</span></span> 

 

## <a name="key-concepts"></a><span data-ttu-id="c7ba8-164">重要概念</span><span class="sxs-lookup"><span data-stu-id="c7ba8-164">Key concepts</span></span>

<span data-ttu-id="c7ba8-165">若要瞭解使用自訂字型的 DirectWrite Api，瞭解這些 Api 基礎的概念模型可能會很有説明。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-165">To understand the DirectWrite APIs for working with custom fonts, it can be helpful to understand the conceptual model that underlies these APIs.</span></span> <span data-ttu-id="c7ba8-166">重要概念將在此說明。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-166">Key concepts will be described here.</span></span> 

<span data-ttu-id="c7ba8-167">當 DirectWrite 進行實際的文字版面配置或轉譯時，它需要存取實際的字型資料。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-167">When DirectWrite does actual text layout or rendering, it needs to access actual font data.</span></span> <span data-ttu-id="c7ba8-168">字型臉部物件會保存實際的字型資料，而這些資料必須存在於本機系統中。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-168">A font face object holds actual font data, which must exist in the local system.</span></span> <span data-ttu-id="c7ba8-169">但是針對其他作業（例如檢查特定字型的可用性或向使用者呈現字型選項），只需要特定字型的參考，而不是實際字型資料本身。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-169">But for other operations, such as checking availability of a particular font, or presenting font choices to a user, all that is needed is a reference to a particular font, not the actual font data itself.</span></span> <span data-ttu-id="c7ba8-170">在 DirectWrite 中，字型參考物件只會包含尋找和具現化字型所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-170">In DirectWrite, a font face reference object holds just the information needed to locate and instantiate a font.</span></span> <span data-ttu-id="c7ba8-171">因為字體臉部參考不會保存實際的資料，所以 DirectWrite 可以處理字型臉部參考，讓實際資料在遠端網路位置，以及實際資料在本機。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-171">Because the font face reference doesn’t hold actual data, DirectWrite can deal with font face references for which actual data is in a remote network location as well as when the actual data is local.</span></span>

<span data-ttu-id="c7ba8-172">字型組是一組字型臉部參考，以及某些基本的參考屬性，可用來參考字型或與其他字型（例如，系列名稱或字型粗細值）進行比較。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-172">A font set is a set of font face references, along with certain basic, informational properties that can be used in referring to the font or in comparing it to other fonts, such as the family name, or a font-weight value.</span></span> <span data-ttu-id="c7ba8-173">各種字型的實際資料可能是本機的，也可能是遠端或某些混合。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-173">The actual data for the various fonts may be local, or it may all be remote, or some mixture.</span></span>

<span data-ttu-id="c7ba8-174">字型組可以用來取得對應的字型集合物件。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-174">A font set can be used to obtain a corresponding font collection object.</span></span> <span data-ttu-id="c7ba8-175">如需詳細資訊，請參閱下方的字型組和字型集合。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-175">See Font sets and font collections below for more details.</span></span> 

<span data-ttu-id="c7ba8-176">IDWriteFontSet 介面所提供的方法，可讓您查詢屬性值（例如系列名稱或字型粗細），或符合特定屬性值的字型臉部參考。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-176">The IDWriteFontSet interface provides methods that allow querying for property values such as family name or font-weight, or for font face references that match particular property values.</span></span> <span data-ttu-id="c7ba8-177">篩選到特定選取專案之後，就可以取得 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) 介面的實例，並使用方法來下載 (如果實際的字型資料目前是遠端) ，以取得可用於版面配置和轉譯的對應 [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) 物件。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-177">After filtering down to a particular selection, an instance of the [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) interface can be obtained, with methods for downloading (if the actual font data is currently remote), for obtaining the corresponding [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) object that can be used for layout and rendering.</span></span> 

<span data-ttu-id="c7ba8-178">IDWriteFontFile 介面會為每個字型或字型臉部參考進行基礎。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-178">The IDWriteFontFile interface underlies each font face or font face reference.</span></span> <span data-ttu-id="c7ba8-179">這代表字型檔案的位置，並有兩個元件：字型檔案載入器和字型檔案索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-179">This represents the location of a font file, and has two components: a font file loader, and a font file key.</span></span> <span data-ttu-id="c7ba8-180">[字型檔案載入器] ([**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) 可用來開啟檔案（如有需要），並傳回具有資料 ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)) 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-180">The font file loader ([**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) is used to open a file if needed, and returns a stream with the data ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)).</span></span> <span data-ttu-id="c7ba8-181">視載入器而定，資料可能位於本機檔案路徑、遠端 URL 或記憶體緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-181">Depending on the loader, the data may be located at a local file path, a remote URL, or in a memory buffer.</span></span> <span data-ttu-id="c7ba8-182">此索引鍵是載入器定義的值，可在載入器內容中唯一識別檔案，讓載入器找出資料並為其建立資料流程。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-182">The key is a loader-defined value that uniquely identifies the file within the loader context, allowing the loader to locate the data and create a stream for it.</span></span> 

<span data-ttu-id="c7ba8-183">您可以輕鬆地將自訂字型加入自訂字型集中，以用於篩選或組織字型資訊，例如建立字型選擇器使用者介面。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-183">Custom fonts can easily be added to a custom font set, which in turn can be used for filtering or organizing font information for purposes such as creating a font-picker user interface.</span></span> <span data-ttu-id="c7ba8-184">字型組也可用來建立用於高階 Api （例如 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 和 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)）的字型集合。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-184">The font set can also be used to create a font collection for use in higher-level APIs like [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="c7ba8-185">[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)介面可以用來建立包含數個自訂字型的自訂字型集。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-185">The [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) interface can be used to create a custom font set that includes several custom fonts.</span></span> <span data-ttu-id="c7ba8-186">它也可以用來建立混合自訂字型和系統提供字型的自訂字型組;或者，將不同來源的字型與實際資料（本機儲存體、遠端 Url 和記憶體）混合。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-186">It can also be used to create a custom font set that mixes custom fonts and system-provided fonts; or that mixes fonts with different sources for the actual data — local storage, remote URLs, and memory.</span></span> 

<span data-ttu-id="c7ba8-187">如前所述，字型臉部參考可能會參考遠端來源的字型資料，但是資料必須是區域，才能取得可用於版面配置和轉譯的字型臉部物件。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-187">As mentioned, a font face reference may refer to font data at a remote source, but the data must be local in order to obtain a font face object that can be used for layout and rendering.</span></span> <span data-ttu-id="c7ba8-188">下載遠端資料是由字型下載佇列所處理。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-188">Downloading of remote data is handled by a font download queue.</span></span> <span data-ttu-id="c7ba8-189">應用程式可以使用 [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 介面將下載遠端字型的要求排入佇列，以起始下載程式，並在下載程式完成時註冊 [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 物件以採取動作。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-189">Apps can use the [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) interface to enqueue requests to download remote fonts to initiate the download process, and to register an [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) object to take action when the download process has completed.</span></span> 

<span data-ttu-id="c7ba8-190">針對此處所述的大部分介面，DirectWrite 提供系統實現。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-190">For most of the interfaces described here, DirectWrite provides system implementations.</span></span> <span data-ttu-id="c7ba8-191">其中一個例外狀況是 [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 介面，應用程式會在本機下載遠端字型時，執行此介面來執行應用程式特定的動作。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-191">The one exception is the [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) interface, which an app implements to take app-specific actions when remote fonts have been downloaded locally.</span></span> <span data-ttu-id="c7ba8-192">應用程式可能會有理由為某些其他介面提供自己的自訂執行，不過這只需要在特定、更先進的案例中使用。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-192">Apps may have reason to provide their own custom implementations for certain other interfaces, though that would only be needed in specific, more advanced scenarios.</span></span> <span data-ttu-id="c7ba8-193">例如，應用程式必須提供 [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 介面的自訂執行，以在使用 WOFF2 容器格式的本機儲存體中處理字型檔案。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-193">For example, an app would need to provide a custom implementation of the [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) interface to handle font files in local storage that use the WOFF2 container format.</span></span> <span data-ttu-id="c7ba8-194">以下將提供其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-194">Additional details will be provided below.</span></span> 

## <a name="fonts-and-font-file-formats"></a><span data-ttu-id="c7ba8-195">字型和字型檔案格式</span><span class="sxs-lookup"><span data-stu-id="c7ba8-195">Fonts and font file formats</span></span>

<span data-ttu-id="c7ba8-196">另一個有助於瞭解的重要概念，就是個別字型臉部和包含它們的字型檔案之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-196">Another key concept that is helpful to understand is the relationship between individual font faces and font files that contain them.</span></span> <span data-ttu-id="c7ba8-197">Ttf 或 otf) 的 OpenType 字型檔案 ( 概念很熟悉。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-197">The idea of an OpenType font file (.ttf or .otf) containing a single font is familiar.</span></span> <span data-ttu-id="c7ba8-198">但 OpenType 字型格式也可讓 OpenType 字型集合 (. simsun18030.ttc 或. otc-n-us-sat-bsa-press) ，也就是包含多個字型的單一檔案。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-198">But the OpenType font format also allows for an OpenType Font Collection (.ttc or .otc), which is a single file that contains multiple fonts.</span></span> <span data-ttu-id="c7ba8-199">OpenType 集合檔案通常用於與緊密相關且對特定字型資料具有相同值的大型字型：藉由將字型合併成單一檔案，可以將通用資料重復資料刪除。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-199">OpenType Collection files are often used for large fonts that are closely related and have identical values for certain font data: by combining the fonts in a single file, the common data can be de-duplicated.</span></span> <span data-ttu-id="c7ba8-200">基於這個理由，字型或字型臉部參考不僅需要參考字型檔案 (或對等的資料來源) ，還必須指定該檔案內的字型索引，因為檔案可能是集合檔案。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-200">For this reason, a font face or font face reference needs to refer not only to a font file (or equivalent data source), but it must also specify a font index within that file, for the general case in which the file may be a Collection file.</span></span> 

<span data-ttu-id="c7ba8-201">針對網路上所使用的字型，字型資料通常會封裝成特定的容器格式 WOFF 或 WOFF2，以提供一些壓縮的字型資料，以及某種程度的保護，以防範字型授權的盜版和違規。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-201">For fonts used on the Web, font data is often packed into certain container formats, WOFF or WOFF2, which provide some compression of the font data and some level of protection against piracy and violation of font licenses.</span></span> <span data-ttu-id="c7ba8-202">功能上，WOFF 或 WOFF2 檔案相當於 OpenType 字型或字型集合檔案，但資料會以不同的格式進行編碼，而這種格式需要先解壓縮才能使用。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-202">Functionally, a WOFF or WOFF2 file is equivalent to an OpenType font or Font Collection file, but the data is encoded in a different format that requires unpacking before it can be used.</span></span> 

<span data-ttu-id="c7ba8-203">某些 DirectWrite Api 可能會處理個別字型的臉部，而其他 Api 則可以處理可能包含包含多個臉部之 OpenType 集合檔案的檔案。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-203">Certain DirectWrite APIs may deal with individual font faces, while other APIs can handle files that might include OpenType Collection files that contain multiple faces.</span></span> <span data-ttu-id="c7ba8-204">同樣地，某些 Api 只會處理未經處理的 OpenType 格式資料，而其他 Api 則可以處理封裝的、WOFF 和 WOFF2 容器格式。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-204">Similarly, certain APIs deal only with raw, OpenType-format data, while other APIs can handle the packed, WOFF and WOFF2 container formats.</span></span> <span data-ttu-id="c7ba8-205">下列討論提供這些詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-205">These details are provided in the discussion below.</span></span> 

## <a name="font-sets-and-font-collections"></a><span data-ttu-id="c7ba8-206">字型組和字型集合</span><span class="sxs-lookup"><span data-stu-id="c7ba8-206">Font sets and font collections</span></span>

<span data-ttu-id="c7ba8-207">某些應用程式可能會實作為使用 [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) 介面的字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-207">Some applications may be implemented to work with fonts using the [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) interface.</span></span> <span data-ttu-id="c7ba8-208">字型集合與字型組之間有直接的對應關係。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-208">There is a direct correspondence between a font collection and a font set.</span></span> <span data-ttu-id="c7ba8-209">每個都可以保存相同的字型，但會將它們呈現給不同的組織。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-209">Each can hold the same fonts, but they present them with a different organization.</span></span> <span data-ttu-id="c7ba8-210">您可以從任何字型集合取得對應的字型集，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-210">From any font collection, a corresponding font set can be obtained, and vice versa.</span></span>

<span data-ttu-id="c7ba8-211">使用多個自訂字型時，最簡單的方式是使用字型組產生器介面來建立自訂字型集，然後在建立字型之後取得字型集合。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-211">When working with a number of custom fonts, it is easiest to use a font set builder interface to create a custom font set, and then obtain a font collection after the font set is created.</span></span> <span data-ttu-id="c7ba8-212">以下將詳細說明建立自訂字型集的程式。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-212">The process for creating a custom font set will be described in detail below.</span></span> <span data-ttu-id="c7ba8-213">若要從字型集取得 [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) 介面，請使用 [**IDWriteFactory3：： CreateFontCollectionFromFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset) 方法。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-213">To obtain an [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) interface from a font set, the [**IDWriteFactory3::CreateFontCollectionFromFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset) method is used.</span></span>

<span data-ttu-id="c7ba8-214">如果應用程式具有集合物件，且需要取得對應的字型集，則可以使用 [**IDWriteFontCollection1：： GetFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) 方法來完成此動作。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-214">If the app has a collection object and needs to obtain a corresponding font set, this can be done using the [**IDWriteFontCollection1::GetFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) method.</span></span> 

## <a name="common-scenarios"></a><span data-ttu-id="c7ba8-215">常見的案例</span><span class="sxs-lookup"><span data-stu-id="c7ba8-215">Common scenarios</span></span>

<span data-ttu-id="c7ba8-216">本節說明一些涉及自訂字型組的最常見案例：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-216">This section describes some of the most common scenarios involving custom font sets:</span></span>

-   <span data-ttu-id="c7ba8-217">在本機檔案系統的路徑上使用任意字型來建立自訂字型集。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-217">Creating a custom font set using arbitrary fonts at paths in the local file system.</span></span>
-   <span data-ttu-id="c7ba8-218">使用已知字型建立自訂字型 (可能與儲存在本機檔案系統中的應用程式) 配套。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-218">Creating a custom font set using known fonts (perhaps bundled with the app) that are stored in the local file system.</span></span>
-   <span data-ttu-id="c7ba8-219">在 Web 上使用已知的遠端字型來建立自訂字型集。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-219">Creating a custom font set using known, remote fonts on the Web.</span></span>
-   <span data-ttu-id="c7ba8-220">使用載入記憶體的字型資料來建立自訂字型集。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-220">Creating a custom font set using font data loaded into memory.</span></span>

<span data-ttu-id="c7ba8-221">這些案例的完整執行是在 [DirectWrite 自訂字型集範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)中提供。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-221">Complete implementations for these scenarios are provided in the [DirectWrite Custom Font Sets sample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/).</span></span> <span data-ttu-id="c7ba8-222">該範例也會說明處理以 WOFF 或 WOFF2 容器格式封裝之字型資料的一個更先進案例，如下所述。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-222">That sample also illustrates one more advanced scenario for handling font data packed in WOFF or WOFF2 container formats, which will be discussed below.</span></span> 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a><span data-ttu-id="c7ba8-223">使用本機檔案系統中的任意字型建立字型組</span><span class="sxs-lookup"><span data-stu-id="c7ba8-223">Creating a font set using arbitrary fonts in the local file system</span></span>

<span data-ttu-id="c7ba8-224">在本機儲存體中處理任意一組字型檔案時， [**IDWriteFontSetBuilder1：： AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 方法很方便，因為在單一呼叫中，它可以處理 Opentype 字型集合檔案內的所有字型，以及 opentype 變數字型的所有實例。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-224">When dealing with an arbitrary set of font files in local storage, the [**IDWriteFontSetBuilder1::AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) method is convenient since, in a single call, it can handle all of the font faces within an OpenType Font Collection file, as well as all instances for an OpenType variable font.</span></span> <span data-ttu-id="c7ba8-225">這項功能可在 Windows 10 Creators Update (preview 組建15021或更新版本的) 中取得，建議您隨時使用。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-225">This is available in the Windows 10 Creators Update (preview build 15021 or later), and is recommended whenever available.</span></span> 

<span data-ttu-id="c7ba8-226">若要使用此方法，請使用下列進程。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-226">To use this method, use the following process.</span></span>

<dl> <span data-ttu-id="c7ba8-227">1. 從建立 <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a> 介面開始：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-227">1. Start by creating the <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a> interface:</span></span> 


```C++
IDWriteFactory5* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
  DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



   
2. <span data-ttu-id="c7ba8-228">使用 factory 來取得 <a href=""></a> [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1)介面：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-228">Use the factory to obtain the <a href=""></a>[**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) interface:</span></span> 


```C++
IDWriteFontSetBuilder1* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
}  
                
```



  
3. <span data-ttu-id="c7ba8-229">針對本機檔案系統中的每個字型檔案，建立參考該檔案的 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) ：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-229">For each font file in the local file system, create an [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) that refers to it:</span></span> 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



   
4. <span data-ttu-id="c7ba8-230">使用 [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile)方法，將 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)物件新增至字型 set builder：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-230">Add the [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) object to the font set builder using the [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) method:</span></span> 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

<span data-ttu-id="c7ba8-231">如果在 [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 的呼叫中指定的檔案路徑參考了支援的 OpenType 檔案以外的內容，則對 [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 的呼叫會傳回錯誤 DWRITE \_ E \_ >fileformat。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-231">If the file path specified in the call to [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) referred to something other than a supported OpenType file, then the call to [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) will return an error, DWRITE\_E\_FILEFORMAT.</span></span>

5. <span data-ttu-id="c7ba8-232">當所有檔案都已新增至字型集建立器之後，即可建立自訂字型組：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-232">After all of the files have been added to the font set builder, the custom font set can be created:</span></span> 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

<span data-ttu-id="c7ba8-233">如果應用程式需要在 Windows 10 Creators Update 之前的 Windows 10 版本上執行，則 AddFontFile 方法將無法使用。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-233">If the app needs to run on Windows 10 versions earlier than the Windows 10 Creators Update, then the AddFontFile method will not be available.</span></span> <span data-ttu-id="c7ba8-234">您可以藉由建立 [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) 介面，然後使用 QueryInterface 來嘗試取得 [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) 介面，來偵測可用性：如果成功，則也會提供 [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 介面和 [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 方法。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-234">Availability can be detected by creating an [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) interface and then using QueryInterface to try to obtain an [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) interface: if this succeeds, then the [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) interface and [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) method will also be available.</span></span>

<span data-ttu-id="c7ba8-235">如果無法使用 AddFontFile 方法，則必須使用 [**IDWriteFontSetBuilder：： AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) 方法來新增個別字型臉部。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-235">If the AddFontFile method is not available, then the [**IDWriteFontSetBuilder::AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) method must be used to add individual font faces.</span></span> <span data-ttu-id="c7ba8-236">若要允許包含多個臉部的 OpenType 字型集合檔案，您可以使用 [**IDWriteFontFile：：分析**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) 方法來判斷檔案中包含的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-236">To allow for OpenType Font Collection files that contain multiple faces, the [**IDWriteFontFile::Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) method can be used to determine the number of faces contained within the file.</span></span> <span data-ttu-id="c7ba8-237">程式如下所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-237">The process is as follows.</span></span>

<dl> <span data-ttu-id="c7ba8-238">1. 從建立 <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a> 介面開始：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-238">1. Start by creating the <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a> interface:</span></span> 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. <span data-ttu-id="c7ba8-239">使用 factory 來取得 [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) 介面：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-239">Use the factory to obtain the [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) interface:</span></span> 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. <span data-ttu-id="c7ba8-240">針對每個字型檔案，建立 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c7ba8-240">For each font file, create an [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), as above:</span></span> 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



<span data-ttu-id="c7ba8-241">我們不會將檔案直接新增至字型組產生器，而是必須判斷臉部數目並建立個別的 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) 物件。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-241">Instead of adding the file directly to the font set builder, we need to determine the number of faces and create individual [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) objects.</span></span>   
4. <span data-ttu-id="c7ba8-242">使用 [ [**分析**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) ] 方法來取得檔案中的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-242">Use the [**Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) method to get the number of faces in the file.</span></span> 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



<span data-ttu-id="c7ba8-243">[**分析**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze)方法也會設定 isSupported 和資料類型參數的值。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-243">The [**Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) method will also set values for the isSupported and fileType parameters.</span></span> <span data-ttu-id="c7ba8-244">如果檔案不是支援的格式，則 isSupported 會是 FALSE，而且可以採取適當的動作，例如忽略檔案。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-244">If the file is not a supported format, then isSupported will be FALSE, and appropriate action, such as ignoring the file, can be taken.</span></span>   
5. <span data-ttu-id="c7ba8-245">對 numberOfFonts 參數中所設定的字型數目進行迴圈。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-245">Loop over the number of fonts set in the numberOfFonts parameter.</span></span> <span data-ttu-id="c7ba8-246">在迴圈中，為每個檔案/索引組建立 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) ，並將其加入至字型 set builder。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-246">Within the loop, create an [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) for each file/index pair, and add that to the font set builder.</span></span> 


```C++
for (uint32_t fontIndex = 0; fontIndex < numberOfFonts; fontIndex++) 
{ 
  IDWriteFontFaceReference* pFontFaceReference;
  hr = pDWriteFactory->CreateFontFaceReference(pFontFile, fontIndex, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);

  if (SUCCEEDED(hr))
  {
    hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference);
  }
} 
```



  
6. <span data-ttu-id="c7ba8-247">將所有臉部都新增至字型組產生器之後，請建立自訂字型集，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-247">After all the faces have been added to the font set builder, create the custom font set, as shown above.</span></span>  
</dl>

<span data-ttu-id="c7ba8-248">您可以設計應用程式，讓它在 Windows 10 Creators Update 上執行時使用慣用的 [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 方法，但在舊版 Windows 10 上執行時，會改回使用 [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) 方法。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-248">An app can be designed so that it will use the preferred [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) method when running on the Windows 10 Creators Update, but fall back to use the [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) method when running on earlier Windows 10 versions.</span></span> <span data-ttu-id="c7ba8-249">如上面所述，測試 [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) 介面的可用性，然後據以進行分支。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-249">Test for availability of the [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) interface, as described above, and then branch accordingly.</span></span> <span data-ttu-id="c7ba8-250">這種方法會在 [DirectWrite 自訂字型組範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)中說明。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-250">This approach is illustrated in the [DirectWrite Custom Font Sets sample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/).</span></span> 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a><span data-ttu-id="c7ba8-251">使用本機檔案系統中的已知字型建立字型組</span><span class="sxs-lookup"><span data-stu-id="c7ba8-251">Creating a font set using known fonts in the local file system</span></span>

<span data-ttu-id="c7ba8-252">如上所述，字型集中的每個字型臉部參考都會與特定的資訊屬性相關聯，例如系列名稱和字型粗細。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-252">As mentioned above, each font face reference in a font set is associated with certain informational properties, such as family name and font weight.</span></span> <span data-ttu-id="c7ba8-253">使用上面所列的 API 呼叫，將自訂字型加入至字型組產生器時，會直接從實際的字型資料取得這些參考屬性，該資料會在新增字型時讀取。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-253">When custom fonts are added to a font set builder using the API calls listed above, these informational properties are obtained directly from the actual font data, which is read as the font is added.</span></span> <span data-ttu-id="c7ba8-254">不過，在某些情況下，如果某個應用程式有另一個字型相關資訊來源，則可能會想要為這些屬性提供自己的自訂值。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-254">In some situations, however, if an app has another source of information about a font, it might wish to provide its own custom values for these properties.</span></span> 

<span data-ttu-id="c7ba8-255">例如，假設應用程式會針對在應用程式內呈現特定使用者介面專案的某些字型進行組合。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-255">As an example of how this might be useful, suppose an app bundles some fonts that are used for presenting particular user-interface elements within the app.</span></span> <span data-ttu-id="c7ba8-256">有時，例如使用新的應用程式版本，應用程式針對這些元素所使用的特定字型可能需要變更。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-256">At times, such as with a new app version, the specific fonts that the app uses for these elements may need to change.</span></span> <span data-ttu-id="c7ba8-257">如果應用程式已對特定字型進行編碼參考，則將某個字型取代為另一個字型需要變更這些參考的每一個字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-257">If the app has encoded references to the specific fonts, then replacement of one font with another will require changing every one of those references.</span></span> <span data-ttu-id="c7ba8-258">相反地，如果應用程式使用自訂屬性，根據所呈現的元素類型或文字來指派功能別名，則會將每個別名對應到一個位置中的特定字型，然後在建立和操作字型的所有內容中使用別名，然後以另一個字型取代字型，只需要變更別名對應至特定字型的一個位置。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-258">Instead, if the app uses custom properties to assign functional aliases based on the type of element or text being rendered, maps each alias to a specific font in one place and then uses the aliases in all the contexts where fonts are created and manipulated, then replacing one font with another requires only changing the one place where the alias is mapped to a specific font.</span></span> 

<span data-ttu-id="c7ba8-259">呼叫 [**IDWriteFontSetBuilder：： AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) 方法時，可以指派資訊屬性的自訂值。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-259">Custom values for informational properties can be assigned when the [**IDWriteFontSetBuilder::AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) method is called.</span></span> <span data-ttu-id="c7ba8-260">執行這項操作的方法如下所示：這可用於任何 Windows 10 版本。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-260">The method for doing this is as follows; this can be used on any Windows 10 version.</span></span> 

<span data-ttu-id="c7ba8-261">如上所示，從取得 [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) 和 [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) 介面開始。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-261">As shown above, start by obtaining the [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) and [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) interfaces.</span></span> <span data-ttu-id="c7ba8-262">針對要新增的每個自訂字型，建立 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-262">For each custom font face to be added, create an [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference), as shown above.</span></span> <span data-ttu-id="c7ba8-263">不過，在步驟5中的迴圈內（如上所示），將這項新增至字型 set builder (中) ，不過，應用程式會定義要使用的自訂屬性值。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-263">Before this is added to the font set builder (within the loop in step 5, shown above), however, the app defines the custom property values to be used.</span></span> 

<span data-ttu-id="c7ba8-264">您可以使用 [**DWRITE \_ 字型 \_ 屬性**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 結構的陣列來定義一組自訂屬性值。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-264">A set of custom property values is defined using an array of [**DWRITE\_FONT\_PROPERTY**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) structures.</span></span> <span data-ttu-id="c7ba8-265">其中每個都會從 [**DWRITE \_ FONT \_ 屬性 \_ 識別碼**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) 列舉識別特定的屬性，以及要使用的對應屬性值。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-265">Each of these identifies a particular property from the [**DWRITE\_FONT\_PROPERTY\_ID**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) enum, and the corresponding property value that is to be used.</span></span>  

<span data-ttu-id="c7ba8-266">請注意，所有的屬性值都會被指派為字串。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-266">Note that all property values are assigned as strings.</span></span> <span data-ttu-id="c7ba8-267">如果稍後可能會向使用者顯示，則可能會設定不同語言的特定屬性替代值，但這並非必要。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-267">If these may later be displayed to users, then alternate values for a given property for different languages may be set, but this is not required.</span></span> <span data-ttu-id="c7ba8-268">另請注意，如果有任何自訂屬性值是由應用程式所設定，則只會在字型集內使用指定的值;DirectWrite 不會直接從字型集合中使用的資訊屬性的字型衍生任何值。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-268">Also note that if any custom property values are set by the app, then only those values that are specified will be used within the Font set; DirectWrite will not derive any values directly from the font for informational properties used in a font set.</span></span> 

<span data-ttu-id="c7ba8-269">下列範例會定義三個資訊屬性的自訂值：系列名稱、完整名稱和字型粗細。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-269">The following example defines custom values for three informational properties: family name, full name, and font weight.</span></span> 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



<span data-ttu-id="c7ba8-270">為字型定義所需的屬性值陣列之後，請呼叫 AddFontFaceRefence，傳遞屬性陣列以及字型臉部參考。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-270">After defining the desired array of property values for a font, make a call to AddFontFaceRefence, passing the property array as well as the font face reference.</span></span> 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

<span data-ttu-id="c7ba8-271">一旦將所有自訂字型新增至字型組產生器，以及其自訂屬性，請建立自訂字型集，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-271">Once all custom font faces have been added to the font set builder, along with their custom properties, create the custom font set, as shown above.</span></span> 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a><span data-ttu-id="c7ba8-272">在 Web 上使用已知的遠端字型來建立自訂字型組</span><span class="sxs-lookup"><span data-stu-id="c7ba8-272">Creating a custom font set using known, remote fonts on the Web</span></span>

<span data-ttu-id="c7ba8-273">自訂屬性對於使用遠端字型而言很重要。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-273">Custom properties are important for working with remote fonts.</span></span> <span data-ttu-id="c7ba8-274">每個字型臉部參考都必須有一些參考屬性來描述字型，並與其他字型區別。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-274">Each font face reference must have some informational properties to characterize the font and distinguish it from other fonts.</span></span> <span data-ttu-id="c7ba8-275">由於遠端字型的字型資料不是本機的，因此 DirectWrite 無法直接從字型資料衍生屬性。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-275">Since the font data for remote fonts is not local, DirectWrite cannot derive properties directly from the font data.</span></span> <span data-ttu-id="c7ba8-276">因此，當您將遠端字型新增至字型組產生器時，必須明確地提供屬性。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-276">Hence, properties must be provided explicitly when adding a remote font to the font set builder.</span></span>

<span data-ttu-id="c7ba8-277">將遠端字型新增至字型組的 API 呼叫順序，類似于前一個案例所述的順序。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-277">The sequence of API calls for adding remote fonts to a font set is similar to the sequence described for the previous scenario.</span></span> <span data-ttu-id="c7ba8-278">但是由於字型資料是遠端的，因此讀取實際字型資料所涉及的作業將會與使用本機儲存體中的檔案時不同。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-278">Since the font data is remote, however, the operations involved for reading the actual font data will be different than when working with files in local storage.</span></span> <span data-ttu-id="c7ba8-279">在此情況下，Windows 10 Creators Update 中新增了較低層級的介面 [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader)。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-279">For this situation, a new lower-level interface, [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader), has been added in the Windows 10 Creators Update.</span></span> 

<span data-ttu-id="c7ba8-280">若要使用遠端字型檔案載入器，它必須先向 DirectWrite factory 註冊。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-280">To use the remote font file loader, it must first be registered with a DirectWrite factory.</span></span> <span data-ttu-id="c7ba8-281">只要使用與其相關聯的字型，應用程式就必須保留載入器。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-281">The loader will need to be held by the app for as long as the fonts associated with it are being used.</span></span> <span data-ttu-id="c7ba8-282">當字型不再使用，且在處理站終結之前的某個時間點，必須將載入器取消註冊。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-282">Once the fonts are no longer in use, and at some point before the factory is destroyed, the loader must be unregistered.</span></span> <span data-ttu-id="c7ba8-283">這可以在擁有載入器物件之類別的函式中完成。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-283">This can be done in the destructor for the class that owns the loader object.</span></span> <span data-ttu-id="c7ba8-284">這些步驟將如下所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-284">These steps will be shown below.</span></span> 

<span data-ttu-id="c7ba8-285">使用遠端字型建立自訂字型集的方法如下所示：這需要 Windows 10 Creators Update。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-285">The method for creating a custom font set using remote fonts is as follows; this requires the Windows 10 Creators Update.</span></span>  

<dl> <span data-ttu-id="c7ba8-286">1. 建立 IDWriteFactory5 介面，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-286">1. Create an IDWriteFactory5 interface, as shown above.</span></span>   
<span data-ttu-id="c7ba8-287">2. 建立 <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a> 介面，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-287">2. Create an <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a> interface, as shown above.</span></span>   
<span data-ttu-id="c7ba8-288">3. 使用 factory 取得 <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-288">3. Use the factory to obtain an <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>.</span></span> 


```C++
IDWriteRemoteFontFileLoader* pRemoteFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateHttpFontFileLoader( 
        /* referrerURL */ nullptr, 
        /* extraHeaders */ nullptr, 
        &pRemoteFontFileLoader 
    ); 
} 
```



<span data-ttu-id="c7ba8-289">這會傳回系統提供的遠端字型檔案載入器介面，此介面能夠處理 HTTP 互動以代表應用程式下載字型資料。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-289">This returns a system-provided implementation of the remote font file loader interface that is able to handle HTTP interactions for downloading font data on behalf of the app.</span></span> <span data-ttu-id="c7ba8-290">如果字型服務或字型來源的服務需要，可以指定查閱者 URL 或額外的標頭。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-290">A referrer URL or extra headers can be specified if required by the font service or services that are the source for the fonts.</span></span>    

> [!IMPORTANT]
> <span data-ttu-id="c7ba8-291">安全性注意事項：嘗試提取遠端字型時，攻擊者可能會偽造將被呼叫的目標伺服器。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-291">Security note: When an attempt is made to fetch a remote font, the potential exists for an attacker to spoof the intended server that will be called.</span></span> <span data-ttu-id="c7ba8-292">在這種情況下，會對攻擊者公開目標和查閱者 Url 和標頭詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-292">In that case, the target and referrer URLs and header details would be disclosed to the attacker.</span></span> <span data-ttu-id="c7ba8-293">應用程式開發人員負責降低此風險。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-293">App developers are responsible for mitigating this risk.</span></span> <span data-ttu-id="c7ba8-294">建議使用 HTTPS 通訊協定，而不是 HTTP。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-294">Use of the HTTPS protocol, rather than HTTP, is recommended.</span></span> 

 

<span data-ttu-id="c7ba8-295">單一遠端字型檔案載入器可以用於多個字型，不過如果字型是從多個具有不同要求者 URL 或額外標頭的服務取得，則可以使用不同的載入器。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-295">A single remote font file loader can be used for multiple fonts, though different loaders can be used if fonts are obtained from multiple services that have different requirements for referrer URL or extra headers.</span></span>   
4. <span data-ttu-id="c7ba8-296">向 factory 註冊遠端字型檔案載入器。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-296">Register the remote font file loader with the factory.</span></span> 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



<span data-ttu-id="c7ba8-297">從現在開始，建立自訂字型組的步驟類似于已知的本機字型檔案所述的步驟，但有兩個重要的例外。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-297">From this point, the steps for creating the custom font set are similar to those described for known, local font files, with two important exceptions.</span></span> <span data-ttu-id="c7ba8-298">首先， [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 物件是使用遠端字型檔案載入器介面來建立，而不是使用 factory。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-298">First, the [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) object is created using the remote font file loader interface rather than using the factory.</span></span> <span data-ttu-id="c7ba8-299">其次，因為字型資料不是在本機，所以無法流量分析方法。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-299">Second, the Analyze method cannot be used since the font data is not local.</span></span> <span data-ttu-id="c7ba8-300">相反地，應用程式必須知道遠端字型檔案是否為 OpenType 字型集合檔案，如果是，則它必須知道所要使用之集合中的字型，以及每個字型的索引。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-300">Instead, the app must know whether the remote font file is an OpenType Font Collection file, and if so, then it must know which of the fonts within the collection it will use, and the index for each.</span></span> <span data-ttu-id="c7ba8-301">因此，其餘步驟如下所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-301">Hence, the remaining steps are as follows.</span></span>   
5. <span data-ttu-id="c7ba8-302">針對每個遠端字型檔案，使用遠端字型檔案載入器介面來建立 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)，並指定存取字型檔案所需的 URL。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-302">For each remote font file, use the remote font file loader interface to create an [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), specifying the URL required to access the font file.</span></span> 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



<span data-ttu-id="c7ba8-303">請注意，您可以在 fontFileUrl 參數中指定完整的 URL，也可以將它分割成基底和相對部分。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-303">Note that the complete URL can be specified in the fontFileUrl parameter, or it can be split into base and relative portions.</span></span> <span data-ttu-id="c7ba8-304">如果指定基底 URL，則 baseUrl 和 fontFileUrl 值的串連必須提供完整的 URL，DirectWrite 將不會提供任何其他分隔符號。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-304">If a base URL is specified, then the concatenation of the baseUrl and fontFileUrl values must provide the complete URL — DirectWrite will not supply any additional delimiter.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="c7ba8-305">安全性/效能附注：嘗試提取遠端字型時，不保證 Windows 會收到伺服器的回應。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-305">Security / performance note: When an attempt is made to fetch a remote font, there is no guarantee that Windows will receive a response from the server.</span></span> <span data-ttu-id="c7ba8-306">在某些情況下，伺服器可能會回應無效相對 URL 的檔案找不到錯誤，但如果收到多個不正確要求，就會停止回應。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-306">In some cases, a server may respond with a file-not-found error for an invalid relative URL, but stop responding if it receives multiple invalid requests.</span></span> <span data-ttu-id="c7ba8-307">如果伺服器沒有回應，Windows 最終將會過期，但如果已起始多個提取，這可能需要幾分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-307">If the server does not respond, Windows will eventually time out, though this may take several minutes if multiple fetches are initiated.</span></span> <span data-ttu-id="c7ba8-308">進行呼叫時，您應該執行哪些動作，以確保 Url 會是有效的。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-308">You should do what you can to ensure that URLs will be valid when calls are made.</span></span> 

 

<span data-ttu-id="c7ba8-309">另請注意，此 URL 可以指向原始的 OpenType 字型檔案 (. ttf、. otf、. simsun18030.ttc、. otc-n-us-sat-bsa-press) ，但它也可以指向 WOFF 或 WOFF2 容器檔案中的字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-309">Also note that the URL can point to a raw OpenType font file (.ttf, .otf, .ttc, .otc), but it can also point to fonts in a WOFF or WOFF2 container file.</span></span> <span data-ttu-id="c7ba8-310">如果參考 WOFF 或 WOFF2 檔案，則遠端字型檔案載入器的 DirectWrite 執行會自動將容器檔案中的字型資料解壓縮。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-310">If a WOFF or WOFF2 file is referenced, then the DirectWrite implementation of the remote font file loader will automatically unpack the font data from the container file.</span></span>   
6. <span data-ttu-id="c7ba8-311">針對要使用的遠端字型檔案中的每個字型臉部索引，建立 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-311">For each font face index within the remote font file that is to be used, create an [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference).</span></span> 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. <span data-ttu-id="c7ba8-312">定義字型的自訂屬性，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-312">Define custom properties for the font face, as shown above.</span></span>   
8. <span data-ttu-id="c7ba8-313">如上面所示，將字型臉部參考連同自訂屬性新增至字型 set builder。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-313">Add the font face reference along with custom properties to the font set builder, as shown above.</span></span>   
9. <span data-ttu-id="c7ba8-314">將所有字型新增至字型組產生器之後，請建立字型集，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-314">After all fonts have been added to the font set builder, create the font set, as shown above.</span></span>   
10. <span data-ttu-id="c7ba8-315">在某個時間點，將不再使用遠端字型時，請取消註冊遠端字型檔案載入器。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-315">At some point when the remote fonts will no longer be used, unregister the remote font file loader.</span></span> 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

<span data-ttu-id="c7ba8-316">建立具有自訂遠端字型的自訂字型之後，字型集會包含遠端字型的參考和參考屬性，但實際的資料仍會在遠端。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-316">Once a custom font set with custom remote fonts is created, the font set contains references and informational properties for the remote fonts, but the actual data is still remote.</span></span> <span data-ttu-id="c7ba8-317">遠端字型的 DirectWrite 支援可讓您在字型集中維護字型臉部參考，並在配置和轉譯中選取要使用的字型，但是實際的資料必須在實際使用時才會下載，例如在執行文字配置時。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-317">DirectWrite support for remote fonts allows a font face reference to be maintained in the font set, and for a font to be selected for use in layout and rendering, but that the actual data is not downloaded until there is an actual need to use it, such as when text layout will be performed.</span></span>  

<span data-ttu-id="c7ba8-318">應用程式可透過要求 DirectWrite 下載字型資料，然後在開始進行字型的任何處理之前等候成功下載的確認，來採取預先的方法。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-318">An app can take an up-front approach by requesting that DirectWrite download the font data and then waiting for confirmation of a successful download before any processing with the font is begun.</span></span> <span data-ttu-id="c7ba8-319">但網路下載意指某些延遲的時間無法預期，而且也不確定成功。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-319">But a network download implies some latency of unpredictable duration, and success is also uncertain.</span></span> <span data-ttu-id="c7ba8-320">基於這個理由，通常最好採用不同的方法，讓版面配置和轉譯一開始先使用已在本機的替代或備用字型，同時要求以平行方式下載所需的遠端字型，然後在所需的字型下載之後更新結果。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-320">For this reason, it will usually be better to take a different approach, allowing layout and rendering to be done initially using alternate or fallback fonts that are already local, while requesting download of the desired, remote font in parallel, and then updating the results once the desired font has been downloaded.</span></span> 

<span data-ttu-id="c7ba8-321">若要要求在使用之前先下載整個字型，可以使用 [**IDWriteFontFaceReference：： EnqueueFontDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) 方法。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-321">To request that the entire font be downloaded before it gets used, the [**IDWriteFontFaceReference::EnqueueFontDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) method can be used.</span></span> <span data-ttu-id="c7ba8-322">如果字型很大，則可能只需要部分資料來處理特定字串。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-322">If the font is very large, only a portion of the data may be needed for processing particular strings.</span></span> <span data-ttu-id="c7ba8-323">DirectWrite 提供其他方法，可用來要求特定內容、 [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) 和 [**EnqueueGlyphDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest)所需的字型資料部分。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-323">DirectWrite provides additional methods that can be used to request portions of the font data needed for particular content, [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) and [**EnqueueGlyphDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest).</span></span>  

<span data-ttu-id="c7ba8-324">假設在應用程式中採取的方法，是讓處理一開始就使用本機、替代或備用字型來完成。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-324">Suppose the approach to be taken in the app is to allow processing to be done initially using local, alternate or fallback fonts.</span></span> <span data-ttu-id="c7ba8-325">IDWriteFontFallback：：[**MapCharacters**](idwritefontfallback-mapcharacters.md) 方法可以用來識別本機的恢復字型，也會自動將要求排入佇列，以下載慣用的字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-325">The IDWriteFontFallback::[**MapCharacters**](idwritefontfallback-mapcharacters.md) method can be used to identify local fallback fonts, and it will also automatically enqueue a request to download the preferred font.</span></span> <span data-ttu-id="c7ba8-326">此外，如果使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ，且版面配置中的部分或全部文字是使用遠端字型參考格式化，則 DirectWrite 會自動使用 **MapCharacters** 方法來取得本機的回復字型，並將下載遠端字型資料的要求排入佇列。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-326">Also, if [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) is used and some or all of the text in the layout is formatted using a remote font reference, then DirectWrite will automatically use the **MapCharacters** method to get local fallback fonts and to enqueue a request to download the remote font data.</span></span> 

<span data-ttu-id="c7ba8-327">DirectWrite 會維護每個處理站的字型下載佇列，而使用上述方法所提出的要求會新增至該佇列。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-327">DirectWrite maintains a font download queue for each factory, and the requests made using the methods mentioned above get added to that queue.</span></span> <span data-ttu-id="c7ba8-328">您可以使用 [**IDWriteFactory3：： GetFontDownloadQueue**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) 方法來取得字型下載佇列。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-328">The font download queue can be obtained using the [**IDWriteFactory3::GetFontDownloadQueue**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) method.</span></span> 

<span data-ttu-id="c7ba8-329">如果已建立下載要求，但字型資料已在本機，則會導致無法執行的作業：不會將任何專案新增至下載佇列。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-329">If a download request is made but the font data is already local, this will result in a no-op: Nothing will be added to the download queue.</span></span> <span data-ttu-id="c7ba8-330">應用程式可以藉由呼叫 [**IDWriteFontDownloadQueue：： IsEmpty**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) 方法，檢查佇列是否為空的，或是否有擱置中的下載要求。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-330">An app can check whether the queue is empty or there are pending download requests by calling the [**IDWriteFontDownloadQueue::IsEmpty**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) method.</span></span> 

<span data-ttu-id="c7ba8-331">將遠端字型要求新增至佇列之後，必須起始下載程式。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-331">After remote font requests have been added to the queue, the download process must be initiated.</span></span> <span data-ttu-id="c7ba8-332">在 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)中使用遠端字型時，會在應用程式呼叫強制版面配置或轉譯作業的 **IDWriteTextLayout** 方法（例如 GetLineMetrics 或 Draw 方法）時自動起始下載。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-332">When remote fonts are used in [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout), the download will be initiated automatically when the app calls **IDWriteTextLayout** methods that force layout or rendering operations, such as the GetLineMetrics or Draw methods.</span></span> <span data-ttu-id="c7ba8-333">在其他情況下，應用程式必須藉由呼叫 [**IDWriteFontDownloadQueue：： BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload)來直接起始下載。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-333">In other scenarios, the app must initiate the download directly by calling [**IDWriteFontDownloadQueue::BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload).</span></span>  

<span data-ttu-id="c7ba8-334">當下載完成時，應用程式會由應用程式採取適當的動作（繼續進行暫止的作業），或一開始使用回復字型完成的重複作業。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-334">When a download is completed, it will be up to the app to take appropriate actions — proceeding with pending operations, or repeating operations that were done initially with fallback fonts.</span></span> <span data-ttu-id="c7ba8-335"> (如果使用 DirectWrite 的文字版面配置，則可以使用 [**IDWriteTextLayout3：： InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) 清除使用回復字型計算的暫存結果。 ) 為了讓應用程式在下載程式完成時收到通知，並採取適當的動作，應用程式必須提供 [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 介面的執行，並將其傳遞至 BeginDownload 呼叫。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-335">(If DirectWrite’s text layout is being used, then [**IDWriteTextLayout3::InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) can be used to clear the temporary results computed using fallback fonts.) In order for the app to be notified when the download process has completed and to take appropriate actions, the app must provide an implementation of the [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) interface, and pass this into the BeginDownload call.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="c7ba8-336">安全性/效能附注：嘗試提取遠端字型時，不保證 Windows 會收到伺服器的回應。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-336">Security / performance note: When an attempt is made to fetch a remote font, there is no guarantee that Windows will receive a response from the server.</span></span> <span data-ttu-id="c7ba8-337">如果伺服器沒有回應，Windows 最終將會出現時間，但如果有多個遠端字型正在提取但失敗，可能需要幾分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-337">If the server does not respond, Windows will eventually time out, though this may take several minutes if multiple remote fonts are being fetched but failing.</span></span> <span data-ttu-id="c7ba8-338">BeginDownload 呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-338">The BeginDownload call will return immediately.</span></span> <span data-ttu-id="c7ba8-339">應用程式不應該在等候 IDWriteFontDownloadListener 時封鎖 UI [**：:D 的 ownloadcompleted**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-339">Apps should not block UI while waiting for [**IDWriteFontDownloadListener::DownloadCompleted**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) to be called.</span></span> 

 

<span data-ttu-id="c7ba8-340">您可以在 [DirectWrite 自訂字型組範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)和 [DirectWrite 可下載字型範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont)中，看到這些與 DirectWrite 的字型下載佇列和 [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener)介面互動的範例。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-340">Sample implementations of these interactions with DirectWrite’s font download queue and of the [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) interface can be seen in the [DirectWrite Custom Font Sets sample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/), and also in the [DirectWrite Downloadable Fonts sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont).</span></span> 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a><span data-ttu-id="c7ba8-341">使用載入至記憶體的字型資料來建立自訂字型組</span><span class="sxs-lookup"><span data-stu-id="c7ba8-341">Creating a custom font set using font data loaded into memory</span></span>

<span data-ttu-id="c7ba8-342">就像從字型檔案讀取資料的低層級作業不同于本機磁片上的檔案與 Web 上的遠端檔案不同，將字型資料載入記憶體緩衝區同樣也是如此。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-342">Just as the low-level operations for reading data from a font file are different for files on a local disk versus remote files on the Web, the same is also true for font data loaded into a memory buffer.</span></span> <span data-ttu-id="c7ba8-343">Windows 10 Creators Update 的 [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader)中加入了新的低層級介面，以處理記憶體中的字型資料。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-343">A new low-level interface for handling in-memory font data has been added in the Windows 10 Creators Update, [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader).</span></span> 

<span data-ttu-id="c7ba8-344">如同遠端字型檔案載入器，記憶體中的字型檔案載入器必須先向 DirectWrite factory 註冊。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-344">As with a remote font file loader, an in-memory font file loader must first be registered with a DirectWrite factory.</span></span> <span data-ttu-id="c7ba8-345">只要使用與其相關聯的字型，應用程式就必須保留載入器。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-345">The loader will need to be held by the app for as long as the fonts associated with it are being used.</span></span> <span data-ttu-id="c7ba8-346">當字型不再使用，且在處理站終結之前的某個時間點，必須將載入器取消註冊。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-346">Once the fonts are no longer in use, and at some point before the factory is destroyed, the loader must be unregistered.</span></span> <span data-ttu-id="c7ba8-347">這可以在擁有載入器物件之類別的函式中完成。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-347">This can be done in the destructor for the class that owns the loader object.</span></span> <span data-ttu-id="c7ba8-348">這些步驟將如下所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-348">These steps will be shown below.</span></span> 

<span data-ttu-id="c7ba8-349">如果應用程式具有資料所代表字型字型的個別相關資訊，則可以將個別字型臉部參考新增至字型集產生器，並指定自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-349">If the app has separate information about the font faces represented by the data, it can add individual font face references to a font set builder with custom properties specified.</span></span> <span data-ttu-id="c7ba8-350">不過，由於字型資料位於本機記憶體中，因此不需要這樣做;DirectWrite 將能夠直接讀取資料，以衍生屬性值。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-350">Since the font data is in local memory, however, this is not required; DirectWrite will be able to read the data directly to derive the property values.</span></span> 

<span data-ttu-id="c7ba8-351">DirectWrite 假設字型資料是原始的 OpenType 格式，相當於 OpenType 檔案 (. ttf、otf、simsun18030.ttc、otc-n-us-sat-bsa-press) ，但在記憶體中，而不是在磁片上。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-351">DirectWrite assumes the font data is in raw, OpenType format, equivalent to an OpenType file (.ttf, .otf, .ttc, .otc), but in memory rather than on disk.</span></span> <span data-ttu-id="c7ba8-352">資料不能是 WOFF 或 WOFF2 容器格式。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-352">The data cannot be in a WOFF or WOFF2 container format.</span></span> <span data-ttu-id="c7ba8-353">資料可以表示 OpenType 字型集合。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-353">The data can represent an OpenType Font Collection.</span></span> <span data-ttu-id="c7ba8-354">如果未使用自訂屬性，則可以使用 [**IDWriteFontSetBuilder1：： AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 方法，在單一呼叫中將所有字型臉部新增至資料。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-354">If custom properties are not being used, then the [**IDWriteFontSetBuilder1::AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) method can be used to add all font faces in the data in a single call.</span></span> 

<span data-ttu-id="c7ba8-355">記憶體內部案例的重要考慮是資料的存留期。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-355">An important consideration for the in-memory scenario is the lifetime of the data.</span></span> <span data-ttu-id="c7ba8-356">如果提供緩衝區的指標給 DirectWrite，而沒有明確指出有擁有者，則 DirectWrite 會將資料的複本複製到它所擁有的新記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-356">If a pointer to the buffer is provided to DirectWrite without a clear indication that there is an owner, then DirectWrite will make a copy of the data into a new memory buffer that it will own.</span></span> <span data-ttu-id="c7ba8-357">為了避免複製資料和額外的記憶體配置，應用程式可以傳遞可執行 IUnknown 的資料擁有者物件，並擁有包含字型資料的記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-357">To avoid copying of data and additional memory allocation, the app can pass a data-owner object that implements IUnknown, and that owns the memory buffer containing the font data.</span></span> <span data-ttu-id="c7ba8-358">藉由執行這個介面，DirectWrite 可以新增至物件的參考計數，藉此確保擁有資料的存留期。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-358">By implementing this interface, DirectWrite can add to the ref count of the object, thereby ensuring the lifetime of the owned data.</span></span> 

<span data-ttu-id="c7ba8-359">使用記憶體中字型資料建立自訂字型集的方法如下所示：這需要 Windows 10 Creators Update。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-359">The method for creating a custom font set using in-memory font data is as follows; this requires the Windows 10 Creators Update.</span></span> <span data-ttu-id="c7ba8-360">這會假設是由應用程式所執行的資料擁有者物件，它會執行 IUnknown，而且也有傳回記憶體緩衝區指標和緩衝區大小的方法。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-360">This will assume an app-implemented data-owner object, that implements IUnknown and also has methods that return a pointer to the memory buffer and the size of the buffer.</span></span> 

<dl> <span data-ttu-id="c7ba8-361">1. 建立 IDWriteFactory5 介面，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-361">1. Create an IDWriteFactory5 interface, as shown above.</span></span>  
<span data-ttu-id="c7ba8-362">2. 建立 [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 介面，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-362">2. Create an [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) interface, as shown above.</span></span>  
<span data-ttu-id="c7ba8-363">3. 使用 factory 取得 IDWriteInMemoryFontFileLoader。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-363">3. Use the factory to obtain an IDWriteInMemoryFontFileLoader.</span></span> 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



<span data-ttu-id="c7ba8-364">這會傳回系統提供的記憶體中字型檔案載入器介面的執行。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-364">This returns a system-provided implementation of the in-memory font file loader interface.</span></span>   
4. <span data-ttu-id="c7ba8-365">使用 factory 註冊記憶體中的字型檔案載入器。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-365">Register the in-memory font file loader with the factory.</span></span> 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. <span data-ttu-id="c7ba8-366">針對每個記憶體中的字型檔案，使用記憶體中的字型檔案載入器來建立 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-366">For each in-memory font file, use the in-memory font file loader to create an [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile).</span></span> 


```C++
IDWriteFontFile* pFontFile; 
hr = pInMemoryFontFileLoader->CreateInMemoryFontFileReference( 
    pDWriteFactory, 
    pFontDataOwner->fontData /* returns void* */, 
    pFontDataOwner->fontDataSize /* returns UINT32 */, 
    pFontDataOwner /* ownerObject, owns the memory with font data and implements IUknown */, 
    &pFontFile 
); 
```



   
6. <span data-ttu-id="c7ba8-367">使用 [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile)方法將 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)物件新增至字型 set builder，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-367">Add the [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) object to the font set builder using the [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) method, as shown above.</span></span>  <span data-ttu-id="c7ba8-368">如果有需要，應用程式可以改為根據 **IDWriteFontFile** 建立個別的 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)物件，並選擇性地定義每個字型臉部參考的自訂屬性，然後使用 [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))方法將自訂屬性的字型臉部參考新增至字型集，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-368">If there is a need, the app can instead create individual [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) objects based on the **IDWriteFontFile**, optionally define custom properties for each font face reference, and then add the font face reference with custom properties to the font set using the [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) method, as shown above.</span></span>   
7. <span data-ttu-id="c7ba8-369">將所有字型新增至字型組產生器之後，請建立自訂字型組，如上所示。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-369">After all fonts have been added to the font set builder, create the custom font set, as shown above.</span></span>   
8. <span data-ttu-id="c7ba8-370">在某個時間點，將無法再使用記憶體中的字型時，請取消註冊記憶體中的字型檔案載入器。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-370">At some point when the in-memory fonts will no longer be used, unregister the in-memory font file loader.</span></span> 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a><span data-ttu-id="c7ba8-371">進階案例</span><span class="sxs-lookup"><span data-stu-id="c7ba8-371">Advanced scenarios</span></span>

<span data-ttu-id="c7ba8-372">有些應用程式可能會有特殊需求，需要比上述程式更先進的處理。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-372">Some apps may have special requirements that require more advanced processing than is described above.</span></span> 

### <a name="combining-font-sets"></a><span data-ttu-id="c7ba8-373">組合字型組</span><span class="sxs-lookup"><span data-stu-id="c7ba8-373">Combining font sets</span></span>

<span data-ttu-id="c7ba8-374">有些應用程式可能需要建立一組字型，其包含其他字型集中的一些專案組合。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-374">Some apps may need to create a font set that comprises some combination of items from other font sets.</span></span> <span data-ttu-id="c7ba8-375">例如，應用程式可能會想要建立一組字型，將安裝在系統上的所有字型與選取的自訂字型合併，或是將符合特定準則的已安裝字型與其他字型合併。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-375">For example, an app may want to create a font set that combines all the fonts installed on the system with a selection of custom fonts, or that combines installed fonts matching certain criteria with other fonts.</span></span> <span data-ttu-id="c7ba8-376">DirectWrite 具有 Api，可支援操作和組合字型組。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-376">DirectWrite has APIs to support manipulation and combining of font sets.</span></span> 

<span data-ttu-id="c7ba8-377">若要結合兩個或多個字型集， [**IDWriteFontSetBuilder：： AddFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) 方法會加入指定字型中的所有字型，以在單一呼叫中新增至字型組產生器。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-377">To combine two or more font sets, the [**IDWriteFontSetBuilder::AddFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) method adds all of the fonts in given font set to be added to a font set builder in a single call.</span></span> <span data-ttu-id="c7ba8-378">如果新的字型集中只需要現有字型的特定字型，則可以使用 [**IDWriteFontSet：： GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) 方法來衍生已篩選成隻包含符合指定屬性之字型的新字型集物件。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-378">If only certain fonts from an existing font set are wanted in the new font set, the [**IDWriteFontSet::GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) method can be used to derive a new font set object that has been filtered to include only fonts matching specified properties.</span></span> <span data-ttu-id="c7ba8-379">這些方法可讓您輕鬆地建立自訂字型組，以結合兩個或多個現有字型集中的字型。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-379">These methods provide an easy way to create a custom font set combining fonts from two or more existing font sets</span></span> 

### <a name="using-local-woff-or-woff2-font-data"></a><span data-ttu-id="c7ba8-380">使用本機 WOFF 或 WOFF2 字型資料</span><span class="sxs-lookup"><span data-stu-id="c7ba8-380">Using local WOFF or WOFF2 font data</span></span>

<span data-ttu-id="c7ba8-381">如果應用程式在本機檔案系統或記憶體緩衝區中有字型檔案，但它們使用 WOFF 或 WOFF2 容器格式，則 DirectWrite (Windows 10 Creator Update 或更新版本) 會提供解除封裝容器格式的方法， [**IDWriteFactory5：： UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile)會傳回 [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-381">If an app has font files in the local file system or in a memory buffer, but they use the WOFF or WOFF2 container formats, DirectWrite (Windows 10 Creator Update or later) provides a method for unpacking the container format, [**IDWriteFactory5::UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile), which returns an [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream).</span></span> 

<span data-ttu-id="c7ba8-382">不過，應用程式需要一種方式，讓 [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 進入字型檔案載入器物件。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-382">However, the app will need a way to get the [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) into a font file loader object.</span></span> <span data-ttu-id="c7ba8-383">其中一個方法是建立包裝資料流程的自訂 [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 執行。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-383">One way to do this is to create a custom [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) implementation that wraps the stream.</span></span> <span data-ttu-id="c7ba8-384">和其他字型檔案載入器一樣，這必須在使用之前註冊，並在處理站超出範圍之前取消註冊。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-384">As with other font file loaders, this must be registered before use, and unregistered before the factory goes out of scope.</span></span>  

<span data-ttu-id="c7ba8-385">如果自訂載入器也將與原始 (搭配使用，而不是封裝) 字型檔案，則應用程式也需要提供 [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 介面的自訂執行，以處理這些檔案。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-385">If the custom loader will also be used with raw (not packed) font files, then the app would also need to provide a custom implementation of the [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) interface for handling those files.</span></span> <span data-ttu-id="c7ba8-386">不過，使用上述 Api 來處理原始字型檔案的方法更簡單。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-386">There are easier ways that use APIs discussed above for handling raw font files, however.</span></span> <span data-ttu-id="c7ba8-387">針對壓縮的字型檔案使用不同的程式碼路徑，而不是原始字型檔案，就可以避免自訂資料流程執行的需求。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-387">The need for a custom stream implementation could be avoided by using separate code paths for packed font files versus raw font files.</span></span> 

<span data-ttu-id="c7ba8-388">建立自訂字型檔案載入器物件之後，會依應用程式特定的方式將壓縮的字型檔案資料新增至載入器。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-388">After a custom font file loader object is created, the packed font file data is added to the loader by app-specific means.</span></span> <span data-ttu-id="c7ba8-389">載入器可以處理多個字型檔案，其中每個都是使用 DirectWrite 不透明的應用程式定義索引鍵來識別。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-389">The loader can handle multiple font files, each of which is identified using an app-defined key that is opaque to DirectWrite.</span></span> <span data-ttu-id="c7ba8-390">將壓縮的字型檔案新增至載入器之後，會使用 [**IDWriteFactory：： CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) 方法，根據指定索引鍵所識別之字型資料的載入器來取得 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-390">After a packed font file has been added to the loader, the [**IDWriteFactory::CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) method is used to obtain an [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) based on that loader for the font data identified by a given key.</span></span>  

<span data-ttu-id="c7ba8-391">當字型新增至載入器時，可以將字型資料的實際解除封裝完成，但是也可以在 [**IDWriteFontFileLoader：： CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) 方法中處理，DirectWrite 將會在第一次需要讀取字型資料時呼叫。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-391">The actual unpacking of the font data can be done as fonts are added to the loader, but can also be handled in the [**IDWriteFontFileLoader::CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) method, which DirectWrite will call when it first needs to read the font data.</span></span> 

<span data-ttu-id="c7ba8-392">建立 IDWriteFontFile 物件之後，將字型新增至自訂字型集的其餘步驟將會如上所述。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-392">After an IDWriteFontFile object has been created, remaining steps for adding the fonts to a custom font set will be as described above.</span></span> 

<span data-ttu-id="c7ba8-393">使用此方法的實作為 [DirectWrite 自訂字型組範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)中的說明。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-393">An implementation using this approach is illustrated in the [DirectWrite Custom Font Sets sample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/).</span></span> 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a><span data-ttu-id="c7ba8-394">使用 DirectWrite 遠端字型機制搭配自訂的低層級網路執行</span><span class="sxs-lookup"><span data-stu-id="c7ba8-394">Using DirectWrite remote font mechanisms with custom low-level network implementation</span></span>

<span data-ttu-id="c7ba8-395">處理遠端字型的 DirectWrite 機制可以分為較高層級的機制，包括包含遠端字型字型參考的字型、檢查字型資料的位置，以及管理字型下載要求的佇列，以及處理實際下載的較低層級機制。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-395">The DirectWrite mechanisms for handling remote fonts can be divided into higher-level mechanisms — having font sets that include font face references for remote fonts, checking locality of the font data, and managing the queue for font download requests — and the lower-level mechanisms that handle actual download.</span></span> <span data-ttu-id="c7ba8-396">有些應用程式可能會想要利用較高層級的遠端字型機制，但也需要自訂網路互動，例如使用 HTTP 以外的通訊協定與伺服器通訊。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-396">Some apps may want to utilize the higher-level remote font mechanisms, but also require custom network interactions, such as communicating with servers using protocols other than HTTP.</span></span> 

<span data-ttu-id="c7ba8-397">在這種情況下，應用程式必須建立 [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 介面的自訂執行，以所需的方式與其他較低層級的介面互動。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-397">For this situation, an app will need to create a custom implementation of the [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) interface that interacts with other lower-level interfaces in the required ways.</span></span> <span data-ttu-id="c7ba8-398">應用程式也必須提供這些較低層級介面的自訂執行： [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)和 [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult)。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-398">The app will also need to provide custom implementations of these lower-level interfaces: [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream), and [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult).</span></span> <span data-ttu-id="c7ba8-399">這三個介面具有回呼方法，DirectWrite 會在下載作業期間呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-399">These three interfaces have callback methods that DirectWrite will call during download operations.</span></span> 

<span data-ttu-id="c7ba8-400">當呼叫 [**IDWriteFontDownloadQueue：： BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) 時，DirectWrite 會對遠端字型檔案載入器進行有關資料位置的查詢，並且會要求遠端資料流。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-400">When [**IDWriteFontDownloadQueue::BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) is called, DirectWrite will make queries to the remote font file loader about locality of the data, and will request the remote stream.</span></span> <span data-ttu-id="c7ba8-401">如果資料不是本機資料，則會呼叫資料流程的 BeginDownload 方法。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-401">If data is not local, then it will call the stream’s BeginDownload method.</span></span> <span data-ttu-id="c7ba8-402">資料流程的執行不應該在該呼叫上封鎖，但應該立即傳回，傳回提供等候控制碼的 [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 物件，DirectWrite 會使用此物件來等候非同步下載作業。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-402">The stream implementation should not block on that call, but should immediately return, passing back an [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) object that provides the wait handle DirectWrite will use to wait on the asynchronous download operation.</span></span> <span data-ttu-id="c7ba8-403">自訂資料流程的執行負責處理遠端通訊。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-403">The custom stream implementation is responsible for handling the remote communication.</span></span> <span data-ttu-id="c7ba8-404">當完成事件發生時，DirectWrite 會呼叫 [**IDWriteAsyncResult：： GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) 來判斷作業的結果。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-404">When the completion event has occurred, then DirectWrite will call [**IDWriteAsyncResult::GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) to determine the result of the operation.</span></span> <span data-ttu-id="c7ba8-405">如果結果成功，則預期針對下載範圍的後續 ReadFragment 呼叫串流將會成功。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-405">If the result is successful, then it’s expected that subsequent ReadFragment calls to the stream for the downloaded ranges will succeed.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="c7ba8-406">安全性/效能附注：嘗試提取遠端字型時，可能是因為攻擊者可能會偽造要呼叫的目標伺服器，或是伺服器可能沒有回應。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-406">Security / performance note: When an attempt is made to fetch a remote font, the potential exists in general for an attacker to spoof the intended server being called, or that the server may not respond.</span></span> <span data-ttu-id="c7ba8-407">如果您正在執行自訂網路互動，您可能會比處理協力廠商伺服器更能掌控緩和措施。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-407">If you are implementing custom network interactions, you may have greater control over mitigations than when dealing with third-party servers.</span></span> <span data-ttu-id="c7ba8-408">不過，您必須考慮適當的緩和措施，以避免資訊洩漏或阻斷服務。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-408">However, it is up to you to consider appropriate mitigations to avoid information disclosure or denial of service.</span></span> <span data-ttu-id="c7ba8-409">建議使用安全的通訊協定，例如 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-409">Secure protocols such as HTTPS are recommended.</span></span> <span data-ttu-id="c7ba8-410">此外，您應該以一些時間來建立，讓傳回給 DirectWrite 的事件控制碼最後會被設定。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-410">Also, you should build in some timeout so that the event handle returned to DirectWrite does eventually get set.</span></span> 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a><span data-ttu-id="c7ba8-411">舊版 Windows 上的支援案例</span><span class="sxs-lookup"><span data-stu-id="c7ba8-411">Supporting scenarios on earlier Windows versions</span></span>

<span data-ttu-id="c7ba8-412">舊版 Windows 上的 DirectWrite 可支援所述的案例，但在應用程式的元件上需要更多自訂的程式，使用 Windows 10 之前可用的較有限 Api。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-412">The scenarios that have been described can be supported in DirectWrite on earlier versions of Windows, but would require much more custom implementation on the part of the app using the more limited APIs that were available prior to Windows 10.</span></span> <span data-ttu-id="c7ba8-413">如需詳細資訊，請參閱 [自訂字型集合 (Windows 7/8) ](custom-font-collections.md)。</span><span class="sxs-lookup"><span data-stu-id="c7ba8-413">For more information, see [Custom Font Collections (Windows 7/8)](custom-font-collections.md).</span></span>

 

 