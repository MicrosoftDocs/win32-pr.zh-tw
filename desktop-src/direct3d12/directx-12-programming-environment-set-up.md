---
title: Direct3D 12 程式設計環境設定
description: 描述組成具生產力之 Direct3D 12 開發環境的安裝、工具和支援的程式庫。
ms.assetid: B2288866-E95F-46B8-A7A1-19888F029C03
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7079207f91185cc14b37d9056a4fa813b251bce5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342813"
---
# <a name="direct3d-12-programming-environment-setup"></a><span data-ttu-id="b6e49-103">Direct3D 12 程式設計環境設定</span><span class="sxs-lookup"><span data-stu-id="b6e49-103">Direct3D 12 programming environment setup</span></span>

<span data-ttu-id="b6e49-104">描述組成具生產力之 Direct3D 12 開發環境的安裝、工具和支援的程式庫。</span><span class="sxs-lookup"><span data-stu-id="b6e49-104">Describes the installation, tools and supported libraries that make up a productive Direct3D 12 development environment.</span></span>

-   [<span data-ttu-id="b6e49-105">開發環境</span><span class="sxs-lookup"><span data-stu-id="b6e49-105">Development environment</span></span>](#development-environment)
-   [<span data-ttu-id="b6e49-106">支援的語言</span><span class="sxs-lookup"><span data-stu-id="b6e49-106">Supported languages</span></span>](#supported-languages)
-   [<span data-ttu-id="b6e49-107">Helper 結構</span><span class="sxs-lookup"><span data-stu-id="b6e49-107">Helper structures</span></span>](#helper-structures)
-   [<span data-ttu-id="b6e49-108">記憶體管理程式庫</span><span class="sxs-lookup"><span data-stu-id="b6e49-108">Memory Management Library</span></span>](#memory-management-library)
-   [<span data-ttu-id="b6e49-109">支援的工具和程式庫</span><span class="sxs-lookup"><span data-stu-id="b6e49-109">Supported tools and libraries</span></span>](#supported-tools-and-libraries)
-   [<span data-ttu-id="b6e49-110">範例</span><span class="sxs-lookup"><span data-stu-id="b6e49-110">Samples</span></span>](#samples)
-   [<span data-ttu-id="b6e49-111">Debug 圖層</span><span class="sxs-lookup"><span data-stu-id="b6e49-111">Debug layer</span></span>](#debug-layer)
-   [<span data-ttu-id="b6e49-112">教育影片</span><span class="sxs-lookup"><span data-stu-id="b6e49-112">Educational videos</span></span>](#educational-videos)
-   [<span data-ttu-id="b6e49-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b6e49-113">Related topics</span></span>](#related-topics)

## <a name="development-environment"></a><span data-ttu-id="b6e49-114">開發環境</span><span class="sxs-lookup"><span data-stu-id="b6e49-114">Development environment</span></span>

<span data-ttu-id="b6e49-115">Direct3D 12 標頭和程式庫是 Windows 10 SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b6e49-115">The Direct3D 12 headers and libraries are part of the Windows 10 SDK.</span></span> <span data-ttu-id="b6e49-116">使用 Direct3D 12 不需要個別的下載或安裝。</span><span class="sxs-lookup"><span data-stu-id="b6e49-116">There is no separate download or installation required to use Direct3D 12.</span></span>

<span data-ttu-id="b6e49-117">在您安裝 Windows 10 SDK 軟體並 Visual Studio 之後，您的 Direct3D 12 程式設計環境設定就會完成。</span><span class="sxs-lookup"><span data-stu-id="b6e49-117">After you install the Windows 10 SDK software, and Visual Studio, the setup of your Direct3D 12 programming environment is complete.</span></span> <span data-ttu-id="b6e49-118">建議使用 Visual Studio 2019，因為它會包含 D3D12 圖形偵錯工具，但舊版的 Visual Studio 適用于程式開發。</span><span class="sxs-lookup"><span data-stu-id="b6e49-118">Visual Studio 2019 is recommended, as it will include the D3D12 graphics debugging tools, but earlier versions of Visual Studio will work for program development.</span></span>

<span data-ttu-id="b6e49-119">若要使用 [Direct3D 12 API](direct3d-12-reference.md)，請包含 D3d12 和 D3d12 的連結，或直接在 D3d12.dll 中查詢進入點。</span><span class="sxs-lookup"><span data-stu-id="b6e49-119">To use the [Direct3D 12 API](direct3d-12-reference.md), include D3d12.h and link to D3d12.lib, or query the entry points directly in D3d12.dll.</span></span>

<span data-ttu-id="b6e49-120">以下是可用的標頭和程式庫。</span><span class="sxs-lookup"><span data-stu-id="b6e49-120">The following headers and libraries are available.</span></span> <span data-ttu-id="b6e49-121">靜態程式庫的位置取決於電腦上執行的 Windows 10)  (32 位或64位的版本。</span><span class="sxs-lookup"><span data-stu-id="b6e49-121">The location of the static libraries depends on the version (32-bit or 64-bit) of Windows 10 that is running on your computer.</span></span>



| <span data-ttu-id="b6e49-122">標頭檔或文件庫檔案名</span><span class="sxs-lookup"><span data-stu-id="b6e49-122">Header or library file name</span></span> | <span data-ttu-id="b6e49-123">Description</span><span class="sxs-lookup"><span data-stu-id="b6e49-123">Description</span></span>                         | <span data-ttu-id="b6e49-124">安裝位置</span><span class="sxs-lookup"><span data-stu-id="b6e49-124">Install location</span></span>      |
|-----------------------------|-------------------------------------|-----------------------|
| <span data-ttu-id="b6e49-125">D3d12。h</span><span class="sxs-lookup"><span data-stu-id="b6e49-125">D3d12.h</span></span>                     | <span data-ttu-id="b6e49-126">Direct3D 12 API 標頭</span><span class="sxs-lookup"><span data-stu-id="b6e49-126">Direct3D 12 API header</span></span>              | <span data-ttu-id="b6e49-127">% WindowsSdkDir \\ 包含 \% WindowsSDKVersion% \\ \um</span><span class="sxs-lookup"><span data-stu-id="b6e49-127">%WindowsSdkDir\\Include\%WindowsSDKVersion%\\\um</span></span> |
| <span data-ttu-id="b6e49-128">D3d12 .lib</span><span class="sxs-lookup"><span data-stu-id="b6e49-128">D3d12.lib</span></span>                   | <span data-ttu-id="b6e49-129">靜態 Direct3D 12 API 存根程式庫</span><span class="sxs-lookup"><span data-stu-id="b6e49-129">Static Direct3D 12 API stub library</span></span> | <span data-ttu-id="b6e49-130">% WindowsSdkDir \\ Lib \% WindowsSDKVersion% \\ \um\arch</span><span class="sxs-lookup"><span data-stu-id="b6e49-130">%WindowsSdkDir\\Lib\%WindowsSDKVersion%\\\um\arch</span></span> |
| <span data-ttu-id="b6e49-131">D3d12.dll</span><span class="sxs-lookup"><span data-stu-id="b6e49-131">D3d12.dll</span></span>                   | <span data-ttu-id="b6e49-132">動態 Direct3D 12 API 程式庫</span><span class="sxs-lookup"><span data-stu-id="b6e49-132">Dynamic Direct3D 12 API library</span></span>     | <span data-ttu-id="b6e49-133">% WINDIR% \\ System32</span><span class="sxs-lookup"><span data-stu-id="b6e49-133">%WINDIR%\\System32</span></span>    |
| <span data-ttu-id="b6e49-134">D3d12SDKLayers。h</span><span class="sxs-lookup"><span data-stu-id="b6e49-134">D3d12SDKLayers.h</span></span>            | <span data-ttu-id="b6e49-135">Direct3D 12 debug 標頭</span><span class="sxs-lookup"><span data-stu-id="b6e49-135">Direct3D 12 debug header</span></span>            | <span data-ttu-id="b6e49-136">% WindowsSdkDir \\ 包含 \% WindowsSDKVersion% \\ \um</span><span class="sxs-lookup"><span data-stu-id="b6e49-136">%WindowsSdkDir\\Include\%WindowsSDKVersion%\\\um</span></span> |
| <span data-ttu-id="b6e49-137">D3d12SDKLayers.dll</span><span class="sxs-lookup"><span data-stu-id="b6e49-137">D3d12SDKLayers.dll</span></span>          | <span data-ttu-id="b6e49-138">動態 Direct3D 12 debug 程式庫</span><span class="sxs-lookup"><span data-stu-id="b6e49-138">Dynamic Direct3D 12 debug library</span></span>   | <span data-ttu-id="b6e49-139">% WINDIR% \\ System32</span><span class="sxs-lookup"><span data-stu-id="b6e49-139">%WINDIR%\\System32</span></span>    |



## <a name="supported-languages"></a><span data-ttu-id="b6e49-140">支援的語言</span><span class="sxs-lookup"><span data-stu-id="b6e49-140">Supported languages</span></span>

<span data-ttu-id="b6e49-141">C + + 是 Direct3D 12 開發的唯一支援語言，c # 和其他 .NET 語言則不受支援。</span><span class="sxs-lookup"><span data-stu-id="b6e49-141">C++ is the only supported language for Direct3D 12 development, C# and other .NET languages are not supported.</span></span>

## <a name="helper-structures"></a><span data-ttu-id="b6e49-142">Helper 結構</span><span class="sxs-lookup"><span data-stu-id="b6e49-142">Helper structures</span></span>

<span data-ttu-id="b6e49-143">有一些協助程式結構，特別是可讓您輕鬆地初始化多個 D3D12 結構。</span><span class="sxs-lookup"><span data-stu-id="b6e49-143">There are a number of helper structures that, in particular, make it easy to initialize a number of the D3D12 structures.</span></span> <span data-ttu-id="b6e49-144">這些結構和一些公用程式函式位於 D3dx12 標頭中。</span><span class="sxs-lookup"><span data-stu-id="b6e49-144">These structures, and some utility functions, are in the header D3dx12.h.</span></span> <span data-ttu-id="b6e49-145">此標頭是開放原始碼，且由開發人員視需要修改-請從 [D3D12 helper 程式庫](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12) 下載，並參考 [Helper 結構和函式以進行 D3D12](helper-structures-and-functions-for-d3d12.md)。</span><span class="sxs-lookup"><span data-stu-id="b6e49-145">This header is open source, and can be modified by a developer as required - download it from [The D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12) and refer to [Helper Structures and Functions for D3D12](helper-structures-and-functions-for-d3d12.md).</span></span>

## <a name="memory-management-library"></a><span data-ttu-id="b6e49-146">記憶體管理程式庫</span><span class="sxs-lookup"><span data-stu-id="b6e49-146">Memory Management Library</span></span>

<span data-ttu-id="b6e49-147">記憶體管理協助程式程式庫可供下載，您可以將它整合到您的應用程式，以更緊密地符合 D3D11 記憶體管理行為。</span><span class="sxs-lookup"><span data-stu-id="b6e49-147">A memory management helper library is available for download that you can integrate into your app to more closely match D3D11 memory management behavior.</span></span> <span data-ttu-id="b6e49-148">作為 D3D11 樣式管理程式庫，這對仍在使用 *認可資源* 樣式配置策略的應用程式最有效。</span><span class="sxs-lookup"><span data-stu-id="b6e49-148">As a D3D11 style management library, it is most effective with apps that are still using a *committed resource* style allocation strategy.</span></span> <span data-ttu-id="b6e49-149">尤其是，程式庫應該會被視為一種逐步執行的石頭，讓您在記憶體受限的案例中 (例如，低端記憶卡、4k、ultra 設定等) ，讓您回到 D3D11 高效能記憶體管理。</span><span class="sxs-lookup"><span data-stu-id="b6e49-149">In particular, the library should be seen as a stepping stone that will get you most of the way back to D3D11 performant memory management when in memory constrained scenarios (for example, low-end memory cards, 4k, ultra settings, and so on).</span></span> <span data-ttu-id="b6e49-150">D3D12 Api 可讓您透過 D3D11 取得更好的記憶體效率，不過這些技術可能是極具挑戰性且耗時的程式。</span><span class="sxs-lookup"><span data-stu-id="b6e49-150">D3D12 APIs do enable techniques that let you get even better memory efficiency over D3D11, though these techniques can be challenging and time consuming to implement.</span></span>

<span data-ttu-id="b6e49-151">請注意，此程式庫是進行中的工作，可能會隨著時間而變更。</span><span class="sxs-lookup"><span data-stu-id="b6e49-151">Note that this library is a work in progress and may change over time.</span></span> <span data-ttu-id="b6e49-152">使用下列連結來存取程式庫和範例。</span><span class="sxs-lookup"><span data-stu-id="b6e49-152">Use the links below to access the library, and samples.</span></span>

-   [<span data-ttu-id="b6e49-153">D3D12 常駐入門程式庫</span><span class="sxs-lookup"><span data-stu-id="b6e49-153">The D3D12 Residency Starter Library</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries)

## <a name="supported-tools-and-libraries"></a><span data-ttu-id="b6e49-154">支援的工具和程式庫</span><span class="sxs-lookup"><span data-stu-id="b6e49-154">Supported tools and libraries</span></span>

<span data-ttu-id="b6e49-155">下列程式庫都可以搭配 Direct3D 12 使用。</span><span class="sxs-lookup"><span data-stu-id="b6e49-155">The following libraries can all be used with Direct3D 12.</span></span>



| <span data-ttu-id="b6e49-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="b6e49-156">Library</span></span>                                                                                 |  <span data-ttu-id="b6e49-157">用途</span><span class="sxs-lookup"><span data-stu-id="b6e49-157">Purpose</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="b6e49-158">文件</span><span class="sxs-lookup"><span data-stu-id="b6e49-158">Documentation</span></span>                                                                                                           |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6e49-159">DirectX 12 的 DirectX 工具套件</span><span class="sxs-lookup"><span data-stu-id="b6e49-159">DirectX Tool Kit for DirectX 12</span></span>](https://github.com/Microsoft/DirectXTK12) | <span data-ttu-id="b6e49-160">用來撰寫通用 Windows 平臺 (UWP) 應用程式的 Direct3D 12 c + + 程式碼、適用于 Windows 10 的 Win32 桌面應用程式，以及 Xbox One 專屬應用程式的一系列 helper 類別。</span><span class="sxs-lookup"><span data-stu-id="b6e49-160">A substantial collection of helper classes for writing Direct3D 12 C++ code for Universal Windows Platform (UWP) apps, Win32 desktop applications for Windows 10, and Xbox One exclusive apps.</span></span>                                                                         | [<span data-ttu-id="b6e49-161">DirectX12TK wiki</span><span class="sxs-lookup"><span data-stu-id="b6e49-161">DirectX12TK wiki</span></span>](https://github.com/Microsoft/DirectXTK12/wiki)                                          |
| [<span data-ttu-id="b6e49-162">DirectXTex</span><span class="sxs-lookup"><span data-stu-id="b6e49-162">DirectXTex</span></span>](https://github.com/Microsoft/DirectXTex)                      | <span data-ttu-id="b6e49-163">您可以使用此功能來讀取和寫入 DDS 檔案，以及執行各種材質內容處理作業，包括調整大小、格式轉換、mip 對應產生、針對 Direct3D 執行時間材質資源封鎖壓縮，以及將高度對應到一般地圖的轉換。</span><span class="sxs-lookup"><span data-stu-id="b6e49-163">Use this for reading and writing DDS files, and performing various texture content processing operations including resizing, format conversion, mip-map generation, block compression for Direct3D runtime texture resources, and height-map to normal-map conversion.</span></span> | [<span data-ttu-id="b6e49-164">DirectXTex wiki</span><span class="sxs-lookup"><span data-stu-id="b6e49-164">DirectXTex wiki</span></span>](https://github.com/Microsoft/DirectXTex/wiki)                                            |
| [<span data-ttu-id="b6e49-165">DirectXMesh</span><span class="sxs-lookup"><span data-stu-id="b6e49-165">DirectXMesh</span></span>](https://github.com/Microsoft/DirectXMesh)                   | <span data-ttu-id="b6e49-166">您可使用此值來執行各種幾何內容處理作業，包括產生法線和正切框架、三角形相鄰計算和頂點快取優化。</span><span class="sxs-lookup"><span data-stu-id="b6e49-166">Use this for performing various geometry content processing operations including generating normals and tangent frames, triangle adjacency computations, and vertex cache optimization.</span></span>                                                                                | [<span data-ttu-id="b6e49-167">DirectXMesh wiki</span><span class="sxs-lookup"><span data-stu-id="b6e49-167">DirectXMesh wiki</span></span>](https://github.com/Microsoft/DirectXMesh/wiki)                                          |
| [<span data-ttu-id="b6e49-168">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="b6e49-168">DirectXMath</span></span>](https://github.com/Microsoft/DirectXMath)                     | <span data-ttu-id="b6e49-169">支援向量、純量、矩陣、四元數及許多其他數學運算的大量協助程式類別和方法。</span><span class="sxs-lookup"><span data-stu-id="b6e49-169">A large number of helper classes and methods to support vectors, scalars, matrices, quaternions, and many other mathematical operations.</span></span>                                                                                                                               | [<span data-ttu-id="b6e49-170">MSDN 上的 DirectXMath 檔</span><span class="sxs-lookup"><span data-stu-id="b6e49-170">DirectXMath documentation at MSDN</span></span>](/windows/desktop/dxmath/ovw-xnamath-progguide) |
| [<span data-ttu-id="b6e49-171">UVAtlas</span><span class="sxs-lookup"><span data-stu-id="b6e49-171">UVAtlas</span></span>](https://github.com/Microsoft/UVAtlas)                         | <span data-ttu-id="b6e49-172">使用此來建立和封裝 isochart 材質塔。</span><span class="sxs-lookup"><span data-stu-id="b6e49-172">Use this for creating and packing an isochart texture atlas.</span></span>                                                                                                                                                                                                           | [<span data-ttu-id="b6e49-173">UVAtlas wiki</span><span class="sxs-lookup"><span data-stu-id="b6e49-173">UVAtlas wiki</span></span>](https://github.com/Microsoft/UVAtlas/wiki)                                                  |



 

## <a name="samples"></a><span data-ttu-id="b6e49-174">範例</span><span class="sxs-lookup"><span data-stu-id="b6e49-174">Samples</span></span>

<span data-ttu-id="b6e49-175">如需工作 D3D12 範例的清單，以及如何尋找和執行這些範例，請參閱 [工作範例](working-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="b6e49-175">For a list of working D3D12 samples and how to locate and run them, refer to [Working Samples](working-samples.md).</span></span>

<span data-ttu-id="b6e49-176">如需如何加入程式碼以啟用特定功能的逐步解說解說，請參閱 [D3D12 程式碼逐步解說-解說](d3d12-code-walk-throughs.md)。</span><span class="sxs-lookup"><span data-stu-id="b6e49-176">For walk-throughs on how to add code to enable particular features, refer to [D3D12 Code Walk-Throughs](d3d12-code-walk-throughs.md).</span></span>

## <a name="debug-layer"></a><span data-ttu-id="b6e49-177">Debug 圖層</span><span class="sxs-lookup"><span data-stu-id="b6e49-177">Debug layer</span></span>

<span data-ttu-id="b6e49-178">Debug 層提供大量的額外參數和一致性驗證 (例如驗證著色器連結和資源系結、驗證參數一致性，以及報告錯誤描述) 。</span><span class="sxs-lookup"><span data-stu-id="b6e49-178">The debug layer provides extensive additional parameter and consistency validation (such as validating shader linkage and resource binding, validating parameter consistency, and reporting error descriptions).</span></span>

> [!Note]  
> <span data-ttu-id="b6e49-179">針對 Windows 10，若要建立支援 debug 層的裝置，請啟用 [圖形工具] 選用功能。</span><span class="sxs-lookup"><span data-stu-id="b6e49-179">For Windows 10, to create a device that supports the debug layer, enable the "Graphics Tools" optional feature.</span></span> <span data-ttu-id="b6e49-180">移至 [設定] 面板中的 [系統、應用程式 & 功能]、[管理選擇性功能]、[新增功能]，然後尋找 [圖形工具]。</span><span class="sxs-lookup"><span data-stu-id="b6e49-180">Go to the Settings panel, under System, Apps & features, Manage optional Features, Add a feature, and then look for "Graphics Tools".</span></span>

<span data-ttu-id="b6e49-181">預設會在 d3d12 中包含支援調試層（D3D12SDKLayers）所需的標頭。</span><span class="sxs-lookup"><span data-stu-id="b6e49-181">The header required to support the debugging layer, D3D12SDKLayers.h, is included by default from d3d12.h.</span></span>

<span data-ttu-id="b6e49-182">當 debug 圖層列出記憶體流失時，它會輸出物件介面指標清單及其易記名稱。</span><span class="sxs-lookup"><span data-stu-id="b6e49-182">When the debug layer lists memory leaks, it outputs a list of object interface pointers along with their friendly names.</span></span> <span data-ttu-id="b6e49-183">預設的易記名稱是「 &lt; 未命名」 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="b6e49-183">The default friendly name is "&lt;unnamed&gt;".</span></span> <span data-ttu-id="b6e49-184">您可以使用 [**ID3D12Object：： SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) 方法來設定易記名稱。</span><span class="sxs-lookup"><span data-stu-id="b6e49-184">You can set the friendly name by using the [**ID3D12Object::SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) method.</span></span> <span data-ttu-id="b6e49-185">一般而言，您應該從生產版本編譯這些呼叫。</span><span class="sxs-lookup"><span data-stu-id="b6e49-185">Typically, you should compile these calls out of your production version.</span></span>

<span data-ttu-id="b6e49-186">建議您使用 debug 層來將您的應用程式進行偵錯工具，以確保這些應用程式的錯誤和警告都已清除。</span><span class="sxs-lookup"><span data-stu-id="b6e49-186">We recommend that you use the debug layer to debug your apps to ensure that they are clean of errors and warnings.</span></span> <span data-ttu-id="b6e49-187">Debug 層可協助您撰寫 Direct3D 12 程式碼。</span><span class="sxs-lookup"><span data-stu-id="b6e49-187">The debug layer helps you write Direct3D 12 code.</span></span> <span data-ttu-id="b6e49-188">此外，當您使用 debug 圖層時，您的產能會增加，因為您可以立即查看其來源的隱匿轉譯錯誤或甚至是黑色畫面的原因。</span><span class="sxs-lookup"><span data-stu-id="b6e49-188">In addition, your productivity can increase when you use the debug layer because you can immediately see the causes of obscure rendering errors or even black screens at their source.</span></span> <span data-ttu-id="b6e49-189">Debug 層提供許多問題的警告。</span><span class="sxs-lookup"><span data-stu-id="b6e49-189">The debug layer provides warnings for many issues.</span></span> <span data-ttu-id="b6e49-190">例如︰</span><span class="sxs-lookup"><span data-stu-id="b6e49-190">For example:</span></span>

-   <span data-ttu-id="b6e49-191">忘記設定材質，但在您的圖元著色器中讀取它。</span><span class="sxs-lookup"><span data-stu-id="b6e49-191">Forgot to set a texture but read from it in your pixel shader.</span></span>
-   <span data-ttu-id="b6e49-192">輸出深度，但沒有系結的深度樣板狀態。</span><span class="sxs-lookup"><span data-stu-id="b6e49-192">Output depth but have no depth-stencil state bound.</span></span>
-   <span data-ttu-id="b6e49-193">材質建立失敗，INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="b6e49-193">Texture creation failed with INVALIDARG.</span></span>

<span data-ttu-id="b6e49-194">設定編譯器定義 D3DCOMPILE \_ DEBUG，告知 HLSL 編譯器將 DEBUG 資訊納入著色器 blob 中。</span><span class="sxs-lookup"><span data-stu-id="b6e49-194">Set the compiler define D3DCOMPILE\_DEBUG to tell the HLSL compiler to include debug information into the shader blob.</span></span>

``` syntax
#define D3DCOMPILE_DEBUG 1
```

<span data-ttu-id="b6e49-195">如需所有 debug 介面和方法的詳細資訊，請參閱 [Debug Layer 參考](direct3d-12-sdklayers-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="b6e49-195">For details of all the debug interfaces and methods, refer to the [Debug Layer Reference](direct3d-12-sdklayers-reference.md).</span></span>

<span data-ttu-id="b6e49-196">如需有關使用 debug layer 的總覽資訊，請參閱 [瞭解 D3D12 的調試層](understanding-the-d3d12-debug-layer.md)。</span><span class="sxs-lookup"><span data-stu-id="b6e49-196">For overview information on using the debug layer, refer to [Understanding the D3D12 Debug Layer](understanding-the-d3d12-debug-layer.md).</span></span>

## <a name="educational-videos"></a><span data-ttu-id="b6e49-197">教育影片</span><span class="sxs-lookup"><span data-stu-id="b6e49-197">Educational videos</span></span>

<span data-ttu-id="b6e49-198">[DirectX advanced learning 影片教學課程](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)有許多 Direct3D 12 和 Windows 10 相關影片，包括圖形偵錯工具的影片，以及報告圖形 bug。</span><span class="sxs-lookup"><span data-stu-id="b6e49-198">There are a number of Direct3D 12 and Windows 10 related videos at [DirectX advanced learning video tutorials](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA), including videos on graphics debugging tools, and reporting graphics bugs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6e49-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="b6e49-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6e49-200">瞭解 Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b6e49-200">Understanding Direct3D 12</span></span>](directx-12-getting-started.md)
</dt> </dl>

 

 