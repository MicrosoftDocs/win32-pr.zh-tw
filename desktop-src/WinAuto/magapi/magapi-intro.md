---
title: 放大 API 總覽
description: 本主題說明放大 API，並說明如何在應用程式中使用它。
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- 放大
- 螢幕縮放比例的應用程式
- 放大
- 自訂影像處理
- Magnification.dll
- 建立放大鏡控制項
- 選擇性放大
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966042"
---
# <a name="magnification-api-overview"></a><span data-ttu-id="57df7-110">放大 API 總覽</span><span class="sxs-lookup"><span data-stu-id="57df7-110">Magnification API Overview</span></span>

<span data-ttu-id="57df7-111">放大 API 可讓輔助技術廠商開發在 Microsoft Windows 上執行的螢幕縮放應用程式。</span><span class="sxs-lookup"><span data-stu-id="57df7-111">The Magnification API enables assistive technology vendors to develop screen magnification applications that run on Microsoft Windows.</span></span> <span data-ttu-id="57df7-112">本主題說明放大 API，並說明如何在應用程式中使用它。</span><span class="sxs-lookup"><span data-stu-id="57df7-112">This topic describes the Magnification API and explains how to use it in an application.</span></span> <span data-ttu-id="57df7-113">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="57df7-113">It contains the following sections:</span></span>

