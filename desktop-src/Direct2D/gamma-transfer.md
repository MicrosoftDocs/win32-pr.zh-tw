---
title: Gamma 傳送效果
description: 使用 gamma 傳送效果，以使用以振幅、指數和您為每個通道提供的位移所建立的 gamma 函式來對應影像的色彩濃度。
ms.assetid: 0E0455CA-CFCA-4C4F-9DFA-1DB6A5205F6A
keywords:
- gamma 傳送效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b806ac8f59efe1b3fad3b61edc7f88f72b143f9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843956"
---
# <a name="gamma-transfer-effect"></a>Gamma 傳送效果

使用 gamma 傳送效果，以使用以振幅、指數和您為每個通道提供的位移所建立的 gamma 函式來對應影像的色彩濃度。

這項效果的 CLSID 是 CLSID \_ D2D1GammaTransfer。 若要使用這項效果，請將 dxguid 新增至連結器相依性。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像



| 之前                                                         |
|----------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)     |
| After                                                          |
| ![轉換後的影像。](images/14-gammatransfer.png) |



 


```C++
ComPtr<ID2D1Effect> gammaTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GammaTransfer, &gammaTransferEffect);

gammaTransferEffect->SetInput(0, bitmap);

gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_EXPONENT, 0.25f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gammaTransferEffect.Get());
m_d2dContext->EndDraw();
```



此效果會根據此處的方程式套用 gamma 傳送函式。

輸入圖元濃度會以 C 和輸出圖元濃度表示為 C '。 C ' = 振幅 \* C<sup>指數</sup> + 位移

此效果適用于直接和預乘的 Alpha 影像。 效果會輸出預乘的 Alpha 點陣圖。

## <a name="effect-properties"></a>效果屬性

> [!Note]  
> 針對 gamma 傳送屬性的所有通道：
>
> -   振幅值未系結，而且沒有單位。
> -   指數值未系結，而且沒有單位。
> -   位移值未系結，而且沒有單位。

 



| 顯示名稱和索引列舉                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedAmplitude<br/> D2D1 \_ GAMMATRANSFER \_ 將 \_ RED \_ 振幅<br/>     | 紅色通道之 gamma 傳送函式的波幅。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| RedExponent<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ 成分紅色 \_ 指數<br/>       | 紅色通道之 gamma 傳送函式的指數。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| RedOffset<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ RED \_ OFFSET<br/>           | 紅色通道之 gamma 傳送函式的位移。 此類型為 FLOAT。<br/> 預設值為 0.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| RedDisable<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ RED \_ DISABLE<br/>         | 如果您將此設定為 TRUE，則不會將傳送函式套用至紅色通道。 使用身分識別傳送函式。 如果您將此設定為 FALSE，則會將 gamma 傳送函式套用至紅色通道。 此類型為 BOOL。<br/> 預設值為 FALSE。<br/>                                                                                                                                                                                                                                                |
| GreenAmplitude<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ 環保 \_ 振幅<br/> | 綠色通道之 gamma 傳送函式的波幅。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| GreenExponent<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ 環保 \_ 指數<br/>   | 綠色通道之 gamma 傳送函數的指數。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| GreenOffset<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ 環保 \_ 位移<br/>       | 綠色通道之 gamma 傳送函式的位移。 此類型為 FLOAT。<br/> 預設值為 0.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| GreenDisable<br/> D2D1 \_ GAMMATRANSFER，a \_ \_ 綠 \_ DISABLE<br/>     | 如果您將此設定為 TRUE，則不會將傳送函式套用至綠色通道。 使用身分識別傳送函式。 如果您將此設定為 FALSE，則會將 gamma 傳送函式套用至綠色通道。 此類型為 BOOL。<br/> 預設值為 FALSE。<br/>                                                                                                                                                                                                                                            |
| BlueAmplitude<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ BLUE \_ 波幅<br/>   | 藍色色板的 gamma 傳送函式幅度。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| BlueExponent<br/> D2D1 GAMMATRANSFER a a a a a a \_ \_ \_ BLUE \_ 指數<br/>     | 藍色通道之 gamma 傳送函式的指數。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| BlueOffset<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ BLUE \_ OFFSET<br/>         | Blue 通道之 gamma 傳送函式的位移。 此類型為 FLOAT。<br/> 預設值為 0.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| BlueDisable<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ BLUE \_ DISABLE<br/>       | 如果您將此設定為 TRUE，則不會將傳送函式套用至藍色通道。 使用身分識別傳送函式。 如果您將此設定為 FALSE，則會將 gamma 傳送函式套用至藍色通道。 此類型為 BOOL。<br/> 預設值為 FALSE。<br/>                                                                                                                                                                                                                                              |
| AlphaAmplitude<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ ALPHA \_ 波幅<br/> | Alpha 色板的 gamma 傳送函式幅度。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| AlphaExponent<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ ALPHA \_ 指數<br/>   | Alpha 色板之 gamma 傳送函式的指數。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| AlphaOffset<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ ALPHA \_ 位移<br/>       | Alpha 色板的 gamma 傳送函式位移。 此類型為 FLOAT。<br/> 預設值為 0.0 f。<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| AlphaDisable<br/> D2D1 \_ GAMMATRANSFER \_ 的 \_ ALPHA \_ 停用<br/>     | 如果您將此設定為 TRUE，則不會將傳送函式套用至 Alpha 通道。 使用身分識別傳送函式。 如果您將此設定為 FALSE，則會將 gamma 傳送函式套用至 Alpha 通道。 此類型為 BOOL。<br/> 預設值為 FALSE。<br/>                                                                                                                                                                                                                                            |
| ClampOutput<br/> D2D1 GAMMATRANSFER 的一種 \_ \_ \_ 夾具 \_ 輸出<br/>       | 效果在效果之前個色彩值是否會將值傳遞給圖形中的下一個效果。 效果會在 premultiplies Alpha 之前個值。<br/> 如果您將此設定為 TRUE，效果會將值設為夾具。 如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。<br/> 此類型為 BOOL。<br/> 預設值為 FALSE。<br/> |



 

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

 

