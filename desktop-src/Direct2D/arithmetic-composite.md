---
title: 算術複合效果
description: 使用算術複合效果，以使用輸入影像中圖元的加權總和來合併2個影像。
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- 算術複合效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934846"
---
# <a name="arithmetic-composite-effect"></a>算術複合效果

使用算術複合效果，以使用輸入影像中圖元的加權總和來合併2個影像。

這項效果的 CLSID 是 CLSID \_ D2D1ArithmeticComposite。

-   [Formula](#formula)
-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="formula"></a>Formula

這裡的公式可用來計算此效果。

輸出<sub>rgba</sub> = C1 \* 來源<sub>rgba</sub> \* 目的地<sub>rgba</sub> + c2 \* 來源<sub>rgba</sub> + c3 \* 目的地<sub>rgba</sub> + c4

其中 C1、C2、C3、C4 是您所設定的係數。

係數會對應至 D2D1 向量中的值 \_ \_ 4F (x、y、z、w) ：

-   x = C1
-   y = C2
-   z = C3
-   w = C4

## <a name="example-image"></a>範例影像

簡單的範例是加入來源和目的地圖元。 在此範例中，會將兩個圓角的矩形組合在一起。 來源矩形為藍色，目的地為紅色。

此處的影像是算術複合效果的輸出，其方程式的係數設定為此處的值。

-   C1 = 0
-   C2 = 1
-   C3 = 1
-   C4 = 0

![範例影像，顯示使用算術複合效果重迭的兩個相同大小的圓角矩形。](images/arithmetic-50-percent.png)

結果是會加入來源和目的地的圖元值。 矩形不會與 RGBA 值重迭的區域全部都是0。 因為 R 和 B 值都是最大值，所以矩形會重迭色彩為洋紅。

以下是另一個包含程式碼的範例影像。



| 影像1之前                                                             |
|----------------------------------------------------------------------------|
| ![效果前的第一個來源影像。](images/default-before.jpg)    |
| 影像2之前                                                             |
| ![效果之前的第二個影像。](images/4-arthimetic-composite2.jpg) |
| After                                                                      |
| ![轉換後的影像。](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 係數<br/> D2D1 ARITHMETICCOMPOSITE 的各種 \_ \_ \_ 係數<br/> | 用來組合兩個輸入影像的方程式係數。 係數沒有單位或未系結。 類型為 D2D1 \_ VECTOR \_ 4F。<br/> 預設值為 {1.0 f、0.0 f、0.0 f、0.0 f}。<br/>                                                                                                                                                                                                                                 |
| ClampOutput<br/> D2D1 ARITHMETICCOMPOSITE 的一種 \_ \_ \_ 夾具 \_ 輸出<br/> | 效果會個色彩值在0和1之間，效果會將值傳遞給圖形中的下一個效果。 <br/> 如果您將此設定為 TRUE，效果會將值設為夾具。 如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。<br/> 類型為 BOOL。<br/> 預設值為 FALSE。<br/> |



 

## <a name="output-bitmap"></a>輸出點陣圖

輸出點陣圖取決於係數值。 這些是可能的輸出點陣圖大小。

-   如果 C1 是唯一的非零係數，則輸出大小是輸入矩形的交集。
-   如果 C2 是唯一的非零係數，輸出大小就是來源矩形的大小。
-   如果 C3 是唯一的非零係數，輸出大小就是目的地矩形的大小。
-   如果所有係數都是零，則輸出大小為空的矩形。
-   針對所有其他係數值，輸出大小為輸入矩形的聯集。

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

 

