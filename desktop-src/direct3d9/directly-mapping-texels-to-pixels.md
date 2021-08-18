---
description: 使用預先轉換的頂點轉譯2D 輸出時，必須小心確保每個材質區域都正確對應到單一圖元區域，否則可能會發生材質扭曲。
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: 將材質直接對應至 (Direct3D 9) 的圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7294b88fb8b672aea980dbb23cb4e7c5bbd2bfdbf4d33a5078a09dbfa3084d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988258"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a>將材質直接對應至 (Direct3D 9) 的圖元

使用預先轉換的頂點轉譯2D 輸出時，必須小心確保每個材質區域都正確對應到單一圖元區域，否則可能會發生材質扭曲。 藉由瞭解 Direct3D 在將三角形進行點陣化時遵循的程式基本概念，您可以確保 Direct3D 應用程式正確轉譯2D 輸出。

![6x6 解析度顯示的圖例](images/maptex-fig1.png)

上圖顯示模型化為正方形的圖元。 不過實際上，圖元是點，而不是正方形。 上圖中的每個正方形表示圖元所亮的區域，但是圖元一律只是正方形中央的點。 這項區別雖然很小，但卻很重要。 下圖顯示相同顯示的更好圖例。

![由圖元組成之顯示器的圖例](images/maptex-fig2.png)

上述圖表會將每個實體圖元正確顯示為每個資料格中央的某個點。 螢幕空間座標 (0、0) 是直接位於左上角圖元，因此位於左上角儲存格的中央。 因此，顯示的左上角是在 (-0.5，-0.5) ，因為它是從左上圖元往左和0.5 儲存格的0.5 儲存格。 Direct3D 會以 (0、0) 和 (4，4) 呈現四個角落，如下圖所示。

![ (0、0) 和 (4，4) 之間 unrasterized 四的外框圖例](images/maptex-fig3.png)

上圖顯示數學四與顯示器之間的關聯性，但不會顯示當 Direct3D 將它柵格化並將其傳送至顯示器之後的四種外觀。 事實上，因為四色的邊緣與圖元儲存格之間的界限不一致，所以點陣顯示器無法完全填滿上述的四顆部分。 換句話說，由於每個圖元只能顯示單一色彩，因此每個圖元儲存格只會填入單一色彩;如果顯示的呈現方式與顯示的完全相同，則四個邊緣的圖元儲存格必須顯示兩個不同的色彩：藍色，在四和白色的範圍中，只顯示背景。

相反地，圖形硬體會負責決定應填滿的圖元以接近四顆四。 此程式稱為「點陣化」，在 [ (Direct3D 9) 的點陣化規則 ](rasterization-rules.md)中有詳細說明。 在此特定案例中，下圖顯示的柵格化四項。

![uNtextured 從 (0、0) 到 (4、4所繪製的四個圖例) ](images/maptex-fig4.png)

請注意，傳遞給 Direct3D 的四個邊角有 (0、0) 和 (4、4) ，但在上圖中 (的點陣化輸出) 的角落為 (-0.5、-0.5) 和 (3.5、3.5) 。 比較前面的兩個圖例以呈現差異。 您可以看到顯示實際上呈現的內容是正確的大小，但已在 x 和 y 方向以-0.5 儲存格移位。 但是，除了多重取樣技術，這是最適合四個的近似值。  (請參閱 [消除鋸齒範例](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) ，以徹底涵蓋多個取樣。 ) 請注意，如果轉譯器填滿四個十字格，則產生的區域會是維度 5 x 5，而不是所需的 4 x 4。

如果您假設螢幕座標源自于顯示格線的左上角，而不是左上角的圖元，則會如預期般地出現四顆四。 不過，當四個材質獲得材質時，差異就變得很清楚。 下圖顯示 4 x 4 材質，您將直接對應到四個材質。

![4x4 材質的圖例](images/maptex-fig5.png)

因為材質是 4 x 4 材質，而四個四個圖元的四個圖元，所以您可能會希望有紋理的四種外觀與材質一模一樣 不過，這不是這種情況;即使是位置稍微改變，也會影響材質的顯示方式。 下圖顯示 (0、0) 和 (4）之間的四個，在進行柵格化和紋理之後，會如何顯示 4) 。

