---
description: DirectShow 常見問題
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: DirectShow 常見問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510110"
---
# <a name="directshow-faq"></a><span data-ttu-id="16b39-103">DirectShow 常見問題</span><span class="sxs-lookup"><span data-stu-id="16b39-103">DirectShow FAQ</span></span>

<span data-ttu-id="16b39-104">本文將回答有關 Microsoft DirectShow 的許多常見問題。</span><span class="sxs-lookup"><span data-stu-id="16b39-104">This article answers many frequently asked questions about Microsoft DirectShow.</span></span>

<span data-ttu-id="16b39-105">**DirectShow 支援哪些作業系統？**</span><span class="sxs-lookup"><span data-stu-id="16b39-105">**What operating systems does DirectShow support?**</span></span>

<span data-ttu-id="16b39-106">DirectShow 適用于所有支援的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="16b39-106">DirectShow is available in all supported versions of Windows.</span></span>

<span data-ttu-id="16b39-107">**我需要使用 DirectShow 進行程式設計的 COM 知識有多高？**</span><span class="sxs-lookup"><span data-stu-id="16b39-107">**How much COM knowledge do I need to program with DirectShow?**</span></span>

<span data-ttu-id="16b39-108">針對應用程式開發，您必須瞭解使用 COM 物件的基本概念：如何將它們具現化、存取它們所公開的介面，以及管理這些介面的參考計數。</span><span class="sxs-lookup"><span data-stu-id="16b39-108">For application development, you need to understand the basics of working with COM objects: how to instantiate them, access the interfaces they expose, and manage reference counts on those interfaces.</span></span> <span data-ttu-id="16b39-109">篩選開發需要更多的 COM 知識。</span><span class="sxs-lookup"><span data-stu-id="16b39-109">Filter development requires more COM knowledge.</span></span>

<span data-ttu-id="16b39-110">**DirectShow 支援哪些格式？**</span><span class="sxs-lookup"><span data-stu-id="16b39-110">**What formats does DirectShow support?**</span></span>

