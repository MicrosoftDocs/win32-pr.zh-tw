---
title: 色調 rotatation 效果
description: 使用 [色調旋轉效果] 可根據旋轉角度套用色彩矩陣，以改變影像的色調。
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- 色調 rotatation 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531ab9b1649db96bc5ee100df98ed10b4021b506e3ad71bb426778655348b2df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569123"
---
# <a name="hue-rotatation-effect"></a>色調 rotatation 效果

使用 [色調旋轉效果] 可根據旋轉角度套用色彩矩陣，以改變影像的色調。

這項效果的 CLSID 是 CLSID \_ D2D1HueRotation。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此處的範例會顯示色調旋轉效果的輸入和輸出影像，旋轉角度為270度。



| 之前                                                       |
|--------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)   |
| After                                                        |
| ![轉換後的影像。](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



效果會依據旋轉角度 (*？*) 您使用 [D2D1 HUEROTATION] [ \_ \_ 屬性角度] 屬性指定，來計算色彩矩陣 \_ 。 以下是矩陣方等。

![色調旋轉計算](images/hue-formula.png)

所建立的矩陣只取決於旋轉角度。 如果您需要特定的矩陣，您可以使用 [色彩矩陣](color-matrix.md) 效果。

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                         | 類型和預設值           | 描述                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| 角度<br/> D2D1 \_ HUEROTATION \_ 的 \_ 角度<br/> | FLOAT<br/> 0.0f<br/> | 用來旋轉色調的角度（以度為單位）。 |



 

## <a name="output-bitmap"></a>輸出點陣圖

輸出點陣圖大小與輸入點陣圖大小相同。

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

 

