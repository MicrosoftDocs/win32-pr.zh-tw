---
title: DPI 和 Device-Independent 圖元
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 深入瞭解： DPI 和 Device-Independent 圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852544"
---
# <a name="dpi-and-device-independent-pixels"></a><span data-ttu-id="7b00f-103">DPI 和 Device-Independent 圖元</span><span class="sxs-lookup"><span data-stu-id="7b00f-103">DPI and Device-Independent Pixels</span></span>

<span data-ttu-id="7b00f-104">若要有效率地使用 Windows 圖形進行程式設計，您必須瞭解兩個相關概念：</span><span class="sxs-lookup"><span data-stu-id="7b00f-104">To program effectively with Windows graphics, you must understand two related concepts:</span></span>

-   <span data-ttu-id="7b00f-105">每吋點數 (DPI)</span><span class="sxs-lookup"><span data-stu-id="7b00f-105">Dots per inch (DPI)</span></span>
-   <span data-ttu-id="7b00f-106">與裝置無關的圖元 (Dip) 。</span><span class="sxs-lookup"><span data-stu-id="7b00f-106">Device-independent pixel (DIPs).</span></span>

<span data-ttu-id="7b00f-107">讓我們從 DPI 開始。</span><span class="sxs-lookup"><span data-stu-id="7b00f-107">Let's start with DPI.</span></span> <span data-ttu-id="7b00f-108">這將需要簡短繞道至印刷樣式。</span><span class="sxs-lookup"><span data-stu-id="7b00f-108">This will require a short detour into typography.</span></span> <span data-ttu-id="7b00f-109">在印刷樣式中，類型的大小是以稱為 *點* 的單位來測量。</span><span class="sxs-lookup"><span data-stu-id="7b00f-109">In typography, the size of type is measured in units called *points*.</span></span> <span data-ttu-id="7b00f-110">一個點等於1/72 英寸。</span><span class="sxs-lookup"><span data-stu-id="7b00f-110">One point equals 1/72 of an inch.</span></span>

<dl> <span data-ttu-id="7b00f-111">1 pt = 1/72 英寸</span><span class="sxs-lookup"><span data-stu-id="7b00f-111">1 pt = 1/72 inch</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="7b00f-112">這是點的桌面發佈定義。</span><span class="sxs-lookup"><span data-stu-id="7b00f-112">This is the desktop publishing definition of point.</span></span> <span data-ttu-id="7b00f-113">在過去，點的確切量值會不同。</span><span class="sxs-lookup"><span data-stu-id="7b00f-113">Historically, the exact measure of a point has varied.</span></span>

 

<span data-ttu-id="7b00f-114">例如，12點字型的設計目的是要容納在 1/6 " (12/72) 行文字中。</span><span class="sxs-lookup"><span data-stu-id="7b00f-114">For example, a 12-point font is designed to fit within a 1/6" (12/72) line of text.</span></span> <span data-ttu-id="7b00f-115">很明顯地，這並不表示字型中的每個字元都是「高度」1/6」。</span><span class="sxs-lookup"><span data-stu-id="7b00f-115">Obviously, this does not mean that every character in the font is exactly 1/6" tall.</span></span> <span data-ttu-id="7b00f-116">事實上，某些字元的高度可能會高於1/6」。</span><span class="sxs-lookup"><span data-stu-id="7b00f-116">In fact, some characters might be taller than 1/6".</span></span> <span data-ttu-id="7b00f-117">例如，在許多字型中，字元Å的高度高於字型的名義高度。</span><span class="sxs-lookup"><span data-stu-id="7b00f-117">For example, in many fonts the character Å is taller than the nominal height of the font.</span></span> <span data-ttu-id="7b00f-118">若要正確地顯示，字型在文字之間需要一些額外的空間。</span><span class="sxs-lookup"><span data-stu-id="7b00f-118">To display correctly, the font needs some additional space between the text.</span></span> <span data-ttu-id="7b00f-119">這個空間稱為「 *前置*」。</span><span class="sxs-lookup"><span data-stu-id="7b00f-119">This space is called the *leading*.</span></span>

