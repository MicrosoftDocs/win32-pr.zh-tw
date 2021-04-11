---
description: Alpha 混色
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: " (DirectShow) 的 Alpha 混色"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109640"
---
# <a name="alpha-blending-directshow"></a><span data-ttu-id="79d5e-103"> (DirectShow) 的 Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="79d5e-103">Alpha Blending (DirectShow)</span></span>

<span data-ttu-id="79d5e-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="79d5e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="79d5e-105">本文說明 (DES) 的 [DirectShow 編輯服務](directshow-editing-services.md) 中的 Alpha 混色。</span><span class="sxs-lookup"><span data-stu-id="79d5e-105">This article describes alpha blending in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="79d5e-106">Alpha 會測量圖元或影像的透明度。</span><span class="sxs-lookup"><span data-stu-id="79d5e-106">Alpha measures the transparency of a pixel or image.</span></span> <span data-ttu-id="79d5e-107">在32位未壓縮的 RGB 影片中，四個元件會定義每個圖元： () 的 Alpha 通道，以及 (RGB) 的三個色彩元件。</span><span class="sxs-lookup"><span data-stu-id="79d5e-107">In 32-bit uncompressed RGB video, four components define each pixel: an alpha channel (A) and three color components (RGB).</span></span> <span data-ttu-id="79d5e-108">Alpha 值為零的圖元是完全透明的。</span><span class="sxs-lookup"><span data-stu-id="79d5e-108">A pixel with an alpha value of zero is completely transparent.</span></span> <span data-ttu-id="79d5e-109">Alpha 值為255的圖元不是透明的。</span><span class="sxs-lookup"><span data-stu-id="79d5e-109">A pixel with an alpha value of 255 is opaque.</span></span> <span data-ttu-id="79d5e-110">在這些值之間，圖元具有不同程度的透明度。</span><span class="sxs-lookup"><span data-stu-id="79d5e-110">Between these values, the pixel has various degrees of transparency.</span></span>

<span data-ttu-id="79d5e-111">DirectShow 定義32位 RGB 影片的兩種媒體類型：</span><span class="sxs-lookup"><span data-stu-id="79d5e-111">DirectShow defines two media types for 32-bit RGB video:</span></span>

-   <span data-ttu-id="79d5e-112">**MEDIASUBTYPE \_ARGB32**：影片是32位 RGB，具有有效的 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="79d5e-112">**MEDIASUBTYPE\_ARGB32**: The video is 32-bit RGB with a valid alpha channel.</span></span>
-   <span data-ttu-id="79d5e-113">**MEDIASUBTYPE \_RGB32**：圖元是32位，但 Alpha 通道不一定是有效的。</span><span class="sxs-lookup"><span data-stu-id="79d5e-113">**MEDIASUBTYPE\_RGB32**: Pixels are 32 bits, but the alpha channel is not necessarily valid.</span></span>

<span data-ttu-id="79d5e-114">若要在 DES 中執行 Alpha 混色，請將影片群組的未壓縮媒體類型設定為 MEDIASUBTYPE \_ ARGB32。</span><span class="sxs-lookup"><span data-stu-id="79d5e-114">To perform alpha blending in DES, set the video group's uncompressed media type to MEDIASUBTYPE\_ARGB32.</span></span> <span data-ttu-id="79d5e-115">在 c + + 中，呼叫 [**IAMTimelineGroup：： SetMediaType**](iamtimelinegroup-setmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="79d5e-115">In C++, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span> <span data-ttu-id="79d5e-116">在 XTL 格式中，將 [**群組**](group-element.md)元素的 [**bitdepth**](bitdepth-attribute.md)屬性設定為32也會完成這項工作。</span><span class="sxs-lookup"><span data-stu-id="79d5e-116">In the XTL format, setting the [**bitdepth**](bitdepth-attribute.md) attribute of the [**group**](group-element.md) element to 32 accomplishes this as well.</span></span>

<span data-ttu-id="79d5e-117">接下來，您需要包含 Alpha 通道的影片資料。</span><span class="sxs-lookup"><span data-stu-id="79d5e-117">Next, you need video data that contains an alpha channel.</span></span> <span data-ttu-id="79d5e-118">有幾個選項：</span><span class="sxs-lookup"><span data-stu-id="79d5e-118">There are several options:</span></span>

