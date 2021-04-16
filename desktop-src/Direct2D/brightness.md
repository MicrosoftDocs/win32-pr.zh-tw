---
title: 亮度效果
description: 使用亮度效果來控制影像的亮度。
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- 亮度效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104561538"
---
# <a name="brightness-effect"></a>亮度效果

使用亮度效果來控制影像的亮度。

這項效果的 CLSID 是 CLSID \_ D2D1Brightness。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像



| 之前                                                      |
|-------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)  |
| After                                                       |
| ![轉換後的影像。](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 屬性顯示名稱                                                 | 類型和預設值                              | Description                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WhitePoint<br/> D2D1 \_ 亮度 \_ 主張的 \_ 白色 \_ 點<br/> | D2D1 \_ 向量 \_ 2f<br/> {1.0 f、1.0 f}<br/> | 亮度傳輸曲線的上半部。 白色點會調整影像最亮部分的外觀。 此屬性適用于 x 值和 y 值（依該順序）。 這個屬性的每個值都介於0和1（含）之間。 |
| BlackPoint<br/> D2D1 \_ 亮度 \_ 的 \_ 黑色 \_ 點<br/> | D2D1 \_ 向量 \_ 2f<br/> {0.0 f，0.0 f}<br/> | 亮度轉印曲線的下半部。 黑色點會調整影像較暗部分的外觀。 此屬性適用于 x 值和 y 值（依該順序）。 這個屬性的每個值都介於0和1（含）之間。   |



 

這種效果會使用指定的白色和黑色點來產生用來調整點陣圖的傳送函數。 下一個方程式描述傳送函式。 輸入濃度的定義介於0和1之間。

![亮度演算法](images/brightness-formula1.png)

效果演算法會執行建立傳送函式的方程式。 我們會使用此函數來調整影像圖元。 黑色點和白色點的 x 和 y 值是兩個維度中連接來形成轉換的座標。 最終輸出方程式的每個部分：

1.  使用這個方程式，將影像資料從線性空間轉換成非線性空間：![helper 函式1](images/brightness-formula2.png)

2.  根據下列值調整影像：
    -   *輸入* 是從0到1的輸入影像圖元濃度值。

    -   *(x，y) 亮色* 圖元濃度的轉換曲線位置。

    -   *黑色的 (x，y)* 是變暗圖元濃度的轉換曲線位置。

3.  使用這個方程式，將影像資料轉換回線性空間： ![helper 函數2](images/brightness-formula3.png)

最後的輸出方程式和元件部分如下所示。

![亮度調整的完整計算](images/brightness-formula4.png)

## <a name="output-bitmap"></a>輸出點陣圖

輸出點陣圖大小與輸入點陣圖大小相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 最低支援的伺服器 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

