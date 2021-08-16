---
title: 亮度到 Alpha 效果
description: 使用 [亮度至 Alpha] 效果，將 Alpha 色板設定為影像的亮度，並將色彩通道設定為0。
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- 亮度到 Alpha 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803070fea76b47c1334803a4e7f8fef510cc77c8b3bc05c8477b572cb0451670
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825250"
---
# <a name="luminance-to-alpha-effect"></a>亮度到 Alpha 效果

使用 [亮度至 Alpha] 效果，將 Alpha 色板設定為影像的亮度，並將色彩通道設定為0。 您可以使用此效果的輸出，根據輸入影像的亮度進行半透明重迭。 或者，您可以使用它來建立影像遮罩。

> [!Note]  
> 此效果沒有屬性。

 

這項效果的 CLSID 是 CLSID \_ D2D1LuminanceToAlpha。

## <a name="example-image"></a>範例影像

這個範例會顯示在白色表面上，顯示亮度的亮度至 Alpha 效果的輸出，以顯示不透明度。



| 之前                                                            |
|-------------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)        |
| After                                                             |
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



此效果會使用此色彩矩陣，將輸出的 Alpha 色板設定為輸入影像的亮度。

![效果用來設定 Alpha 通道的色彩矩陣。](images/luminance-to-alpha-math1.png)

此效果會取用和輸出預乘的 Alpha 影像。 除非完全不透明，否則效果無法用於直接的 Alpha 影像。

> [!Note]
>
> 因為影像是以 gamma 補償格式儲存，所以在計算影像的亮度之前，您應該先執行反向 gamma 更正，以取得影像的真實色彩值。 因為影像通常會儲存在 2.2 gamma，所以您可以使用 Gamma 傳送效果搭配 (1/2.2) 的指數，然後使用該效果的輸出。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="output-bitmap"></a>輸出點陣圖

輸出的大小與輸入影像相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
