---
title: 例外狀況
description: 本主題說明在舊版硬體上使用 Direct3D 11 時的例外狀況。
ms.assetid: b3f85036-8572-40ee-b522-3b677443b840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97920ae42347cf618b22df82abc3b6e06bd5200d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316273"
---
# <a name="exceptions"></a><span data-ttu-id="90997-103">例外狀況</span><span class="sxs-lookup"><span data-stu-id="90997-103">Exceptions</span></span>

<span data-ttu-id="90997-104">Direct3D 11 的部分功能並非由功能等級完全指定。</span><span class="sxs-lookup"><span data-stu-id="90997-104">Some features of Direct3D 11 are not fully specified by feature levels.</span></span> <span data-ttu-id="90997-105">本主題說明在舊版硬體上使用 Direct3D 11 時的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="90997-105">This topic describes exceptions when using Direct3D 11 on downlevel hardware.</span></span> <span data-ttu-id="90997-106">這可能是在定義功能層級之後新增的功能 (而且需要更新的驅動程式) 或可能有不同的 Gpu 可執行廣泛的不同的執行方式。</span><span class="sxs-lookup"><span data-stu-id="90997-106">Perhaps a feature was added after the feature level is defined (and requires an updated driver) or perhaps different GPUs implement widely different implementations.</span></span> <span data-ttu-id="90997-107">功能層級的例外狀況可以收集至下列群組：</span><span class="sxs-lookup"><span data-stu-id="90997-107">Feature level exceptions can be gathered into the following groups:</span></span>

