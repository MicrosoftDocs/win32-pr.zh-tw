---
title: 飽和度效果
description: 使用此效果來改變影像的飽和度。
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- 飽和度效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024970"
---
# <a name="saturation-effect"></a>飽和度效果

使用此效果來改變影像的飽和度。 飽和度效果是 [色彩矩陣](color-matrix.md) 效果的特製化。

這項效果的 CLSID 是 CLSID \_ D2D1Saturation。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此處的範例顯示飽和度為0% 的飽和度效果輸入和輸出影像。



| 之前                                                      |
|-------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)  |
| After                                                       |
| ![轉換後的影像。](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



效果會根據在此方程式中的飽和度值 (*s* 來計算色彩矩陣，) 您使用 [D2D1 \_ 飽和度 \_ ] \_ 屬性飽和度屬性來指定。 矩陣方程式如下所示。

![計算飽和度矩陣的公式。](images/saturation-formula.png)

所建立的矩陣只取決於飽和度值。 如果您需要特定的矩陣，您可以使用 [色彩矩陣](color-matrix.md) 效果。

此效果會取用和輸出預乘的 Alpha 影像。 除非完全不透明，否則效果無法用於直接的 Alpha 影像。

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                  | 類型和預設值           | Description                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 飽和度<br/> D2D1 \_ 飽和度 \_ 的 \_ 飽和度<br/> | FLOAT<br/> 0.5 f<br/> | 影像的飽和度。 您可以將飽和度設定為介於0和1之間的值。 如果您將它設定為1，則輸出影像會完全飽和。 如果您將它設定為0，則輸出影像為單色。 飽和度值沒有用。 |



 

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

 

