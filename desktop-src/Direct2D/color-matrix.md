---
title: 色彩矩陣效果
description: 使用色彩矩陣效果來改變點陣圖的 RGBA 值。
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- 色彩矩陣效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8bb461698e4f8b39eef3bed57fc21947f3cc1175c1bdf4f990629db87e1c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653300"
---
# <a name="color-matrix-effect"></a>色彩矩陣效果

使用色彩矩陣效果來改變點陣圖的 RGBA 值。

您可以使用此效果：

-   從影像中移除色彩通道。
-   減少影像中的色彩。
-   交換色彩通道。
-   結合色彩通道。

許多內建效果都是色彩矩陣的特製化，已針對效果的預期用途進行優化。 範例包括 [飽和度](saturation.md)、 [色調旋轉](hue-rotate.md)、 [棕褐色](sepia-effect.md)和 [溫度和色調](temperature-and-tint-effect.md)。

這項效果的 CLSID 是 CLSID \_ D2D1ColorMatrix。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [Alpha 模式](#alpha-modes)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此處的範例會顯示交換紅色和藍色通道之色彩矩陣效果的輸入和輸出影像。



| 之前                                                       |
|--------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)   |
| After                                                        |
| ![轉換後的影像。](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



此效果會將影像的 RGBA 值乘以此方程式所示的5x4、資料行主要矩陣。

![範例矩陣定義。](images/color-matrix-formula.png)

此效果適用于直接和預乘的 Alpha 影像。

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ColorMatrix<br/> D2D1 \_ COLORMATRIX \_ 的 \_ 色彩 \_ 矩陣<br/> | Float 值的5x4 矩陣。 矩陣中的元素未系結，而且沒有單位。<br/> 預設值為識別矩陣。<br/> 此類型為 D2D1 \_ 矩陣 \_ 5X4 \_ F。<br/> 預設值為 Matrix5x4F (1、0、0、0、0、1、0、0、0、0、1、0、0、0、0、1、0、0、0、0) 。 <br/>                                                                                                                                                                                                                        |
| AlphaMode<br/> D2D1 \_ COLORMATRIX \_ 的 \_ ALPHA \_ 模式<br/>     | 輸出的 Alpha 模式。 如需詳細資訊，請參閱 [Alpha 模式](#alpha-modes) 。 <br/> 此類型為 D2D1 \_ COLORMATRIX \_ ALPHA \_ 模式。<br/> 預設值是預乘的 D2D1 \_ COLORMATRIX \_ ALPHA \_ 模式 \_ 。<br/>                                                                                                                                                                                                                                                                                                    |
| ClampOutput<br/> D2D1 COLORMATRIX 的一種 \_ \_ \_ 夾具 \_ 輸出<br/> | 效果在效果之前個色彩值是否會將值傳遞給圖形中的下一個效果。 效果會在 premultiplies Alpha 之前個值。<br/> 如果您將此設定為 TRUE，效果會將值設為夾具。 如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。<br/> 此類型為 BOOL。<br/> 預設值為 FALSE。<br/> |



 

## <a name="alpha-modes"></a>Alpha 模式



| 名稱                                          | 描述                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 預 \_ 乘的 D2D1 COLORMATRIX \_ ALPHA \_ 模式 \_ | 此效果會取消 premultiplies 輸入、套用色彩矩陣，以及 premultiplies 輸出。<br/> |
| D2D1 \_ COLORMATRIX \_ ALPHA \_ 模式 \_ 直接      | 效果會將色彩矩陣直接套用至輸入，而且不會 premultiply 輸出。<br/> |



 

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

 

