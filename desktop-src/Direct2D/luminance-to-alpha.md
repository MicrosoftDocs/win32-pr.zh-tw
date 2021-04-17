---
title: 亮度到 Alpha 效果
description: 使用 [亮度至 Alpha] 效果，將 Alpha 色板設定為影像的亮度，並將色彩通道設定為0。
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- 亮度到 Alpha 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104560277"
---
# <a name="luminance-to-alpha-effect"></a><span data-ttu-id="74410-104">亮度到 Alpha 效果</span><span class="sxs-lookup"><span data-stu-id="74410-104">Luminance to alpha effect</span></span>

<span data-ttu-id="74410-105">使用 [亮度至 Alpha] 效果，將 Alpha 色板設定為影像的亮度，並將色彩通道設定為0。</span><span class="sxs-lookup"><span data-stu-id="74410-105">Use the luminance to alpha effect to set the alpha channel to the luminance of the image and sets the color channels to 0.</span></span> <span data-ttu-id="74410-106">您可以使用此效果的輸出，根據輸入影像的亮度進行半透明重迭。</span><span class="sxs-lookup"><span data-stu-id="74410-106">You can use the output of this effect to make a semitransparent overlay based on the brightness of the input image.</span></span> <span data-ttu-id="74410-107">或者，您可以使用它來建立影像遮罩。</span><span class="sxs-lookup"><span data-stu-id="74410-107">Or you can use it to make an image mask.</span></span>

> [!Note]  
> <span data-ttu-id="74410-108">此效果沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="74410-108">This effect has no properties.</span></span>

 

<span data-ttu-id="74410-109">這項效果的 CLSID 是 CLSID \_ D2D1LuminanceToAlpha。</span><span class="sxs-lookup"><span data-stu-id="74410-109">The CLSID for this effect is CLSID\_D2D1LuminanceToAlpha.</span></span>

## <a name="example-image"></a><span data-ttu-id="74410-110">範例影像</span><span class="sxs-lookup"><span data-stu-id="74410-110">Example image</span></span>

<span data-ttu-id="74410-111">這個範例會顯示在白色表面上，顯示亮度的亮度至 Alpha 效果的輸出，以顯示不透明度。</span><span class="sxs-lookup"><span data-stu-id="74410-111">This example shows the output of the luminance to alpha effect composited over a white surface to show opacity.</span></span>



| <span data-ttu-id="74410-112">之前</span><span class="sxs-lookup"><span data-stu-id="74410-112">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)        |
| <span data-ttu-id="74410-114">After</span><span class="sxs-lookup"><span data-stu-id="74410-114">After</span></span>                                                             |
| ![轉換後的影像。](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="74410-116">此效果會使用此色彩矩陣，將輸出的 Alpha 色板設定為輸入影像的亮度。</span><span class="sxs-lookup"><span data-stu-id="74410-116">This effect sets the alpha channel of the output to the luminance of the input image using this color matrix.</span></span>

![效果用來設定 Alpha 通道的色彩矩陣。](images/luminance-to-alpha-math1.png)

<span data-ttu-id="74410-118">此效果會取用和輸出預乘的 Alpha 影像。</span><span class="sxs-lookup"><span data-stu-id="74410-118">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="74410-119">除非完全不透明，否則效果無法用於直接的 Alpha 影像。</span><span class="sxs-lookup"><span data-stu-id="74410-119">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

> [!Note]
>
> <span data-ttu-id="74410-120">因為影像是以 gamma 補償格式儲存，所以在計算影像的亮度之前，您應該先執行反向 gamma 更正，以取得影像的真實色彩值。</span><span class="sxs-lookup"><span data-stu-id="74410-120">Because images are stored in a gamma-compensated format, before you calculate the luminance for an image you should first perform inverse gamma correction to get the true color values for the image.</span></span> <span data-ttu-id="74410-121">因為影像通常會儲存在 2.2 gamma，所以您可以使用 Gamma 傳送效果搭配 (1/2.2) 的指數，然後使用該效果的輸出。</span><span class="sxs-lookup"><span data-stu-id="74410-121">Since images are normally stored at 2.2 gamma, you can use the Gamma transfer effect with an exponent of (1/2.2) and then use the output of that effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="74410-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="74410-122">Requirements</span></span>



| <span data-ttu-id="74410-123">需求</span><span class="sxs-lookup"><span data-stu-id="74410-123">Requirement</span></span> | <span data-ttu-id="74410-124">值</span><span class="sxs-lookup"><span data-stu-id="74410-124">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="74410-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74410-125">Minimum supported client</span></span> | <span data-ttu-id="74410-126">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74410-126">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="74410-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74410-127">Minimum supported server</span></span> | <span data-ttu-id="74410-128">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74410-128">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="74410-129">標頭</span><span class="sxs-lookup"><span data-stu-id="74410-129">Header</span></span>                   | <span data-ttu-id="74410-130">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="74410-130">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="74410-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="74410-131">Library</span></span>                  | <span data-ttu-id="74410-132">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="74410-132">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="output-bitmap"></a><span data-ttu-id="74410-133">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="74410-133">Output bitmap</span></span>

<span data-ttu-id="74410-134">輸出的大小與輸入影像相同。</span><span class="sxs-lookup"><span data-stu-id="74410-134">The output is the same size as the input image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74410-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="74410-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74410-136">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="74410-136">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