-   [<span data-ttu-id="90997-108">擴充格式</span><span class="sxs-lookup"><span data-stu-id="90997-108">Extended Formats</span></span>](#extended-formats)
-   [<span data-ttu-id="90997-109">多級化消除鋸齒</span><span class="sxs-lookup"><span data-stu-id="90997-109">Multisample Anti-Aliasing</span></span>](#multisample-anti-aliasing)
-   [<span data-ttu-id="90997-110">Texture2D 大小</span><span class="sxs-lookup"><span data-stu-id="90997-110">Texture2D Sizes</span></span>](#texture2d-sizes)
-   [<span data-ttu-id="90997-111">功能等級9的介面卡特殊行為</span><span class="sxs-lookup"><span data-stu-id="90997-111">Special Behavior of Adapters for Feature Level 9</span></span>](#special-behavior-of-adapters-for-feature-level-9)
-   [<span data-ttu-id="90997-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="90997-112">Related topics</span></span>](#related-topics)

<span data-ttu-id="90997-113">[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。</span><span class="sxs-lookup"><span data-stu-id="90997-113">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="extended-formats"></a><span data-ttu-id="90997-114">擴充格式</span><span class="sxs-lookup"><span data-stu-id="90997-114">Extended Formats</span></span>

<span data-ttu-id="90997-115">延伸格式是針對功能層級 10 \_ 0 和 10 1 新增至 direct3d 10.1 和 direct3d 11 的像素格式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="90997-115">An extended format is a pixel format added to Direct3D 10.1 and Direct3D 11 for feature levels 10\_0 and 10\_1.</span></span> <span data-ttu-id="90997-116">延伸格式需要 Direct3D 10 \_ 1 或以下) 的更新版驅動程式 (。</span><span class="sxs-lookup"><span data-stu-id="90997-116">An extended format requires an updated driver (for Direct3D 10\_1 or below).</span></span> <span data-ttu-id="90997-117">使用 [**ID3D11Device：： CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) 和 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) 來查詢這些延伸格式的支援。</span><span class="sxs-lookup"><span data-stu-id="90997-117">Use [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) and [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) to query for support for these extended formats.</span></span>

<span data-ttu-id="90997-118">延伸格式：</span><span class="sxs-lookup"><span data-stu-id="90997-118">An extended format:</span></span>

-   <span data-ttu-id="90997-119">新增每個元件資源8位 BGRA 順序的支援。</span><span class="sxs-lookup"><span data-stu-id="90997-119">Adds support for BGRA order of 8-bit per-component resources.</span></span>
-   <span data-ttu-id="90997-120">允許轉換整數值交換鏈緩衝區。</span><span class="sxs-lookup"><span data-stu-id="90997-120">Allows casting of an integer-value swap-chain buffer.</span></span> <span data-ttu-id="90997-121">這可讓應用程式新增或移除 \_ SRGB 尾碼，或轉譯成 XR \_ 偏差交換鏈。</span><span class="sxs-lookup"><span data-stu-id="90997-121">This allows an application to add or remove the \_SRGB suffix or render to an XR\_BIAS swap chain.</span></span>
-   <span data-ttu-id="90997-122">為 DXGI \_ 格式 \_ R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM 新增選擇性支援。</span><span class="sxs-lookup"><span data-stu-id="90997-122">Adds optional support for DXGI\_FORMAT\_R10G10B10\_XR\_BIAS\_A2\_UNORM.</span></span>
-   <span data-ttu-id="90997-123">保證 \_ 會顯示 DXGI 格式 \_ R16G16B16A16 \_ 浮點數交換鏈，如同所包含的資料未進行 sRGB 編碼。</span><span class="sxs-lookup"><span data-stu-id="90997-123">Guarantees that a DXGI\_FORMAT\_R16G16B16A16\_FLOAT swap chain is presented as if the data contained is not sRGB-encoded.</span></span>

<span data-ttu-id="90997-124">完整支援或不支援一組完整的延伸格式，但 XR \_ 偏差格式除外。</span><span class="sxs-lookup"><span data-stu-id="90997-124">The full set of extended formats are either fully supported or not supported, with the exception of the XR\_BIAS format.</span></span> <span data-ttu-id="90997-125">XR \_ 偏差格式為：</span><span class="sxs-lookup"><span data-stu-id="90997-125">The XR\_BIAS format is:</span></span>

-   <span data-ttu-id="90997-126">在任何9層級中不支援</span><span class="sxs-lookup"><span data-stu-id="90997-126">Unsupported in any 9 level</span></span>
-   <span data-ttu-id="90997-127">在 10 \_ 0 或 10 \_ 1 層級中為選擇性</span><span class="sxs-lookup"><span data-stu-id="90997-127">Optional in either the 10\_0 or 10\_1 level</span></span>
-   <span data-ttu-id="90997-128">保證為 11 \_ 0 層級</span><span class="sxs-lookup"><span data-stu-id="90997-128">Guaranteed at the 11\_0 level</span></span>

## <a name="multisample-anti-aliasing"></a><span data-ttu-id="90997-129">多級化消除鋸齒</span><span class="sxs-lookup"><span data-stu-id="90997-129">Multisample Anti-Aliasing</span></span>

<span data-ttu-id="90997-130">MSAA 的執行在 GPU 的執行上並不常見。</span><span class="sxs-lookup"><span data-stu-id="90997-130">MSAA implementations have little in common across GPU implementations.</span></span> <span data-ttu-id="90997-131">功能層級10.1 已新增一些定義完善的最小值，但在較低的功能層級上，必須使用 [**ID3D11Device：： CheckMultisampleQualityLevels**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkmultisamplequalitylevels)明確測試 MSAA。</span><span class="sxs-lookup"><span data-stu-id="90997-131">Feature Level 10.1 added some well-defined minima, but at lower feature levels, MSAA must be tested explicitly using [**ID3D11Device::CheckMultisampleQualityLevels**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkmultisamplequalitylevels).</span></span>

## <a name="texture2d-sizes"></a><span data-ttu-id="90997-132">Texture2D 大小</span><span class="sxs-lookup"><span data-stu-id="90997-132">Texture2D Sizes</span></span>

<span data-ttu-id="90997-133">功能等級保證可以建立最小大小，不過，應用程式可以建立較大的紋理，直到 GPU 支援的完整大小。</span><span class="sxs-lookup"><span data-stu-id="90997-133">A feature level guarantees that a minimum size can be created, however, an application can create larger textures up to the full size supported by the GPU.</span></span> <span data-ttu-id="90997-134">如果超過最大值，則應用程式應該會預期從 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) 之類的方法失敗。</span><span class="sxs-lookup"><span data-stu-id="90997-134">An application should expect failure from a method such as [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) if a maximum is exceeded.</span></span>

## <a name="special-behavior-of-adapters-for-feature-level-9"></a><span data-ttu-id="90997-135">功能等級9的介面卡特殊行為</span><span class="sxs-lookup"><span data-stu-id="90997-135">Special Behavior of Adapters for Feature Level 9</span></span>

<span data-ttu-id="90997-136">三個最低的功能層 \_ 級 \_ ： d3d 功能等級 \_ 9 \_ 1、D3D \_ 功能 \_ 層級 \_ 9 \_ 2 和 D3D \_ 功能 \_ 層級 \_ 9 \_ 3，共用通用的實作為範本，並將 [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) 引數視為作為 \[ \] 裝置建立的一部分來 D3D11CreateDevice AndSwapchain。</span><span class="sxs-lookup"><span data-stu-id="90997-136">The three lowest feature levels D3D\_FEATURE\_LEVEL\_9\_1, D3D\_FEATURE\_LEVEL\_9\_2 and D3D\_FEATURE\_LEVEL\_9\_3, share a common implementation DLL and treat the [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) argument to D3D11CreateDevice\[AndSwapchain\] as a template adapter and create their own adapter as part of device creation.</span></span> <span data-ttu-id="90997-137">這表示傳入建立常式的 **IDXGIAdapter** 將不會與透過 IDXGIDevice：： GetAdapter 從裝置上取出的介面卡相同。</span><span class="sxs-lookup"><span data-stu-id="90997-137">This means that the **IDXGIAdapter** passed into the creation routine will not be the same adapter as that retrieved from the device via IDXGIDevice::GetAdapter.</span></span> <span data-ttu-id="90997-138">這種情況的影響是從傳入的介面卡列舉的 **IDXGIOutputs** 無法使用任何層級9裝置來輸入全螢幕，因為這些輸出不是裝置的介面卡所擁有。</span><span class="sxs-lookup"><span data-stu-id="90997-138">The impact of this is that the **IDXGIOutputs** enumerated from the passed-in adapter cannot be used to enter fullscreen using any level 9 device, since those outputs are not owned by the device's adapter.</span></span> <span data-ttu-id="90997-139">建議您捨棄傳入的範本介面卡，並使用 IDXGIDevice：： GetAdapter 抓取裝置所建立的介面卡，其中 [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) 可使用來自 Direct3D 裝置介面的 QueryInterface 抓取。</span><span class="sxs-lookup"><span data-stu-id="90997-139">It is good practice to discard the passed-in template adapter and retrieve the device's created adapter using IDXGIDevice::GetAdapter, where [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) can be retrieved using QueryInterface from the Direct3D device interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90997-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="90997-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90997-141">舊版硬體上的 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="90997-141">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 