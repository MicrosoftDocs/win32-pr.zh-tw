---
title: Direct3D 11.1 功能
description: 以下是在 Direct3D 11.1 中新增的功能，其中包含在 Windows 8、Windows RT 和 Windows Server 2012 中。
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dece9ed6e0a40ade28857277c344be0e9f2e7ce1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682406"
---
# <a name="direct3d-111-features"></a>Direct3D 11.1 功能

以下是在 Direct3D 11.1 中新增的功能，其中包含在 Windows 8、Windows RT 和 Windows Server 2012 中。 您可以透過 windows 7 的平臺[更新，在](/windows/desktop/direct3darticles/platform-update-for-windows-7)windows 7 和 windows Server 2008 R2 上取得[Direct3D 11.1](direct3d-11-features.md)的部分支援（可透過[windows 7 的平臺更新取得](https://support.microsoft.com/kb/2670838)）。

-   [著色器追蹤和編譯器增強功能](#shader-tracing-and-compiler-enhancements)
-   [Direct3D 裝置共用](#direct3d-device-sharing)
-   [檢查支援新的 Direct3D 11.1 功能和格式](#check-support-of-new-direct3d-111-features-and-formats)
-   [使用 HLSL 最小有效位數](#use-hlsl-minimum-precision)
-   [在功能層級9和更高版本上，指定 HLSL 中的使用者剪輯平面](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [建立比著色器可以存取的大型常數緩衝區](#create-larger-constant-buffers-than-a-shader-can-access)
-   [在呈現目標中使用邏輯作業](#use-logical-operations-in-a-render-target)
-   [強制範例計數建立轉譯器狀態](#force-the-sample-count-to-create-a-rasterizer-state)
-   [使用著色器處理影片資源](#process-video-resources-with-shaders)
-   [共用 Texture2D 資源的擴充支援](#extended-support-for-shared-texture2d-resources)
-   [使用新的複製選項變更子資源](#change-subresources-with-new-copy-options)
-   [捨棄資源和資源檢視](#discard-resources-and-resource-views)
-   [支援更大量的 UAVs](#support-a-larger-number-of-uavs)
-   [將常數緩衝區的子範圍系結至著色器](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [取出系結至著色器的常數緩衝區子範圍](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [清除所有或部分資源檢視](#clear-all-or-part-of-a-resource-view)
-   [不覆寫的動態緩衝區對應 SRVs \_](/windows)
-   [在每個管線階段使用 UAVs](#use-uavs-at-every-pipeline-stage)
-   [對變形裝置的擴充支援](#extended-support-for-warp-devices)
-   [在會話0進程中使用 Direct3D](#use-direct3d-in-session-0-processes)
-   [功能層級9的陰影緩衝區支援](#support-for-shadow-buffer-on-feature-level-9)
-   [相關主題](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>著色器追蹤和編譯器增強功能

Direct3D 11.1 可讓您使用著色器追蹤，以確保您的程式碼會如預期執行，如果不是，您可以找出並修復問題。 適用于 Windows 8 的 Windows 軟體開發套件 (SDK) 包含 HLSL 編譯器增強功能。 著色器追蹤和 HLSL 編譯器會在 D3dcompilernn.dll 中執行 \_ 。

著色器追蹤 API 和 HLSL 編譯器的增強功能包含下列方法和函式。

-   [**ID3D11RefDefaultTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions)
-   [**ID3D11RefTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions)
-   [**ID3D11TracingDevice::SetShaderTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11TracingDevice::SetShaderTrackingOptionsByType**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11ShaderTraceFactory::CreateShaderTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace)
-   [**ID3D11ShaderTrace::TraceReady**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-traceready)
-   [**ID3D11ShaderTrace::ResetTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace)
-   [**ID3D11ShaderTrace::GetTraceStats**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats)
-   [**ID3D11ShaderTrace：:P SSelectStamp**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-psselectstamp)
-   [**ID3D11ShaderTrace::GetInitialRegisterContents**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents)
-   [**ID3D11ShaderTrace::GetStep**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getstep)
-   [**ID3D11ShaderTrace::GetWrittenRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister)
-   [**ID3D11ShaderTrace::GetReadRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getreadregister)
-   [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2)
-   [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)
-   [**D3DDisassemble11Trace**](/windows/desktop/direct3dhlsl/d3ddisassemble11trace)
-   [**D3DDisassembleRegion**](/windows/desktop/direct3dhlsl/d3ddisassembleregion)
-   [**D3DGetTraceInstructionOffsets**](/windows/desktop/direct3dhlsl/d3dgettraceinstructionoffsets)
-   [**D3DReadFileToBlob**](/windows/desktop/direct3dhlsl/d3dreadfiletoblob)
-   [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart)
-   [**D3DWriteBlobToFile**](/windows/desktop/direct3dhlsl/d3dwriteblobtofile)

D3dcompiler .lib 程式庫需要 D3dcompiler \_nn.dll。 此 DLL 不是 Windows 8 的一部分;它位於 Windows SDK 的 \\ bin 資料夾中，Windows 8 以及 Fxc.exe 命令列版本的 HLSL 編譯器。

> [!Note]  
> 雖然您可以使用此程式庫和 DLL 組合進行開發，但無法部署使用此組合的 Windows Store 應用程式。 因此，您必須改為先編譯 HLSL 著色器，再寄送您的 Windows Store 應用程式。 您可以將 HLSL 編譯二進位檔寫入磁片，或編譯器可以產生包含著色器 blob 資料之靜態位元組陣列的標頭。 您可以使用 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) 介面來存取 blob 資料。 若要開發您的 Windows Store 應用程式，請呼叫 [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) 或 [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) 來編譯原始 HLSL 來源，然後將產生的 Blob 資料摘要至 Direct3D。

 

## <a name="direct3d-device-sharing"></a>Direct3D 裝置共用

Direct3D 11.1 可讓 Direct3D 10 Api 和 Direct3D 11 Api 使用一個基礎轉譯裝置。

此 Direct3D 11.1 功能包含下列方法和介面。

-   [**ID3D11Device1::CreateDeviceCoNtextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceCoNtext1::SwapDeviceCoNtextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceCoNtextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>檢查支援新的 Direct3D 11.1 功能和格式

Direct3D 11.1 可讓您檢查圖形驅動程式可能支援的新功能，以及裝置上支援格式的新方式。 Microsoft DirectX Graphic Infrastructure (DXGI) 1.2 也會指定新的 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 值。

此 Direct3D 11.1 功能包含下列 API。

-   [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) 與 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)、 [**D3D11 \_ 功能 \_ 資料 \_ 結構 \_ 資訊**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info)、 [**D3D11 \_ 功能 \_ 資料 \_ D3D9 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options)、 [**D3D11 \_ 功能 \_ 資料 \_ 著色器 \_ 最小 \_ 精確度 \_ 支援**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)，以及 [**D3D11 \_ 功能 \_ 資料 \_ D3D9 \_ 陰影 \_ 支援**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support) 結構
-   具有 D3D11 格式的 [**ID3D11Device：： CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) [**\_ \_ 支援 \_ 解碼器 \_ 輸出**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)、 [**D3D11 \_ 格式 \_ 支援 \_ 視頻 \_ 處理器 \_ 輸出**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)、 [**D3D11 \_ 格式 \_ 支援 \_ 視頻 \_ 處理器 \_ 輸入**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)、 [**D3D11 \_ 格式 \_ 支援 \_ 影片 \_ 編碼器**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)，以及 [**D3D11 \_ 格式 \_ SUPPORT2 \_ 輸出 \_ 合併 \_ 邏輯 \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

## <a name="use-hlsl-minimum-precision"></a>使用 HLSL 最小有效位數

從 Windows 8 開始，圖形驅動程式可以使用任何有效位數大於或等於指定的位精確度，來執行最小有效位數 HLSL 純量 [資料類型](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) 。 當您的 HLSL 最小精確度著色器程式碼在實 HLSL 最小精確度的硬體上使用時，您會使用較少的記憶體頻寬，因此您也會使用較少的系統電源。

您可以藉由呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) 與 [**D3D11 \_ 功能 \_ 著色器的 \_ 最小 \_ 精確度 \_ 支援**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) 值，來查詢圖形驅動程式所提供的最小精確度支援。 在這個 **ID3D11Device：： CheckFeatureSupport** 呼叫中，將指標傳遞至 [**D3D11 \_ 功能 \_ 資料 \_ 著色器的 \_ 最小 \_ 精確度 \_ 支援**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) 結構， **ID3D11Device：： CheckFeatureSupport** 會填滿驅動程式支援的最小精確度層級（適用于圖元著色器階段和其他著色器階段）。 傳回的資訊只會指出圖形硬體可以用比標準的32位浮點數有效位數更低的精確度來執行 HLSL 作業，但不保證圖形硬體會實際以較低的精確度執行。

您不需要撰寫多個執行和不使用最小精確度的著色器。 相反地，如果圖形驅動程式回報不支援任何最小有效位數，則建立具有最小精確度的著色器，且最小精確度變數的行為會是完整的32位有效位數。 如需 HLSL 最小精確度的詳細資訊，請參閱 [使用 HLSL 最小有效位數](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision)。

HLSL 最小精確度著色器無法在 Windows 8 之前的作業系統上運作。

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>在功能層級9和更高版本上，指定 HLSL 中的使用者剪輯平面

從 Windows 8 開始，您可以 [在 HLSL 函](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax)式宣告（而不是 [SV \_ ClipDistance](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) ）中使用 **clipplanes** 函式屬性，讓您的著色器能在 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md)9 \_ x 以及功能層級10和更高版本上運作。 如需詳細資訊，請參閱「 [功能等級9硬體上的使用者剪輯平面](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)」。

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>建立比著色器可以存取的大型常數緩衝區

Direct3D 11.1 可讓您建立大於著色器可存取之常數緩衝區大小上限的常數緩衝區， (4096 32 位 \* 4-元件常數– 64kb) 。 稍後，當您將緩衝區系結至管線時（例如透過 [**PSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) 或 [**PSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)），您可以指定可供著色器存取且符合4096限制的緩衝區範圍。

Direct3D 11.1 會更新這項功能的 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) 方法。

## <a name="use-logical-operations-in-a-render-target"></a>在呈現目標中使用邏輯作業

Direct3D 11.1 可讓您使用邏輯作業，而不是在轉譯目標中混合。 不過，您無法在多個呈現目標之間混合使用邏輯作業。

此 Direct3D 11.1 功能包含下列 API。

-   [**ID3D11Device1：： CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1)與 [ **D3D11 \_ 邏輯 \_ OP**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>強制範例計數建立轉譯器狀態

當您建立轉譯器狀態時，Direct3D 11.1 可讓您指定強制取樣計數。

此 Direct3D 11.1 功能包含下列 API。

-   [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> 如果您想要將取樣計數強制轉譯為1或更大，您必須遵循下列指導方針：
>
> -   不要系結深度樣板的觀點。
> -   停用深度測試。
> -   確定著色器不會輸出深度。
> -   如果您有任何系結目標視圖系結 (D3D11 系結轉譯 [**\_ \_ \_ 目標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)) ，而您強制取樣計數大於1，請確定每個轉譯目標只有一個樣本。
> -   請勿以取樣頻率操作著色器。 因此， [**ID3D11ShaderReflection：： IsSampleFrequencyShader**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader) 會傳回 **FALSE**。
>
> 否則，轉譯行為未定義。 如需如何設定深度範本的詳細資訊，請參閱設定 [Depth-Stencil 功能](d3d10-graphics-programming-guide-depth-stencil.md)。

 

## <a name="process-video-resources-with-shaders"></a>使用著色器處理影片資源

Direct3D 11.1 可讓您建立 (SRV/RTV/UAV) 至影片資源的視圖，讓 Direct3D 著色器可以處理這些影片資源。 基礎影片資源的格式會限制視圖可使用的格式。 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列舉包含新的影片資源格式值。 這些 **DXGI \_ 格式** 值會指定您可以建立的有效視圖格式，以及 Direct3D 11.1 執行時間如何對應此視圖。 您可以為相同介面的不同部分建立多個視圖，根據格式，視圖的大小可能會彼此不同。

Direct3D 11.1 會更新這項功能的下列方法。

-   [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)
-   [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview)
-   [**ID3D11Device::CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview)

## <a name="extended-support-for-shared-texture2d-resources"></a>共用 Texture2D 資源的擴充支援

Direct3D 11.1 可保證您可以共用以特定資源類型和格式建立的 Texture2D 資源。 若要共用 Texture2D 資源，請使用 [**D3D11 \_ 資源的 \_ 其他 \_ 共用**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)、 [**D3D11 資源的 \_ \_ 其他 \_ 共用 \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)，或 D3D11 資源的其他共用 **\_ \_ \_ \_ KEYEDMUTEX** 和 [**D3D11 \_ 資源 \_ 其他 \_ 共用 \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 的組合 (新的 Windows 8) 旗標在建立這些資源時使用。

Direct3D 11.1 保證您可以共用以這些 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 值建立的 Texture2D 資源：

-   DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM
-   DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB
-   DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM
-   DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB
-   DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM
-   DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB
-   DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM
-   DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT

此外，Direct3D 11.1 可保證您可共用以1、陣列大小為1的 mipmap 層級、陣列大小為1的系結旗標、D3D11 系結 [**\_ \_ 著色器 \_ 資源**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) 的系結旗標和 D3D11 系結轉譯 [**\_ \_ \_ 目標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) 的系結 Texture2D 資源、使用預設 ([**D3D11 \_ 使用方式 \_ 預設**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) ，以及僅限這些 [**D3D11 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 標值：

-   [**D3D11 \_ 資源 \_ 其他 \_ 共用**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ 資源的 \_ 其他 \_ 共用 \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ 資源的 \_ 其他 \_ 共用 \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ 與資源的 \_ 其他 \_ GDI \_ 相容**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Direct3D 11.1 可讓您共用更多的 Texture2D 資源類型和格式。 您可以藉由呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) 與 [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) 值，來查詢圖形驅動程式和硬體是否支援擴充 Texture2D 資源分享。 在這個 **ID3D11Device：： CheckFeatureSupport** 呼叫中，將指標傳遞至 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) 結構。 如果硬體和驅動程式支援擴充的 D3D11 資源分享， **ID3D11Device：： CheckFeatureSupport** 會將 **D3D11 \_ FEATURE \_ DATA \_ Texture2D \_ 選項** 的 **ExtendedResourceSharing** 成員設定為 **TRUE** 。

如果 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)在 **ExtendedResourceSharing** 中傳回 **TRUE** ，您就可以共用以這些 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)值建立的資源：

-   DXGI \_ 格式 \_ R32G32B32A32 無別 \_
-   DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT
-   DXGI \_ 格式 \_ R32G32B32A32 \_ UINT
-   DXGI \_ 格式 \_ R32G32B32A32 \_ 聖
-   DXGI \_ 格式 \_ R16G16B16A16 無別 \_
-   DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT
-   DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM
-   DXGI \_ 格式 \_ R16G16B16A16 \_ UINT
-   DXGI \_ 格式 \_ R16G16B16A16 \_ SNORM
-   DXGI \_ 格式 \_ R16G16B16A16 \_ 聖
-   DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM
-   DXGI \_ 格式 \_ R10G10B10A2 \_ UINT
-   DXGI \_ 格式 \_ R8G8B8A8 無別 \_
-   DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM
-   DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB
-   DXGI \_ 格式 \_ R8G8B8A8 \_ UINT
-   DXGI \_ 格式 \_ R8G8B8A8 \_ SNORM
-   DXGI \_ 格式 \_ R8G8B8A8 \_ 聖
-   DXGI \_ 格式 \_ B8G8R8A8 無別 \_
-   DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM
-   DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM
-   DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB
-   DXGI \_ 格式 \_ B8G8R8X8 無別 \_
-   DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB
-   DXGI \_ 格式 \_ R32 無別 \_
-   DXGI \_ 格式 \_ R32 \_ FLOAT
-   DXGI \_ 格式 \_ R32 \_ UINT
-   DXGI \_ 格式 \_ R32 \_ 聖
-   DXGI \_ 格式 \_ R16 無別 \_
-   DXGI \_ 格式 \_ R16 \_ FLOAT
-   DXGI \_ 格式 \_ R16 \_ UNORM
-   DXGI \_ 格式 \_ R16 \_ UINT
-   DXGI \_ 格式 \_ R16 \_ SNORM
-   DXGI \_ 格式 \_ R16 \_ 聖
-   DXGI \_ 格式 \_ R8 無別 \_
-   DXGI \_ 格式 \_ R8 \_ UNORM
-   DXGI \_ 格式 \_ R8 \_ UINT
-   DXGI \_ 格式 \_ R8 \_ SNORM
-   DXGI \_ 格式 \_ R8 \_ 聖
-   DXGI \_ 格式 \_ A8 \_ UNORM
-   DXGI \_ 格式 \_ AYUV
-   DXGI \_ 格式 \_ YUY2
-   DXGI \_ 格式 \_ NV12
-   DXGI \_ 格式 \_ NV11
-   DXGI \_ 格式 \_ P016
-   DXGI \_ 格式 \_ P010
-   DXGI \_ 格式 \_ Y216
-   DXGI \_ 格式 \_ Y210
-   DXGI \_ 格式 \_ Y416
-   DXGI \_ 格式 \_ Y410

如果 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)在 **ExtendedResourceSharing** 中傳回 **TRUE** ，您可以使用這些功能和旗標來共用您所建立的資源：

-   [**D3D11 \_ 使用方式 \_ 預設值**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**D3D11 系結 \_ \_ 著色器 \_ 資源**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 系結轉譯 \_ \_ \_ 目標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ 資源 \_ 其他 \_ 產生 \_ MIPS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 系結未 \_ \_ 排序 \_ 存取**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Mipmap 層級 (在2D 材質資源中) 的一或多個層級 (在 [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)的 **MipLevels** 成員中指定) 
-   2D 材質資源的陣列 ([**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)的 **ArraySize** 成員中指定的一或多個材質)  () 
-   [**D3D11 系結 \_ \_ 解碼器**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ 資源的 \_ 其他 \_ 受限制 \_ 內容**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ 資源 \_ 其他 \_ 限制 \_ 共用 \_ 資源**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ 資源 \_ 其他 \_ 限制 \_ 共用 \_ 資源 \_ 驅動程式**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> 當 **ExtendedResourceSharing** 為 **TRUE** 時，當您指定系結旗標以共用 Texture2D 資源時，會有更大的彈性。 圖形驅動程式和硬體不僅支援更多系結旗標，也支援更可能的系結旗標組合。 例如，您可以只指定 D3D11 系結轉譯 [**\_ \_ \_ 目標**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) 或沒有系結旗標等等。

 

即使 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)在 **ExtendedResourceSharing** 中傳回 **TRUE** ，您仍無法共用以這些功能和旗標建立的資源：

-   [**D3D11 系結 \_ \_ 深度樣板 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   以多重取樣消除鋸齒的2D 材質資源 (MSAA) 模式 (以 [**DXGI \_ 範例 \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) 指定) 
-   [**D3D11 \_ 資源 \_ 其他 \_ 資源的資源 \_ 夾具**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_使用 \_ 不可變**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)、 [**D3D11 \_ 使用 \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)或 [**D3D11 \_ 使用 \_ 暫存**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) (也就是可映射) 
-   [**D3D11 \_ 資源的 \_ 其他 \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>使用新的複製選項變更子資源

Direct3D 11.1 可讓您使用新的複製旗標來複製和更新子資源。 當您複製 subresource 時，來源和目的地資源可以相同，而且來源和目的地區域可以重迭。

此 Direct3D 11.1 功能包含下列 API。

-   [**ID3D11DeviceCoNtext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceCoNtext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>捨棄資源和資源檢視

Direct3D 11.1 可讓您從裝置內容中捨棄資源的資源和觀點。 這項新功能會通知 GPU，不再需要資源或資源檢視中的現有內容。

此 Direct3D 11.1 功能包含下列 API。

-   [**ID3D11DeviceCoNtext1：:D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceCoNtext1：:D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceCoNtext1：:D iscardView1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>支援更大量的 UAVs

當您將資源系結至 [輸出合併階段](d3d10-graphics-programming-guide-output-merger-stage.md) ，以及為未排序的資源設定 views 陣列時，Direct3D 11.1 可讓您使用更大量的 UAVs。

Direct3D 11.1 會更新這項功能的下列方法。

-   [**>id3d11devicecoNtext：： OMSetRenderTargetsAndUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**>id3d11devicecoNtext：： CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>將常數緩衝區的子範圍系結至著色器

Direct3D 11.1 可讓您系結常數緩衝區的子範圍，以供著色器存取。 您可以提供較大的常數緩衝區，並指定著色器可以使用的子範圍。

此 Direct3D 11.1 功能包含下列 API。

-   [**ID3D11DeviceCoNtext1::CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceCoNtext1：:D SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceCoNtext1::GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceCoNtext1::HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceCoNtext1：:P SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceCoNtext1::VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>取出系結至著色器的常數緩衝區子範圍

Direct3D 11.1 可讓您取得系結至著色器之常數緩衝區的子範圍。

此 Direct3D 11.1 功能包含下列 API。

-   [**ID3D11DeviceCoNtext1::CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceCoNtext1：:D SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceCoNtext1::GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceCoNtext1::HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceCoNtext1：:P SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceCoNtext1::VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>清除所有或部分資源檢視

Direct3D 11.1 可讓您清除 RTV、UAV 或 Texture2D surface) 的任何影片視圖 (的資源檢視。 您可以將相同的色彩值套用到此視圖的所有部分。

此 Direct3D 11.1 功能包含下列 API。

-   [**ID3D11DeviceCoNtext1::ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>不覆寫的動態緩衝區對應 SRVs \_

Direct3D 11.1 可讓您將著色器資源檢視 (SRV) 的動態緩衝區，與 D3D11 \_ map \_ WRITE \_ NO \_ OVERWRITE 對應。 Direct3D 11 和較早的執行時間會限制對應至頂點或索引緩衝區。

Direct3D 11.1 會更新這項功能的 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) 方法。

## <a name="use-uavs-at-every-pipeline-stage"></a>在每個管線階段使用 UAVs

Direct3D 11.1 可讓您在先前只用于圖元著色器和計算著色器的所有著色器階段，使用下列著色器模型5.0 指令。

-   [已 \_ 輸入的 dcl uav \_](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [已 \_ 原始的 dcl uav \_](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [\_uav \_ 結構化的 dcl](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [ld \_ raw](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [ld \_ 結構化](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [ld \_ uav \_ 類型](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [儲存 \_ 原始](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [商店 \_ 結構化](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [儲存 \_ uav \_ 類型](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [同步 \_ uglobal](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   所有的 atomics 和立即 atomics (例如，不可部分完成的 [ \_ 和](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) 和 imm 不可部分完成 [ \_ \_ 和](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-)) 

Direct3D 11.1 會更新這項功能的下列方法。

-   [**>id3d11devicecoNtext：： CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**>id3d11devicecoNtext：： CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**>id3d11devicecoNtext：： CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**>id3d11devicecoNtext：： CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**>id3d11devicecoNtext：： CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

這些指示存在於 ps \_ 5 \_ 0 和 cs \_ 5 0 的 Direct3D 11.0 中 \_ 。 由於 Direct3D 11.1 讓 UAVs 可在所有著色器階段使用，因此，所有著色器階段都可使用這些指示。

如果您傳遞已編譯的著色器 (VS/HS/DS/HS) ，而這些指示在每個 (階段) 都不支援 UAVs 的裝置上使用任何這些指示（例如 [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)），則建立著色器函式會失敗。 如果著色器嘗試使用的 UAV 位置超出硬體支援的一組 UAV 插槽，則建立著色器函式也會失敗。

這些指示所參考的 UAVs 會在所有管線階段間共用。 例如，在 [輸出合併階段](d3d10-graphics-programming-guide-output-merger-stage.md) 系結于插槽0的 UAV，可在位置0到 VS/HS/DS/GS/PS 之間取得。

UAV 您在指定的繪圖 () 內或跨著色器階段所發出的存取， \* 或是您在分派 () 內從計算著色器發出的存取 \* 權，並不保證會依照您發出的順序來完成。 但是，所有的 UAV 存取會在 () 結束時完成， \* 或分派 \* () 。

## <a name="extended-support-for-warp-devices"></a>對變形裝置的擴充支援

Direct3D 11.1 延伸了對 [變形](overviews-direct3d-11-devices-create-warp.md)裝置的支援，您可以在 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)的 *DriverType* 參數中傳遞 [**D3D \_ 驅動程式 \_ 類型 \_ 變形**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)來建立這些裝置。

從 Direct3D 11.1 變形裝置開始支援：

-   從9.1 到11.1 的所有 Direct3D[功能層級](overviews-direct3d-11-devices-downlevel-intro.md)
-   [計算著色](direct3d-11-advanced-stages-compute-shader.md)器和[鑲嵌](direct3d-11-advanced-stages-tessellation.md)式
-   共用的表面。 也就是說，您可以在變形裝置之間以及不同進程中的變形裝置之間完全共用表面。

變形裝置不支援這些選用功能：

-   [雙打](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [影片編碼或解碼](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [最小精確度著色器支援](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

當您在 (VM) Hyper-v 中執行虛擬機器，而圖形處理單元 (GPU) 停用或沒有顯示驅動程式時，您會得到一個易記的裝置，其易記名稱是「Microsoft 基本顯示器介面卡」。 此變形裝置可執行完整的 Windows 體驗，包括 DWM、Internet Explorer 和 Windows Store 應用程式。 此變形裝置也支援執行繼承應用程式，這些應用程式會使用 [DirectDraw](/windows/desktop/directdraw/directdraw) 或正在執行使用 direct3d 3 至 direct3d 11.1 的應用程式。

## <a name="use-direct3d-in-session-0-processes"></a>在會話0進程中使用 Direct3D

從 Windows 8 和 Windows Server 2012 開始，您可以在會話0進程中使用大部分的 Direct3D Api。

> [!Note]  
> 這些輸出、視窗、交換鏈和展示相關的 Api 無法在會話0進程中使用，因為它們不適用於會話0環境：
>
> -   [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)
> -   [**IDXGIFactory::GetWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-getwindowassociation)
> -   [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation)
> -   [**IDXGIAdapter::EnumOutputs**](/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs)
> -   [**ID3D11Debug::SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)
> -   [**ID3D11Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay)
> -   [**ID3D11Debug::SetSwapChain**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setswapchain)
> -   [**ID3D10Debug::SetFeatureMask**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask)
> -   [**ID3D10Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay)
> -   [**ID3D10Debug::SetSwapChain**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setswapchain)
> -   [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain)
> -   [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)
> -   [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)
>
> 如果您在會話0進程中呼叫上述其中一個 Api，它會傳回 [**\_ \_ \_ 目前無法 \_ 使用的 DXGI 錯誤**](/windows/desktop/direct3ddxgi/dxgi-error)。

 

## <a name="support-for-shadow-buffer-on-feature-level-9"></a>功能層級9的陰影緩衝區支援

使用 Direct3D 10 \_ 0 + 陰影緩衝區功能的子集來執行 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 x 的陰影效果 \_ 。 如需在功能層級 9 x 上執行陰影效果的相關資訊 \_ ，請參閱針對 [Direct3D 功能層級9執行陰影緩衝區](/previous-versions/windows/apps/jj262110(v=win.10))。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 的新功能](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 