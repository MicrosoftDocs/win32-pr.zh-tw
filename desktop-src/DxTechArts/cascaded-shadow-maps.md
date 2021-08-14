---
title: 重疊的陰影圖
description: 串聯陰影地圖 (網網的) ，是對抗其中一個最常見的錯誤與遮蔽的角度別名的最佳方式。
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29498dc882133215c910f3bd6caa5966aa0e141aaf4f7a68051834d33f2a3b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649604"
---
# <a name="cascaded-shadow-maps"></a>重疊的陰影圖

串聯陰影地圖 (網網的) 是對抗其中一個最常見錯誤與遮蔽的最佳方式：透視別名。 這份技術檔（假設讀者已經熟悉陰影對應） esposito 著手處理了網的主題。 具體而言，它會：

-   說明網網的複雜性;
-   提供 CSM 演算法可能變異的詳細資料;
-   描述兩個最常見的篩選技術—在篩選 (PCF) ，以及使用差異陰影對應 (VSMs) ，來進行篩選;
-   識別並解決一些與新增篩選至網的常見錯誤相關的問題;和
-   示範如何透過 Direct3D 11 硬體，將網達10網的網到 Direct3D 10。

本文中所使用的程式碼可在 CascadedShadowMaps11 和 VarianceShadows11 範例中的 DirectX 軟體發展工具組 (SDK) 中找到。 本文將在執行技術檔中涵蓋的技術文章、[改善陰影深度地圖的常見技巧，以](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps)充分發揮最大效用。

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a>串聯陰影地圖和透視別名

陰影地圖中的觀點別名是最難克服的問題之一。 在技術檔中，有改善陰影深度地圖的常見技術、描述觀點別名，以及一些可減輕問題的方法。 在實務上，網達業界的解決方案通常是最適合的解決方案，而且通常會在新式遊戲中採用。

網基礎網的基本概念很容易理解。 相機的不同區域必須具有不同解析度的陰影對應。 最接近眼睛的物件所需的解析度，必須比更遠的物件更高。 事實上，當眼睛非常接近幾何時，最接近眼睛的圖元可能需要這麼多的解析度，即使4096×4096陰影地圖也不夠。

網基礎網的基本概念是將分割區分割成多個 frusta。 針對每個 subfrustum 呈現陰影對應;然後，圖元著色器會從對應中最符合所需解析度的地圖取樣 (圖 2) 。

**圖1。陰影對應涵蓋範圍**

![陰影對應涵蓋範圍](images/shadow-map-coverage.png)

在 [圖 1] 中，品質會顯示 (從最高到最低的) 向右。 代表陰影地圖的方格系列，以紅色的 (反轉錐形) 顯示圖元涵蓋範圍如何受到不同解析度陰影對應的影響。 陰影為最高品質 (白色圖元) 當陰影地圖中的材質為亮空間的1:1 比率對應圖元時。 以大型、blocky 材質地圖的形式來呈現外觀別名， (左影像) 當圖元數對應到相同的陰影材質時。 當陰影地圖太大時，就會受到取樣。 在此情況下，系統會略過材質、引進 shimmering 成品，並影響效能。

**[圖 2]CSM 陰影品質**

![csm 陰影品質](images/csm-shadow-quality.png)

[圖 2] 顯示 [圖 1] 中每個陰影地圖中最高品質區段的切口。 具有最接近放置圖元 (在頂點) 的陰影地圖最接近眼睛。 技術上來說，這些都是相同大小的地圖，使用白色和灰階來說明點串聯陰影地圖的成功。 白色很理想，因為它會顯示良好的涵蓋範圍，也就是眼睛空間圖元和陰影對應材質的1:1 比例。

網網的每個畫面都需要執行下列步驟。

1.  將分割區分割成 subfrusta。
2.  計算每個 subfrustum 的正射投射。
3.  轉譯每個 subfrustum 的陰影對應。
4.  呈現場景。

    1.  系結陰影對應和呈現。
    2.  頂點著色器會執行下列動作：

        -   計算每個淺色 subfrustum (的材質座標，除非在圖元著色器中計算所需的材質座標) 。
        -   轉換和燈光頂點等等。

    3.  圖元著色器會執行下列動作：

        -   判斷適當的陰影對應。
        -   視需要轉換材質座標。
        -   範例 cascade。
        -   燈光圖元。

