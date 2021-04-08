---
title: 線性傳送效果
description: 使用線性傳送效果，利用從您為每個通道提供的值清單建立的線性函式，來對應影像的色彩濃度。
ms.assetid: 22DC496E-2958-4726-A74D-B3DE934F507C
keywords:
- 線性傳送效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfedbb79f057ee871ce23cc086034afc3e6cdda0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686651"
---
# <a name="linear-transfer-effect"></a>線性傳送效果

使用線性傳送效果，利用從您為每個通道提供的值清單建立的線性函式，來對應影像的色彩濃度。

這項效果的 CLSID 是 CLSID \_ D2D1LinearTransfer。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像



| 之前                                                          |
|-----------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)      |
| After                                                           |
| ![轉換後的影像。](images/13-lineartransfer.png) |



 


```C++
ComPtr<ID2D1Effect> linearTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LinearTransfer, &linearTransferEffect);

linearTransferEffect->SetInput(0, bitmap);

linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_SLOPE, 2.5f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE, 5.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(linearTransferEffect.Get());
m_d2dContext->EndDraw();
```



線性傳送函式是根據您指定的每個通道的斜率和 y 攔截來建立。 輸出圖元濃度 C 的計算方式是使用方程式： C ' = mC + B，其中 m 是線性函式的斜率，而 B 是線性函式的 Y 攔截。

此效果適用于直接和預乘的 Alpha 影像。 效果會輸出預乘的 Alpha 點陣圖。

## <a name="effect-properties"></a>效果屬性

> [!Note]  
> 針對線性傳送屬性的所有通道：
>
> -   Y 攔截未系結，而且沒有用。
> -   斜率未系結，而且沒有用。

 



| 顯示名稱和索引列舉                                                    | 類型和預設值           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ 的 \_ RED \_ Y \_ 截距<br/>     | FLOAT<br/> 0.0f<br/> | 紅色通道之線性函式的 Y 截距。                                                                                                                                                                                                                                                                                                                                                                                                   |
| RedSlope<br/> D2D1 \_ LINEARTRANSFER \_ 的 \_ 紅色 \_ 斜率<br/>                 | FLOAT<br/> 1.0f<br/> | 紅色通道之線性函式的斜率。                                                                                                                                                                                                                                                                                                                                                                                                         |
| RedDisable<br/> D2D1 \_ LINEARTRANSFER \_ 的 \_ RED \_ DISABLE<br/>             | BOOL<br/> FALSE<br/> | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至紅色通道。 如果您將此設定為 FALSE，效果會將 RedLinearTransfer 函式套用至紅色通道。                                                                                                                                                                                                                                                                    |
| GreenYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ 為 \_ 綠色的 \_ Y \_ 攔截<br/> | FLOAT<br/> 0.0f<br/> | 綠色通道的線性函式的 Y 攔截。                                                                                                                                                                                                                                                                                                                                                                                                 |
| GreenSlope<br/> D2D1 \_ LINEARTRANSFER \_ 的 \_ 環保 \_ 斜率<br/>             | FLOAT<br/> 1.0f<br/> | 綠色通道線性函式的斜率。                                                                                                                                                                                                                                                                                                                                                                                                       |
| GreenDisable<br/> D2D1 \_ LINEARTRANSFER，a \_ \_ 綠 \_ DISABLE<br/>         | BOOL<br/> FALSE<br/> | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至綠色通道。 如果您將此設定為 FALSE，則會將 GreenLinearTransfer 函式套用至綠色通道。                                                                                                                                                                                                                                                                      |
| BlueYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ 的 \_ 藍色 \_ Y \_ 截距<br/>   | FLOAT<br/> 0.0f<br/> | 藍色色板線性函式的 Y 攔截。                                                                                                                                                                                                                                                                                                                                                                                                  |
| BlueSlope<br/> D2D1 \_ LINEARTRANSFER \_ 的 \_ 藍色 \_ 斜率<br/>               | FLOAT<br/> 1.0f<br/> | 藍色色板的線性函數斜率。                                                                                                                                                                                                                                                                                                                                                                                                        |
| BlueDisable<br/> D2D1 \_ LINEARTRANSFER \_ 的 \_ BLUE \_ DISABLE<br/>           | BOOL<br/> FALSE<br/> | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至藍色通道。 如果您將此設定為 FALSE，則會將 BlueLinearTransfer 函式套用至藍色通道。                                                                                                                                                                                                                                                                         |
| AlphaYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ 的 \_ ALPHA \_ Y \_ 截距<br/> | FLOAT<br/> 0.0f<br/> | Alpha 色板線性函式的 Y 攔截。                                                                                                                                                                                                                                                                                                                                                                                                 |
| AlphaSlope<br/> D2D1 \_ LINEARTRANSFER \_ 的 \_ ALPHA \_ 斜率<br/>             | FLOAT<br/> 0.0f<br/> | Alpha 色板線性函數的斜率。                                                                                                                                                                                                                                                                                                                                                                                                       |
| AlphaDisable<br/> D2D1 \_ LINEARTRANSFER \_ 的 \_ ALPHA \_ 停用<br/>         | BOOL<br/> FALSE<br/> | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至 Alpha 通道。 如果您將此設定為 FALSE，則會將 AlphaLinearTransfer 函式套用至 Alpha 色板。                                                                                                                                                                                                                                                                      |
| ClampOutput<br/> D2D1 LINEARTRANSFER 的一種 \_ \_ \_ 夾具 \_ 輸出<br/>           | BOOL<br/> FALSE<br/> | 效果在效果之前個色彩值是否會將值傳遞給圖形中的下一個效果。 效果會在 premultiplies Alpha 之前個值。<br/> 如果您將此設定為 TRUE，效果會將值設為夾具。 如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。<br/> |



 

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

 