<span data-ttu-id="7b00f-120">下圖顯示72點字型。</span><span class="sxs-lookup"><span data-stu-id="7b00f-120">The following illustration shows a 72-point font.</span></span> <span data-ttu-id="7b00f-121">實線會在文字周圍顯示1個高度周框方塊。</span><span class="sxs-lookup"><span data-stu-id="7b00f-121">The solid lines show a 1" tall bounding box around the text.</span></span> <span data-ttu-id="7b00f-122">虛線稱為 *基準*。</span><span class="sxs-lookup"><span data-stu-id="7b00f-122">The dashed line is called the *baseline*.</span></span> <span data-ttu-id="7b00f-123">字型中的大部分字元都是在基準上的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="7b00f-123">Most of the characters in a font rest on the baseline.</span></span> <span data-ttu-id="7b00f-124">字型的高度包括基準之上的部分 (*上升* 的) ，以及高於基準的部分 (*下降*) 。</span><span class="sxs-lookup"><span data-stu-id="7b00f-124">The height of the font includes the portion above the baseline (the *ascent*) and the portion below the baseline (the *descent*).</span></span> <span data-ttu-id="7b00f-125">在這裡顯示的字型中，上升是56點，下降則是16點。</span><span class="sxs-lookup"><span data-stu-id="7b00f-125">In the font shown here, the ascent is 56 points and the descent is 16 points.</span></span>

![顯示72點字型的圖例。](images/graphics11.png)

<span data-ttu-id="7b00f-127">不過，在電腦顯示時，測量文字大小會有問題，因為圖元的大小不是相同的。</span><span class="sxs-lookup"><span data-stu-id="7b00f-127">When it comes to a computer display, however, measuring text size is problematic, because pixels are not all the same size.</span></span> <span data-ttu-id="7b00f-128">圖元的大小取決於兩個因素：顯示解析度，以及監視的實體大小。</span><span class="sxs-lookup"><span data-stu-id="7b00f-128">The size of a pixel depends on two factors: the display resolution, and the physical size of the monitor.</span></span> <span data-ttu-id="7b00f-129">因此，實體英寸不是有用的量值，因為實體的圖元與圖元之間沒有固定的關聯性。</span><span class="sxs-lookup"><span data-stu-id="7b00f-129">Therefore, physical inches are not a useful measure, because there is no fixed relation between physical inches and pixels.</span></span> <span data-ttu-id="7b00f-130">相反地，會以 *邏輯* 單元來測量字型。</span><span class="sxs-lookup"><span data-stu-id="7b00f-130">Instead, fonts are measured in *logical* units.</span></span> <span data-ttu-id="7b00f-131">72點字型的定義是一種邏輯英寸高度。</span><span class="sxs-lookup"><span data-stu-id="7b00f-131">A 72-point font is defined to be one logical inch tall.</span></span> <span data-ttu-id="7b00f-132">邏輯英寸接著會轉換成圖元。</span><span class="sxs-lookup"><span data-stu-id="7b00f-132">Logical inches are then converted to pixels.</span></span> <span data-ttu-id="7b00f-133">多年來，Windows 使用了下列轉換：一個邏輯英寸等於96圖元。</span><span class="sxs-lookup"><span data-stu-id="7b00f-133">For many years, Windows used the following conversion: One logical inch equals 96 pixels.</span></span> <span data-ttu-id="7b00f-134">使用此縮放比例，72點字型會轉譯為96圖元高。</span><span class="sxs-lookup"><span data-stu-id="7b00f-134">Using this scaling factor, a 72-point font is rendered as 96 pixels tall.</span></span> <span data-ttu-id="7b00f-135">12點字型的高度為16圖元。</span><span class="sxs-lookup"><span data-stu-id="7b00f-135">A 12-point font is 16 pixels tall.</span></span>

<dl> <span data-ttu-id="7b00f-136">12點 = 12/72 邏輯英寸 = 1/6 邏輯英寸 = 96/6 圖元 = 16 圖元</span><span class="sxs-lookup"><span data-stu-id="7b00f-136">12 points = 12/72 logical inch = 1/6 logical inch = 96/6 pixels = 16 pixels</span></span>  
</dl>