## <a name="partitioning-the-frustum"></a>分割分割區

分割分割區是建立 subfrusta 的動作。 分割分割的一項技術是以 Z 方向計算從零到100% 的間隔。 接著，每個間隔表示接近平面，而最接近平面的平面是以 Z 軸的百分比表示。

**圖3。查看任意分割的 frustums**

![查看任意分割的 frustums](images/view-frustums-partitioned-arbitrarily.png)

在實務上，重新計算每個畫面格的分割分割會導致陰影邊緣 shimmer。 一般接受的作法是在每個案例中使用一組靜態串聯間隔。 在此案例中，沿著 Z 軸的間隔會用來描述分割分割區時所發生的 subfrustum。 判斷指定場景的正確大小間隔取決於數個因素。

### <a name="orientation-of-the-scene-geometry"></a>場景幾何的方向

至於場景幾何，相機方向會影響串聯間隔選取。 例如，像是足球遊戲中的地面鏡頭，它的一組靜態串聯間隔和天空中的攝影機不同。

[圖 4] 顯示一些不同的攝影機和各自的磁碟分割。 當場景的 Z 範圍很大時，需要更多的分割平面。 例如，當眼睛非常接近地面，但仍然可以看到遠的物件時，可能需要多個層級。 分割分割，讓更多分割接近眼睛 (其中的觀點別名會變更最快的) 也很重要。 當大部分的幾何聚集到一個社區段時 (例如，額外負荷視圖或視圖分割的飛行模擬器) ，則需要較少的程式。

**[圖 4]不同的設定需要不同的分割分割**

![不同的設定需要不同的分割分割](images/different-configurations-require-different-frustum-splits.png)

當幾何在 Z 中有很高的動態範圍時 (左) ，需要大量的多個級聯。  (中心) 當幾何在 Z 中有低動態範圍時，多個 frustums 的優點很小。  (右) 當動態範圍為 [中] 時，只需要三個數據分割。

### <a name="orientation-of-the-light-and-the-camera"></a>光線和相機的方向

每一個串聯的投射矩陣都會緊密配合其對應的 subfrustum。 在觀看攝影機和燈光方向為正向的設定中，您可以在重迭的情況下緊密地配合。 重迭會變得更大，因為燈光和鏡頭相機會移至平行對齊 (圖 5) 。 當光線和觀賞攝影機幾乎平行時，它稱為「dueling frusta」，這是大部分遮蔽演算法的很困難案例。 將光源和相機限制為不會發生這種情況並不常見。 但是在此案例中，網網網的執行效能比其他許多演算法更好。

**[圖 5]。串聯重迭會隨著光線方向與相機方向平行變成平行**

