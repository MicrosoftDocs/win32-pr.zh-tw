---
title: 鑲嵌階段
description: Direct3D 11 執行時間支援三個新階段來執行鑲嵌式，這會將低細節的細分圖介面轉換成 GPU 上較高的基本專案。
ms.assetid: 4ad2fd3e-6e1a-4326-8469-3198acf931dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d272ad1db53c6e70a856255c1826f4867f069897b42da0219cd334d48226d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099230"
---
# <a name="tessellation-stages"></a>鑲嵌階段

Direct3D 11 執行時間支援三個新階段來執行鑲嵌式，這會將低細節的細分圖介面轉換成 GPU 上較高的基本專案。 鑲嵌並排顯示高位表面 (或將其分裂) 成為適合轉譯的結構。

藉由在硬體中實作鑲嵌，圖形管線可以評估較低細節的 (較少的多邊形數) 模型並以更高細節呈現。 雖然軟體鑲嵌是可做到的，但硬體實作的鑲嵌會產生不可思議的視覺細節數量 (包括位移對應的支援)，而不需要新增模型大小的視覺細節和造成運作癱瘓的更新頻率。

-   [鑲嵌式優點](#tessellation-benefits)
-   [新管線階段](#new-pipeline-stages)
    -   [輪廓-著色器階段](#hull-shader-stage)
    -   [鑲嵌階段](#tessellator-stage)
    -   [網域著色器階段](#domain-shader-stage)
-   [用於初始化鑲嵌階段的 Api](#apis-for-initializing-tessellation-stages)
-   [作法：](#how-tos)
-   [相關主題](#related-topics)

## <a name="tessellation-benefits"></a>鑲嵌式優點

鑲嵌：

-   節省大量的記憶體和頻寬，讓應用程式能夠從低解析度模型轉譯更高的詳細表面。 在 Direct3D 11 管線中執行的鑲嵌技術也支援置換對應，這可能會產生出色數量的表面詳細資料。
-   支援可擴充轉譯技術，例如可即時計算的連續或視野相依細節層級。
-   以較低頻率執行昂貴的計算 (在較低的詳細模型) 上執行計算，以改善效能。 這可能包括將混合形狀或變形目標 (morph target) 用於寫實動畫的混合計算，或用於撞擊偵測或軟體動力 (soft body dynamics) 的物理計算。

Direct3D 11 管線可在硬體中實行鑲嵌式，以將 CPU 的工作從 CPU 載入至 GPU。 如果應用程式實作大量變形目標和/或更加複雜的皮膚形變 (skinning)/變形模型，這可能會導致非常大的效能改進。 若要存取新的鑲嵌式功能，您必須瞭解一些新的管線階段。

## <a name="new-pipeline-stages"></a>新管線階段

鑲嵌使用 GPU，從四邊形塊面 (quad patch)、三角形塊面 (triangle patch) 或等高線 (isoline) 建構而來的表面計算更詳細的表面。 為了近似高位表面，每個塊面細分成三角形、點或使用鑲嵌因數的線。 Direct3D 11 管線會使用三個新的管線階段來實行鑲嵌：

-   輪廓[-著色器階段](#hull-shader-stage)-一種可程式化的著色器階段，會產生幾何修補程式 (和修補常數，) 對應至每個輸入修補程式 (四、三角形或行) 。
-   [鑲嵌階段](#tessellator-stage) -固定的函式管線階段，可建立代表幾何修補程式之定義域的取樣模式，並產生一組較小的物件， (三角形、點或線) 連接這些範例。
-   [網域著色器階段](#domain-shader-stage) -可程式化的著色器階段，可計算對應至每個網域範例的頂點位置。

下圖強調 Direct3D 11 管線的新階段。

![direct3d 11 管線圖，反白顯示輪廓著色器、曲面細分器和網域著色器階段](images/d3d11-pipeline-stages-tessellation.png)

下圖顯示鑲嵌階段的進展。 從低細節的細分表面開始進展。 進展接下來會使用對應幾何塊面、網域樣本，和連接這些樣本的三角形，反白顯示輸入塊面。 進展最後會反白顯示對應於這些樣本的頂點。

![鑲嵌進展圖](images/tess-prog.png)

### <a name="hull-shader-stage"></a>Hull-Shader 階段

輪廓著色器--每個修補程式都會叫用一次--將定義低序位表面的輸入控制點，轉換成構成修補程式的控制點。 它也會執行一些每個修補程式計算，以提供鑲嵌階段和網域階段的資料。 在最簡單的黑箱層級中，輪廓著色器階段看起來會像下圖。

![輪廓著色器階段圖](images/d3d11-hull-shader.png)

輪廓著色器會使用 HLSL 函式來執行，並具有下列屬性：

-   著色器輸入介於1到32的控制點之間。
-   著色器輸出介於 1 到 32 個控制點之間，無論鑲嵌係數的數目為何。 輪廓著色器的控制點輸出可以由網域著色器階段取用。 網域著色器可以使用修補程式常數資料;鑲嵌因數可由網域著色器和鑲嵌階段取用。
-   鑲嵌係數決定每個塊面要細分成多少數目。
-   著色器會宣告鑲嵌階段所需的狀態。 這些資訊包括控制點數目、塊面的類型，以及鑲嵌時分割使用的類型。 這項資訊會顯示為宣告，通常是在著色器程式碼的前方。
-   如果輪廓著色器階段將任何邊緣鑲嵌因數設定為 = 0 或 NaN，則會挑選修補程式。 如此一來，曲面細分器階段就不一定會執行，網域著色器將不會執行，而該塊面也不會產生任何可見的輸出。

在更深入的層級中，輪廓著色器實際上是以兩個階段操作：一個控制點階段和一個修補程式常數階段，這些階段會由硬體平行執行。 HLSL 編譯器會擷取輪廓著色器中的平行處理原則，並將它編碼成驅動硬體的位元組程式碼。

-   控制點階段會針對每個控制點執行一次，讀取塊面的控制點，以及產生一個輸出控制點 (以 ControlPointID 識別)。
-   塊面常數階段會針對每個塊面執行一次，以產生邊緣鑲嵌係數，和其他每個塊面常數。 在內部，許多塊面常數階段可能同時執行。 塊面常數階段對於所有輸入和輸出控制點有唯讀存取權。

以下是輪廓著色器的範例：


```
[patchsize(12)]
[patchconstantfunc(MyPatchConstantFunc)]
MyOutPoint main(uint Id : SV_ControlPointID,
     InputPatch<MyInPoint, 12> InPts)
{
     MyOutPoint result;
     
     ...
     
     result = TransformControlPoint( InPts[Id] );

     return result;
}
```



如需建立輪廓著色器的範例，請參閱 [如何：建立輪廓著色器](direct3d-11-advanced-stages-hull-shader-create.md)。

### <a name="tessellator-stage"></a>鑲嵌階段

鑲嵌是藉由將輪廓著色器系結至管線來初始化的固定函式階段 (參閱 [如何：初始化鑲嵌階段](direct3d-11-advanced-stages-tessellator-initialize.md)) 。 曲面細分器階段的目的是將網域 (四邊形、三角形或線) 細分成很多較小的物件 (三角形、點或線)。 曲面細分器在標準化 (零到一) 座標系統中並排顯示標準網域。 例如，四邊形網域被鑲嵌為單位正方形。

使用從輪廓著色器階段傳入的鑲嵌因數 (這指定網域被鑲嵌的細微程度) 和分割類型 (指定用於切割塊面的演算法)，曲面細分器每個塊面運作一次。 曲面細分器輸出 uv (和選擇性 w) 座標及表面拓撲至網域著色器階段。

就內部而言，鑲嵌會以兩個階段運作：

-   第一相位處理鑲嵌因數、修正進位問題、處理非常小因數、降低並結合因數，使用 32 位元浮點算術。
-   第二個相位根據所選分割的類型產生點或拓撲清單。 這是曲面細分器階段的核心工作，並使用 16 位元分數搭配固定點算術。 固定點算術允許硬體加速，同時維持可接受的精確度。 例如，假設有 64 公尺寬塊面，這個精確度可以 2 公釐解析度放置點。



| 分割類型 | 範圍                       |
|----------------------|-----------------------------|
| \_奇數小數      | \[1 ... 63\]                  |
| 偶數的分數 \_     | TessFactor 範圍： \[ 2.. 64\] |
| 整數              | TessFactor 範圍： \[ 1.. 64\] |
| pow2                 | TessFactor 範圍： \[ 1.. 64\] |



 

### <a name="domain-shader-stage"></a>Domain-Shader 階段

網域著色器會在輸出修補程式中計算細分點的頂點位置。 每個鑲嵌階段輸出點都會執行一次網域著色器，並具有鑲嵌階段輸出 UV 座標、輪廓著色器輸出修補程式的唯讀存取權，以及輪廓著色器輸出修補程式常數，如下圖所示。

![網域著色器階段圖](images/d3d11-domain-shader.png)

網域著色器的屬性包括：

-   從鑲嵌階段，每個輸出座標都會叫用一次網域著色器。
-   網域著色器會使用來自輪廓著色器階段的輸出控制點。
-   網域著色器會輸出頂點的位置。
-   輸入是輪廓著色器輸出，包括控制點、修補常數資料和鑲嵌式因素。 鑲嵌式因素可以包含固定函式鑲嵌所使用的值，以及在依整數鑲嵌進行四捨五入之前 (的原始值，例如) ，以協助 geomorphing。

在網域著色器完成後，鑲嵌完成，管線資料會繼續至下一個管線階段 (幾何著色器、圖元著色器等) 。 預期相鄰基本類型 (例如每個三角形 6 個頂點) 在鑲嵌為使用中時無效 (這樣會導致未定義的行為，偵錯層將會抱怨此行為)。

以下是網域著色器的範例：


```
void main( out    MyDSOutput result, 
           float2 myInputUV : SV_DomainPoint, 
           MyDSInput DSInputs,
           OutputPatch<MyOutPoint, 12> ControlPts, 
           MyTessFactors tessFactors)
{
     ...

     result.Position = EvaluateSurfaceUV(ControlPoints, myInputUV);
}
```



## <a name="apis-for-initializing-tessellation-stages"></a>用於初始化鑲嵌階段的 Api

鑲嵌會使用兩個新的可程式化著色器階段來執行：輪廓著色器和網域著色器。 這些新的著色器階段是使用著色器模型5中定義的 HLSL 程式碼進行程式設計。 新的著色器目標為： hs \_ 5 \_ 0 和 ds \_ 5 \_ 0。 就像所有的可程式化著色器階段一樣，當著色器使用 [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) 和 [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)等 api 系結至管線時，會從編譯的著色器中將硬體的程式碼解壓縮。 但首先，您必須使用 [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) 和 [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)等 api 來建立著色器。

藉由建立輪廓著色器並將它繫結至輪廓著色器階段 (這會自動設定曲面細分器階段)，來啟用鑲嵌。 若要從鑲嵌塊面產生最終頂點位置，您也需要建立網域著色器並將其繫結至網域著色器階段。 啟用鑲嵌之後，輸入組合語言階段的資料輸入必須是修補資料。 也就是說，輸入組合語言拓撲必須是來自 [**D3D11 \_ 基本 \_ 拓撲**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) 設定 [**IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)的修補程式常數拓撲。

若要停用鑲嵌，將輪廓著色器和網域著色器設定為 **NULL**。 幾何著色器階段和資料流程輸出階段都不能讀取輪廓著色器的輸出控制點或修補資料。

-   輸入組合語言階段的新拓撲，這是此列舉的延伸模組。

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    拓撲會使用 IASetPrimitiveTopology 設定為輸入組合語言階段[ ](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

-   當然，新的可程式化著色器階段需要設定其他狀態，以將常數緩衝區、樣本和著色器資源系結至適當的管線階段。 這些新的 ID3D11Device 方法會實作為設定此狀態。
    -   [**DSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetconstantbuffers)
    -   [**DSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetsamplers)
    -   [**DSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshader)
    -   [**DSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshaderresources)
    -   [**DSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetconstantbuffers)
    -   [**DSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetsamplers)
    -   [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader)
    -   [**DSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshaderresources)
    -   [**HSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetconstantbuffers)
    -   [**HSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshaderresources)
    -   [**HSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetsamplers)
    -   [**HSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshader)
    -   [**HSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetconstantbuffers)
    -   [**HSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetsamplers)
    -   [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)
    -   [**HSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshaderresources)

## <a name="how-tos"></a>作法：

此檔也包含初始化鑲嵌階段的範例。



| 項目                                                                                                                                                                                                                                                                                           | 描述                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[如何：建立輪廓著色器](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                                     | 建立輪廓著色器。<br/>              |
| <span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[如何：設計輪廓著色器](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                                     | 設計輪廓著色器。<br/>              |
| <span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[如何：初始化鑲嵌階段](direct3d-11-advanced-stages-tessellator-initialize.md)<br/> | 初始化鑲嵌階段。<br/> |
| <span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[如何：建立網域著色器](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                                           | 建立網域著色器。<br/>            |
| <span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[如何：設計定義域著色器](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                                           | 建立網域著色器。<br/>            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖形管線](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 

