---
title: 置換地圖效果
description: 使用置換地圖效果，以第二個輸入影像的濃度值取代輸入影像的圖元。
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- 置換地圖效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73888d8168e411bf0f8daee1f2e04801353ee8358d27ba4d5cc9b1f71630a762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833010"
---
# <a name="displacement-map-effect"></a>置換地圖效果

使用置換地圖效果，以第二個輸入影像的濃度值取代輸入影像的圖元。

這項效果的 CLSID 是 CLSID \_ D2D1DisplacementMap。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [色彩頻道](#color-channels)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像



| 之前                                                           |
|------------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)       |
| After                                                            |
| ![轉換後的影像。](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



輸出中圖元的位置是使用下列公式來決定：

C ' (x，y) = C (x + 縮放 \* (XChannelSelector (置換點陣圖 (x、y) ) -0.5) 、y + 尺規 \* (YChannelSelector (置換點陣圖 (x、y) ) -0.5) ) 

其中：<dl> *C (x，y)* 是 (x，y) 的輸出圖元。  
*C (x，y)* 是 (x，y) 的輸入圖元。  
*置換點陣圖 (x，y)* 是指定座標的位移圖元濃度  
從以 X 方向取代輸入影像的置換點陣圖， *XChannelSelector* 所選 RGBA 通道的濃度。  
從以 Y 方向取代輸入影像的置換點陣圖， *YChannelSelector* 所選 RGBA 通道的濃度。  
</dl>

效果會根據尺規屬性和置換影像的強度來 resamples 輸入影像。 如果在輸入影像中的圖元之間進行取樣，則會使用雙線性插補。

此效果適用于直接和預乘的 Alpha 影像。 輸出 Alpha 格式與輸入格式相同。

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                   | 類型和預設值                                                   | 描述                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 調整<br/> D2D1 \_ DISPLACEMENTMAP \_ 的 \_ 範圍調整<br/>                       | FLOAT<br/> 0.0f<br/>                                         | 將所選通道的強度與置換影像相乘。 您設定此屬性的愈高，效果越多取代圖元<br/>                       |
| XChannelSelect<br/> D2D1 \_ DISPLACEMENTMAP \_ 精選 \_ X \_ CHANNEL \_ SELECT<br/> | D2D1 \_ 通道 \_ 選取器<br/> D2D1 \_ 通道 \_ 選取器 \_ A<br/> | 效果會從這個色頻中取出濃度，並用它來以 X 方向取代影像。 如需詳細資訊，請參閱 [色彩通道](#color-channels) 。<br/> |
| YChannelSelect<br/> D2D1 \_ DISPLACEMENTMAP \_ 的 \_ Y \_ 通道 \_ 選取<br/> | D2D1 \_ 通道 \_ 選取器<br/> D2D1 \_ 通道 \_ 選取器 \_ A<br/> | 效果會從這個色頻中取出濃度，並用它來以 Y 方向取代影像。 如需詳細資訊，請參閱 [色彩通道](#color-channels) 。<br/> |



 

## <a name="color-channels"></a>色彩頻道



| 列舉型別                | 描述                                                      |
|----------------------------|------------------------------------------------------------------|
| D2D1 \_ 通道 \_ 選取器 \_ R | 效果會將紅色通道的強度輸出解壓縮。   |
| D2D1 \_ 通道 \_ 選取器 \_ G | 效果會從綠色頻道中取出濃度輸出。 |
| D2D1 \_ 通道 \_ 選取器 \_ B | 效果會從藍色通道中解壓縮濃度輸出。  |
| D2D1 \_ 通道 \_ 選取器 \_ A | 效果會將 Alpha 色板的濃度輸出解壓縮。 |



 

## <a name="output-bitmap"></a>輸出點陣圖

您可以使用下列方程式來判斷輸出點陣圖的大小上限：

輸出點陣圖？ 圖元 = (輸入點陣圖大小？ (Dip) + 縮放) \* (使用者 DPI/96) 

輸出點陣圖<sub>y</sub> 圖元 = (輸入點陣圖大小<sub>y</sub> (dip) + 縮放) \* (使用者 DPI/96) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