<span data-ttu-id="7b00f-137">此縮放比例描述為每英寸96點 (DPI) 。</span><span class="sxs-lookup"><span data-stu-id="7b00f-137">This scaling factor is described as 96 dots per inch (DPI).</span></span> <span data-ttu-id="7b00f-138">「點」（term）是指從列印開始，其中會將筆墨的實體點放在紙張上。</span><span class="sxs-lookup"><span data-stu-id="7b00f-138">The term dots derives from printing, where physical dots of ink are put onto paper.</span></span> <span data-ttu-id="7b00f-139">對於電腦顯示而言，每個邏輯英寸應以96圖元為單位，但已停滯一詞。</span><span class="sxs-lookup"><span data-stu-id="7b00f-139">For computer displays, it would be more accurate to say 96 pixels per logical inch, but the term DPI has stuck.</span></span>

<span data-ttu-id="7b00f-140">因為實際的圖元大小有所差異，所以在一個監視器上可讀取的文字可能會在另一個監視器上太小。</span><span class="sxs-lookup"><span data-stu-id="7b00f-140">Because actual pixel sizes vary, text that is readable on one monitor might be too small on another monitor.</span></span> <span data-ttu-id="7b00f-141">此外，人們也會有不同的喜好設定，有些人偏好較大的文字。</span><span class="sxs-lookup"><span data-stu-id="7b00f-141">Also, people have different preferences—some people prefer larger text.</span></span> <span data-ttu-id="7b00f-142">基於這個理由，Windows 可讓使用者變更 DPI 設定。</span><span class="sxs-lookup"><span data-stu-id="7b00f-142">For this reason, Windows enables the user to change the DPI setting.</span></span> <span data-ttu-id="7b00f-143">例如，如果使用者將顯示器設定為 144 DPI，72-point 字型會是144圖元高。</span><span class="sxs-lookup"><span data-stu-id="7b00f-143">For example, if the user sets the display to 144 DPI, a 72-point font is 144 pixels tall.</span></span> <span data-ttu-id="7b00f-144">標準 DPI 設定為 100% (96 DPI) 、125% (120 DPI) 和 150% (144 DPI) 。</span><span class="sxs-lookup"><span data-stu-id="7b00f-144">The standard DPI settings are 100% (96 DPI), 125% (120 DPI), and 150% (144 DPI).</span></span> <span data-ttu-id="7b00f-145">使用者也可以套用自訂設定。</span><span class="sxs-lookup"><span data-stu-id="7b00f-145">The user can also apply a custom setting.</span></span> <span data-ttu-id="7b00f-146">從 Windows 7 開始，DPI 是每個使用者的設定。</span><span class="sxs-lookup"><span data-stu-id="7b00f-146">Starting in Windows 7, DPI is a per-user setting.</span></span>

## <a name="dwm-scaling"></a><span data-ttu-id="7b00f-147">DWM 調整</span><span class="sxs-lookup"><span data-stu-id="7b00f-147">DWM Scaling</span></span>

<span data-ttu-id="7b00f-148">如果程式不會考慮 DPI，則在高 DPI 設定上可能會有下列瑕疵：</span><span class="sxs-lookup"><span data-stu-id="7b00f-148">If a program does not account for DPI, the following defects might be apparent at high-DPI settings:</span></span>

-   <span data-ttu-id="7b00f-149">裁剪的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="7b00f-149">Clipped UI elements.</span></span>
-   <span data-ttu-id="7b00f-150">版面配置不正確。</span><span class="sxs-lookup"><span data-stu-id="7b00f-150">Incorrect layout.</span></span>
-   <span data-ttu-id="7b00f-151">圖元出點陣圖和圖示。</span><span class="sxs-lookup"><span data-stu-id="7b00f-151">Pixelated bitmaps and icons.</span></span>
-   <span data-ttu-id="7b00f-152">不正確的滑鼠座標，可能會影響點擊測試、拖放等等。</span><span class="sxs-lookup"><span data-stu-id="7b00f-152">Incorrect mouse coordinates, which can affect hit testing, drag and drop, and so forth.</span></span>

