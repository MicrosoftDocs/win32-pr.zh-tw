---
title: 有效圖形中的有效位數和數位裁剪
description: 使用 Direct2D 轉譯效果的應用程式必須謹慎，才能達到所需的品質和可預測性（相對於數值有效位數）。
ms.assetid: 6fd1d77f-e613-534f-3205-bad11fa24c30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f2af6fdee4561caa60ea22a0c700593f2333727e6c5a63c5346fdc78bbdb40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160474"
---
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a>有效圖形中的有效位數和數位裁剪

使用 Direct2D 轉譯效果的應用程式必須謹慎，才能達到所需的品質和可預測性（相對於數值有效位數）。 本主題說明 Direct2D 中的最佳作法和相關設定，這些設定在下列情況下很有用：

-   您的效果圖形依賴高數值有效位數或 \[ 0 （1）範圍以外的色彩 \] ，而您想要確保這些都能隨時可用
-   或者，您的效果圖形依賴轉譯程式來將中繼色彩夾具至 \[ 0，1個 \] 範圍，而且您想要確保此固定一律會發生

Direct2D 通常會將效果圖形分成各區段，並在個別的步驟中轉譯每個區段。 某些步驟的輸出可能會儲存在中繼 Direct3D 紋理中，依預設會有有限的數值範圍和精確度。 Direct2D 不會保證是否使用這些中繼紋理。 此行為可能會根據 GPU 功能以及 Windows 版本之間的不同而有所不同。

在 Windows 10 中，Direct2D 會使用較少的中繼紋理，因為它使用著色器連結。 因此，Direct2D 可能會產生與先前 Windows 版本中的預設設定不同的結果。 這主要會影響著色器連結可能在效果圖形中的案例，而該圖表也包含產生擴充範圍輸出色彩的效果。

## <a name="overview-of-effect-rendering-and-intermediates"></a>效果轉譯和中繼的總覽

為了呈現效果圖形，Direct2D 會先尋找「轉換」的基礎圖形，其中的轉換是在效果中使用的圖形節點。 有不同類型的轉換，包括提供 Direct3D 著色器供 Direct2D 使用。

例如，Direct2D 可能會轉譯效果圖形，如下所示：

![具有中繼紋理的效果圖表](images/precision-and-clipping-1.png)

Direct2D 會尋找機會減少用來呈現效果圖形的數位中繼紋理;此邏輯對應用程式而言是不透明的。 例如，您可以使用單一 Direct3D draw 呼叫和沒有中繼紋理來 Direct2D 轉譯下圖：

![沒有中繼紋理的效果圖表](images/precision-and-clipping-2.png)

在 Windows 10 之前，如果在相同效果圖形中使用多個圖元著色器，Direct2D 一律會使用中繼紋理。 大部分的內建效果，只要調整色彩值 (例如亮度或飽和度，) 使用圖元著色器來進行。

在 Windows 10 中，Direct2D 現在可以避免在這種情況下使用中繼紋理。 其運作方式是在內部連結連續的圖元著色器。 例如：

![具有多個圖元著色器且沒有中繼材質的 windows 10 效果圖形](images/precision-and-clipping-3.png)

請注意，圖表中並非所有連續的圖元著色器都可以連結在一起，因此只有特定圖形會在 Windows 10 上產生不同的輸出。 如需完整的詳細資訊，請參閱 [效果著色器連結](effect-shader-linking.md)。 主要限制如下：

-   如果第一個效果是連接到多個效果的輸入，則效果將不會與使用其輸出的效果相連結。
-   如果第一個效果將其輸入的輸入在不同的邏輯位置（而非其輸出），效果將不會與效果集合連結做為其輸入。 例如，色彩矩陣效果可能會與其輸入連結，但不會有卷積效果。

## <a name="built-in-effect-behavior"></a>內建效果行為

許多內建效果可能會 \[ 在 unpremultiplied 色彩空間中的0（1）之外產生色彩 \] ，即使它們的輸入色彩在該範圍內也一樣。 發生這種情況時，這類色彩可能會受到數位裁剪的影響。 請注意，即使內建效果通常會在預乘空間中產生色彩，但請務必考慮 unpremultiplied 空間中的色彩範圍。 這可確保色彩維持在範圍內，即使其他效果接著 unpremultiply 它們也是如此。

可能會發出這些超出範圍色彩的某些效果會提供 "ClampOutput" 屬性。 其中包含：

-   [色彩矩陣](color-matrix.md)
-   [算術複合](arithmetic-composite.md)
-   [>Convolve](convolve-matrix.md)
-   [傳送效果](built-in-effects.md)

在這些效果上將 ClampOutput 屬性設定為 TRUE，可確保不論是否有著色器連結等因素，都能達成一致的結果。 請注意，固定會發生在 unpremultiplied 空間中。