-   <span data-ttu-id="79d5e-119">您可以使用已具有 Alpha 資料的32位 RGB 影片的 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="79d5e-119">You can use an AVI file that already has 32-bit RGB video with alpha data.</span></span> <span data-ttu-id="79d5e-120">目前， (WMF) 原始程式檔中的 MPEG 或 Microsoft Windows Media 格式不支援 Alpha。</span><span class="sxs-lookup"><span data-stu-id="79d5e-120">Currently, alpha is not supported for MPEG or Microsoft Windows Media Format (WMF) source files.</span></span>
-   <span data-ttu-id="79d5e-121">DES 支援32位點陣圖 ( .bmp) 和 Targa (. 使用 Alpha 資料 tga) 檔。</span><span class="sxs-lookup"><span data-stu-id="79d5e-121">DES supports 32-bit bitmap (.bmp) and Targa (.tga) files with alpha data.</span></span>
-   <span data-ttu-id="79d5e-122">您可以撰寫自訂來源篩選器，以使用 Alpha 建立32位 RGB 資料。</span><span class="sxs-lookup"><span data-stu-id="79d5e-122">You can write a custom source filter that creates 32-bit RGB data with alpha.</span></span> <span data-ttu-id="79d5e-123">輸出媒體類型必須是 **MEDIASUBTYPE \_ ARGB32**。</span><span class="sxs-lookup"><span data-stu-id="79d5e-123">The output media type must be **MEDIASUBTYPE\_ARGB32**.</span></span> <span data-ttu-id="79d5e-124">在時間軸來源物件中使用篩選做為子物件。</span><span class="sxs-lookup"><span data-stu-id="79d5e-124">Use the filter as the subobject in a timeline source object.</span></span>

<span data-ttu-id="79d5e-125">如果您的影片來源沒有 Alpha，您可以使用會建立 Alpha 資料的效果。</span><span class="sxs-lookup"><span data-stu-id="79d5e-125">If your video source does not have alpha, you can use an effect that creates alpha data.</span></span> <span data-ttu-id="79d5e-126">[Alpha Setter 效果](alpha-setter-effect.md)會將整個影像的 Alpha 通道設定為常數值。</span><span class="sxs-lookup"><span data-stu-id="79d5e-126">The [Alpha Setter Effect](alpha-setter-effect.md) sets the alpha channel for the entire image to a constant value.</span></span> <span data-ttu-id="79d5e-127">若要在一段時間內改變 Alpha，請使用具有 Alpha Setter 效果的 [**IPropertySetter**](ipropertysetter.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="79d5e-127">To vary the alpha over time, use the [**IPropertySetter**](ipropertysetter.md) interface with the Alpha Setter Effect.</span></span> <span data-ttu-id="79d5e-128">只要群組的未壓縮媒體類型是 **MEDIASUBTYPE \_ ARGB32**，原始來源就不需要是32位。</span><span class="sxs-lookup"><span data-stu-id="79d5e-128">The original source does not have to be 32 bits, as long as the group's uncompressed media type is **MEDIASUBTYPE\_ARGB32**.</span></span>

<span data-ttu-id="79d5e-129">最後，將影片傳遞給執行 Alpha 混色的效果或轉換。</span><span class="sxs-lookup"><span data-stu-id="79d5e-129">Finally, pass the video to an effect or transition that performs alpha blending.</span></span> <span data-ttu-id="79d5e-130">[組合器轉換](compositor-transition.md)會執行 Alpha 混合，而[按鍵轉換](key-transition.md)可以使用 Alpha 值來做為索引鍵。</span><span class="sxs-lookup"><span data-stu-id="79d5e-130">The [Compositor Transition](compositor-transition.md) performs alpha blending, and the [Key Transition](key-transition.md) can key by alpha value.</span></span>

<span data-ttu-id="79d5e-131">下列範例 XTL 專案會執行 Alpha 混色：</span><span class="sxs-lookup"><span data-stu-id="79d5e-131">The following sample XTL project performs alpha blending:</span></span>


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a><span data-ttu-id="79d5e-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="79d5e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79d5e-133">使用 DirectShow 編輯服務</span><span class="sxs-lookup"><span data-stu-id="79d5e-133">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