<span data-ttu-id="7b00f-153">為了確保舊版程式在高 DPI 設定下運作，DWM 會執行有用的回復。</span><span class="sxs-lookup"><span data-stu-id="7b00f-153">To ensure that older programs work at high-DPI settings, the DWM implements a useful fallback.</span></span> <span data-ttu-id="7b00f-154">如果程式未標示為 DPI 感知，則 DWM 會調整整個 UI 以符合 DPI 設定。</span><span class="sxs-lookup"><span data-stu-id="7b00f-154">If a program is not marked as being DPI aware, the DWM will scale the entire UI to match the DPI setting.</span></span> <span data-ttu-id="7b00f-155">例如，在 144 DPI，UI 是以150% 來調整，包括文字、圖形、控制項和視窗大小。</span><span class="sxs-lookup"><span data-stu-id="7b00f-155">For example, at 144 DPI, the UI is scaled by 150%, including text, graphics, controls, and window sizes.</span></span> <span data-ttu-id="7b00f-156">如果程式建立500×500視窗，此視窗實際上會顯示為750×750圖元，並據此調整視窗的內容。</span><span class="sxs-lookup"><span data-stu-id="7b00f-156">If the program creates a 500 × 500 window, the window actually appears as 750 × 750 pixels, and the contents of the window are scaled accordingly.</span></span>

<span data-ttu-id="7b00f-157">此行為表示較舊的程式會在高 DPI 設定下「立即運作」。</span><span class="sxs-lookup"><span data-stu-id="7b00f-157">This behavior means that older programs "just work" at high-DPI settings.</span></span> <span data-ttu-id="7b00f-158">不過，縮放比例也會產生稍微模糊的外觀，因為縮放是在視窗繪製之後套用。</span><span class="sxs-lookup"><span data-stu-id="7b00f-158">However, scaling also results in a somewhat blurry appearance, because the scaling is applied after the window is drawn.</span></span>

## <a name="dpi-aware-applications"></a><span data-ttu-id="7b00f-159">DPI-Aware 應用程式</span><span class="sxs-lookup"><span data-stu-id="7b00f-159">DPI-Aware Applications</span></span>

<span data-ttu-id="7b00f-160">為了避免 DWM 調整，程式可以將本身標示為 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="7b00f-160">To avoid DWM scaling, a program can mark itself as DPI-aware.</span></span> <span data-ttu-id="7b00f-161">這會告知 DWM 不要執行任何自動的 DPI 縮放比例。</span><span class="sxs-lookup"><span data-stu-id="7b00f-161">This tells the DWM not to perform any automatic DPI scaling.</span></span> <span data-ttu-id="7b00f-162">所有新的應用程式都應該設計為 DPI 感知，因為 DPI 感知可改善較高 DPI 設定的 UI 外觀。</span><span class="sxs-lookup"><span data-stu-id="7b00f-162">All new applications should be designed to be DPI-aware, because DPI awareness improves the appearance of the UI at higher DPI settings.</span></span>

<span data-ttu-id="7b00f-163">程式會透過應用程式資訊清單宣告本身的 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="7b00f-163">A program declares itself DPI-aware through its application manifest.</span></span> <span data-ttu-id="7b00f-164">*資訊清單* 只是描述 DLL 或應用程式的 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="7b00f-164">A *manifest* is a simply an XML file that describes a DLL or application.</span></span> <span data-ttu-id="7b00f-165">資訊清單通常內嵌在可執行檔中，不過可以提供為個別的檔案。</span><span class="sxs-lookup"><span data-stu-id="7b00f-165">The manifest is typically embedded in the executable file, although it can be provided as a separate file.</span></span> <span data-ttu-id="7b00f-166">資訊清單包含 DLL 相依性、要求的許可權層級，以及程式設計用途的 Windows 版本等資訊。</span><span class="sxs-lookup"><span data-stu-id="7b00f-166">A manifest contains information such as DLL dependencies, the requested privilege level, and what version of Windows the program was designed for.</span></span>

<span data-ttu-id="7b00f-167">若要宣告您的程式為 DPI 感知，請在資訊清單中包含下列資訊。</span><span class="sxs-lookup"><span data-stu-id="7b00f-167">To declare that your program is DPI-aware, include the following information in the manifest.</span></span>

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

<span data-ttu-id="7b00f-168">此處所示的清單只是部分資訊清單，但 Visual Studio 連結器會自動為您產生資訊清單的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="7b00f-168">The listing shown here is only a partial manifest, but the Visual Studio linker generates the rest of the manifest for you automatically.</span></span> <span data-ttu-id="7b00f-169">若要在專案中包含部分資訊清單，請在 Visual Studio 中執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="7b00f-169">To include a partial manifest in your project, perform the following steps in Visual Studio.</span></span>