<span data-ttu-id="16b39-111">請參閱 [DirectShow 中支援的格式](supported-formats-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="16b39-111">See [Supported Formats in DirectShow](supported-formats-in-directshow.md).</span></span>

<span data-ttu-id="16b39-112">**有 (HCL) 的 DirectShow 硬體相容性清單嗎？**</span><span class="sxs-lookup"><span data-stu-id="16b39-112">**Is there a DirectShow Hardware Compatibility List (HCL)?**</span></span>

<span data-ttu-id="16b39-113">不會。</span><span class="sxs-lookup"><span data-stu-id="16b39-113">No.</span></span> <span data-ttu-id="16b39-114">DirectShow 使用 Microsoft DirectDraw 和 Microsoft DirectSound 硬體功能（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="16b39-114">DirectShow uses Microsoft DirectDraw and Microsoft DirectSound hardware capabilities if they are available.</span></span> <span data-ttu-id="16b39-115">當沒有特殊硬體可用時，DirectShow 會使用 GDI 來繪製影片，並使用 **waveOut** \* 多媒體 api 來播放音訊。</span><span class="sxs-lookup"><span data-stu-id="16b39-115">When no special hardware is available, DirectShow uses GDI to draw video and the **waveOut** \* multimedia APIs to play audio.</span></span>

<span data-ttu-id="16b39-116">**我可以使用哪些語言來撰寫 DirectShow 應用程式？**</span><span class="sxs-lookup"><span data-stu-id="16b39-116">**What languages can I use to write a DirectShow application?**</span></span>

<span data-ttu-id="16b39-117">DirectShow 主要是針對 c + + 開發所設計。</span><span class="sxs-lookup"><span data-stu-id="16b39-117">DirectShow is designed primarily for C++ development.</span></span> <span data-ttu-id="16b39-118">您可以透過 Visual Basic 6.0 來公開 DirectShow API 的小型子集合;不過，這項功能已被取代。</span><span class="sxs-lookup"><span data-stu-id="16b39-118">A small sub-set of the DirectShow API is exposed through Visual Basic 6.0; however, this feature is deprecated.</span></span>

<span data-ttu-id="16b39-119">**您是否可以透過受控碼來存取 DirectShow？**</span><span class="sxs-lookup"><span data-stu-id="16b39-119">**Will DirectShow ever be accessible through managed code?**</span></span>

<span data-ttu-id="16b39-120">Microsoft 目前沒有任何計畫可實行受控的 DirectShow API。</span><span class="sxs-lookup"><span data-stu-id="16b39-120">Microsoft has no current plans to implement a managed DirectShow API.</span></span>

<span data-ttu-id="16b39-121">**我需要什麼編譯器才能進行 DirectShow 開發？**</span><span class="sxs-lookup"><span data-stu-id="16b39-121">**What compiler do I need for DirectShow development?**</span></span>

<span data-ttu-id="16b39-122">只要編譯器的環境已正確設定，任何能夠產生元件物件模型 (COM) 物件的編譯器都應可運作。</span><span class="sxs-lookup"><span data-stu-id="16b39-122">Any compiler capable of generating Component Object Model (COM) objects should work once the compiler's environment has been configured correctly.</span></span>

<span data-ttu-id="16b39-123">**DirectShow 與 Microsoft DirectX 有何關聯？**</span><span class="sxs-lookup"><span data-stu-id="16b39-123">**How does DirectShow relate to Microsoft DirectX?**</span></span>

<span data-ttu-id="16b39-124">在內部，當硬體支援時，DirectShow 會使用 DirectSound 和 DirectDraw。</span><span class="sxs-lookup"><span data-stu-id="16b39-124">Internally, DirectShow uses DirectSound and DirectDraw when the hardware supports it.</span></span> <span data-ttu-id="16b39-125">影片轉譯器和覆迭混音器篩選器會使用 DirectDraw 3 和 DirectDraw 5 的表面。</span><span class="sxs-lookup"><span data-stu-id="16b39-125">The Video Renderer and Overlay Mixer filters use DirectDraw 3 and DirectDraw 5 surfaces.</span></span> <span data-ttu-id="16b39-126">影片混用轉譯器 7 (Windows XP 只) 使用 DirectDraw 7 表面。</span><span class="sxs-lookup"><span data-stu-id="16b39-126">The Video Mixing Renderer 7 (Windows XP only) uses DirectDraw 7 surfaces.</span></span> <span data-ttu-id="16b39-127">影片混合轉譯器9和增強型影片轉譯器會使用最新的 Microsoft Direct3D Api。</span><span class="sxs-lookup"><span data-stu-id="16b39-127">The Video Mixing Renderer 9 and the Enhanced Video Renderer use the latest Microsoft Direct3D APIs.</span></span> <span data-ttu-id="16b39-128">您不需要使用其他 DirectX Api 來撰寫 DirectShow 應用程式，雖然可以將它們合併。</span><span class="sxs-lookup"><span data-stu-id="16b39-128">You do not need to use the other DirectX APIs to write a DirectShow application, although it is possible to combine them.</span></span>

<span data-ttu-id="16b39-129">**DirectShow 與 Microsoft ActiveMovie 有何關聯？**</span><span class="sxs-lookup"><span data-stu-id="16b39-129">**How does DirectShow relate to Microsoft ActiveMovie?**</span></span>

<span data-ttu-id="16b39-130">ActiveMovie 是 DirectShow 的原始名稱。</span><span class="sxs-lookup"><span data-stu-id="16b39-130">ActiveMovie was the original name for DirectShow.</span></span> <span data-ttu-id="16b39-131">詞彙 ActiveMovie 已不再使用。</span><span class="sxs-lookup"><span data-stu-id="16b39-131">The term ActiveMovie is no longer used.</span></span>

<span data-ttu-id="16b39-132">**GraphEdit 公用程式是否有原始程式碼可供使用？可以轉散發 GraphEdit 嗎？**</span><span class="sxs-lookup"><span data-stu-id="16b39-132">**Is the source code to the GraphEdit utility available? Can GraphEdit be redistributed?**</span></span>

<span data-ttu-id="16b39-133">否，來源無法使用，而且 Graphedt.exe 無法轉散發。</span><span class="sxs-lookup"><span data-stu-id="16b39-133">No, the source is not available, and Graphedt.exe is not redistributable.</span></span>

<span data-ttu-id="16b39-134">**DMOs 更換 DirectShow 篩選嗎？**</span><span class="sxs-lookup"><span data-stu-id="16b39-134">**Do DMOs replace DirectShow filters?**</span></span>

<span data-ttu-id="16b39-135">Microsoft DirectX Media 物件 (DMOs) 可用於 DirectShow 應用程式。</span><span class="sxs-lookup"><span data-stu-id="16b39-135">Microsoft DirectX Media Objects (DMOs) can be used in a DirectShow application.</span></span> <span data-ttu-id="16b39-136">針對編碼器、解碼器和效果，建議您撰寫一則，而非 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="16b39-136">For encoders, decoders, and effects, you are encouraged to write a DMO instead of a DirectShow filter.</span></span> <span data-ttu-id="16b39-137"> (注意：如果您想要在您的解碼器中使用 DirectX Video 加速，您必須將它實作為篩選器。 ) 基於其他用途，DirectShow 篩選器可能更適合。</span><span class="sxs-lookup"><span data-stu-id="16b39-137">(Note: If you want to use DirectX Video Acceleration in your decoder, you must implement it as a filter.) For other purposes, a DirectShow filter might be more appropriate.</span></span> <span data-ttu-id="16b39-138">如需 DMOs 的詳細資訊，請參閱 [DirectX 媒體物件](directx-media-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="16b39-138">For more information about DMOs, see [DirectX Media Objects](directx-media-objects.md).</span></span>

<span data-ttu-id="16b39-139">**我要使用 Windows Media Player 來播放 AVI 格式檔案。我可以聽到音訊，但似乎沒有任何影片，而只是看到黑色。怎麼了？**</span><span class="sxs-lookup"><span data-stu-id="16b39-139">**I'm playing an AVI format file with Windows Media Player. I can hear the audio, but there doesn't seem to be any video-instead, I just see black. What's wrong?**</span></span>

<span data-ttu-id="16b39-140">檔案可能是以您系統上不存在的編解碼器編碼。</span><span class="sxs-lookup"><span data-stu-id="16b39-140">Probably the file was encoded with a codec that is not present on your system.</span></span> <span data-ttu-id="16b39-141">雖然 AVI 檔案格式很常見，但您可以使用許多不同的壓縮格式來建立 AVI 檔案 (編解碼器) 。</span><span class="sxs-lookup"><span data-stu-id="16b39-141">Although the AVI file format is common, AVI files can be created with many different compression formats (codecs).</span></span> <span data-ttu-id="16b39-142">如果您嘗試播放的 AVI 檔案使用不支援的編解碼器，您可能會聽到音訊元件，但影片會顯示為黑色畫面，或螢幕內容將保持不變。</span><span class="sxs-lookup"><span data-stu-id="16b39-142">If you try to play an AVI file that uses an unsupported codec, you might hear the audio component, but the video will display as a black screen or the screen contents will remain unchanged.</span></span>

> [!Note]  
> <span data-ttu-id="16b39-143">如果您的系統上沒有編解碼器，Windows Media Player 通常會嘗試下載並安裝它。</span><span class="sxs-lookup"><span data-stu-id="16b39-143">Windows Media Player often attempts to download and install a codec if it is not present on your system.</span></span>

 

<span data-ttu-id="16b39-144">**如何? 建立我的應用程式？我需要哪些程式庫和標頭檔？**</span><span class="sxs-lookup"><span data-stu-id="16b39-144">**How do I build my application? What libraries and header files do I need?**</span></span>

<span data-ttu-id="16b39-145">請參閱 [設定組建環境](setting-up-the-build-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="16b39-145">See [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="16b39-146">**GraphEdit 會顯示許多未記載的篩選準則。這些篩選準則為何？**</span><span class="sxs-lookup"><span data-stu-id="16b39-146">**GraphEdit displays a lot of filters that aren't documented. What are these filters?**</span></span>

<span data-ttu-id="16b39-147">GraphEdit 會列舉在您的系統上的篩選準則類別中註冊的所有篩選準則。</span><span class="sxs-lookup"><span data-stu-id="16b39-147">GraphEdit enumerates all of the filters that are registered on your system in a filter category.</span></span> <span data-ttu-id="16b39-148">這可能包括由協力廠商應用程式安裝的篩選，或其他 Microsoft 技術（例如 Windows Media 或 NetMeeting）所安裝的篩選。</span><span class="sxs-lookup"><span data-stu-id="16b39-148">This might include filters installed by third-party applications, or installed by other Microsoft technologies, such as Windows Media or NetMeeting.</span></span> <span data-ttu-id="16b39-149">此外，某些 DirectShow 篩選器可作為編解碼器或硬體裝置的包裝函式，每個編解碼器或裝置會顯示為不同的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="16b39-149">Also, some DirectShow filters act as wrappers for codecs or hardware devices, with each codec or device appearing as a distinct filter.</span></span> <span data-ttu-id="16b39-150">Microsoft h.264 Video 編解碼器是由 NetMeeting 使用，且在 DirectShow 中已不再受支援。</span><span class="sxs-lookup"><span data-stu-id="16b39-150">The Microsoft H.263 Video Codec is used by NetMeeting and is no longer supported in DirectShow.</span></span> <span data-ttu-id="16b39-151">如需詳細資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="16b39-151">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="16b39-152">**我在以程式設計方式建立自訂圖形時遇到問題。**</span><span class="sxs-lookup"><span data-stu-id="16b39-152">**I'm having trouble building my custom graph programmatically.**</span></span>

<span data-ttu-id="16b39-153">首先，嘗試使用 GraphEdit 來建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="16b39-153">First try building the filter graph with GraphEdit.</span></span> <span data-ttu-id="16b39-154">這項工具可讓您快速模擬許多可能性。</span><span class="sxs-lookup"><span data-stu-id="16b39-154">This tool enables you to simulate lots of possibilities quickly.</span></span> <span data-ttu-id="16b39-155">GraphEdit 在嘗試以原始程式碼建立之前，一律是測試圖形的絕佳位置。</span><span class="sxs-lookup"><span data-stu-id="16b39-155">GraphEdit is always a great place to test out the graph before attempting to build it with source code.</span></span>

<span data-ttu-id="16b39-156">如需有關圖形建立的詳細資訊，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="16b39-156">For more information about graph building, see the following articles:</span></span>

-   [<span data-ttu-id="16b39-157">建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="16b39-157">Building the Filter Graph</span></span>](building-the-filter-graph.md)
-   [<span data-ttu-id="16b39-158">列舉篩選圖形中的物件</span><span class="sxs-lookup"><span data-stu-id="16b39-158">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)

<span data-ttu-id="16b39-159">**如何偵測指定電腦上是否已安裝 DirectShow？**</span><span class="sxs-lookup"><span data-stu-id="16b39-159">**How can I detect whether DirectShow is installed on a given machine?**</span></span>

<span data-ttu-id="16b39-160">呼叫 **CoCreateInstance** 以建立篩選圖形管理員的實例。</span><span class="sxs-lookup"><span data-stu-id="16b39-160">Call **CoCreateInstance** to create an instance of the Filter Graph Manager.</span></span> <span data-ttu-id="16b39-161">如果此呼叫成功，則會在電腦上安裝 DirectShow。</span><span class="sxs-lookup"><span data-stu-id="16b39-161">If this call succeeds, DirectShow is installed on the machine.</span></span> <span data-ttu-id="16b39-162">下列程式碼示範如何執行這項作業：</span><span class="sxs-lookup"><span data-stu-id="16b39-162">The following code shows how to do this:</span></span>


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



<span data-ttu-id="16b39-163">**如何? 變更篩選器的設定，而不顯示內容頁嗎？**</span><span class="sxs-lookup"><span data-stu-id="16b39-163">**How do I change a filter's settings without displaying the property page?**</span></span>

<span data-ttu-id="16b39-164">大部分的篩選器會公開一或多個介面來設定篩選準則的屬性。</span><span class="sxs-lookup"><span data-stu-id="16b39-164">Most filters expose one or more interfaces for setting properties on the filter.</span></span> <span data-ttu-id="16b39-165">請參閱 [參考] 頁面中有問題的篩選。</span><span class="sxs-lookup"><span data-stu-id="16b39-165">Consult the reference page for the filter in question.</span></span> <span data-ttu-id="16b39-166"> (查看 [DirectShow 篩選器](directshow-filters.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="16b39-166">(See [DirectShow Filters](directshow-filters.md).)</span></span>

<span data-ttu-id="16b39-167">**我可以使用 GraphEdit 來測試篩選嗎？**</span><span class="sxs-lookup"><span data-stu-id="16b39-167">**Can I test my filter with GraphEdit?**</span></span>

<span data-ttu-id="16b39-168">當您正在開發篩選器時，GraphEdit 可協助您將篩選之間的連接視覺化。</span><span class="sxs-lookup"><span data-stu-id="16b39-168">While you are developing a filter, GraphEdit can help you to visualize the connections between filters.</span></span> <span data-ttu-id="16b39-169">它也可以提供篩選功能的快速測試。</span><span class="sxs-lookup"><span data-stu-id="16b39-169">It can also provide a quick test of a filter's functionality.</span></span> <span data-ttu-id="16b39-170">但是，它並不是健全的測試平臺。</span><span class="sxs-lookup"><span data-stu-id="16b39-170">However, it is not meant as a robust test platform.</span></span>

<span data-ttu-id="16b39-171">**篩選準則會在哪個特殊許可權環形執行？**</span><span class="sxs-lookup"><span data-stu-id="16b39-171">**At what privilege ring do filters run?**</span></span>

<span data-ttu-id="16b39-172">篩選準則會在 ring 3 執行，不過某些篩選器會控制在 ring 0 執行的串流裝置。</span><span class="sxs-lookup"><span data-stu-id="16b39-172">Filters run at ring 3, although some filters control streaming devices that run at ring 0.</span></span> <span data-ttu-id="16b39-173">如需詳細資訊，請參閱 [硬體裝置如何參與篩選圖形](how-hardware-devices-participate-in-the-filter-graph.md)。</span><span class="sxs-lookup"><span data-stu-id="16b39-173">For more information, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>

<span data-ttu-id="16b39-174">**我是否需要使用內核偵錯工具？**</span><span class="sxs-lookup"><span data-stu-id="16b39-174">**Do I need to use a kernel debugger?**</span></span>

<span data-ttu-id="16b39-175">這取決於您的特定專案。</span><span class="sxs-lookup"><span data-stu-id="16b39-175">That depends on your specific project.</span></span> <span data-ttu-id="16b39-176">安裝 DirectX 偵錯工具執行時間程式庫表示您會安裝 debug 驅動程式和其他核心模式元件，如果您的應用程式在其中一個元件中造成 debug assert，則您的電腦將會自動重新開機，除非您已將內核偵錯工具附加至您的進程。</span><span class="sxs-lookup"><span data-stu-id="16b39-176">Installing the DirectX debug runtime libraries means that you are installing debug drivers and other kernel mode components, and that if your application causes a debug assert in one of these components, your machine will automatically reboot unless you have a kernel debugger attached to your process.</span></span>

<span data-ttu-id="16b39-177">**當我在偵錯工具中執行應用程式時，它會當機。**</span><span class="sxs-lookup"><span data-stu-id="16b39-177">**When I run my application in the debugger, it crashes.**</span></span>

<span data-ttu-id="16b39-178">當應用程式附加至偵錯工具時，某些解碼器設計為無法運作。</span><span class="sxs-lookup"><span data-stu-id="16b39-178">Some decoders are designed not to work while the application is attached to the debugger.</span></span> <span data-ttu-id="16b39-179">嘗試在偵錯工具外執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="16b39-179">Try running the application outside the debugger.</span></span>

<span data-ttu-id="16b39-180">**定義 \_ GUID 宏的運作方式為何？**</span><span class="sxs-lookup"><span data-stu-id="16b39-180">**How does the DEFINE\_GUID macro work?**</span></span>

<span data-ttu-id="16b39-181">**定義 \_ guid** 宏可解決在 `extern` 原始程式碼中宣告 GUID 值參考的問題。</span><span class="sxs-lookup"><span data-stu-id="16b39-181">The **DEFINE\_GUID** macro solves the problem of declaring `extern` references to GUID values in your source code.</span></span> <span data-ttu-id="16b39-182">例如，假設您的專案有三個原始程式檔： Src1 .cpp、Src2 收取 .cpp 和 Src3 .cpp，而這三個檔案都使用您已定義的特定 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="16b39-182">For example, suppose that your project has three source files, Src1.cpp, Src2.cpp, and Src3.cpp, and all three files use a certain GUID value that you have defined.</span></span> <span data-ttu-id="16b39-183">您必須在專案中明確定義 GUID 值一次，而其他原始程式檔必須宣告 `extern` 它的參考。</span><span class="sxs-lookup"><span data-stu-id="16b39-183">The GUID value must be defined exactly once in your project, and the other source files must declare `extern` references to it.</span></span> <span data-ttu-id="16b39-184">使用 **DEFINE \_ GUID** 宏，您可以使用相同的標頭檔來進行這兩種用途。</span><span class="sxs-lookup"><span data-stu-id="16b39-184">With the **DEFINE\_GUID** macro, you can use the same header file for both purposes.</span></span> <span data-ttu-id="16b39-185">在您的標頭檔中，宣告 GUID，如下所示：</span><span class="sxs-lookup"><span data-stu-id="16b39-185">In your header file, declare the GUID as follows:</span></span>


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



<span data-ttu-id="16b39-186"> (在此範例中為零，請放入實際的 GUID 值。 ) 您可以使用 Guidgen.exe 公用程式來建立新的 GUID，並將其貼入 **定義 \_ guid** 格式的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="16b39-186">(Where this example has zeroes, put the actual GUID values.) You can use the Guidgen.exe utility to create a new GUID and paste it into the header file in the **DEFINE\_GUID** format.</span></span> <span data-ttu-id="16b39-187">在每個參考 GUID 的原始程式檔中包含此標頭檔。</span><span class="sxs-lookup"><span data-stu-id="16b39-187">Include this header file in every source file that references the GUID.</span></span> <span data-ttu-id="16b39-188">在剛好一個原始程式檔中，將標頭檔 Initguid 包含在標頭檔之前。</span><span class="sxs-lookup"><span data-stu-id="16b39-188">In exactly one of the source files, include the header file Initguid.h before your header file.</span></span> <span data-ttu-id="16b39-189">例如：</span><span class="sxs-lookup"><span data-stu-id="16b39-189">For example:</span></span>


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



<span data-ttu-id="16b39-190">無論 Initguid .h 標頭檔不包含在內， **DEFINE \_ guid** 宏都會建立 `extern` guid 值的參考。</span><span class="sxs-lookup"><span data-stu-id="16b39-190">Wherever the Initguid.h header file is not included, the **DEFINE\_GUID** macro creates an `extern` reference to the GUID value.</span></span> <span data-ttu-id="16b39-191">包含 Initguid .h 標頭檔時，會重新定義 **定義 \_ guid** 宏，讓 **定義 \_ guid** 建立 guid 的定義宣告。</span><span class="sxs-lookup"><span data-stu-id="16b39-191">When the Initguid.h header file is included, it redefines the **DEFINE\_GUID** macro so that **DEFINE\_GUID** creates a defining declaration of the GUID.</span></span>

<span data-ttu-id="16b39-192">如果您沒有在任何來源檔案中包含 Initguid，您將會收到「無法解析的外部符號」連結錯誤。</span><span class="sxs-lookup"><span data-stu-id="16b39-192">If you do not include Initguid.h in any of the source files, you will get a link error "unresolved external symbol."</span></span> <span data-ttu-id="16b39-193">如果您在相同的 GUID 中包含 Initguid 兩次，您將會收到編譯錯誤「重新定義;多重初始化」。</span><span class="sxs-lookup"><span data-stu-id="16b39-193">If you include Initguid.h twice for the same GUID, you will get a compile error "redefinition; multiple initialization."</span></span> <span data-ttu-id="16b39-194">若要解決這些錯誤，請確定 Initguid 只包含一次。</span><span class="sxs-lookup"><span data-stu-id="16b39-194">To resolve these errors, make sure that Initguid.h is included exactly once.</span></span> <span data-ttu-id="16b39-195">此外，請勿在先行編譯標頭檔中包含 Initguid，因為在效果中，先行編譯標頭檔會包含在每個原始程式檔中。</span><span class="sxs-lookup"><span data-stu-id="16b39-195">Also, do not include Initguid.h inside a precompiled header file, because in effect the precompiled header is included in every source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16b39-196">相關主題</span><span class="sxs-lookup"><span data-stu-id="16b39-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16b39-197">DirectShow 簡介</span><span class="sxs-lookup"><span data-stu-id="16b39-197">Introduction to DirectShow</span></span>](introduction-to-directshow.md)
</dt> </dl>

 

 



