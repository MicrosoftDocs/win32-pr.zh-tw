---
title: Direct3D 11.2 功能
description: 下列是在 Direct3D 11.2 中新增的功能，包括在 Windows 8.1、Windows RT 8.1 和 Windows Server 2012 R2 中。
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299b720bfb91297043c8e7d76beb50067eb64e17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971737"
---
# <a name="direct3d-112-features"></a><span data-ttu-id="93a8a-103">Direct3D 11.2 功能</span><span class="sxs-lookup"><span data-stu-id="93a8a-103">Direct3D 11.2 Features</span></span>

<span data-ttu-id="93a8a-104">下列是在 Direct3D 11.2 中新增的功能，包括在 Windows 8.1、Windows RT 8.1 和 Windows Server 2012 R2 中。</span><span class="sxs-lookup"><span data-stu-id="93a8a-104">The following functionality has been added in Direct3D 11.2, which is included with Windows 8.1, Windows RT 8.1, and Windows Server 2012 R2.</span></span>

-   [<span data-ttu-id="93a8a-105">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a8a-105">Tiled resources</span></span>](#tiled-resources)
    -   [<span data-ttu-id="93a8a-106">檢查磚資源支援</span><span class="sxs-lookup"><span data-stu-id="93a8a-106">Check tiled resources support</span></span>](#check-tiled-resources-support)
-   [<span data-ttu-id="93a8a-107">對變形裝置的擴充支援</span><span class="sxs-lookup"><span data-stu-id="93a8a-107">Extended support for WARP devices</span></span>](#extended-support-for-warp-devices)
-   [<span data-ttu-id="93a8a-108">標注圖形命令</span><span class="sxs-lookup"><span data-stu-id="93a8a-108">Annotate graphics commands</span></span>](#annotate-graphics-commands)
-   [<span data-ttu-id="93a8a-109">HLSL 著色器連結</span><span class="sxs-lookup"><span data-stu-id="93a8a-109">HLSL shader linking</span></span>](#hlsl-shader-linking)
    -   [<span data-ttu-id="93a8a-110">函數連結圖形 (FLG) </span><span class="sxs-lookup"><span data-stu-id="93a8a-110">Function linking graph (FLG)</span></span>](#function-linking-graph-flg)
-   [<span data-ttu-id="93a8a-111">收件匣 HLSL 編譯器</span><span class="sxs-lookup"><span data-stu-id="93a8a-111">Inbox HLSL compiler</span></span>](#inbox-hlsl-compiler)
-   [<span data-ttu-id="93a8a-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="93a8a-112">Related topics</span></span>](#related-topics)

## <a name="tiled-resources"></a><span data-ttu-id="93a8a-113">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a8a-113">Tiled resources</span></span>

<span data-ttu-id="93a8a-114">Direct3D 11.2 可讓您建立可視為大型邏輯資源（使用少量實體記憶體）的磚資源。</span><span class="sxs-lookup"><span data-stu-id="93a8a-114">Direct3D 11.2 lets you create tiled resources that can be thought of as large logical resources that use small amounts of physical memory.</span></span> <span data-ttu-id="93a8a-115">並排顯示的資源很有用 (例如) 與遊戲中的地形和應用程式 UI。</span><span class="sxs-lookup"><span data-stu-id="93a8a-115">Tiled resources are useful (for example) with terrain in games, and app UI.</span></span>

<span data-ttu-id="93a8a-116">藉由指定 D3D11 資源的「 [**\_ \_ 其他 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 並排顯示」旗標來建立並排的資源。</span><span class="sxs-lookup"><span data-stu-id="93a8a-116">Tiled resources are created by specifying the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> <span data-ttu-id="93a8a-117">若要使用已磚的資源，請使用下列 API：</span><span class="sxs-lookup"><span data-stu-id="93a8a-117">To work with tiled resource, use these API:</span></span>

-   [<span data-ttu-id="93a8a-118">**ID3D11Device2::GetResourceTiling**</span><span class="sxs-lookup"><span data-stu-id="93a8a-118">**ID3D11Device2::GetResourceTiling**</span></span>](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [<span data-ttu-id="93a8a-119">**ID3D11DeviceCoNtext2::UpdateTiles**</span><span class="sxs-lookup"><span data-stu-id="93a8a-119">**ID3D11DeviceContext2::UpdateTiles**</span></span>](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [<span data-ttu-id="93a8a-120">**ID3D11DeviceCoNtext2::UpdateTileMappings**</span><span class="sxs-lookup"><span data-stu-id="93a8a-120">**ID3D11DeviceContext2::UpdateTileMappings**</span></span>](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [<span data-ttu-id="93a8a-121">**ID3D11DeviceCoNtext2::CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="93a8a-121">**ID3D11DeviceContext2::CopyTiles**</span></span>](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [<span data-ttu-id="93a8a-122">**ID3D11DeviceCoNtext2::CopyTileMappings**</span><span class="sxs-lookup"><span data-stu-id="93a8a-122">**ID3D11DeviceContext2::CopyTileMappings**</span></span>](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [<span data-ttu-id="93a8a-123">**ID3D11DeviceCoNtext2::ResizeTilePool**</span><span class="sxs-lookup"><span data-stu-id="93a8a-123">**ID3D11DeviceContext2::ResizeTilePool**</span></span>](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [<span data-ttu-id="93a8a-124">**ID3D11DeviceCoNtext2::TiledResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="93a8a-124">**ID3D11DeviceContext2::TiledResourceBarrier**</span></span>](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   <span data-ttu-id="93a8a-125">**D3D11 \_使用 ID3D11Debug：： SetFeatureMask 的 DEBUG 功能停用並排顯示 \_ \_ \_ \_ 資源 \_ 對應 \_ 追蹤 \_ 和 \_ 驗證** 旗標 [](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)</span><span class="sxs-lookup"><span data-stu-id="93a8a-125">**D3D11\_DEBUG\_FEATURE\_DISABLE\_TILED\_RESOURCE\_MAPPING\_TRACKING\_AND\_VALIDATION** flag with [**ID3D11Debug::SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)</span></span>

<span data-ttu-id="93a8a-126">如需磚資源的詳細資訊，請參閱並排顯示的 [資源](tiled-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="93a8a-126">For more info about tiled resources, see [Tiled resources](tiled-resources.md).</span></span>

### <a name="check-tiled-resources-support"></a><span data-ttu-id="93a8a-127">檢查磚資源支援</span><span class="sxs-lookup"><span data-stu-id="93a8a-127">Check tiled resources support</span></span>

<span data-ttu-id="93a8a-128">使用已磚的資源之前，您必須先找出裝置是否支援磚的資源。</span><span class="sxs-lookup"><span data-stu-id="93a8a-128">Before you use tiled resources, you need to find out if the device supports tiled resources.</span></span> <span data-ttu-id="93a8a-129">以下是檢查磚資源支援的方式：</span><span class="sxs-lookup"><span data-stu-id="93a8a-129">Here's how you check for support for tiled resources:</span></span>


```C++
HRESULT hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    creationFlags,              // Set debug and Direct2D compatibility flags.
    featureLevels,              // List of feature levels this app can support.
    ARRAYSIZE(featureLevels),   // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_d3dFeatureLevel,         // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (SUCCEEDED(hr))
{
    D3D11_FEATURE_DATA_D3D11_OPTIONS1 featureData;
    DX::ThrowIfFailed(
        device->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS1, &featureData, sizeof(featureData))
        );

    m_tiledResourcesTier = featureData.TiledResourcesTier;
}
```



## <a name="extended-support-for-warp-devices"></a><span data-ttu-id="93a8a-130">對變形裝置的擴充支援</span><span class="sxs-lookup"><span data-stu-id="93a8a-130">Extended support for WARP devices</span></span>

<span data-ttu-id="93a8a-131">Direct3D 11.2 延伸了對 [變形](overviews-direct3d-11-devices-create-warp.md)裝置的支援，您可以在 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)的 *DriverType* 參數中傳遞 [**D3D \_ 驅動程式 \_ 類型 \_ 變形**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)來建立這些裝置。</span><span class="sxs-lookup"><span data-stu-id="93a8a-131">Direct3D 11.2 extends support for [WARP](overviews-direct3d-11-devices-create-warp.md) devices, which you create by passing [**D3D\_DRIVER\_TYPE\_WARP**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) in the *DriverType* parameter of [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice).</span></span> <span data-ttu-id="93a8a-132">Direct3D 11.2 中的變形軟體轉譯器加入了對 Direct3D [功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 11 1 的完整支援，包括並排顯示的 \_ [資源](#tiled-resources)、 [**IDXGIDevice3：： Trim**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim)、共用 BCn 表面、minblend 和地圖預設。</span><span class="sxs-lookup"><span data-stu-id="93a8a-132">The WARP software renderer in Direct3D 11.2 adds full support for Direct3D [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 11\_1, including [tiled resources](#tiled-resources), [**IDXGIDevice3::Trim**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim), shared BCn surfaces, minblend, and map default.</span></span> <span data-ttu-id="93a8a-133">HLSL 著色器中的[雙重](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)支援也已啟用，並支援 16x MSAA。</span><span class="sxs-lookup"><span data-stu-id="93a8a-133">[Double](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) support in HLSL shaders has also been enabled along with support for 16x MSAA.</span></span>

## <a name="annotate-graphics-commands"></a><span data-ttu-id="93a8a-134">標注圖形命令</span><span class="sxs-lookup"><span data-stu-id="93a8a-134">Annotate graphics commands</span></span>

<span data-ttu-id="93a8a-135">Direct3D 11.2 可讓您使用下列 API 將圖形命令加上批註：</span><span class="sxs-lookup"><span data-stu-id="93a8a-135">Direct3D 11.2 lets you annotate graphics commands with these API:</span></span>

-   [<span data-ttu-id="93a8a-136">**ID3D11DeviceCoNtext2::IsAnnotationEnabled**</span><span class="sxs-lookup"><span data-stu-id="93a8a-136">**ID3D11DeviceContext2::IsAnnotationEnabled**</span></span>](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [<span data-ttu-id="93a8a-137">**ID3D11DeviceCoNtext2::BeginEventInt**</span><span class="sxs-lookup"><span data-stu-id="93a8a-137">**ID3D11DeviceContext2::BeginEventInt**</span></span>](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [<span data-ttu-id="93a8a-138">**ID3D11DeviceCoNtext2::SetMarkerInt**</span><span class="sxs-lookup"><span data-stu-id="93a8a-138">**ID3D11DeviceContext2::SetMarkerInt**</span></span>](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [<span data-ttu-id="93a8a-139">**ID3D11DeviceCoNtext2::EndEvent**</span><span class="sxs-lookup"><span data-stu-id="93a8a-139">**ID3D11DeviceContext2::EndEvent**</span></span>](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a><span data-ttu-id="93a8a-140">HLSL 著色器連結</span><span class="sxs-lookup"><span data-stu-id="93a8a-140">HLSL shader linking</span></span>

<span data-ttu-id="93a8a-141">Windows 8.1 新增個別的 HLSL 著色器編譯和連結，可讓圖形程式設計人員建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</span><span class="sxs-lookup"><span data-stu-id="93a8a-141">Windows 8.1 adds separate compilation and linking of HLSL shaders, which allows graphics programmers to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run-time.</span></span> <span data-ttu-id="93a8a-142">這基本上相當於 C/c + + 個別編譯、程式庫和連結，並且可讓程式設計人員在有更多資訊可供完成計算時，撰寫先行編譯的 HLSL 程式碼。</span><span class="sxs-lookup"><span data-stu-id="93a8a-142">This is essentially an equivalent of C/C++ separate compilation, libraries, and linking, and it allows programmers to compose precompiled HLSL code when more information becomes available to finalize the computation.</span></span> <span data-ttu-id="93a8a-143">如需如何使用著色器連結的詳細資訊，請參閱 [使用著色器連結](/windows/desktop/direct3dhlsl/using-shader-linking)。</span><span class="sxs-lookup"><span data-stu-id="93a8a-143">For more info about how to use shader linking, see [Using shader linking](/windows/desktop/direct3dhlsl/using-shader-linking).</span></span>

<span data-ttu-id="93a8a-144">完成這些步驟，以在執行時間使用動態連結來建立最後的著色器。</span><span class="sxs-lookup"><span data-stu-id="93a8a-144">Complete these steps to create a final shader using dynamic linkage at run time.</span></span>

<span data-ttu-id="93a8a-145">**建立和使用著色器連結**</span><span class="sxs-lookup"><span data-stu-id="93a8a-145">**To create and use shader linking**</span></span>

1.  <span data-ttu-id="93a8a-146">建立代表連結內容的 [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) 連結器物件。</span><span class="sxs-lookup"><span data-stu-id="93a8a-146">Create a [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) linker object, which represents a linking context.</span></span> <span data-ttu-id="93a8a-147">單一內容無法用來產生多個著色器;連結內容用來產生單一著色器，然後將連結內容擲回。</span><span class="sxs-lookup"><span data-stu-id="93a8a-147">A single context can't be used to produce multiple shaders; a linking context is used to produce a single shader and then the linking context is thrown away.</span></span>
2.  <span data-ttu-id="93a8a-148">使用 [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) 從其程式庫 blob 載入和設定程式庫。</span><span class="sxs-lookup"><span data-stu-id="93a8a-148">Use [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) to load and set libraries from their library blobs.</span></span>
3.  <span data-ttu-id="93a8a-149">使用 [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) 載入和設定專案著色器 blob，或建立 [FLG 著色器](#function-linking-graph-flg)。</span><span class="sxs-lookup"><span data-stu-id="93a8a-149">Use [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) to load and set an entry shader blob, or create an [FLG shader](#function-linking-graph-flg).</span></span>
4.  <span data-ttu-id="93a8a-150">使用 [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)：：[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) 來建立 [**ID3D11ModuleInstance**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) 物件，然後在這些物件上呼叫函式，以將資源重新系結至其最終位置。</span><span class="sxs-lookup"><span data-stu-id="93a8a-150">Use [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)::[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) to create [**ID3D11ModuleInstance**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) objects, then call functions on these objects to rebind resources to their final slots.</span></span>
5.  <span data-ttu-id="93a8a-151">將程式庫新增至連結器，然後呼叫 [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)：：[**Link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) 來產生最終的著色器位元組程式碼，然後在執行時間中載入及使用，就像完整先行編譯和連結的著色器一樣。</span><span class="sxs-lookup"><span data-stu-id="93a8a-151">Add the libraries to the linker, then call [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)::[**Link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) to produce final shader byte code that can then be loaded and used in the runtime just like a fully precompiled and linked shader.</span></span>

### <a name="function-linking-graph-flg"></a><span data-ttu-id="93a8a-152">函數連結圖形 (FLG) </span><span class="sxs-lookup"><span data-stu-id="93a8a-152">Function linking graph (FLG)</span></span>

<span data-ttu-id="93a8a-153">Windows 8.1 也會新增函數連結圖形 (FLG) 。</span><span class="sxs-lookup"><span data-stu-id="93a8a-153">Windows 8.1 also adds the Function Linking Graph (FLG).</span></span> <span data-ttu-id="93a8a-154">您可以使用 FLG 來建立著色器，其中包含一連串預先編譯的函式調用，可將值傳遞給彼此。</span><span class="sxs-lookup"><span data-stu-id="93a8a-154">You can use FLG to construct shaders that consist of a sequence of precompiled function invocations that pass values to each other.</span></span> <span data-ttu-id="93a8a-155">使用 FLG 時，不需要撰寫 HLSL 並叫用 HLSL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="93a8a-155">When using the FLG, there is no need to write HLSL and invoke the HLSL compiler.</span></span> <span data-ttu-id="93a8a-156">相反地，會使用 c + + API 呼叫以程式設計方式指定著色器結構。</span><span class="sxs-lookup"><span data-stu-id="93a8a-156">Instead, the shader structure is specified programmatically using C++ API calls.</span></span> <span data-ttu-id="93a8a-157">FLG 節點代表輸入和輸出的簽章，以及先行編譯程式庫函數的調用。</span><span class="sxs-lookup"><span data-stu-id="93a8a-157">FLG nodes represent input and output signatures and invocations of precompiled library functions.</span></span> <span data-ttu-id="93a8a-158">註冊函式呼叫節點的順序會定義調用的順序。</span><span class="sxs-lookup"><span data-stu-id="93a8a-158">The order of registering the function-call nodes defines the sequence of invocations.</span></span> <span data-ttu-id="93a8a-159">必須先指定輸入簽章節點，而且必須最後指定輸出簽章節點。</span><span class="sxs-lookup"><span data-stu-id="93a8a-159">The input signature node must be specified first, while the output signature node must be specified last.</span></span> <span data-ttu-id="93a8a-160">FLG 邊緣定義值如何從一個節點傳遞至另一個節點。</span><span class="sxs-lookup"><span data-stu-id="93a8a-160">FLG edges define how values are passed from one node to another.</span></span> <span data-ttu-id="93a8a-161">傳遞值的資料類型必須相同;沒有隱含類型轉換。</span><span class="sxs-lookup"><span data-stu-id="93a8a-161">The data types of passed values must be the same; there is no implicit type conversion.</span></span> <span data-ttu-id="93a8a-162">Shape 和 swizzling 規則會遵循 HLSL 行為，而且值只能在這個順序中向前傳遞。</span><span class="sxs-lookup"><span data-stu-id="93a8a-162">Shape and swizzling rules follow the HLSL behavior and values can only be passed forward in this sequence.</span></span> <span data-ttu-id="93a8a-163">如需 FLG API 的詳細資訊，請參閱 [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph)。</span><span class="sxs-lookup"><span data-stu-id="93a8a-163">For info on the FLG API, see [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph).</span></span>

## <a name="inbox-hlsl-compiler"></a><span data-ttu-id="93a8a-164">收件匣 HLSL 編譯器</span><span class="sxs-lookup"><span data-stu-id="93a8a-164">Inbox HLSL compiler</span></span>

<span data-ttu-id="93a8a-165">HLSL 編譯器現在是 Windows 8.1 和更新版本上的收件匣。</span><span class="sxs-lookup"><span data-stu-id="93a8a-165">The HLSL compiler is now inbox on Windows 8.1 and later.</span></span> <span data-ttu-id="93a8a-166">現在，適用于著色器程式設計的大部分 Api 都可以在針對 Windows 8.1 和更新版本建立的 Windows Store 應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="93a8a-166">Now, most APIs for shader programming can be used in Windows Store apps that are built for Windows 8.1 and later.</span></span> <span data-ttu-id="93a8a-167">適用于著色器程式設計的許多 Api 無法在針對 Windows 8 所建立的 Windows Store 應用程式中使用;這些 Api 的參考頁面會以附注標示。</span><span class="sxs-lookup"><span data-stu-id="93a8a-167">Many APIs for shader programming couldn't be used in Windows Store apps that were built for Windows 8; the reference pages for these APIs were marked with a note.</span></span> <span data-ttu-id="93a8a-168">但某些著色器 Api (例如， [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)) 仍然只能用來開發 windows store 應用程式，而不能用於您提交至 windows 市集中的應用程式;這些 Api 的參考頁面仍會以附注標示。</span><span class="sxs-lookup"><span data-stu-id="93a8a-168">But some shader APIs (for example, [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)) can still only be used to develop Windows Store apps, and not in apps that you submit to the Windows Store; the reference pages for these APIs are still marked with a note.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93a8a-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="93a8a-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93a8a-170">Direct3D 11 的新功能</span><span class="sxs-lookup"><span data-stu-id="93a8a-170">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 