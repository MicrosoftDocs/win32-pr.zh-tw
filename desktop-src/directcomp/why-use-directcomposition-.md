---
title: 為何要使用 DirectComposition
description: 本主題說明 Microsoft DirectComposition 的功能和優點。
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- 為何要使用 DirectComposition
- 使用 DirectComposition 的原因
- DirectComposition 功能和優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965252"
---
# <a name="why-use-directcomposition"></a><span data-ttu-id="494a9-106">為何要使用 DirectComposition？</span><span class="sxs-lookup"><span data-stu-id="494a9-106">Why use DirectComposition?</span></span>

> [!NOTE]
> <span data-ttu-id="494a9-107">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="494a9-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="494a9-108">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="494a9-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="494a9-109">本主題說明 Microsoft DirectComposition 的功能和優點。</span><span class="sxs-lookup"><span data-stu-id="494a9-109">This topic describes the capabilities and benefits of Microsoft DirectComposition.</span></span> <span data-ttu-id="494a9-110">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="494a9-110">It contains the following sections:</span></span>

-   [<span data-ttu-id="494a9-111">建立視覺效果吸引人的使用者介面</span><span class="sxs-lookup"><span data-stu-id="494a9-111">Create a visually engaging user interface</span></span>](#create-a-visually-engaging-user-interface)
-   [<span data-ttu-id="494a9-112">為您的應用程式啟用豐富且流暢的動畫</span><span class="sxs-lookup"><span data-stu-id="494a9-112">Enable rich, smooth animations for your application</span></span>](#enable-rich-smooth-animations-for-your-application)
-   [<span data-ttu-id="494a9-113">結合各種來源的點陣圖</span><span class="sxs-lookup"><span data-stu-id="494a9-113">Combine bitmaps from a variety of sources</span></span>](#combine-bitmaps-from-a-variety-of-sources)
-   [<span data-ttu-id="494a9-114">透過與 DWM 整合來節省記憶體</span><span class="sxs-lookup"><span data-stu-id="494a9-114">Memory savings though integration with DWM</span></span>](#memory-savings-though-integration-with-dwm)
-   [<span data-ttu-id="494a9-115">保留您現有的內容</span><span class="sxs-lookup"><span data-stu-id="494a9-115">Keep what you already have</span></span>](#keep-what-you-already-have)
-   [<span data-ttu-id="494a9-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="494a9-116">Related topics</span></span>](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a><span data-ttu-id="494a9-117">建立視覺效果吸引人的使用者介面</span><span class="sxs-lookup"><span data-stu-id="494a9-117">Create a visually engaging user interface</span></span>

<span data-ttu-id="494a9-118">DirectComposition 可讓您結合和製作 [*視覺效果*](directcomposition-glossary.md) ，為您的 Windows 應用程式建立視覺互動的 UI。</span><span class="sxs-lookup"><span data-stu-id="494a9-118">DirectComposition lets you combine and animate [*visuals*](directcomposition-glossary.md) to create a visually engaging UI for your Windows-based applications.</span></span> <span data-ttu-id="494a9-119">它可協助讓您的應用程式具有獨特的外觀和風格，以建立與其他應用程式分開設定的身分識別。</span><span class="sxs-lookup"><span data-stu-id="494a9-119">It can help give your application a unique look and feel, establishing an identity that sets it apart from other applications.</span></span>

<span data-ttu-id="494a9-120">DirectComposition 也可以讓您的應用程式更容易使用。</span><span class="sxs-lookup"><span data-stu-id="494a9-120">DirectComposition can also help make your applications easier to use.</span></span> <span data-ttu-id="494a9-121">例如，您可使用視覺層來建立視覺提示和動畫螢幕轉換，而後者可顯示螢幕上項目之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="494a9-121">For example, you can use it to create visual cues and animated screen transitions that show relationships among items on the screen.</span></span>

## <a name="enable-rich-smooth-animations-for-your-application"></a><span data-ttu-id="494a9-122">為您的應用程式啟用豐富且流暢的動畫</span><span class="sxs-lookup"><span data-stu-id="494a9-122">Enable rich, smooth animations for your application</span></span>

<span data-ttu-id="494a9-123">DirectComposition 是一種高效能點陣圖組合引擎，其使用硬體加速圖形來達到高畫面播放速率，以平滑且一致地移動、滾動和複雜內容的動畫。</span><span class="sxs-lookup"><span data-stu-id="494a9-123">DirectComposition is a high-performance bitmap composition engine that uses hardware-accelerated graphics to achieve high frame rates, resulting in smooth and consistent panning, scrolling, and animations of complex content.</span></span> <span data-ttu-id="494a9-124">因為它的運作方式與用來呈現應用程式 UI 的執行緒不同，所以 DirectComposition 絕對不能「使」 UI 執行緒，也不會干擾應用程式繪製其 UI 元素的能力。</span><span class="sxs-lookup"><span data-stu-id="494a9-124">Because it operates on a dedicated thread that is separate from the thread used to render the application UI, DirectComposition can never "starve" the UI thread or interfere with the application's ability to draw its UI elements.</span></span>

## <a name="combine-bitmaps-from-a-variety-of-sources"></a><span data-ttu-id="494a9-125">結合各種來源的點陣圖</span><span class="sxs-lookup"><span data-stu-id="494a9-125">Combine bitmaps from a variety of sources</span></span>

<span data-ttu-id="494a9-126">許多以 Windows 為基礎的應用程式都有一個由各種不同圖形架構所建立的元素所組成的 UI。</span><span class="sxs-lookup"><span data-stu-id="494a9-126">Many Windows-based applications have a UI that consists of elements created by a variety of different graphics frameworks.</span></span> <span data-ttu-id="494a9-127">例如，應用程式可能會使用 Windows Forms 來建立狀態列、Windows 圖形裝置介面 (GDI) 來建立主視窗內容、Microsoft DirectX for Graphics 內容等等。</span><span class="sxs-lookup"><span data-stu-id="494a9-127">For example, an application might use Windows Forms to create a status bar, Windows Graphics Device Interface (GDI) to create the main window content, Microsoft DirectX for graphics content, and so on.</span></span> <span data-ttu-id="494a9-128">DirectComposition 可讓您結合各種圖形架構的內容，並將其轉譯為相同的最上層或子視窗，而不需要擔心來自不同 framework 的內容重迭時，會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="494a9-128">DirectComposition enables you to combine the content from a variety of graphics frameworks and have it render to the same top-level or child window without needing to worry about what happens if the content from different frameworks overlaps.</span></span>

## <a name="memory-savings-though-integration-with-dwm"></a><span data-ttu-id="494a9-129">透過與 DWM 整合來節省記憶體</span><span class="sxs-lookup"><span data-stu-id="494a9-129">Memory savings though integration with DWM</span></span>

<span data-ttu-id="494a9-130">DirectComposition 所建立的組合和動畫會傳遞至 Windows 的內建元件，稱為 [桌面視窗管理員 (DWM) ](/windows/desktop/dwm/dwm-overview) 以轉譯至螢幕。</span><span class="sxs-lookup"><span data-stu-id="494a9-130">Compositions and animations created by DirectComposition are passed to a built-in component of Windows called [Desktop Window Manager (DWM)](/windows/desktop/dwm/dwm-overview) for rendering to the screen.</span></span> <span data-ttu-id="494a9-131">因此，電腦上不需要任何特殊的呈現元件或 UI 架構。</span><span class="sxs-lookup"><span data-stu-id="494a9-131">Therefore, no special rendering components or UI frameworks are required on the computer.</span></span>

## <a name="keep-what-you-already-have"></a><span data-ttu-id="494a9-132">保留您現有的內容</span><span class="sxs-lookup"><span data-stu-id="494a9-132">Keep what you already have</span></span>

<span data-ttu-id="494a9-133">以 Windows 為基礎的現有應用程式中的 UI 程式碼代表大量投資。</span><span class="sxs-lookup"><span data-stu-id="494a9-133">The UI code in an existing Windows-based application represents a significant investment.</span></span> <span data-ttu-id="494a9-134">在大部分的情況下，DirectComposition 可讓您撰寫現有的 UI 內容，並製作其動畫。</span><span class="sxs-lookup"><span data-stu-id="494a9-134">For the most part, DirectComposition lets you compose and animate your existing UI content.</span></span> <span data-ttu-id="494a9-135">這表示您可以使用 DirectComposition 對您的應用程式 UI 進行重大更新和增強，而不需要對現有的 UI 程式碼基底進行大量變更。</span><span class="sxs-lookup"><span data-stu-id="494a9-135">This means you can use DirectComposition to make significant updates and enhancements to your application UI without needing to make extensive changes to your existing UI code base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="494a9-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="494a9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="494a9-137">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="494a9-137">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 