![從 (0、0) 和 (4，4) 繪製的材質四個圖](images/maptex-fig6.png)

在上圖中繪製的四個範例顯示有紋理的輸出 (具有線性篩選模式，以及使用重迭的點陣化輪廓) 的夾具定址模式。 本文的其餘部分將說明輸出看起來的樣子，而不是像材質一樣，但是對於需要解決方案的人而言，它是：輸入的邊緣必須在圖元儲存格之間的界限線上。 只要將 x 和 y 四倍座標以-0.5 單位來移動，材質儲存格就能完全涵蓋圖元儲存格，而且可以完全在螢幕上重建四顆四。  (本主題中的最後一個圖例，會以修正的座標顯示四個。 ) 

為什麼點陣化輸出只會對輸入材質造成輕微非常相似的詳細資料，與 Direct3D 定址和範例紋理的方式直接相關。 接下來會假設您已充分瞭解 [材質座標空間](texture-coordinates.md) 和 [雙線性材質篩選](bilinear-texture-filtering.md)。

回頭查看奇怪的圖元輸出，將輸出色彩追蹤回圖元著色器是合理的：圖元著色器是針對每個選取要成為柵格化圖形一部分的圖元來呼叫。 先前圖例中所描述的藍色四顆四色可能會有特別簡單的著色器：


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



針對有紋理的四個四個圖元，必須稍微變更圖元著色器：


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



該程式碼假設 4 x 4 材質儲存在 MyTexture 中。 如圖所示，MySampler 材質取樣器設定為在 MyTexture 上執行雙線性篩選。 圖元著色器會針對每個柵格化圖元呼叫一次，而且每次傳回的色彩是取樣的材質色彩時，vTexCoord。 每次呼叫圖元著色器時，vTexCoord 引數都會設定為該圖元的材質座標。 這表示著色器會在圖元的確切位置要求紋理取樣器，以篩選紋理色彩，如下圖所述。

![紋理座標取樣位置的圖例](images/maptex-fig7.png)

顯示重迭) 的材質 (會直接在圖元位置取樣 (以黑色點) 顯示。 材質座標不受點陣 (的影響，它們會保留在原始四) 的投射螢幕空間中。 黑色點會顯示點陣化圖元的位置。 每個圖元的材質座標都可以藉由將儲存在每個頂點的座標插值來輕鬆地判斷：位於 (0 的圖元，0) 與 (0、0) ; 的頂點相符;因此，該圖元的材質座標只是儲存在該頂點的材質座標，也就是 UV (0.0，0.0) 。 針對 (3，1) 的圖元，插補座標為 UV (0.75，0.25) ，因為該圖元位於材質寬度的三 fourths 和其高度的四分之一。 這些插補座標是傳遞給圖元著色器的結果。

在此範例中，材質不會對齊圖元;每個圖元都 (，因此每個取樣點) 都會放置在四個材質的角落。 由於篩選模式設定為線性，因此取樣器會平均共用該角落四個材質的色彩。 這會說明為什麼圖元必須是紅色的，其實是三 fourths 的灰色，加上第四個紅色，則應為綠色的圖元是一半灰色，加上第四個紅色加上第四個綠色，依此類推。

若要修正這個問題，您只需要將四個四個圖元正確地對應到圖元，就能正確地將材質對應到圖元。 下圖顯示在 (-0.5、-0.5) 和 (3.5 3.5) 之間繪製相同四種的結果，這是一開始的四項設計。

![符合柵格化四顆紋理的四顆紋理圖](images/maptex-fig8.png)

上圖說明從 (-0.5，-0.5) 到 (3.5，3.5) ) 所顯示的四 (完全符合柵格化區域。

## <a name="summary"></a>摘要

總而言之，圖元和材質實際上是點，而非穩固的區塊。 螢幕空間源自左上角圖元，但材質座標源自材質方格的左上角。 最重要的是，當您在轉換的螢幕空間中工作時，請記得從頂點位置的 x 和 y 元件減去0.5 單位，以便正確地對齊材質與圖元。

下列程式碼範例會將256的頂點偏移256正方形，以適當地在轉換的螢幕空間中顯示 256 x 256 紋理。


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質座標](texture-coordinates.md)
</dt> </dl>

 

 