- [<span data-ttu-id="57df7-114">快速入門</span><span class="sxs-lookup"><span data-stu-id="57df7-114">Getting Started</span></span>](#getting-started)
- [<span data-ttu-id="57df7-115">基本概念</span><span class="sxs-lookup"><span data-stu-id="57df7-115">Basic Concepts</span></span>](#basic-concepts)
  - [<span data-ttu-id="57df7-116">放大鏡的類型</span><span class="sxs-lookup"><span data-stu-id="57df7-116">Types of Magnifiers</span></span>](#types-of-magnifiers)
  - [<span data-ttu-id="57df7-117">放大因數</span><span class="sxs-lookup"><span data-stu-id="57df7-117">Magnification Factor</span></span>](#magnification-factor)
  - [<span data-ttu-id="57df7-118">色彩效果</span><span class="sxs-lookup"><span data-stu-id="57df7-118">Color Effects</span></span>](#color-effects)
  - [<span data-ttu-id="57df7-119">來源矩形</span><span class="sxs-lookup"><span data-stu-id="57df7-119">Source Rectangle</span></span>](#source-rectangle)
  - [<span data-ttu-id="57df7-120">篩選清單</span><span class="sxs-lookup"><span data-stu-id="57df7-120">Filter List</span></span>](#filter-list)
  - [<span data-ttu-id="57df7-121">輸入轉換</span><span class="sxs-lookup"><span data-stu-id="57df7-121">Input Transform</span></span>](#input-transform)
  - [<span data-ttu-id="57df7-122">系統資料指標</span><span class="sxs-lookup"><span data-stu-id="57df7-122">System Cursor</span></span>](#system-cursor)
- [<span data-ttu-id="57df7-123">初始化放大鏡執行時間程式庫</span><span class="sxs-lookup"><span data-stu-id="57df7-123">Initializing the Magnifier Run-time Library</span></span>](#initializing-the-magnifier-run-time-library)
- [<span data-ttu-id="57df7-124">使用 Full-Screen 放大鏡</span><span class="sxs-lookup"><span data-stu-id="57df7-124">Using the Full-Screen Magnifier</span></span>](#using-the-full-screen-magnifier)
- [<span data-ttu-id="57df7-125">使用放大鏡控制項</span><span class="sxs-lookup"><span data-stu-id="57df7-125">Using the Magnifier Control</span></span>](#using-the-magnifier-control)
  - [<span data-ttu-id="57df7-126">建立放大鏡控制項</span><span class="sxs-lookup"><span data-stu-id="57df7-126">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
  - [<span data-ttu-id="57df7-127">初始化控制項</span><span class="sxs-lookup"><span data-stu-id="57df7-127">Initializing the Control</span></span>](#initializing-the-control)
  - [<span data-ttu-id="57df7-128">設定來源矩形</span><span class="sxs-lookup"><span data-stu-id="57df7-128">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
  - [<span data-ttu-id="57df7-129">套用色彩效果</span><span class="sxs-lookup"><span data-stu-id="57df7-129">Applying Color Effects</span></span>](#applying-color-effects)
  - [<span data-ttu-id="57df7-130">選擇性放大</span><span class="sxs-lookup"><span data-stu-id="57df7-130">Selective Magnification</span></span>](#selective-magnification)
- [<span data-ttu-id="57df7-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="57df7-131">Related topics</span></span>](#related-topics)

## <a name="getting-started"></a><span data-ttu-id="57df7-132">開始使用</span><span class="sxs-lookup"><span data-stu-id="57df7-132">Getting Started</span></span>

<span data-ttu-id="57df7-133">Windows Vista 和更新版本的作業系統支援放大 API 的原始版本。</span><span class="sxs-lookup"><span data-stu-id="57df7-133">The original release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="57df7-134">在 Windows 8 和更新版本上，API 支援其他功能，包括全螢幕縮放比例，以及設定放大的系統游標可見度。</span><span class="sxs-lookup"><span data-stu-id="57df7-134">On Windows 8 and later, the API supports additional features, including full-screen magnification and setting the visibility of the magnified system cursor.</span></span>

<span data-ttu-id="57df7-135">放大 API 的支援是由 Magnification.dll 提供。</span><span class="sxs-lookup"><span data-stu-id="57df7-135">Support for the Magnification API is provided by Magnification.dll.</span></span> <span data-ttu-id="57df7-136">若要編譯您的應用程式，請包含放大和連結至放大程式庫。</span><span class="sxs-lookup"><span data-stu-id="57df7-136">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="57df7-137">在 WOW64 下不支援放大 API;也就是說，32位的放大鏡應用程式將無法在64位 Windows 上正確執行。</span><span class="sxs-lookup"><span data-stu-id="57df7-137">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="basic-concepts"></a><span data-ttu-id="57df7-138">基本概念</span><span class="sxs-lookup"><span data-stu-id="57df7-138">Basic Concepts</span></span>

<span data-ttu-id="57df7-139">本節說明放大 API 所依據的基本概念。</span><span class="sxs-lookup"><span data-stu-id="57df7-139">This section describes the fundamental concepts that the magnification API is based on.</span></span> <span data-ttu-id="57df7-140">其中包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="57df7-140">It contains the following parts:</span></span>

- [<span data-ttu-id="57df7-141">放大鏡的類型</span><span class="sxs-lookup"><span data-stu-id="57df7-141">Types of Magnifiers</span></span>](#types-of-magnifiers)
- [<span data-ttu-id="57df7-142">放大因數</span><span class="sxs-lookup"><span data-stu-id="57df7-142">Magnification Factor</span></span>](#magnification-factor)
- [<span data-ttu-id="57df7-143">色彩效果</span><span class="sxs-lookup"><span data-stu-id="57df7-143">Color Effects</span></span>](#color-effects)
- [<span data-ttu-id="57df7-144">來源矩形</span><span class="sxs-lookup"><span data-stu-id="57df7-144">Source Rectangle</span></span>](#source-rectangle)
- [<span data-ttu-id="57df7-145">篩選清單</span><span class="sxs-lookup"><span data-stu-id="57df7-145">Filter List</span></span>](#filter-list)
- [<span data-ttu-id="57df7-146">輸入轉換</span><span class="sxs-lookup"><span data-stu-id="57df7-146">Input Transform</span></span>](#input-transform)
- [<span data-ttu-id="57df7-147">系統資料指標</span><span class="sxs-lookup"><span data-stu-id="57df7-147">System Cursor</span></span>](#system-cursor)

### <a name="types-of-magnifiers"></a><span data-ttu-id="57df7-148">放大鏡的類型</span><span class="sxs-lookup"><span data-stu-id="57df7-148">Types of Magnifiers</span></span>

<span data-ttu-id="57df7-149">此 API 支援兩種類型的放大鏡，也就是 *全螢幕放大鏡* 和 *放大鏡控制項*。</span><span class="sxs-lookup"><span data-stu-id="57df7-149">The API supports two types of magnifiers, the *full-screen magnifier* and the *magnifier control*.</span></span> <span data-ttu-id="57df7-150">全螢幕放大鏡會放大整個畫面的內容，而放大鏡控制項會放大螢幕上特定區域的內容，並在視窗中顯示內容。</span><span class="sxs-lookup"><span data-stu-id="57df7-150">The full-screen magnifier magnifies the content of the entire screen, while the magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="57df7-151">針對這兩種放大鏡，影像和文字都會放大，而且兩者都可讓您控制縮放量。</span><span class="sxs-lookup"><span data-stu-id="57df7-151">For both magnifiers, images and text are magnified, and both enable you to control the amount of magnification.</span></span> <span data-ttu-id="57df7-152">您也可以將色彩效果套用至放大的螢幕內容，以便更輕鬆地查看具有色彩缺陷的人員，或需要色彩有更多或更少對比的人員。</span><span class="sxs-lookup"><span data-stu-id="57df7-152">You can also apply color effects to the magnified screen content, making it easier to see for people who have color deficiencies or need colors that have more or less contrast.</span></span>

> [!Important]  
> <span data-ttu-id="57df7-153">放大鏡控制項 API 適用于 Windows Vista 和更新版本的作業系統，而全螢幕放大鏡 API 僅適用于 Windows 8 和更新版本的作業系統。</span><span class="sxs-lookup"><span data-stu-id="57df7-153">The magnifier control API is available on Windows Vista and later operating systems, while the full-screen magnifier API is available only on Windows 8 and later operating systems.</span></span>

### <a name="magnification-factor"></a><span data-ttu-id="57df7-154">放大因數</span><span class="sxs-lookup"><span data-stu-id="57df7-154">Magnification Factor</span></span>

<span data-ttu-id="57df7-155">全螢幕放大鏡和放大鏡控制項都套用縮放轉換來放大螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="57df7-155">Both the full-screen magnifier and the magnifier control apply a scale transformation to magnify screen content.</span></span> <span data-ttu-id="57df7-156">調整規模轉換所套用的放大量稱為「 *縮放比例因數*」。</span><span class="sxs-lookup"><span data-stu-id="57df7-156">The amount of magnification applied by the scale transformation is called the *magnification factor*.</span></span> <span data-ttu-id="57df7-157">它是以浮點數表示，其中1.0 對應到無縮放比例，而較大的值則會產生相對應的放大量。</span><span class="sxs-lookup"><span data-stu-id="57df7-157">It is expressed as a floating-point value where 1.0 corresponds to no magnification, and larger values result in a corresponding amount of magnification.</span></span> <span data-ttu-id="57df7-158">例如，值為1.5 時，會放大螢幕內容50%。</span><span class="sxs-lookup"><span data-stu-id="57df7-158">For example, a value of 1.5 makes the screen content 50 percent larger.</span></span> <span data-ttu-id="57df7-159">小於1.0 的放大因數無效。</span><span class="sxs-lookup"><span data-stu-id="57df7-159">A magnification factor less than 1.0 is not valid.</span></span>

### <a name="color-effects"></a><span data-ttu-id="57df7-160">色彩效果</span><span class="sxs-lookup"><span data-stu-id="57df7-160">Color Effects</span></span>

<span data-ttu-id="57df7-161">色彩效果的達成方式是將5到5的色彩轉換矩陣套用至放大螢幕內容的色彩。</span><span class="sxs-lookup"><span data-stu-id="57df7-161">Color effects are achieved by applying a 5-by-5 color transformation matrix to the colors of the magnified screen content.</span></span> <span data-ttu-id="57df7-162">矩陣會決定內容之紅色、藍色、綠色和 Alpha 元件的濃度。</span><span class="sxs-lookup"><span data-stu-id="57df7-162">The matrix determines the intensities of the red, blue, green, and alpha components of the content.</span></span> <span data-ttu-id="57df7-163">如需詳細資訊，請參閱在 Windows GDI + 檔中 [使用色彩矩陣轉換單一色彩](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) 。</span><span class="sxs-lookup"><span data-stu-id="57df7-163">For more information, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the Windows GDI+ documentation.</span></span>

### <a name="source-rectangle"></a><span data-ttu-id="57df7-164">來源矩形</span><span class="sxs-lookup"><span data-stu-id="57df7-164">Source Rectangle</span></span>

<span data-ttu-id="57df7-165">全螢幕放大鏡會將縮放轉換和色彩轉換套用至整個畫面。</span><span class="sxs-lookup"><span data-stu-id="57df7-165">The full-screen magnifier applies the scale transformation and color transformation to the entire screen.</span></span> <span data-ttu-id="57df7-166">另一方面，放大鏡控制項會將螢幕的區域（稱為 *來源矩形*）複製到螢幕點陣圖。</span><span class="sxs-lookup"><span data-stu-id="57df7-166">The magnifier control, on the other hand, copies an area of the screen, called the *source rectangle*, to an off-screen bitmap.</span></span> <span data-ttu-id="57df7-167">接下來，控制項會將縮放轉換和色彩轉換（如果有的話）套用至非螢幕點陣圖。</span><span class="sxs-lookup"><span data-stu-id="57df7-167">Next, the control applies the scale transformation and the color transformation, if any, to the off-screen bitmap.</span></span> <span data-ttu-id="57df7-168">最後，控制項會在 [放大鏡控制] 視窗中顯示縮放和色彩轉換的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="57df7-168">Finally, the control displays the scaled and color-transformed bitmap in the magnifier control window.</span></span>

### <a name="filter-list"></a><span data-ttu-id="57df7-169">篩選清單</span><span class="sxs-lookup"><span data-stu-id="57df7-169">Filter List</span></span>

<span data-ttu-id="57df7-170">根據預設，「放大鏡」控制項會放大指定來源矩形中的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="57df7-170">By default, the magnifier control magnifies all windows in the specified source rectangle.</span></span> <span data-ttu-id="57df7-171">不過，藉由提供視窗控制碼的 *篩選清單* ，您可以控制哪些視窗包含在放大的內容中，而不是。</span><span class="sxs-lookup"><span data-stu-id="57df7-171">However, by providing a *filter list* of window handles, you can control which windows are included in the magnified content, and which are not.</span></span> <span data-ttu-id="57df7-172">如需詳細資訊，請參閱 [選擇性放大](#selective-magnification)。</span><span class="sxs-lookup"><span data-stu-id="57df7-172">For more information, see [Selective Magnification](#selective-magnification).</span></span>

<span data-ttu-id="57df7-173">全螢幕放大鏡不支援篩選清單;它一律會放大螢幕上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="57df7-173">The full-screen magnifier does not support a filter list; it always magnifies all windows on the screen.</span></span>

### <a name="input-transform"></a><span data-ttu-id="57df7-174">輸入轉換</span><span class="sxs-lookup"><span data-stu-id="57df7-174">Input Transform</span></span>

<span data-ttu-id="57df7-175">一般來說，使用者畫筆或觸控輸入的放大螢幕內容會「隱藏」。</span><span class="sxs-lookup"><span data-stu-id="57df7-175">Normally, magnified screen content is "invisible" to user pen or touch input.</span></span> <span data-ttu-id="57df7-176">例如，如果使用者按下控制項的放大影像，則系統不一定會將輸入傳遞給控制項。</span><span class="sxs-lookup"><span data-stu-id="57df7-176">For example, if the user taps the magnified image of a control, the system does not necessarily pass the input to the control.</span></span> <span data-ttu-id="57df7-177">相反地，如果有任何) 位於 unmagnified 桌面上的點擊螢幕座標，系統就會將輸入傳遞到 (的任何專案。</span><span class="sxs-lookup"><span data-stu-id="57df7-177">Instead, the system passes the input to whatever item (if any) resides at the tapped screen coordinates on the unmagnified desktop.</span></span> <span data-ttu-id="57df7-178">[**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform)函式可讓您指定 *輸入轉換*，將放大螢幕內容的座標空間對應到實際的 (unmagnified) 螢幕座標空間。</span><span class="sxs-lookup"><span data-stu-id="57df7-178">The [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) function enables you to specify an *input transformation* that maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space.</span></span> <span data-ttu-id="57df7-179">這可讓系統將在放大螢幕內容中輸入的畫筆或觸控輸入，傳遞至畫面上正確的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="57df7-179">This enables the system to pass pen or touch input that is entered in magnified screen content, to the correct UI element on the screen.</span></span>

> [!Note]  
> <span data-ttu-id="57df7-180">呼叫進程必須具有 UIAccess 許可權才能設定輸入轉換。</span><span class="sxs-lookup"><span data-stu-id="57df7-180">The calling process must have UIAccess privileges to set the input transform.</span></span> <span data-ttu-id="57df7-181">如需詳細資訊，請參閱 [消費者介面自動化安全性考慮](../uiauto-securityoverview.md) 和 [/MANIFESTUAC (在資訊清單) 中內嵌 UAC 資訊 ](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest)。</span><span class="sxs-lookup"><span data-stu-id="57df7-181">For more information, see [UI Automation Security Considerations](../uiauto-securityoverview.md) and [/MANIFESTUAC (Embeds UAC information in manifest)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span></span>

### <a name="system-cursor"></a><span data-ttu-id="57df7-182">系統資料指標</span><span class="sxs-lookup"><span data-stu-id="57df7-182">System Cursor</span></span>

<span data-ttu-id="57df7-183">[**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor)函數可讓您顯示或隱藏系統資料指標。</span><span class="sxs-lookup"><span data-stu-id="57df7-183">The [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function enables you to show or hide the system cursor.</span></span> <span data-ttu-id="57df7-184">如果您在全螢幕放大鏡為使用中時顯示系統游標，系統游標一律會與其余的螢幕內容一同放大。</span><span class="sxs-lookup"><span data-stu-id="57df7-184">If you show the system cursor when the full-screen magnifier is active, the system cursor is always magnified along with the rest of the screen content.</span></span> <span data-ttu-id="57df7-185">如果您在全螢幕放大鏡處於作用中狀態時隱藏系統游標，則完全不會顯示系統游標。</span><span class="sxs-lookup"><span data-stu-id="57df7-185">If you hide the system cursor when the full-screen magnifier is active, the system cursor is not visible at all.</span></span>

<span data-ttu-id="57df7-186">使用 [放大鏡] 控制項， [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) 函式會顯示或隱藏 unmagnified 系統資料指標，但不會影響放大的系統資料指標。</span><span class="sxs-lookup"><span data-stu-id="57df7-186">With the magnifier control, the [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function shows or hides the unmagnified system cursor, but has no effect on the magnified system cursor.</span></span> <span data-ttu-id="57df7-187">放大的系統游標可見度取決於放大鏡控制項是否有 [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="57df7-187">The visibility of the magnified system cursor depends on whether the magnifier control has the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style.</span></span> <span data-ttu-id="57df7-188">如果有此樣式，則每當系統游標進入來源矩形時，[放大鏡] 控制項就會顯示放大的系統游標以及放大的螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="57df7-188">If it has this style, the magnifier control displays the magnified system cursor, along with the magnified screen content, whenever the system cursor enters the source rectangle.</span></span>

## <a name="initializing-the-magnifier-run-time-library"></a><span data-ttu-id="57df7-189">初始化放大鏡執行時間程式庫</span><span class="sxs-lookup"><span data-stu-id="57df7-189">Initializing the Magnifier Run-time Library</span></span>

<span data-ttu-id="57df7-190">您必須藉由呼叫 [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) 函式來建立並初始化放大鏡執行時間物件，才能呼叫任何其他放大鏡 API 函式。</span><span class="sxs-lookup"><span data-stu-id="57df7-190">Before you can call any other magnifier API functions, you must create and initialize the magnifier run-time objects by calling the [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) function.</span></span> <span data-ttu-id="57df7-191">同樣地，在您完成使用放大鏡 API 之後，請呼叫 [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) 函式來終結放大鏡執行時間物件，並釋放相關聯的系統資源。</span><span class="sxs-lookup"><span data-stu-id="57df7-191">Similarly, after you finish using the magnifier API, call the [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) function to destroy the magnifier run-time objects and free the associated system resources.</span></span>

## <a name="using-the-full-screen-magnifier"></a><span data-ttu-id="57df7-192">使用 Full-Screen 放大鏡</span><span class="sxs-lookup"><span data-stu-id="57df7-192">Using the Full-Screen Magnifier</span></span>

<span data-ttu-id="57df7-193">若要使用全螢幕放大鏡，請呼叫 [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) 函式。</span><span class="sxs-lookup"><span data-stu-id="57df7-193">To use the full-screen magnifier, call the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function.</span></span> <span data-ttu-id="57df7-194">*MagLevel* 參數會指定放大因數。</span><span class="sxs-lookup"><span data-stu-id="57df7-194">The *magLevel* parameter specifies the magnification factor.</span></span> <span data-ttu-id="57df7-195">*XOffset* 和 *yOffset* 參數指定放大的螢幕內容相對於螢幕的放置方式。</span><span class="sxs-lookup"><span data-stu-id="57df7-195">The *xOffset* and *yOffset* parameters specify how the magnified screen content is positioned relative to the screen.</span></span>

<span data-ttu-id="57df7-196">螢幕內容放大時，會變得大於螢幕本身。</span><span class="sxs-lookup"><span data-stu-id="57df7-196">When the screen content is magnified, it becomes larger than the screen itself.</span></span> <span data-ttu-id="57df7-197">部分內容會延伸到超出螢幕邊緣，並對使用者變得看不見。</span><span class="sxs-lookup"><span data-stu-id="57df7-197">Some portion of the content extends beyond the edges of the screen and becomes invisible to the user.</span></span> <span data-ttu-id="57df7-198">[**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform)函式的 *xOffset* 和 *yOffset* 參數會決定螢幕上會顯示放大螢幕內容的哪一部分。</span><span class="sxs-lookup"><span data-stu-id="57df7-198">The *xOffset* and *yOffset* parameters of the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function determine which portion of the magnified screen content appears on the screen.</span></span> <span data-ttu-id="57df7-199">參數會一起指定 unmagnified 螢幕內容中某個點的座標。</span><span class="sxs-lookup"><span data-stu-id="57df7-199">Together, the parameters specify the coordinates of a point in the unmagnified screen content.</span></span> <span data-ttu-id="57df7-200">當內容放大時，會將指定的點放置在螢幕的左上角。</span><span class="sxs-lookup"><span data-stu-id="57df7-200">When the content is magnified, it is positioned with the specified point at the upper-left corner of the screen.</span></span>

<span data-ttu-id="57df7-201">下列範例會設定全螢幕放大鏡的縮放因數，並將放大的螢幕內容置中放在螢幕的中央。</span><span class="sxs-lookup"><span data-stu-id="57df7-201">The following example sets the magnification factor for the full-screen magnifier and places the center of the magnified screen content at the center of the screen.</span></span>

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

<span data-ttu-id="57df7-202">您可以使用 [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) 函式，藉由設定應用程式定義的色彩轉換矩陣，將色彩效果套用至全螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="57df7-202">Use the [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) function to apply color effects to the full-screen content by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="57df7-203">例如，下列範例會設定將色彩轉換成灰階的色彩轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="57df7-203">For example, the following example sets a color transformation matrix that converts colors to grayscale.</span></span>

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

<span data-ttu-id="57df7-204">您可以藉由呼叫 [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) 函式來取得目前的放大因數和位移值。</span><span class="sxs-lookup"><span data-stu-id="57df7-204">You can retrieve the current magnification factor and offset values by calling the [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) function.</span></span> <span data-ttu-id="57df7-205">您可以藉由呼叫 [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) 函數來取出目前的色彩轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="57df7-205">You can retrieve the current color transformation matrix by calling the [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) function.</span></span>

## <a name="using-the-magnifier-control"></a><span data-ttu-id="57df7-206">使用放大鏡控制項</span><span class="sxs-lookup"><span data-stu-id="57df7-206">Using the Magnifier Control</span></span>

<span data-ttu-id="57df7-207">放大鏡控制項會放大螢幕上特定區域的內容，並在視窗中顯示內容。</span><span class="sxs-lookup"><span data-stu-id="57df7-207">The magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="57df7-208">本節說明如何使用 [放大鏡] 控制項。</span><span class="sxs-lookup"><span data-stu-id="57df7-208">This section describes how to use the magnifier control.</span></span> <span data-ttu-id="57df7-209">其中包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="57df7-209">It contains the following parts:</span></span>

- [<span data-ttu-id="57df7-210">建立放大鏡控制項</span><span class="sxs-lookup"><span data-stu-id="57df7-210">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
- [<span data-ttu-id="57df7-211">初始化控制項</span><span class="sxs-lookup"><span data-stu-id="57df7-211">Initializing the Control</span></span>](#initializing-the-control)
- [<span data-ttu-id="57df7-212">設定來源矩形</span><span class="sxs-lookup"><span data-stu-id="57df7-212">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
- [<span data-ttu-id="57df7-213">套用色彩效果</span><span class="sxs-lookup"><span data-stu-id="57df7-213">Applying Color Effects</span></span>](#applying-color-effects)
- [<span data-ttu-id="57df7-214">選擇性放大</span><span class="sxs-lookup"><span data-stu-id="57df7-214">Selective Magnification</span></span>](#selective-magnification)

### <a name="creating-the-magnifier-control"></a><span data-ttu-id="57df7-215">建立放大鏡控制項</span><span class="sxs-lookup"><span data-stu-id="57df7-215">Creating the Magnifier Control</span></span>

<span data-ttu-id="57df7-216">放大鏡控制項必須裝載在使用 [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) 擴充樣式建立的視窗中。</span><span class="sxs-lookup"><span data-stu-id="57df7-216">The magnifier control must be hosted in a window created with the [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) extended style.</span></span> <span data-ttu-id="57df7-217">建立主視窗之後，呼叫 [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) 以設定主機視窗的不透明度。</span><span class="sxs-lookup"><span data-stu-id="57df7-217">After creating the host window, call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) to set the opacity of the host window.</span></span> <span data-ttu-id="57df7-218">主機視窗通常會設定為完全不透明，以防止顯示基礎螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="57df7-218">The host window is typically set to full opacity to prevent the underlying screen content from showing though.</span></span> <span data-ttu-id="57df7-219">下列範例示範如何將主機視窗設定為完全不透明：</span><span class="sxs-lookup"><span data-stu-id="57df7-219">The following example shows how to set the host window to full opacity:</span></span>

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

<span data-ttu-id="57df7-220">如果您將 [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) 樣式套用至主機視窗，則會將滑鼠點擊動作傳遞至滑鼠游標位置的主機視窗後方的任何物件。</span><span class="sxs-lookup"><span data-stu-id="57df7-220">If you apply the [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) style to the host window, mouse clicks are passed to whatever object is behind the host window at the location of the mouse cursor.</span></span> <span data-ttu-id="57df7-221">請注意，因為主視窗不會處理滑鼠點擊，使用者將無法使用滑鼠移動或調整縮放視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="57df7-221">Be aware that, because the host window does not process mouse clicks, the user will not be able to move or resize the magnification window by using the mouse.</span></span>

<span data-ttu-id="57df7-222">[放大鏡] 控制項視窗的視窗類別必須是 **WC_MAGNIFIER**。</span><span class="sxs-lookup"><span data-stu-id="57df7-222">The window class of the magnifier control window must be **WC_MAGNIFIER**.</span></span> <span data-ttu-id="57df7-223">如果您套用 [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) 樣式，[放大鏡] 控制項就會在放大的螢幕內容中包含系統游標，而且游標會與螢幕內容一起放大。</span><span class="sxs-lookup"><span data-stu-id="57df7-223">If you apply the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style, the magnifier control includes the system cursor in the magnified screen contents, and the cursor is magnified along with the screen contents.</span></span>

<span data-ttu-id="57df7-224">建立 [放大鏡] 控制項之後，請保留視窗控制碼，讓您可以將它傳遞至其他函式。</span><span class="sxs-lookup"><span data-stu-id="57df7-224">After you create the magnifier control, keep the window handle so that you can pass it to other functions.</span></span>

<span data-ttu-id="57df7-225">下列範例顯示如何建立放大鏡控制項。</span><span class="sxs-lookup"><span data-stu-id="57df7-225">The following example shows how to create the magnifier control.</span></span>

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a><span data-ttu-id="57df7-226">初始化控制項</span><span class="sxs-lookup"><span data-stu-id="57df7-226">Initializing the Control</span></span>

<span data-ttu-id="57df7-227">建立 [放大鏡] 控制項之後，您必須呼叫 [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) 函數來指定放大因數。</span><span class="sxs-lookup"><span data-stu-id="57df7-227">After creating the magnifier control, you must call the [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) function to specify the magnification factor.</span></span> <span data-ttu-id="57df7-228">這只是指定矩陣</span><span class="sxs-lookup"><span data-stu-id="57df7-228">This is simply a matter of specifying a matrix of</span></span>

<span data-ttu-id="57df7-229"> (*n*、0.0、0.0) </span><span class="sxs-lookup"><span data-stu-id="57df7-229">(*n*, 0.0, 0.0)</span></span>

<span data-ttu-id="57df7-230"> (0.0、 *n*、0.0) </span><span class="sxs-lookup"><span data-stu-id="57df7-230">(0.0, *n*, 0.0)</span></span>

<span data-ttu-id="57df7-231"> (0.0、0.0、1.0) </span><span class="sxs-lookup"><span data-stu-id="57df7-231">(0.0, 0.0, 1.0)</span></span>

<span data-ttu-id="57df7-232">其中 *n* 為放大因數。</span><span class="sxs-lookup"><span data-stu-id="57df7-232">where *n* is the magnification factor.</span></span>

<span data-ttu-id="57df7-233">下列範例顯示如何設定 [放大鏡] 控制項的放大因數。</span><span class="sxs-lookup"><span data-stu-id="57df7-233">The following example shows how to set the magnification factor for the magnifier control.</span></span>

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a><span data-ttu-id="57df7-234">設定來源矩形</span><span class="sxs-lookup"><span data-stu-id="57df7-234">Setting the Source Rectangle</span></span>

<span data-ttu-id="57df7-235">當使用者將滑鼠游標移到螢幕周圍時，您的應用程式會呼叫 [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) 函式，以指定要放大的基礎螢幕部分。</span><span class="sxs-lookup"><span data-stu-id="57df7-235">As the user moves the mouse cursor around the screen, your application calls the [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) function to specify the part of the underlying screen that is to be magnified.</span></span>

<span data-ttu-id="57df7-236">下列範例函式會根據滑鼠位置和放大鏡視窗的尺寸除以放大因數) 來計算來源矩形的位置和維度 (，並據此設定來源矩形。</span><span class="sxs-lookup"><span data-stu-id="57df7-236">The following example function calculates the position and dimensions of the source rectangle (based on the mouse position and the dimensions of the magnifier window divided by the magnification factor) and sets the source rectangle accordingly.</span></span> <span data-ttu-id="57df7-237">函式也會將主機視窗的工作區放在滑鼠位置。</span><span class="sxs-lookup"><span data-stu-id="57df7-237">The function also centers the client area of the host window at the mouse position.</span></span> <span data-ttu-id="57df7-238">此函式會依間隔呼叫，以更新放大視窗。</span><span class="sxs-lookup"><span data-stu-id="57df7-238">This function would be called at intervals to update the magnification window.</span></span>

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a><span data-ttu-id="57df7-239">套用色彩效果</span><span class="sxs-lookup"><span data-stu-id="57df7-239">Applying Color Effects</span></span>

<span data-ttu-id="57df7-240">具有 [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) 樣式的放大鏡控制項會套用內建的色彩轉換矩陣，以反轉放大螢幕內容的色彩。</span><span class="sxs-lookup"><span data-stu-id="57df7-240">A magnifier control that has the [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) style applies a built-in color transformation matrix that inverts the colors of the magnified screen content.</span></span> <span data-ttu-id="57df7-241">下圖顯示具有 **MS_INVERTCOLORS** 樣式的 [放大鏡] 控制項中的螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="57df7-241">The following illustration shows screen content in a magnifier control that has the **MS_INVERTCOLORS** style.</span></span>

![具有反轉色彩之放大內容的螢幕擷取畫面](images/color-inversion.png)

<span data-ttu-id="57df7-243">[**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect)函式可讓您設定應用程式定義的色彩轉換矩陣，以套用其他色彩效果。</span><span class="sxs-lookup"><span data-stu-id="57df7-243">The [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) function enables you to apply other color effects by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="57df7-244">例如，下列函式會設定將色彩轉換成灰階的色彩轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="57df7-244">For example, the following function sets a color transformation matrix that converts colors to grayscale.</span></span>


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

<span data-ttu-id="57df7-245">如需色彩轉換如何運作的詳細資訊，請參閱在 GDI + 檔中 [使用色彩矩陣轉換單一色彩](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) 。</span><span class="sxs-lookup"><span data-stu-id="57df7-245">For more information about how color transformations work, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the GDI+ documentation.</span></span>

### <a name="selective-magnification"></a><span data-ttu-id="57df7-246">選擇性放大</span><span class="sxs-lookup"><span data-stu-id="57df7-246">Selective Magnification</span></span>

<span data-ttu-id="57df7-247">根據預設，縮放比例會套用至縮放視窗本身以外的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="57df7-247">By default, magnification is applied to all windows other than the magnification window itself.</span></span> <span data-ttu-id="57df7-248">若要指定要放大的視窗，請呼叫 [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) 函數。</span><span class="sxs-lookup"><span data-stu-id="57df7-248">To specify which windows are to be magnified, call the [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) function.</span></span> <span data-ttu-id="57df7-249">這個方法會採用要放大的 windows 清單，或是要從縮放比例排除的 windows 清單。</span><span class="sxs-lookup"><span data-stu-id="57df7-249">This method takes either a list of windows to magnify, or a list of windows to exclude from magnification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57df7-250">相關主題</span><span class="sxs-lookup"><span data-stu-id="57df7-250">Related topics</span></span>

[<span data-ttu-id="57df7-251">放大 API</span><span class="sxs-lookup"><span data-stu-id="57df7-251">Magnification API</span></span>](entry-magapi-sdk.md)