![串聯重迭會隨著光線方向與相機方向平行變成平行](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

許多 CSM 的採用都使用固定大小的 frusta。 當分割以固定大小的間隔分割時，圖元著色器可以使用 Z 深度來編制維陣列的索引。

## <a name="calculating-a-view-frustum-bound"></a>計算系結 View-Frustum

一旦選取了間隔間隔之後，就會使用下列兩種的其中一種來建立 subfrusta：適用于場景，並符合 cascade。

### <a name="fit-to-scene"></a>符合場景

所有的 frusta 都可以使用相同的接近平面來建立。 這會強制將串聯重迭。 CascadedShadowMaps11 範例會針對場景呼叫這項技術。

### <a name="fit-to-cascade"></a>符合 Cascade

或者，您可以使用實際的資料分割間隔來建立 frusta，以作為接近和遠的平面。 這會造成更緊密的配合，但會變質為適用于 dueling frusta 的場景。 CascadedShadowMaps11 範例會將這項技術適當地呼叫，以進行串聯。

圖6顯示這兩種方法。 配合串聯可減少解析度。 符合 cascade 的問題是，正向投射會根據視圖的錐的方向來放大和縮小。 「調整成場景」技術會以視圖的大小上限來填補正向投射，以移除在移動攝影機移動時所顯示的構件。 [改善陰影深度的常見技術地圖](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps)可解決在「以材質大小遞增」一節中移動燈光時所顯示的構件。

**[圖 6]。符合場景與縮放比例**

![符合場景或符合 cascade](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a>呈現陰影地圖

CascadedShadowMaps11 範例會將陰影地圖轉譯成一個大型緩衝區。 這是因為材質陣列上的 PCF 是 Direct3D 10.1 功能。 針對每個串聯，會建立一個區域，其中涵蓋對應于該 cascade 的深度緩衝區區段。 因為只需要深度，所以會系結 null 圖元著色器。 最後，會針對每個串聯設定正確的視口和陰影矩陣，因為深度對應會在一次轉譯成主要陰影緩衝區。

## <a name="render-the-scene"></a>呈現場景

包含陰影的緩衝區現在已系結至圖元著色器。 有兩種方法可以選取在 CascadedShadowMaps11 範例中執行的 cascade。 這兩個方法會使用著色器程式碼來說明。

### <a name="interval-based-cascade-selection"></a>Interval-Based Cascade 選取範圍

**[圖 7]。以間隔為基礎的 cascade 選取範圍**

![以間隔為基礎的 cascade 選取範圍](images/interval-based-cascade-selection.jpg)

在以間隔為基礎的選取 ([圖 7]) 中，頂點著色器會計算頂點世界空間中的位置。


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



圖元著色器會接收插補深度。


```C++
fCurrentPixelDepth = Input.vDepth;
```



以間隔為基礎的串聯選取會使用向量比較和點乘積來判斷正確的 cacade。 串聯 \_ 計數旗標會 \_ 指定 CASCADE 的數目。 M \_ fCascadeFrustumsEyeSpaceDepths \_ 資料會限制視圖的分割分割區。 在比較之後，fComparison 會包含值1，其中目前的圖元大於關卡，而當目前的串聯較小時，則為0值。 點乘積會將這些值加總成陣列索引。


```C++
        float4 vCurrentPixelDepth = Input.vDepth;
        float4 fComparison = ( vCurrentPixelDepth > m_fCascadeFrustumsEyeSpaceDepths_data[0]);
        float fIndex = dot(
        float4( CASCADE_COUNT_FLAG > 0,
        CASCADE_COUNT_FLAG > 1,
        CASCADE_COUNT_FLAG > 2,
        CASCADE_COUNT_FLAG > 3)
        , fComparison );

        fIndex = min( fIndex, CASCADE_COUNT_FLAG );
        iCurrentCascadeIndex = (int)fIndex;
```



選取 cascade 之後，材質座標必須轉換成正確的 cascade。


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



接著會使用這個材質座標，利用 X 座標和 Y 座標來取樣紋理。 Z 座標用於進行最後的深度比較。

### <a name="map-based-cascade-selection"></a>Map-Based Cascade 選取範圍

以地圖為基礎的選取範圍 (圖 8) 測試，以進行串聯的四邊，以找出涵蓋特定圖元的嚴謹對應。 頂點著色器會計算每個串聯的視圖空間位置，而不是計算世界空間中的位置。 圖元著色器會反復查看整個層級，以便縮放和移動材質座標，使其索引目前的串聯。 然後，紋理座標會針對材質界限進行測試。 當材質座標的 X 和 Y 值落在 cascade 內時，會用來取樣材質。 Z 座標用於進行最後的深度比較。

**圖8。以地圖為基礎的 cascade 選取範圍**

![以地圖為基礎的 cascade 選取範圍](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a>Interval-Based 選取專案與 Map-Based 選取專案

以間隔為基礎的選取比以地圖為基礎的選擇稍微快一點，因為串聯選取可以直接完成。 以地圖為基礎的選取範圍必須與具有串聯界限的材質座標相交。

當陰影地圖未完全對齊 (請參閱 [圖 8]) ，以地圖為基礎的選項更有效率地使用 cascade。

## <a name="blend-between-cascades"></a>在級聯之間 Blend

本文稍後討論的 VSMs () 和篩選技術（例如 PCF）可以搭配低解析度網用來產生軟陰影。 可惜的是，這會導致在串聯圖層之間看到接合 (圖 9) ，因為解析度不相符。 解決方法是在陰影地圖之間建立陰影測試，以同時針對這兩個級聯的執行陰影測試。 著色器接著會根據 blend 波段中圖元的位置，以線性方式在兩個值之間進行插補。 範例 CascadedShadowMaps11 和 VarianceShadows11 提供 GUI 滑杆，可用來增加和減少這個模糊頻外。 著色器會執行動態分支，因此大部分的圖元都只會從目前的串聯讀取。

**[圖 9]。串聯接縫**

![串聯接縫](images/cascade-seams.jpg)

 (左) 可在重迭的情況下看見可見的接合。  (右) 當串聯混合在一起時，不會發生接合。

## <a name="filtering-shadow-maps"></a>篩選陰影地圖

### <a name="pcf"></a>PCF

篩選一般陰影對應不會產生軟性模糊的陰影。 篩選硬體會模糊深度值，然後將這些模糊的值與 [光線空間] 材質進行比較。 通過/失敗測試所產生的硬性邊緣仍然存在。 模糊陰影對應只是為了錯誤地移動固定邊緣。 PCF 可篩選陰影對應。 PCF 的一般概念是根據 subsamples 總數通過深度測試的 subsamples 數目，來計算陰影中圖元的百分比。

Direct3D 10 和 Direct3D 11 硬體可以執行 PCF。 PCF 取樣器的輸入是由材質座標和比較深度值所組成。 為了簡單起見，PCF 會以四分點的篩選來說明。 紋理取樣器會讀取紋理四次，類似于標準篩選。 不過，傳回的結果是通過深度測試的圖元百分比。 [圖 10] 顯示在四個深度測試中通過的圖元如何以陰影顯示25%。 實際傳回的值是以材質讀取的 subtexel 座標為基礎的線性插補，以產生平滑漸層。 如果沒有這個線性插補，四點點的 PCF 只能傳回五個值： {0.0、0.25、0.5、0.75、1.0}。

**[圖 10]PCF 篩選影像，涵蓋所選圖元的25%**

![pcf 篩選影像，涵蓋所選圖元的25%](images/pcf-filtered-image.png)

您也可以在沒有硬體支援的情況下進行 PCF，或將 PCF 延伸至較大的核心。 有些技術甚至是具有加權核心的範例。 若要這樣做，請建立一個核心 (，例如 N × N 方格的高斯) 。 權數必須新增至1。 然後紋理會取樣 N2 次。 每個範例都會依核心中的對應權數進行調整。 CascadedShadowMaps11 範例會使用這個方法。

### <a name="depth-bias"></a>深度偏差

使用大型 PCF 核心時，深度偏差會變得更重要。 它只有在比較圖元的亮空間深度與它在深度對應中所對應的圖元時才有效。 深度對應材質的相鄰位置參考不同的位置。 此深度很可能很類似，但可能會因場景而有所不同。 [圖 11] 反白顯示發生的構件。 單一深度會與陰影地圖中的三個相鄰材質比較。 其中一個深度測試失敗，因為它的深度與目前幾何的計算出的光線空間深度沒有關聯。 此問題的建議解決方案是使用較大的位移。 但位移過大，可能會導致 Peter 移動。 計算緊密接近的平面和目前的平面有助於降低使用位移的效果。

**[圖 11]錯誤的自我遮蔽**

![錯誤的自我遮蔽](images/erroneous-self-shadowing.png)

錯誤的自我遮蔽結果，是因為比較光線空間深度的圖元與陰影地圖中未相互關聯的材質。 輕量空間的深度會與深度對應中的陰影材質2相關聯。 材質1大於光空間深度，而2等於，3則較少。 材質2和3通過深度測試，而材質1失敗。

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a>使用針對大型 PCFs 的 DDX 和 DDY 來計算 Per-Texel 深度偏差

使用 **ddx** 來計算每個材質深度偏差和大型 PCFs 的 **ddy** ，是針對相鄰陰影對應材質計算正確深度偏差（假設表面為平面）的技術。

這項技術使用衍生資訊來配合平面的比較深度。 由於這項技術的運算複雜度很複雜，因此只有在 GPU 有計算迴圈可供使用時，才應該使用此技術。 使用非常大型的核心時，這可能是唯一能移除自行遮蔽成品，而不會造成 Peter 移動的技巧。

[圖 12] 強調問題。 針對正在比較的一個材質，已知空間的深度是已知的。 對應至深度對應中相鄰材質的光線空間深度未知。

**[圖 12]場景和深度對應**

![場景和深度對應](images/scene-and-depth-map.png)

轉譯的場景會顯示在左側，而具有範例材質區塊的深度對應會顯示在右側。 眼睛空間材質會對應至區塊中央中標示為 D 的圖元。 這項比較是正確的。 眼睛空間的正確深度，與鄰近 D 未知的圖元相關聯。 只有當我們假設圖元與 D 的相同三角形時，才可以將連續的材質對應回眼睛空間。

材質的深度已知可與光線空間位置相互關聯。 深度對應中的鄰近材質深度未知。

概括而言，這項技術會使用 **ddx** 和 **ddy** HLSL 作業來尋找亮空間位置的衍生。 這是重要的，因為衍生作業會傳回相對於螢幕空間的光線空間深度漸層。 若要將此轉換為與光線空間相關的光線空間深度漸層，則必須計算轉換矩陣。

### <a name="explanation-with-shader-code"></a>著色器程式碼的說明

演算法其餘部分的詳細資料會提供給執行這項作業的著色器程式碼的說明。 您可以在 CascadedShadowMaps11 範例中找到此程式碼。 [圖 13] 顯示輕量材質座標如何對應至深度對應，以及如何使用 X 和 Y 中的衍生來建立轉換矩陣。

**[圖 13]畫面-空間至淺色矩陣**

![畫面-空間至淺色矩陣](images/screen-space-to-light-space-matrix.png)

X 和 Y 中的輕量位置的衍生項會用來建立此矩陣。

第一個步驟是計算淺色視圖空間位置的衍生。


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



Direct3D 11 類別 Gpu 會以平行方式執行2×2四個圖元的方式來計算這些衍生，並從 X **中的相鄰** 節點減去 **ddy** 的鄰近區的材質座標。 這兩個衍生項組成了2×2矩陣的資料列。 在其目前的表單中，這個矩陣可用來將螢幕空間連續的圖元轉換成輕量傾斜。 不過，需要這個矩陣的反向。 需要將亮空間相鄰圖元轉換成螢幕空間傾斜的矩陣。


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



**圖14。輕量到螢幕空間**

![輕量到螢幕空間](images/light-space-to-screen-space.png)

然後，這個矩陣會用來將上述兩個材質轉換成目前材質的右邊和右邊。 這些鄰近專案會表示為與目前材質的位移。


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



矩陣所建立的比率最後乘以深度衍生，以計算相鄰圖元的深度位移。


```C++
            float fUpTexelDepthDelta =
            vUpTexelDepthRatio.x * vShadowTexDDX.z
            + vUpTexelDepthRatio.y * vShadowTexDDY.z;
            float fRightTexelDepthDelta =
            vRightTexelDepthRatio.x * vShadowTexDDX.z
            + vRightTexelDepthRatio.y * vShadowTexDDY.z;
```



這些權數現在可用於 PCF 迴圈，以將位移新增至位置。


```C++
    for( int x = m_iPCFBlurForLoopStart; x < m_iPCFBlurForLoopEnd; ++x ) 
    {
        for( int y = m_iPCFBlurForLoopStart; y < m_iPCFBlurForLoopEnd; ++y )
            {
            if ( USE_DERIVATIVES_FOR_DEPTH_OFFSET_FLAG )
            {
            depthcompare += fRightTexelDepthDelta * ( (float) x ) +
            fUpTexelDepthDelta * ( (float) y );
            }
            // Compare the transformed pixel depth to the depth read
            // from the map.
            fPercentLit += g_txShadow.SampleCmpLevelZero( g_samShadow,
            float2(
            vShadowTexCoord.x + ( ( (float) x ) * m_fNativeTexelSizeInX ) ,
            vShadowTexCoord.y + ( ( (float) y ) * m_fTexelSize )
            ),
            depthcompare
            );
            }
     }
```



## <a name="pcf-and-csms"></a>PCF 和網達網

PCF 無法在 Direct3D 10 中的材質陣列上運作。 若要使用 PCF，所有的級聯都會儲存在一個大型材質塔中。

### <a name="derivative-based-offset"></a>Derivative-Based 位移

新增網網的衍生式位移會帶來一些挑戰。 這是因為分歧的流程式控制制內的衍生計算所致。 此問題的發生原因是 Gpu 運作的基本方式。 Direct3D11 Gpu 在2×2四邊形的圖元上運作。 為了執行衍生，Gpu 通常會從該相同變數的相鄰圖元複本減去目前圖元的變數複本。 這種情況的發生方式會因 GPU 而異。 材質座標取決於以地圖為基礎或以間隔為基礎的 cascade 選取。 圖元中的某些圖元會選擇不同于圖元其餘部分的 cascade。 這會導致陰影地圖之間出現接縫，因為衍生的位移現在是完全錯誤的。 解決方法是在亮色空間材質座標上執行衍生。 這些座標組每個串聯都是相同的。

### <a name="padding-for-pcf-kernels"></a>PCF 核心的填補

如果未填補陰影緩衝區，則為串聯分割區以外的 PCF 核心索引。 解決方法是以 PCF 核心的一半大小來填補 cascade 的外緣。 這必須在著色器中執行，以選取要在投影矩陣中選取串聯和，且必須將框線轉譯得夠大，才能保留框線。

## <a name="variance-shadow-maps"></a>差異陰影地圖

VSMs (如需詳細資訊，請參閱 Donnelly 和 Lauritzen 的變異數 [陰影](https://portal.acm.org/citation.cfm?doid=1111411.1111440) 對應，) 啟用直接陰影對應篩選。 使用 VSMs 時，可以使用材質篩選硬體的所有功能。 三線性和各向異性 ([圖 15]) 篩選都可以使用。 此外，VSMs 也可以直接透過卷積來模糊。 VSMs 的確有一些缺點;您必須將兩個深度資料通道儲存 (深度和深度平方) 。 當陰影重迭時，輕不規則很常見。 不過，它們的運作方式很低，而且可以與網達網的結合。

**[圖 15]各向異性篩選**

![各向異性篩選](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a>演算法詳細資料

將深度和深度平方轉譯成雙聲道陰影地圖，以 VSMs 工作。 然後，這兩個通道的陰影地圖可以模糊並篩選，就像一般材質一樣。 然後，演算法會在圖元著色器中使用 Chebychev 的不相等，來估計會通過深度測試的圖元區域分數。

圖元著色器會提取深度和深度平方值。


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



會執行深度比較。


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



如果深度比較失敗，則會預估光線的圖元百分比。 變異數是以平均平方減去平均平方來計算。


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



FPercentLit 值是 Chebychev 不相等的估計值。


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a>光線不規則

VSMs 的最大缺點是淺不規則 (圖 16) 。 當多個陰影輪子彼此遮蔽時，就會發生輕微的不規則情形。 VSMs 會根據深度 disparities 來為陰影邊緣加上陰影。 當遮蔽互相重迭時，區域中間的深度差異會存在於應遮蔽的區域中。 這是使用 VSM 演算法的問題。

**[圖 16]VSM 光線不規則**

![vsm 光線不規則](images/vsm-light-bleeding.png)

問題的部分解決方法是將 fPercentLit 提升至電源。 這有抑制模糊的效果，這可能會導致深度差異很小的構件。 有時候會有可緩和問題的神奇值。


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



提高乘冪百分比的替代方式是避免陰影重迭的設定。 甚至高度調整的陰影設定在燈光、攝影機和幾何上有數個限制。 使用較高解析度紋理也可減少輕量。

分層變異數陰影對應 (LVSMs) 解決此問題，代價是將分割分解為與光線垂直的圖層。 當您也使用了網達者時，所需的地圖數量會相當大。

此外，Andrew Lauritzen 是 VSMs 的白皮書共同作者，以及 LVSMs 的作者，討論了如何將指數陰影地圖 (ESMs) 與 VSMs 結合，以在 [Beyond3D 論壇](https://forum.beyond3d.com/showthread.php?t=47427)中抵禦淺的混合。

## <a name="vsms-with-csms"></a>使用網 VSMs

範例 VarianceShadow11 結合了 VSMs 和網。 組合相當簡單。 此範例會遵循與 CascadedShadowMaps11 範例相同的步驟。 因為未使用 PCF，所以陰影在兩個可分隔的可分離的卷積中會模糊。 若未使用 PCF，也會讓範例使用材質陣列，而不是使用材質塔。 材質陣列上的 PCF 是 Direct3D 10.1 功能。

### <a name="gradients-with-csms"></a>使用網網的漸層

使用具有網的漸層時，可以在兩個層級的框線之間產生接合，如圖17所示。 範例指令會使用圖元之間的衍生，來計算篩選所需的資訊，例如 mipmap 層級。 這會造成 mipmap 選擇或非特殊篩選的特殊問題。 當四個四個圖元在著色器中採用不同的分支時，GPU 硬體所計算的衍生衍生項就會無效。 這會導致沿著陰影地圖的不規則接合。

**[圖 17]由於具有分歧流程式控制制的非等向篩選，因此出現串聯框線的接縫**

![由於具有分歧流程式控制制的非等向篩選，因此出現串聯框線的接縫](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

此問題的解決方式是在亮視野空間中的位置計算衍生的衍生項;輕量空間座標不是選取的串聯所特有。 計算的衍生範圍可依投射紋理矩陣的縮放部分，調整為正確的 mipmap 層級。


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a>VSMs 相較于具有 PCF 的標準陰影

VSMs 和 PCF 都會嘗試接近將通過深度測試的圖元區域分數。 VSMs 使用篩選硬體，並可利用可分隔的核心加以模糊處理。 可分離的卷積核心比完整核心更便宜。 此外，VSMs 會比較一個光線空間深度與輕量空間深度對應中的一個值。 這表示 VSMs 與 PCF 沒有相同的位移問題。 技術上來說，VSMs 是較大區域的取樣深度，以及執行統計分析。 這比 PCF 更精確。 在實務上，VSMs 會進行一項非常好的混合作業，這會導致需要的位移較少。 如上所述，VSMs 的一種缺點是輕量。

VSMs 和 PCF 代表 GPU 計算能力和 GPU 材質頻寬之間的取捨。 VSMs 需要執行更多數學運算來計算變異數。 PCF 需要更多紋理記憶體頻寬。 大型 PCF 核心可能會因為材質頻寬很快就會變成瓶頸。 隨著 gpu 計算能力的成長速度比 GPU 頻寬更快，VSMs 會變得更實際的這兩種演算法。 由於混合和篩選，VSMs 也能以較低解析度的陰影地圖呈現更好的效果。

## <a name="summary"></a>摘要

網網的解決方案提供了觀點別名問題的解決方案。 有幾個可能的設定可取得標題的需要視覺精確度。 PCF 和 VSMs 廣泛使用，且應與網合併以減少別名。

## <a name="references"></a>參考資料

Donnelly、W. 和 Lauritzen，A. 變異數 [陰影對應](https://portal.acm.org/citation.cfm?doid=1111411.1111440)。 在 SI3D ' 06：互動式3D 圖形和遊戲的 2006 symposium 的訴訟。 2006。 pp. 161-165。 美國紐約州紐約市：執行長按。

Lauritzen、Andrew 和 McCool、Michael。 [分層變異數陰影對應](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992)。 圖形介面2008、5月28日、30、2008、Windsor、安大略省、加拿大的訴訟。

Engel，Woflgang f. 第4節。 串聯陰影地圖。 ShaderX5，Advanced 轉譯技巧，Wolfgang Engel，Ed。 麻塞諸塞州波士頓 Charles 河媒體。 2006。 pp. 197 –206。

 

 