其他內建效果也可能會產生超出0的輸出色彩 \[ ， \] unpremultiplied 空間中的1個範圍，即使在該範圍內有任何) ，也可能會產生色彩圖元 (和 "Color" 屬性。 其中包含：

-   在插補模式屬性為立方或高品質的三種情況下， ([轉換和調整效果](built-in-effects.md)) 
-   [光源效果](built-in-effects.md)
-   覆迭邊緣屬性為 TRUE 時， [Edge 偵測](edge-detection-effect.md) () 
-   [曝光](exposure-effect.md)
-   當 Mode 屬性為加號時，[複合](composite.md) () 
-   [溫度和色調](temperature-and-tint-effect.md)
-   [懷舊](sepia-effect.md)
-   [飽和度](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a>在效果圖形內強制進行數位裁剪

使用上方所列的效果沒有 ClampOutput 屬性時，應用程式應該考慮強制執行數值固定。 這可以藉由在圖形中插入個其圖元的額外效果來完成。 您可以使用色彩矩陣效果，並將其 ' ClampOutput ' 屬性設定為 TRUE，並將 ' ColorMatrix ' 屬性保留為預設 (傳遞) 值。

達到一致結果的第二個選項，是要求 Direct2D 使用具有較高精確度的中繼紋理。 如下所述。

## <a name="controlling-precision-of-intermediate-textures"></a>控制中繼紋理的精確度

Direct2D 提供數種方式來控制圖形的精確度。 在 Direct2D 中使用高精確度格式之前，應用程式必須確定 GPU 可充分支援這些格式。 若要檢查這一點，請使用 [**ID2D1DeviceCoNtext：： IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported)。

應用程式可以使用變形 (軟體模擬) 來建立 Direct3D 裝置，以保證所有緩衝區精確度都支援獨立于裝置上的實際 GPU 硬體。 這在儲存至磁片的情況下，建議您將效果套用到相片。 即使 Direct2D 在 GPU 上支援高精確度的緩衝區格式，在此案例中，建議在功能層級6.x 的 Gpu 上使用變形，因為著色器算術的精確度有限，並取樣一些低功率行動 Gpu。

在以下每個案例中，所要求的精確度實際上是 Direct2D 將使用的最小有效位數。 如果不需要中繼，則可以使用較高的有效位數。 Direct2D 可能也會共用相同圖表的不同部分或完全不同圖形的中繼紋理。 在此情況下，Direct2D 會使用針對所有相關作業要求的最大精確度。

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a>從 ID2D1DeviceCoNtext：： SetRenderingControls 的精確度選取範圍

控制 Direct2d 中繼材質精確度的最簡單方式是使用 [**ID2D1DeviceCoNtext：： SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))。 這會控制所有中繼紋理的精確度，只要不是手動手動設定效果或轉換的精確度也一樣。


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  // Get the current rendering controls
  D2D1_RENDERING_CONTROLS renderingControls = {};
  Context->GetRenderingControls(&renderingControls);

  // Switch the precision within the rendering controls and set it
  renderingControls.bufferPrecision = D2D1_BUFFER_PRECISION_32BPC_FLOAT;
  Context->SetRenderingControls(&renderingControls);
}
              
```



### <a name="precision-selection-from-inputs-and-render-targets"></a>輸入和轉譯目標的精確度選取範圍

應用程式可能也會依賴效果圖形輸入的精確度，來控制中繼紋理的精確度。 只要沒有使用 [**ID2D1DeviceCoNtext：： SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))指定緩衝區有效位數，而且不會直接在效果和轉換上手動設定，就會有這種情況。

效果的輸入精確度會透過圖形傳播，以選取下游中繼的精確度。 當效果圖形中的不同分支符合時，就會使用任何輸入的最大有效位數。

根據 Direct2D 點陣圖所選取的有效位數取決於其像素格式。 針對 [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) 所選取的精確度，是由用來建立 **ID2D1ImageSource** 之基礎 IWICBitmapSource 的 WIC 像素格式所決定。 請注意，Direct2D 不允許使用 Direct2D 和 GPU 不支援的精確度來建立具有 WIC 來源的影像來源。

Direct2D 無法根據輸入來指派有效位數的有效位數。 當效果沒有任何輸入，或使用 [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) 時（沒有特定精確度），就會發生這種情況。 在此情況下，中繼紋理的有效位數是由點陣圖集合中的內容目前轉譯目標所決定。

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a>直接在效果和轉換上選取精確度

您也可以在效果圖形中的明確位置設定中繼紋理的最小有效位數。 這只建議用於 advanced 案例。

您可以使用效果上的屬性來設定最小有效位數，如下所示：


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



在效果的執行中，可以使用 ID2D1RenderInfo：： SetOutputPrecision 來設定最小有效位數，如下所示：


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



請注意，在效果上設定的有效位數會傳播至相同效果圖形中的下游效果，除非這些下游效果設定了不同的精確度。 在效果內轉換中設定的有效位數不會影響下游轉換節點的有效位數。

以下是完整的遞迴邏輯，用來判斷儲存指定轉換節點輸出之中繼緩衝區的最小有效位數：

![中繼緩衝區的最小精確度邏輯](images/precision-and-clipping-4.png)

 

 