1.  <span data-ttu-id="7b00f-170">在 [ **專案** ] 功能表上，按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="7b00f-170">On the **Project** menu, click **Property**.</span></span>
2.  <span data-ttu-id="7b00f-171">在左窗格中，依序展開 [設定 **屬性**]、[ **資訊清單工具**]，然後按一下 [ **輸入和輸出**]。</span><span class="sxs-lookup"><span data-stu-id="7b00f-171">In the left pane, expand **Configuration Properties**, expand **Manifest Tool**, and then click **Input and Output**.</span></span>
3.  <span data-ttu-id="7b00f-172">在 [ **其他資訊清單** 檔案] 文字方塊中，輸入資訊清單檔案的名稱，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="7b00f-172">In the **Additional Manifest Files** text box, type the name of the manifest file, and then click **OK**.</span></span>

<span data-ttu-id="7b00f-173">將程式標示為 DPI 感知，就會告知 DWM 不要調整您的應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="7b00f-173">By marking your program as DPI-aware, you are telling the DWM not to scale your application window.</span></span> <span data-ttu-id="7b00f-174">現在，如果您建立500×500視窗，不論使用者的 DPI 設定為何，此視窗都會佔用500×500圖元。</span><span class="sxs-lookup"><span data-stu-id="7b00f-174">Now if you create a 500 × 500 window, the window will occupy 500 × 500 pixels, regardless of the user's DPI setting.</span></span>

## <a name="gdi-and-dpi"></a><span data-ttu-id="7b00f-175">GDI 和 DPI</span><span class="sxs-lookup"><span data-stu-id="7b00f-175">GDI and DPI</span></span>

<span data-ttu-id="7b00f-176">GDI 繪圖是以圖元為單位。</span><span class="sxs-lookup"><span data-stu-id="7b00f-176">GDI drawing is measured in pixels.</span></span> <span data-ttu-id="7b00f-177">這表示，如果您的程式標示為 DPI 感知，而且您要求 GDI 繪製200×100矩形，則產生的矩形將會是螢幕上的200圖元寬和100圖元高度。</span><span class="sxs-lookup"><span data-stu-id="7b00f-177">That means if your program is marked as DPI-aware, and you ask GDI to draw a 200 × 100 rectangle, the resulting rectangle will be 200 pixels wide and 100 pixels tall on the screen.</span></span> <span data-ttu-id="7b00f-178">不過，GDI 字型的大小會調整為目前的 DPI 設定。</span><span class="sxs-lookup"><span data-stu-id="7b00f-178">However, GDI font sizes are scaled to the current DPI setting.</span></span> <span data-ttu-id="7b00f-179">換句話說，如果您建立72點字型，字型的大小會是96圖元（96 DPI），但144圖元為 144 DPI。</span><span class="sxs-lookup"><span data-stu-id="7b00f-179">In other words, if you create a 72-point font, the size of the font will be 96 pixels at 96 DPI, but 144 pixels at 144 DPI.</span></span> <span data-ttu-id="7b00f-180">以下是使用 GDI 以 144 DPI 呈現的72點字型。</span><span class="sxs-lookup"><span data-stu-id="7b00f-180">Here is a 72 point font rendered at 144 DPI using GDI.</span></span>

![顯示 gdi 中 DPI 字型縮放比例的圖表。](images/graphics12.png)

<span data-ttu-id="7b00f-182">如果您的應用程式為 DPI 感知，而且您使用 GDI 進行繪製，請調整所有繪圖座標以符合 DPI。</span><span class="sxs-lookup"><span data-stu-id="7b00f-182">If your application is DPI-aware and you use GDI for drawing, scale all of your drawing coordinates to match the DPI.</span></span>

## <a name="direct2d-and-dpi"></a><span data-ttu-id="7b00f-183">Direct2D 和 DPI</span><span class="sxs-lookup"><span data-stu-id="7b00f-183">Direct2D and DPI</span></span>

