---
title: 長條圖效果
description: 使用長條圖效果，根據指定的 bin 數目產生輸入點陣圖的長條圖。
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- 長條圖效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384493"
---
# <a name="histogram-effect"></a>長條圖效果

使用長條圖效果，根據指定的 bin 數目產生輸入點陣圖的長條圖。

這項效果的 CLSID 是 CLSID \_ D2D1Histogram。

-   [範例](#example)
-   [效果屬性](#effect-properties)
-   [通道選取器](#channel-selectors)
-   [資料輸出](#data-output)
-   [備註](#remarks)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example"></a>範例



| 之前                                                     |
|------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg) |
| 長條圖輸出資料的圖表                         |
| ![轉換後的影像。](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a>效果屬性

以下是產生輸出的方程式。

![產生長條圖效果輸出的方程式。](images/histogram-formula.png)

*我* 會從0到 bin 數目進行評估。效果會產生介於0和1之間圖元值的長條圖。 此範圍外的值會壓制至範圍。 特定值區的範圍取決於 bucket 數目。 此效果適用于純點陣圖圖元。 輸入點陣圖的色彩通道是由 Alpha 色板除以，以計算此效果。



| 顯示名稱和索引列舉                                             | 類型和預設值                                                   | Description                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NumBins<br/> D2D1 \_ 長條圖 \_ 的 \_ 數目 \_ 分類<br/>                 | UINT32<br/> 256<br/>                                         | 指定用於長條圖的 bin 數目。 落在特定值區中的濃度值範圍取決於指定的 bucket 數目。                              |
| ChannelSelect<br/> D2D1 \_ 長條圖 \_ 的 \_ \_ 選擇通道<br/>     | D2D1 \_ 通道 \_ 選取器<br/> D2D1 \_ 通道 \_ 選取器 \_ R<br/> | 指定用來產生長條圖的通道。 此效果具有對應至指定通道的單一資料輸出。 如需詳細資訊，請參閱 [通道選取器](#channel-selectors) 。 |
| HistogramOutput<br/> D2D1 \_ 長條圖 \_ 的 \_ 長條圖 \_ 輸出<br/> | 浮動\[\]<br/> 僅限輸出屬性。<br/>                    | 輸出陣列。                                                                                                                                                                             |



 

## <a name="channel-selectors"></a>通道選取器



| 列舉型別                | 描述                                                           |
|----------------------------|-----------------------------------------------------------------------|
| D2D1 \_ 通道 \_ 選取器 \_ R | 效果會根據紅色通道產生長條圖輸出。   |
| D2D1 \_ 通道 \_ 選取器 \_ G | 效果會根據綠色通道產生長條圖輸出。 |
| D2D1 \_ 通道 \_ 選取器 \_ B | 效果會根據藍色通道產生長條圖輸出。  |
| D2D1 \_ 通道 \_ 選取器 \_ A | 效果會根據 Alpha 色板產生長條圖輸出。 |



 

## <a name="data-output"></a>資料輸出

此效果會輸出浮點數 \[ \] ，其中包含對應至指定之 bin 數目的專案數目。FLOAT 中的每個元素 \[ \] 都是浮點數。 元素的值會對應到該 bin 中的元素數目。

## <a name="remarks"></a>備註

> [!Note]  
> 如果裝置不支援 DirectCompute， [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) 方法會失敗，並傳回 HRESULT = D2DERR 的 \_ \_ 裝置 \_ 功能不足。 所有支援 DirectCompute 的 DirectX11 卡和 DirectX10 卡片都可以使用效果。

 

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

 

