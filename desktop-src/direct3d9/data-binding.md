---
description: 您可以使用 SasHostParameterValue 集合來定義主應用程式值的集合，以及其類型和成員，而這些值會公開給效果。
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: 資料繫結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317592"
---
# <a name="data-binding"></a>資料繫結

您可以使用 [SasHostParameterValue 集合](#sashostparametervalue-collection) 來定義主應用程式值的集合，以及其類型和成員，而這些值會公開給效果。 使用效果檔案中的 [SasBindAddress](#sasbindaddress) 注釋，將效果參數與其在主應用程式中對應的參數產生關聯。

## <a name="sashostparametervalue-collection"></a>SasHostParameterValue 集合

SasHostParameterValue 是使用效果檔案 () 語法來定義。 語法與效果檔案語法非常類似，但有一些差異。 例如，物件類型（例如 texture2d、取樣器和字串）在實際效果檔案中是不正確，但在 SasHostParameterValue 中是有效的。 主機應用程式可以使用任何方式來執行 SasHostParameterValue，只要它符合以下的描述即可：實際的定義位於 DXSAS 標準效果中，包括 file (\[ SDK Root \] /Utilities/Source/Sas/Sas.fxh) 。

請注意，SasHostParameterValue 中的陣列（例如燈光或攝影機）的長度不限。 這表示效果可以系結至這些陣列中的任何任意索引，而主應用程式必須在無法提供任何應用程式值的情況下，提供有意義的預設值。

某些類型和常數必須在 DXSAS 標準包含中定義，如標準包含的定義中所述。 這可讓您輕鬆地將 SasHostParameterValue 的匯總值系結至結構化效果參數。



| SasHostParameterValue 集合    | 類型            | 成員                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [Time](#time)                       | FLOAT           | 目前的 Sas。                                 |
|                                     | FLOAT           | Sas。上次時間                                |
|                                     | int             | FrameNumber                         |
| [環境對應](#environment-map) | textureCUBE     | Sas. EnvironmentMap                           |
| [相機](#camera)                   | SasCamera       | Sas 攝影機                                   |
|                                     | float4x4        | WorldToView                       |
|                                     | float4x4        | Sas. 投影                        |
|                                     | float2          | NearFarClipping                   |
| [淺色](#light)                     | SasAmbientLight | AmbientLight \[ ZeroOrMore \] ;                  |
|                                     | int             | Sas. NumAmbientLights                         |
|                                     | SasAmbientLight | DirectionalLight \[ ZeroOrMore \] ;              |
|                                     | int             | Sas. NumDirectionalLights                     |
|                                     | SasAmbientLight | PointLight \[ ZeroOrMore \] ;                    |
|                                     | int             | Sas. NumPointLights                           |
|                                     | SasAmbientLight | 焦點 \[ ZeroOrMore \] ;                     |
|                                     | int             | Sas. NumSpotLights                            |
| [Shadow](#shadow)                   | float4x4        | Sas. Shadow \[ ZeroOrMore \] 。WorldToShadow       |
|                                     | texture2D       | Sas. Shadow \[ ZeroOrMore \] 。ShadowMap           |
| [骨架](#skeleton)               | float4x4        | MeshToJointToWorld \[ OneOrMore\] |
|                                     | int             | NumJoints                       |



 

### <a name="time"></a>Time

主機應用程式的虛擬時鐘或時間值。 成員包括：

-   Sas。現在-將轉譯效果的時間點的主機應用程式虛擬時鐘的值。
-   [上一步]-目前在先前轉譯時的值。
-   FrameNumber-每個轉譯框架都會遞增一次的計數器值。

效果必須適當地處理這些成員的值可能會在非常長的執行時間內換行的事實。 現在和最後的值可能會非常大。

### <a name="environment-map"></a>環境對應

立方環境對應。 如果效果嘗試系結至 EnvironmentMap，則主應用程式必須提供有效的 cube 紋理。

### <a name="camera"></a>相機

目前呈現的相機。 成員包括：

-   WorldToView-相機的複合世界視圖矩陣。
-   Sas. 投影-相機的投射矩陣。
-   NearFarClipping-接近或遠裁剪平面的值。

### <a name="light"></a>淺色

一或多個場景燈。 光源的集合會宣告為數組，其中：

-   色彩-RGB 色彩。 預設值為 (0,0,0)。
-   方向-淺色方向。 預設值為 (0,0,0)。
-   範圍-光線對場景沒有任何作用的距離。 預設值為 0。
-   Theta-焦點的內部錐形角度，以弧度為單位。 預設值為 0。
-   Phi-焦點的外部錐形角度，以弧度為單位。 預設值為 0。

燈光數目必須設定為系結至相關聯陣列的燈光數目。 效果可以選擇忽略燈光的數目，並系結至其中一個燈光陣列的任何元素。 因此，主機應用程式必須針對陣列中的燈光數目以外的元素提供有效的系結。

ZeroOrMore 意指陣列可以有任意數目的元素。

### <a name="shadow"></a>陰影

陰影緩衝區，其中包含：

-   WorldToShadow-矩陣的陣列。
-   ShadowMap-2D 材質檔。

ZeroOrMore 意指陣列可以有任意數目的元素 (零表示) 的空陣列。

效果會宣告取樣器，如下所示：


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a>骨架

組成目前呈現物件的框架組。 畫面格範例包括骨骼和轉換。 這包括：

-   MeshToJointToWorld-矩陣的陣列。
-   NumJoints-基本架構中的接點數目。

OneOrMore 意指陣列至少有一個，而且可以包含任何數目的元素。

定義支援使用相同的一組 [SasHostParameterValue 集合](#sashostparametervalue-collection) 值搭配不同的轉譯，來支援固定和 skinned 的網狀物件。

## <a name="sasbindaddress"></a>SasBindAddress

這個批註會新增到效果檔案的頂端，以將效果參數與其在 [SasHostParameterValue 集合](#sashostparametervalue-collection)中定義的對應參數產生關聯。 批註的宣告方式如下：


```
string SasBindAddress = "SasHostParameterValue";
```



此範例會將效果世界矩陣系結至 MeshToJointToWorld 矩陣：


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



這個批註會告知主應用程式，它必須使用 MeshToJointToWorld 矩陣中的資料來設定效果世界矩陣的值。

系結位址注釋語法的定義與 [**ID3DXEffect**](id3dxeffect.md) 用來取得和設定效果參數的語法非常類似。 DXSAS 文法和 **ID3DXEffect** 方法之間的唯一差異在於新增星號索引標記。 以下是使用星號索引的另一個範例：


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



星號索引標記表示特定主控制項 envirnmant 值陣列的所有元素，在此案例中 (色彩) 應該在相關聯的參數中系結。 多個星號索引標記可讓效果系結至結構陣列的子項目，而不需要系結整個結構本身。 此範例會將前六個燈的色彩值系結至效果參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX 標準注釋和語義參考](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