<span data-ttu-id="7b00f-184">Direct2D 會自動執行調整以符合 DPI 設定。</span><span class="sxs-lookup"><span data-stu-id="7b00f-184">Direct2D automatically performs scaling to match the DPI setting.</span></span> <span data-ttu-id="7b00f-185">在 Direct2D 中，座標是以與 *裝置無關的圖元為* 單位來測量， (dip) 。</span><span class="sxs-lookup"><span data-stu-id="7b00f-185">In Direct2D, coordinates are measured in units called *device-independent pixels* (DIPs).</span></span> <span data-ttu-id="7b00f-186">DIP 定義為 *邏輯* 英寸的 1/計算1/96。</span><span class="sxs-lookup"><span data-stu-id="7b00f-186">A DIP is defined as 1/96th of a *logical* inch.</span></span> <span data-ttu-id="7b00f-187">在 Direct2D 中，所有繪製作業都是在 Dip 中指定，然後調整為目前的 DPI 設定。</span><span class="sxs-lookup"><span data-stu-id="7b00f-187">In Direct2D, all drawing operations are specified in DIPs and then scaled to the current DPI setting.</span></span>



| <span data-ttu-id="7b00f-188">DPI 設定</span><span class="sxs-lookup"><span data-stu-id="7b00f-188">DPI setting</span></span> | <span data-ttu-id="7b00f-189">DIP 大小</span><span class="sxs-lookup"><span data-stu-id="7b00f-189">DIP size</span></span>    |
|-------------|-------------|
| <span data-ttu-id="7b00f-190">96</span><span class="sxs-lookup"><span data-stu-id="7b00f-190">96</span></span>          | <span data-ttu-id="7b00f-191">1 佹萺慒</span><span class="sxs-lookup"><span data-stu-id="7b00f-191">1 pixel</span></span>     |
| <span data-ttu-id="7b00f-192">120</span><span class="sxs-lookup"><span data-stu-id="7b00f-192">120</span></span>         | <span data-ttu-id="7b00f-193">1.25 圖元</span><span class="sxs-lookup"><span data-stu-id="7b00f-193">1.25 pixels</span></span> |
| <span data-ttu-id="7b00f-194">144</span><span class="sxs-lookup"><span data-stu-id="7b00f-194">144</span></span>         | <span data-ttu-id="7b00f-195">1.5 圖元</span><span class="sxs-lookup"><span data-stu-id="7b00f-195">1.5 pixels</span></span>  |



 

<span data-ttu-id="7b00f-196">例如，如果使用者的 DPI 設定為 144 DPI，而您要求 Direct2D 繪製200×100矩形，矩形將會是300×150實體圖元。</span><span class="sxs-lookup"><span data-stu-id="7b00f-196">For example, if the user's DPI setting is 144 DPI, and you ask Direct2D to draw a 200 × 100 rectangle, the rectangle will be 300 × 150 physical pixels.</span></span> <span data-ttu-id="7b00f-197">此外，DirectWrite 會以 Dip 量值來測量字型大小，而不是點。</span><span class="sxs-lookup"><span data-stu-id="7b00f-197">In addition, DirectWrite measures font sizes in DIPs, rather than points.</span></span> <span data-ttu-id="7b00f-198">若要建立12點字型，請指定 16 Dip (12 點 = 1/6 logical 英寸 = 96/6 Dip) 。</span><span class="sxs-lookup"><span data-stu-id="7b00f-198">To create a 12-point font, specify 16 DIPs (12 points = 1/6 logical inch = 96/6 DIPs).</span></span> <span data-ttu-id="7b00f-199">在螢幕上繪製文字時，Direct2D 會將 Dip 轉換為實體圖元。</span><span class="sxs-lookup"><span data-stu-id="7b00f-199">When the text is drawn on the screen, Direct2D converts the DIPs to physical pixels.</span></span> <span data-ttu-id="7b00f-200">此系統的優點是，不論目前的 DPI 設定為何，測量單位都一致以進行文字和繪圖。</span><span class="sxs-lookup"><span data-stu-id="7b00f-200">The benefit of this system is that the units of measurement are consistent for both text and drawing, regardless of the current DPI setting.</span></span>

<span data-ttu-id="7b00f-201">有一點要注意：滑鼠和視窗座標仍然是以實體圖元為單位，而不是 Dip。</span><span class="sxs-lookup"><span data-stu-id="7b00f-201">A word of caution: Mouse and window coordinates are still given in physical pixels, not DIPs.</span></span> <span data-ttu-id="7b00f-202">例如，如果您處理 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息，則會以實體圖元為單位提供滑鼠下位置。</span><span class="sxs-lookup"><span data-stu-id="7b00f-202">For example, if you process the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, the mouse-down position is given in physical pixels.</span></span> <span data-ttu-id="7b00f-203">若要在該位置繪製點，您必須將圖元座標轉換為 Dip。</span><span class="sxs-lookup"><span data-stu-id="7b00f-203">To draw a point at that position, you must convert the pixel coordinates to DIPs.</span></span>

