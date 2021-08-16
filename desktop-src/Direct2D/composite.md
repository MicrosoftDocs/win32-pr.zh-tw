---
title: 複合效果
description: 使用複合效果結合2個或多個影像。 此效果有13個不同的複合模式。
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- 複合效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cf326e5d0bfb33b3dc927ba7366eb6d2b343a1a50db462de58fac8ef648bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826570"
---
# <a name="composite-effect"></a>複合效果

使用複合效果結合2個或多個影像。 此效果有13個不同的複合模式。 T

複合效果接受2個以上的輸入。 當您指定2個影像時，目的地是第一個輸入 (索引 0) ，而來源是第二個輸入 (索引 1) 。 如果您指定2個以上的輸入，則影像會從第一個輸入開始，而第二個則是從第一個輸入開始，依此類推。

此效果會使用圖形處理器 (GPU) 的混合單位來執行所有模式。

這項效果的 CLSID 是 CLSID \_ D2D1Composite。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [模式類型](#mode-types)
-   [範例程式碼](#sample-code)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此處的影像顯示兩個相同大小重迭的圓角矩形。 藍色矩形是來源，紅色矩形是目的地。 這些映射是由來源 Over 模式所撰寫。

![範例影像，顯示使用來源 over 模式重迭的兩個相同大小的圓角矩形。](images/composite-over.png)

以下是使用預設模式的另一個範例。



| 影像1之前                                                          |
|-------------------------------------------------------------------------|
| ![效果前的第一個來源影像。](images/default-before.jpg) |
| 影像2之前                                                          |
| ![效果之前的第二個影像。](images/3-composite(2of2).png)    |
| After                                                                   |
| ![轉換後的影像。](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                     | 類型和預設值                                                          | 描述                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| [模式]<br/> D2D1 \_ 複合 \_ \_ 模型模式<br/> | D2D1 \_ 複合 \_ 模式<br/> D2D1 \_ 複合 \_ 模式 \_ 來源 \_<br/> | 效果所使用的模式。 |



 

## <a name="mode-types"></a>模式類型

此處的表格顯示此效果的模式。 表格中所列的方能使用下列元素：

-   O = 輸出
-   S = 來源
-   SA = 來源 Alpha
-   D = 目的地
-   DA = 目的地 Alpha



| 列舉型別                                  | 方程                          | 輸出點陣圖大小                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| D2D1 \_ 複合 \_ 模式 \_ 來源 \_          | O = S + (1 SA) \* D             | 來源和目的地點陣圖的聯集                                                                 |
| D2D1 \_ 複合 \_ 模式 \_ 目的地 \_     | O = (1 DA) \* S + D             | 來源和目的地點陣圖的聯集                                                                 |
| D2D1 \_ 複合 \_ 模式 \_ 來源 \_            | O = DA \* S                       | 來源和目的地點陣圖的交集                                                          |
| D2D1 \_ 複合 \_ 模式 \_ 目的地 \_       | O = SA \* D                       | 來源和目的地點陣圖的交集                                                          |
| D2D1 \_ 複合 \_ 模式 \_ 來源 \_ 輸出           | O = (1-DA) \* S                 | 來源點陣圖的區域                                                                             |
| D2D1 \_ 複合 \_ 模式 \_ 目的地 \_ 輸出      | O = (1-SA) \* D                 | 目的地點陣圖的區域                                                                        |
| D2D1 \_ 複合 \_ 模式 \_ 來源 \_          | O = DA \* S + (1-SA) \* D       | 目的地點陣圖的區域                                                                        |
| D2D1 \_ 複合 \_ 模式 \_ 目的地 \_     | O = (1-DA) \* S + SA \* D       | 來源點陣圖的區域                                                                             |
| D2D1 \_ 複合 \_ 模式 \_ XOR                   | O = (1-DA) \* S + (1-SA) \* D | 來源和目的地點陣圖的聯集                                                                 |
| D2D1 \_ 複合 \_ 模式 \_ 加號                  | O = S + D                         | 來源和目的地點陣圖的聯集                                                                 |
| D2D1 \_ 複合 \_ 模式 \_ 來源 \_ 複製          | O = S                             | 來源點陣圖的區域                                                                             |
| D2D1 \_ 複合 \_ 模式系結 \_ \_ 來源 \_ 複製 | O = S (只有在來源存在時)   | 來源和目的點陣圖的聯集。 來源不存在時，不會覆寫目的地。 |
| D2D1 \_ 複合 \_ 模式 \_ 遮罩 \_ 倒轉          | O = (1 D) \* S + (1 SA) \* D  | 來源和目的點陣圖的聯集。Alpha 值是不變的。                                 |



 

下圖顯示每個模式的範例，其中包含不透明度為1.0 或0.5 的影像。

![每個模式的範例影像，其不透明度設定為1.0 或0.5。](images/composite-types.png)

## <a name="sample-code"></a>範例程式碼

如需此效果的範例，請下載 [Direct2D 複合效果模式範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)。

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

 

