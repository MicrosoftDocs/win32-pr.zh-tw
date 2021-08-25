---
title: 卷積矩陣效果
description: 使用 >convolve 矩陣效果將任意2D 核心套用至影像。 您可以使用此效果來模糊、偵測邊緣、浮凸或對影像進行銳化。
ms.assetid: D9C23AC4-0090-4F16-AC59-B952FB616FA9
keywords:
- '>convolve 矩陣效果'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3b988e0bd48fece4d767fad29b63fe021c82d49d07dae5ab3f1b10b3f9794f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833370"
---
# <a name="convolve-matrix-effect"></a>卷積矩陣效果

使用 >convolve 矩陣效果將任意2D 核心套用至影像。 您可以使用此效果來模糊、偵測邊緣、浮凸或對影像進行銳化。

這項效果的 CLSID 是 CLSID \_ D2D1ConvolveMatrix。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [調整模式](#scale-modes)
-   [框線模式](#border-modes)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此處的範例顯示具有 3 x 3 核心的 >convolve 矩陣效果的輸入和輸出。



| 之前                                                         |
|----------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)     |
| After                                                          |
| ![轉換後的影像。](images/6-convolvematrix.png) |



 


```C++
ComPtr<ID2D1Effect> convolveMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ConvolveMatrix, &convolveMatrixEffect);

convolveMatrixEffect->SetInput(0, bitmap);
float matrix[9] = {-1, -1, -1, -1, 9, -1, -1, -1, -1};
convolveMatrixEffect->SetValue(D2D1_CONVOLVEMATRIX_PROP_KERNEL_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(convolveMatrixEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KernelUnitLength<br/> D2D1 \_ CONVOLVEMATRIX \_ 的 \_ 核心 \_ 單位 \_ 長度<br/> | 核心中一個單位的大小。 單位位於 (Dip/核心單位) ，其中核心單位是卷積核心中的元素大小。 值 1 (DIP/核心單位) 對應至影像中的一個圖元（96 DPI）。<br/> 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                   |
| ScaleMode<br/> D2D1 \_ CONVOLVEMATRIX \_ 的 \_ 範圍調整 \_ 模式<br/>                 | 效果用來將影像調整為對應核心單位長度的插補模式。 有六個調整模式的品質和速度。<br/> 此類型為 D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ 模式。<br/> 預設值為 D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ 線性。<br/>                                                                                                                                                                                                                     |
| KernelSizeX<br/> D2D1 \_ CONVOLVEMATRIX \_ 的 \_ 核心 \_ 大小 \_ X<br/>           | 核心矩陣的寬度。 單位是以核心單位來指定。 此類型為 UINT32。<br/> 預設值是 3。<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| KernelSizeY<br/> D2D1 \_ CONVOLVEMATRIX \_ 的 \_ 核心 \_ 大小 \_ Y<br/>           | 核心矩陣的高度。 單位是以核心單位來指定。 此類型為 UINT32。<br/> 預設值是 3。<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| KernelMatrix<br/> D2D1 \_ CONVOLVEMATRIX \_ 的 \_ 核心 \_ 矩陣<br/>           | 要套用至映射的核心矩陣。 核心元素未系結，並指定為浮動。<br/> 浮點數中的第一組 *KernelSizeX* 數位會 \[ \] 對應至核心中的第一個資料列。 第二組 *KernelSizeX* 號碼會對應到第二個數據列，依此類推，直到 *KernelSizeY* 資料列為止。<br/> 此類型為 FLOAT \[ \] 。<br/> 預設值為 {0.0 f、0.0 f、0.0 f、0.0 f、1.0 f、0.0 f、0.0 f、0.0 f、0.0 f}。<br/>                                                       |
| 除數<br/> D2D1 \_ CONVOLVEMATRIX 的 \_ \_<br/>                       | 核心矩陣會套用至圖元，然後結果會除以此值。 <br/> 0的行為是 float epsilon 的值。<br/> 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                           |
| 偏差<br/> D2D1 \_ CONVOLVEMATRIX 的情況 \_ \_ 偏差<br/>                             | 效果會套用核心矩陣、除數，然後將偏差新增至結果。 偏差未系結且沒有用。 此類型為 FLOAT。<br/> 預設值為 0.0 f。<br/>                                                                                                                                                                                                                                                                                                                              |
| KernelOffset<br/> D2D1 \_ CONVOLVEMATRIX \_ 的 \_ 核心 \_ 位移<br/>           | 將卷積核心從輸出圖元上的置中位置移至您指定的左/右和向上/向下位置。 位移是以核心單位來定義。<br/> 有一些位移和核心大小，硬碟上的核心樣本不會落在圖元影像中心。 核心樣本的圖元值是透過雙線性插補來計算。<br/> 此類型為 D2D1 \_ VECTOR \_ 2f。<br/> 預設值為 {0.0 f，0.0 f}。<br/>                                                          |
| PreserveAlpha<br/> D2D1 \_ CONVOLVEMATRIX \_ 的 \_ \_ 分量保留 ALPHA<br/>         | 指定是否要將卷積核心套用至 Alpha 色板或只套用色頻。<br/> 如果您將此設定為 **TRUE** ，則只會將卷積核心套用至色彩通道。<br/> 如果您將此設定為 **FALSE** ，則會將卷積核心套用至所有通道。<br/> 此類型為 BOOL。<br/> 預設值為 FALSE。<br/>                                                                                                                                               |
| BorderMode<br/> D2D1 \_ CONVOLVEMATRIX \_ 的 \_ 樣式框線 \_ 模式<br/>               | 用來計算影像（軟或硬）框線的模式。 如需詳細資訊，請參閱 [框線模式](https://www.bing.com/search?q=Border+modes) 。<br/> 此類型為 D2D1 \_ 框線 \_ 模式。<br/> 預設值為 [D2D1 \_ 框線 \_ 模式] \_ 。<br/>                                                                                                                                                                                                                                                                                     |
| ClampOutput<br/> D2D1 CONVOLVEMATRIX 的一種 \_ \_ \_ 夾具 \_ 輸出<br/>             | 效果在效果之前個色彩值是否會將值傳遞給圖形中的下一個效果。 效果會在 premultiplies Alpha 之前個值。<br/> 如果您將此設定為 TRUE，效果會將值設為夾具。 如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。<br/> 此類型為 BOOL。<br/> 預設值為 FALSE。<br/> |



 

## <a name="scale-modes"></a>調整模式



| 列舉型別                                              | 描述                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 CONVOLVEMATRIX 調整模式     | 範例最接近的單一點，並使用該點。 這個模式會使用較少的處理時間，但會輸出最低品質的影像。                                                                           |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ 模式 \_ 線性                | 使用四個點取樣和線性插補。 此模式會輸出比最近的鄰近模式更高的品質影像。                                                                              |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ 模式 \_ 立方                 | 使用16個範例三核心來進行插補。 這個模式會使用大部分的處理時間，但會輸出較高品質的影像。                                                                        |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ 多重 \_ 範例 \_ 線性 | 使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。 這種模式適合用來在具有少量圖元的影像上相應減少量。                                              |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ 模式 \_ 非等           | 根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。                                                                                                     |
| D2D1 \_ CONVOLVEMATRIX \_ 調整 \_ 模式 \_ 高 \_ 品質 \_ 三階  | 如果 downscaling 與轉換矩陣有關，則使用可變大小的高品質三核心來執行預先縮小的影像。 然後使用三次插補模式來進行最終輸出。 |



 

> [!Note]  
> 如果您未選取模式，效果會預設為 D2D1 \_ CONVOLVEMATRIX \_ 縮放 \_ 模式 \_ 線性。

 

## <a name="border-modes"></a>框線模式



| 名稱                     | 描述                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 框線 \_ 模式 \_ 軟 | 此效果會在輸入影像套用卷積核心時，以透明的黑色圖元為單位，以透明的方式在輸入界限之外取得樣本。 這會建立影像的軟邊緣，並且在進程中依核心的大小展開輸出點陣圖。<br/> |
| D2D1 \_ 框線 \_ 模式 \_ 硬性 | 效果會使用鏡像類型的框線轉換來擴充輸入界限之外樣本的輸入影像。 輸出點陣圖的大小等於輸入點陣圖的大小。<br/>                                                                       |



 

## <a name="output-bitmap"></a>輸出點陣圖

效果的輸出大小取決於卷積核心的大小、核心位移、核心單位長度和框線模式設定。

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

 

