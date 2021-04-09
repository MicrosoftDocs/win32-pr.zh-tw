---
description: 若要撰寫至螢幕或執行浮點運算，您必須在正確的色彩空間中工作。
ms.assetid: 1DD8E2D3-430F-4EE4-9C41-78736C904920
title: 轉換色彩空間的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b5dbec2f826c40d5274cbddb3b54d1cdd9f695
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687644"
---
# <a name="converting-data-for-the-color-space"></a><span data-ttu-id="d2b1d-103">轉換色彩空間的資料</span><span class="sxs-lookup"><span data-stu-id="d2b1d-103">Converting data for the color space</span></span>

<span data-ttu-id="d2b1d-104">若要撰寫至螢幕或執行浮點運算，您必須在正確的色彩空間中工作。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-104">To compose to the screen or perform floating-point operations, you need to work in the correct color space.</span></span> <span data-ttu-id="d2b1d-105">我們建議您線上性色彩空間中執行浮點數運算。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-105">We recommend that you perform floating point operations in a linear color space.</span></span> <span data-ttu-id="d2b1d-106">然後，若要在螢幕上顯示影像，請將資料轉換成標準 RGB 資料 (sRGB、gamma 2.2-已更正) 色彩空間。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-106">Then, to present your images to the screen, convert the data to standard RGB data (sRGB, gamma 2.2-corrected) color space.</span></span> <span data-ttu-id="d2b1d-107">在 sRGB 色彩空間中呈現畫面，對色彩精確度而言很重要。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-107">Presenting to the screen in sRGB color space is important for color accuracy.</span></span> <span data-ttu-id="d2b1d-108">如果影像不是 gamma 2.2 修正，則會配置過多的位或太多的頻寬，以醒目顯示人們無法區分的部分，而且會有太少的位或頻寬來遮蔽人們敏感性的值，因此需要更多的位或頻寬才能維持相同的視覺品質。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-108">If images are not gamma 2.2-corrected, they allocate too many bits or too much bandwidth to highlights that people can't differentiate, and too few bits or bandwidth to shadow values that people are sensitive to, and so would require more bits or bandwidth to maintain the same visual quality.</span></span> <span data-ttu-id="d2b1d-109">因此，若要確保最佳的色彩精確度，請將影像呈現至已修正 gamma 2.2 的螢幕。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-109">Therefore, to ensure the best color accuracy, present images to the screen that are gamma 2.2-corrected.</span></span>