## <a name="converting-physical-pixels-to-dips"></a><span data-ttu-id="7b00f-204">將實體圖元轉換成 Dip</span><span class="sxs-lookup"><span data-stu-id="7b00f-204">Converting Physical Pixels to DIPs</span></span>

<span data-ttu-id="7b00f-205">從實體圖元轉換到 Dip 會使用下列公式。</span><span class="sxs-lookup"><span data-stu-id="7b00f-205">The conversion from physical pixels to DIPs uses the following formula.</span></span>

<dl> <span data-ttu-id="7b00f-206">Dip = 圖元/ (DPI/96.0) </span><span class="sxs-lookup"><span data-stu-id="7b00f-206">DIPs = pixels / (DPI/96.0)</span></span>  
</dl>

<span data-ttu-id="7b00f-207">若要取得 DPI 設定，請呼叫 [**ID2D1Factory：： GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 方法。</span><span class="sxs-lookup"><span data-stu-id="7b00f-207">To get the DPI setting, call the [**ID2D1Factory::GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method.</span></span> <span data-ttu-id="7b00f-208">DPI 會以兩個浮點數（X 軸的值，一個是 y 軸）的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="7b00f-208">The DPI is returned as two floating-point values, one for the x-axis and one for the y-axis.</span></span> <span data-ttu-id="7b00f-209">理論上，這些值可能會不同。</span><span class="sxs-lookup"><span data-stu-id="7b00f-209">In theory, these values can differ.</span></span> <span data-ttu-id="7b00f-210">為每個軸計算個別的調整比例。</span><span class="sxs-lookup"><span data-stu-id="7b00f-210">Calculate a separate scaling factor for each axis.</span></span>


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



<span data-ttu-id="7b00f-211">如果您不是使用 Direct2D，以下是取得 DPI 設定的替代方法：</span><span class="sxs-lookup"><span data-stu-id="7b00f-211">Here is an alternate way to get the DPI setting if you are not using Direct2D:</span></span>


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> <span data-ttu-id="7b00f-212">在 Windows 10 上，版本1903、  [**ID2D1Factory：： GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 已淘汰，建議為適用于 Windows Store 應用程式的 [**DisplayInformation：： LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) ，或適用于桌面應用程式的 [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) 。</span><span class="sxs-lookup"><span data-stu-id="7b00f-212">On Windows 10, version 1903,  [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) is deprecated and the recommendation is [**DisplayInformation::LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) for Windows Store Apps or [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) for desktop apps.</span></span> <span data-ttu-id="7b00f-213">如果您仍然想要使用它，請在 [**ID2D1Factory：： GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi)呼叫 [**#pragma 警告 (隱藏： 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) ，以隱藏編譯器錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="7b00f-213">If you still want to use it, suppress the compiler error message by writing the line [**#pragma warning(suppress: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) just before the [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) call.</span></span> <span data-ttu-id="7b00f-214">雖然不建議這麼做，但您可以使用 [**SetProcessDpiAwarenessCoNtext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext)，以程式設計的方式設定預設的 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="7b00f-214">Although it is not recommended, it is possible to set the default DPI awareness programmatically using [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span></span> <span data-ttu-id="7b00f-215">在您的進程中建立了一個 (HWND) 的視窗之後，就不再支援變更 DPI 感知模式。</span><span class="sxs-lookup"><span data-stu-id="7b00f-215">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="7b00f-216">如果您要以程式設計方式設定進程預設的 DPI 感知模式，您必須在建立任何 Hwnd 之前呼叫對應的 API。</span><span class="sxs-lookup"><span data-stu-id="7b00f-216">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span> <span data-ttu-id="7b00f-217">如需詳細資訊，請參閱 [設定進程的預設 DPI 感知](../hidpi/setting-the-default-dpi-awareness-for-a-process.md)。</span><span class="sxs-lookup"><span data-stu-id="7b00f-217">For information see [Setting the default DPI awareness for a process](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span></span>

## <a name="resizing-the-render-target"></a><span data-ttu-id="7b00f-218">調整呈現目標的大小</span><span class="sxs-lookup"><span data-stu-id="7b00f-218">Resizing the Render Target</span></span>

<span data-ttu-id="7b00f-219">如果視窗的大小變更，您必須調整轉譯目標的大小以符合。</span><span class="sxs-lookup"><span data-stu-id="7b00f-219">If the size of the window changes, you must resize the render target to match.</span></span> <span data-ttu-id="7b00f-220">在大多數情況下，您也需要更新配置並重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="7b00f-220">In most cases, you will also need to update the layout and repaint the window.</span></span> <span data-ttu-id="7b00f-221">下列程式碼顯示這些步驟。</span><span class="sxs-lookup"><span data-stu-id="7b00f-221">The following code shows these steps.</span></span>


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="7b00f-222">[**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect)函式會取得工作區的新大小（以實體圖元為單位）， (不是 dip) 。</span><span class="sxs-lookup"><span data-stu-id="7b00f-222">The [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) function gets the new size of the client area, in physical pixels (not DIPs).</span></span> <span data-ttu-id="7b00f-223">[**ID2D1HwndRenderTarget：： Resize**](../direct2d/id2d1hwndrendertarget-resize.md)方法會更新轉譯目標的大小，也會以圖元為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="7b00f-223">The [**ID2D1HwndRenderTarget::Resize**](../direct2d/id2d1hwndrendertarget-resize.md) method updates the size of the render target, also specified in pixels.</span></span> <span data-ttu-id="7b00f-224">[**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)函式會藉由將整個工作區新增至視窗的更新區域，來強制重新繪製。</span><span class="sxs-lookup"><span data-stu-id="7b00f-224">The [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function forces a repaint by adding the entire client area to the window's update region.</span></span> <span data-ttu-id="7b00f-225"> (在模組1中，請參閱 [繪製視窗](painting-the-window.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="7b00f-225">(See [Painting the Window](painting-the-window.md), in Module 1.)</span></span>

<span data-ttu-id="7b00f-226">當視窗增加或縮小時，您通常需要重新計算您繪製之物件的位置。</span><span class="sxs-lookup"><span data-stu-id="7b00f-226">As the window grows or shrinks, you will typically need to recalculate the position of the objects that you draw.</span></span> <span data-ttu-id="7b00f-227">例如，在 circle 程式中，必須更新半徑和中心點：</span><span class="sxs-lookup"><span data-stu-id="7b00f-227">For example, in the circle program, the radius and center point must be updated:</span></span>


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



<span data-ttu-id="7b00f-228">[**ID2D1RenderTarget：： GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize)方法會以 dip 傳回轉譯目標的大小， (不是圖元) ，也就是計算版面配置的適當單位。</span><span class="sxs-lookup"><span data-stu-id="7b00f-228">The [**ID2D1RenderTarget::GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) method returns the size of the render target in DIPs (not pixels), which is the appropriate unit for calculating layout.</span></span> <span data-ttu-id="7b00f-229">有一個密切相關的方法 [**ID2D1RenderTarget：： GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize)，會以實體圖元傳回大小。</span><span class="sxs-lookup"><span data-stu-id="7b00f-229">There is a closely related method, [**ID2D1RenderTarget::GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), that returns the size in physical pixels.</span></span> <span data-ttu-id="7b00f-230">針對 **HWND** 轉譯目標，此值會符合 [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect)傳回的大小。</span><span class="sxs-lookup"><span data-stu-id="7b00f-230">For an **HWND** render target, this value matches the size returned by [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span></span> <span data-ttu-id="7b00f-231">但是請記住，繪圖是以 Dip 而非圖元來執行。</span><span class="sxs-lookup"><span data-stu-id="7b00f-231">But remember that drawing is performed in DIPs, not pixels.</span></span>

## <a name="next"></a><span data-ttu-id="7b00f-232">下一個</span><span class="sxs-lookup"><span data-stu-id="7b00f-232">Next</span></span>

[<span data-ttu-id="7b00f-233">在 Direct2D 中使用色彩</span><span class="sxs-lookup"><span data-stu-id="7b00f-233">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)

 

 
