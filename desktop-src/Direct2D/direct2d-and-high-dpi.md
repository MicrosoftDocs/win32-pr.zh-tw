---
title: Direct2D 和高 DPI
description: 描述 Direct2D 如何容納高 DPI 顯示器。
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D，高 DPI
- 高 DPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933558"
---
# <a name="direct2d-and-high-dpi"></a><span data-ttu-id="acbab-105">Direct2D 和高 DPI</span><span class="sxs-lookup"><span data-stu-id="acbab-105">Direct2D and High-DPI</span></span>

<span data-ttu-id="acbab-106">撰寫 DPI 感知的應用程式是讓使用者介面 (UI 的關鍵，) 在各式各樣的高 DPI 顯示器設定中的外觀一致。</span><span class="sxs-lookup"><span data-stu-id="acbab-106">Writing a DPI-aware application is the key to making a user interface (UI) look consistently good across a wide variety of high-DPI display settings.</span></span> <span data-ttu-id="acbab-107">非 DPI 感知但在高 DPI 顯示器設定上執行的應用程式，可能會受到許多視覺構件的影響，包括不正確地調整 UI 元素、剪下文字和模糊影像。</span><span class="sxs-lookup"><span data-stu-id="acbab-107">An application that is not DPI-aware but is running on a high-DPI display setting can suffer from many visual artifacts, including incorrect scaling of UI elements, clipped text, and blurry images.</span></span> <span data-ttu-id="acbab-108">藉由在應用程式中加入支援 DPI 感知的功能，您可以更容易預測應用程式的 UI，讓使用者更具視覺效果且更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="acbab-108">By adding support in your application for DPI-awareness, you make the presentation of your application's UI more predictable, making it more visually appealing and easier to read for users.</span></span> <span data-ttu-id="acbab-109">幸運的是，Direct2D 可讓您更輕鬆地撰寫在高 DPI 中運作正常的應用程式。</span><span class="sxs-lookup"><span data-stu-id="acbab-109">Fortunately, Direct2D makes it easier than ever to write applications that work well in high-DPI.</span></span> <span data-ttu-id="acbab-110">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="acbab-110">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="acbab-111">Direct2D 中的高 DPI 支援</span><span class="sxs-lookup"><span data-stu-id="acbab-111">High-DPI Support in Direct2D</span></span>](#high-dpi-support-in-direct2d)
-   [<span data-ttu-id="acbab-112">Windows 8 和高 DPI</span><span class="sxs-lookup"><span data-stu-id="acbab-112">Windows 8 and High-DPI</span></span>](#windows-8-and-high-dpi)
-   [<span data-ttu-id="acbab-113">什麼是 DIP？</span><span class="sxs-lookup"><span data-stu-id="acbab-113">What is a DIP?</span></span>](#what-is-a-dip)
-   [<span data-ttu-id="acbab-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="acbab-114">Related topics</span></span>](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a><span data-ttu-id="acbab-115">Direct2D 中的高 DPI 支援</span><span class="sxs-lookup"><span data-stu-id="acbab-115">High-DPI Support in Direct2D</span></span>

<span data-ttu-id="acbab-116">Direct2D 提供下列功能來處理高 DPI 案例：</span><span class="sxs-lookup"><span data-stu-id="acbab-116">Direct2D provides the following features for working with high-DPI scenarios:</span></span>

-   <span data-ttu-id="acbab-117">只要應用程式資訊清單指出應用程式正確處理 DPI，就會在建立視窗化轉譯目標時自動接受系統 DPI。</span><span class="sxs-lookup"><span data-stu-id="acbab-117">It automatically honors the system DPI when creating a windowed render target, so long as the application manifest indicates that the application handles DPI correctly.</span></span> <span data-ttu-id="acbab-118"> (需如何宣告應用程式為 DPI 感知的詳細資訊，請參閱 [如何確保您的應用程式在高 DPI 顯示器上正確顯示](how-to--size-a-window-properly-for-high-dpi-displays.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="acbab-118">(For information on how to declare that your application is DPI-aware, see [How to Ensure That Your Application Displays Properly on High-DPI Displays](how-to--size-a-window-properly-for-high-dpi-displays.md).)</span></span>
-   <span data-ttu-id="acbab-119">它會以 Dip (與裝置無關的圖元為單位來表示座標) ，可讓應用程式在 DPI 設定變更時自動調整。</span><span class="sxs-lookup"><span data-stu-id="acbab-119">It expresses coordinates in DIPs (Device Independent Pixels), which enables the application to scale automatically when the DPI setting changes.</span></span>
-   <span data-ttu-id="acbab-120">它可讓點陣圖具有 DPI，並藉由將 DPI 納入考慮，以正確地調整它們的規模。</span><span class="sxs-lookup"><span data-stu-id="acbab-120">It enables bitmaps to have a DPI and correctly scales them by taking the DPI into account.</span></span> <span data-ttu-id="acbab-121">這項功能也可以用來維護不同解析度的圖示。</span><span class="sxs-lookup"><span data-stu-id="acbab-121">This feature can also be used to maintain icons at different resolutions.</span></span>
-   <span data-ttu-id="acbab-122">它會以 Dip 表示大部分的資源，讓資源自動獨立于解析度之外。</span><span class="sxs-lookup"><span data-stu-id="acbab-122">It expresses most resources in DIPs, which makes the resources automatically independent of resolution.</span></span>
-   <span data-ttu-id="acbab-123">它使用浮點座標空間和消除鋸齒，因此任何內容都可以調整成任意的 DPI。</span><span class="sxs-lookup"><span data-stu-id="acbab-123">It uses a floating-point coordinate space and antialiasing, so any content can be scaled to any arbitrary DPI.</span></span>

<span data-ttu-id="acbab-124">Direct2D 圖形管線的設計目的是要從 96 DPI 調整為1200DPI。</span><span class="sxs-lookup"><span data-stu-id="acbab-124">The Direct2D graphics pipeline is designed to scale from 96 DPI to 1200DPI.</span></span>

## <a name="windows-8-and-high-dpi"></a><span data-ttu-id="acbab-125">Windows 8 和高 DPI</span><span class="sxs-lookup"><span data-stu-id="acbab-125">Windows 8 and High-DPI</span></span>

<span data-ttu-id="acbab-126">從 Windows 8 開始，有高 DPI 支援的額外功能。</span><span class="sxs-lookup"><span data-stu-id="acbab-126">Starting with Windows 8, there are additional features for high-DPI support.</span></span>

<span data-ttu-id="acbab-127">如果裝置內容 DPI 夠高，Direct2D 會變更它用來啟用文字垂直消除鋸齒的閾值。</span><span class="sxs-lookup"><span data-stu-id="acbab-127">If the device context DPI is high enough, Direct2D changes the threshold it uses to enable vertical antialiasing of text.</span></span> <span data-ttu-id="acbab-128">這會導致在高 DPI 顯示器上更快速地呈現文字。</span><span class="sxs-lookup"><span data-stu-id="acbab-128">This results in faster text rendering on high-DPI displays.</span></span> <span data-ttu-id="acbab-129">此外，您也可以使用 [**ID2D1DeviceCoNtext：： SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) 方法，將單元模式切換成圖元而不是 dip。</span><span class="sxs-lookup"><span data-stu-id="acbab-129">Additionally, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span> <span data-ttu-id="acbab-130">如果您將單位模式設定為圖元，並將裝置內容 DPI 設定為螢幕 DPI，則仍會啟用優化。</span><span class="sxs-lookup"><span data-stu-id="acbab-130">If you set the unit mode to pixels and the device context DPI to the screen DPI, the optimization is still enabled.</span></span>

## <a name="what-is-a-dip"></a><span data-ttu-id="acbab-131">什麼是 DIP？</span><span class="sxs-lookup"><span data-stu-id="acbab-131">What is a DIP?</span></span>

<span data-ttu-id="acbab-132">與裝置無關的圖元 (DIP) 是一個邏輯圖元，會透過純量（DPI）對應至實體裝置的圖元。</span><span class="sxs-lookup"><span data-stu-id="acbab-132">A device independent pixel (DIP) is a logical pixel that maps to the pixels of the physical device through a scalar, the DPI.</span></span> <span data-ttu-id="acbab-133">DPI 代表每英寸的點，其中點代表實體裝置圖元。</span><span class="sxs-lookup"><span data-stu-id="acbab-133">DPI stands for dots per inch, where a dot represents a physical device pixel.</span></span> <span data-ttu-id="acbab-134"> (的命名法來自列印，其中的點是列印程式可產生) 的最小筆墨點。</span><span class="sxs-lookup"><span data-stu-id="acbab-134">(The nomenclature comes from printing, where dots are the smallest ink dot that a printing process can produce).</span></span> <span data-ttu-id="acbab-135">因為標準監視器是用來在每個英寸各有96的點，所以 DPI 96 表示與裝置無關的圖元 (或 DIP) 對應1:1 與實體圖元。</span><span class="sxs-lookup"><span data-stu-id="acbab-135">Because a standard monitor used to have 96 dots per inch, a DPI of 96 meant that a device independent pixel (or DIP) mapped 1:1 with a physical pixel.</span></span> <span data-ttu-id="acbab-136">例如，如果 DPI 為 96 \* 2 = 192，則單一 DIP 會包含兩個實體圖元。</span><span class="sxs-lookup"><span data-stu-id="acbab-136">For example, if the DPI were 96\*2 = 192, then a single DIP would encompass two physical pixels.</span></span>

<span data-ttu-id="acbab-137">應用程式不一定會正確處理此調整的原因有很多;最簡單的原因之一是它需要額外的工作，才能在轉譯時探索和使用此純量值。</span><span class="sxs-lookup"><span data-stu-id="acbab-137">There are many reasons why applications don't necessarily handle this scaling correctly; one of the simplest reasons is that it requires extra work to discover and use this scalar value when rendering.</span></span> <span data-ttu-id="acbab-138">在 Direct2D 中，預設會套用調整。</span><span class="sxs-lookup"><span data-stu-id="acbab-138">In Direct2D, the scaling is applied by default.</span></span> <span data-ttu-id="acbab-139">由於這項對應，實體裝置圖元可能會以小數 DIP 座標為單位，這是 Direct2D 使用浮點座標空間的原因之一。</span><span class="sxs-lookup"><span data-stu-id="acbab-139">Because of this mapping, physical device pixels might end up at fractional DIP coordinates, which is one of the reasons why Direct2D uses a floating-point coordinate space.</span></span>

<dl> <span data-ttu-id="acbab-140">實體圖元 = (dip × DPI) /96</span><span class="sxs-lookup"><span data-stu-id="acbab-140">physical pixel = (dip × DPI) / 96</span></span>  
</dl>

<span data-ttu-id="acbab-141">若要將實體圖元轉換為 DIP，請使用下列公式：</span><span class="sxs-lookup"><span data-stu-id="acbab-141">To convert a physical pixel to a DIP, use this formula:</span></span>

<dl> <span data-ttu-id="acbab-142">dip = (實體圖元× 96) /DPI</span><span class="sxs-lookup"><span data-stu-id="acbab-142">dip = (physical pixel × 96) / DPI</span></span>  
</dl>

> [!Note]
>
> <span data-ttu-id="acbab-143">從 Windows 8 開始，您可以使用 [**ID2D1DeviceCoNtext：： SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) 方法，將單元模式切換成圖元而不是 dip。</span><span class="sxs-lookup"><span data-stu-id="acbab-143">Starting with Windows 8, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="acbab-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="acbab-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acbab-145">如何確保您的應用程式在高 DPI 顯示器上正確顯示</span><span class="sxs-lookup"><span data-stu-id="acbab-145">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 