-   [<span data-ttu-id="d2b1d-110">色彩精確度</span><span class="sxs-lookup"><span data-stu-id="d2b1d-110">Color accuracy</span></span>](#color-accuracy)
-   [<span data-ttu-id="d2b1d-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2b1d-111">Related topics</span></span>](#related-topics)

## <a name="color-accuracy"></a><span data-ttu-id="d2b1d-112">色彩精確度</span><span class="sxs-lookup"><span data-stu-id="d2b1d-112">Color accuracy</span></span>

<span data-ttu-id="d2b1d-113">針對展示，整數值顯示格式 (例如 [**DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)、 [**dxgi \_ 格式 \_ R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)等等) 一律包含 SRGB gamma 更正的資料。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-113">For presentation, integer-valued display formats (such as [**DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI\_FORMAT\_R10G10B10\_XR\_BIAS\_A2\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), and so on) always contain sRGB gamma-corrected data.</span></span> <span data-ttu-id="d2b1d-114">浮點值顯示格式 (目前只有 [**DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) 包含線性值資料。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-114">Float-valued display formats (currently only [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) contain linear-valued data.</span></span>

<span data-ttu-id="d2b1d-115">\_SRGB[格式修飾](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)詞會向作業系統指出，以協助應用程式將 SRGB 資料放置在螢幕上。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-115">The \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) indicates to the operating system to help the app place sRGB data on the screen.</span></span> <span data-ttu-id="d2b1d-116">應用程式必須一律將 sRGB 資料放入具有整數值格式的背景緩衝區，以便在螢幕上呈現 sRGB 資料，即使資料的格式名稱未採用此格式修飾詞也一樣。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-116">The app must always place sRGB data into back buffers with integer-valued formats to present the sRGB data to the screen, even if the data doesn't have this format modifier in its format name.</span></span> <span data-ttu-id="d2b1d-117">如需顯示掃描輸出格式的完整清單：</span><span class="sxs-lookup"><span data-stu-id="d2b1d-117">For a complete list of display scan-out formats:</span></span>

-   [<span data-ttu-id="d2b1d-118">Direct3D 功能等級12.1 硬體的 DXGI 格式支援</span><span class="sxs-lookup"><span data-stu-id="d2b1d-118">DXGI Format Support for Direct3D Feature Level 12.1 Hardware</span></span>](hardware-support-for-direct3d-12-1-formats.md)
-   [<span data-ttu-id="d2b1d-119">Direct3D 功能等級12.0 硬體的 DXGI 格式支援</span><span class="sxs-lookup"><span data-stu-id="d2b1d-119">DXGI Format Support for Direct3D Feature Level 12.0 Hardware</span></span>](hardware-support-for-direct3d-12-0-formats.md)
-   [<span data-ttu-id="d2b1d-120">Direct3D 功能等級11.1 硬體的 DXGI 格式支援</span><span class="sxs-lookup"><span data-stu-id="d2b1d-120">DXGI Format Support for Direct3D Feature Level 11.1 Hardware</span></span>](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [<span data-ttu-id="d2b1d-121">Direct3D 功能等級11.0 硬體的 DXGI 格式支援</span><span class="sxs-lookup"><span data-stu-id="d2b1d-121">DXGI Format Support for Direct3D Feature Level 11.0 Hardware</span></span>](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   <span data-ttu-id="d2b1d-122">[Direct3D 10Level9 格式的硬體支援](/previous-versions//ff471324(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2b1d-122">[Hardware Support for Direct3D 10Level9 Formats](/previous-versions//ff471324(v=vs.85))</span></span>
-   <span data-ttu-id="d2b1d-123">[Direct3D 10.1 格式的硬體支援](/previous-versions//cc627091(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2b1d-123">[Hardware Support for Direct3D 10.1 Formats](/previous-versions//cc627091(v=vs.85))</span></span>
-   <span data-ttu-id="d2b1d-124">[適用于 Direct3D 10 格式的硬體支援](/previous-versions//cc627090(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2b1d-124">[Hardware Support for Direct3D 10 Formats](/previous-versions//cc627090(v=vs.85))</span></span>

<span data-ttu-id="d2b1d-125">當您使用系結至管線的 SRGB 格式修飾詞，將圖元著色器的浮點輸出值寫入轉譯目標視圖 (**RenderTargetView** s) 時 \_ ， [](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline)您可以將它們轉換為 gamma 2.2 修正的色彩空間。 [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="d2b1d-125">When you write floating-point output values from the pixel shader into render-target views (**RenderTargetView** s) with the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) that are bound to the [pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline), you convert them to gamma 2.2-corrected color space.</span></span> <span data-ttu-id="d2b1d-126">同樣地，當使用 SRGB 格式修飾詞 (**ShaderResourceView** s) 的著色器資源檢視系結 \_ 至管線時，您會在從 **ShaderResourceView** 中讀取時，將值從 gamma 2.2 更正的色彩空間轉換成線性色彩空間。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-126">Similarly, when shader-resource views (**ShaderResourceView** s) with the \_SRGB format modifier are bound to the pipeline, you convert the values from gamma 2.2-corrected color space to linear color space when you read them from the **ShaderResourceView** s.</span></span> <span data-ttu-id="d2b1d-127">著色器接著可以對其執行作業。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-127">The shader can then perform operations on them.</span></span>

<span data-ttu-id="d2b1d-128">例如，使用與此類似的程式碼，從著色器將浮點輸出值寫入至 **RenderTargetView** 格式：</span><span class="sxs-lookup"><span data-stu-id="d2b1d-128">For example, use code similar to this to write floating-point output values from a shader into a **RenderTargetView** format:</span></span>


```
struct PSOut
{
    float4 color : SV_Target;
};

PSOut S( PSIn input )
{
    PSOut output;
    output.color = float4( 1.0, 0.0, 0.0, 1.0 );
    return output;
}
```



<span data-ttu-id="d2b1d-129">當其 ' 常式傳回時，浮點數 (1，0，0，1) 值會轉換成 **RenderTargetView** 格式。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-129">When the 'S' routine returns, the floating point (1, 0, 0, 1) values are converted to the **RenderTargetView** format.</span></span> <span data-ttu-id="d2b1d-130">然後，如果您將 \_ SRGB [格式修飾](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 詞指派給 **RenderTargetView**，則會發生 gamma 轉換。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-130">Then, if you assign the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) to the **RenderTargetView**, the gamma conversion occurs.</span></span>

<span data-ttu-id="d2b1d-131">這些步驟可確保畫面上顯示的內容具有最佳色彩精確度。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-131">These are steps to follow to ensure that the content that is displayed on the screen has the best color accuracy.</span></span>

<span data-ttu-id="d2b1d-132">**確保管線中的色彩精確度**</span><span class="sxs-lookup"><span data-stu-id="d2b1d-132">**To ensure color accuracy in the pipeline**</span></span>

1.  <span data-ttu-id="d2b1d-133">如果材質有 sRGB 內容，請確定 **ShaderResourceView** 具有 \_ srgb [格式修飾](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 詞，因此當您從 **ShaderResourceView** 讀取著色器時，會將材質內容從 gamma 2.2 更正的色彩空間轉換成線性色彩空間。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-133">If a texture has sRGB content, ensure the **ShaderResourceView** has the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) so when you read from the **ShaderResourceView** into the shader, you convert the texture content from gamma 2.2-corrected color space to linear color space.</span></span>
2.  <span data-ttu-id="d2b1d-134">確定 **RenderTargetView** 也具有 \_ SRGB [格式修飾](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 詞，因此著色器輸出值為 gamma 轉換。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-134">Ensure the **RenderTargetView** also has the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) so the shader output values are gamma converted.</span></span>

<span data-ttu-id="d2b1d-135">如果您遵循上述步驟，當您呼叫 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 方法時，畫面上顯示的內容具有最佳的色彩精確度。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-135">If you follow the preceding steps, when you call the [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) method, the content that is displayed on the screen has the best color accuracy.</span></span>

<span data-ttu-id="d2b1d-136">您可以使用 [**ID3D11Device：： CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview)方法，從您以 **DXGI \_ 格式 \_ \* \_ UNORM** 格式建立的交換鏈，在背景緩衝區建立 **DXGI \_ 格式的 \_ \* \_ SRGB** views。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-136">You can use the [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) method to create **DXGI\_FORMAT\_\*\_SRGB** views on back buffers from a swap chain that you create only with a **DXGI\_FORMAT\_\*\_UNORM** format.</span></span> <span data-ttu-id="d2b1d-137">這是建立轉譯目標視圖規則的特殊例外狀況，這表示只有當您建立了想要以 **DXGI \_ 格式 \_ \* \_** 的類型來查看的資源時，才能使用與 **ID3D11Device：： CreateRenderTargetView** 不同的格式。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-137">This is a special exception to the rule for creating render-target views, which states that you can use a different format with **ID3D11Device::CreateRenderTargetView** only if you created the resource that you want to view with **DXGI\_FORMAT\_\*\_TYPELESS**.</span></span>

<span data-ttu-id="d2b1d-138">如需轉換資料之規則的詳細資訊，請參閱 [資料轉換規則](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion)。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-138">For more info about rules for converting data, see [Data Conversion Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).</span></span>

<span data-ttu-id="d2b1d-139">如需如何同時讀取和寫入材質的詳細資訊，請參閱將 [DXGI 格式解壓縮和封裝 \_ 用於 In-Place 影像編輯](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format)。</span><span class="sxs-lookup"><span data-stu-id="d2b1d-139">For info about how to simultaneously both read from and write to a texture, see [Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2b1d-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2b1d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2b1d-141">使用翻轉模型、中途矩形和捲動區域增強簡報</span><span class="sxs-lookup"><span data-stu-id="d2b1d-141">Enhancing presentation with the flip model, dirty rectangles, and scrolled areas</span></span>](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
