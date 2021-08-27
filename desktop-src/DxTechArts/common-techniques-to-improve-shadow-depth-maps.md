---
title: 改善陰影深度圖的常見技術
description: 本技術檔概述一些常見的陰影深度對應演算法和常見的成品，並說明數種技術（範圍從基本到中級的困難），可用來提高標準陰影對應的品質。
ms.assetid: bf994838-a261-0379-9301-eb9b250d216c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafff1b537830ae0ee681ed32932cca2b6274a4d9da3e0471ef498e0bef2d483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102468"
---
# <a name="common-techniques-to-improve-shadow-depth-maps"></a>改善陰影深度圖的常見技術

陰影對應是在1978中第一次引進的，是將陰影新增至遊戲的常見技術。 過去三年來，儘管硬體和軟體的進展，遮蔽成品（也就是 shimmering 邊緣、觀點別名和其他精確問題）仍會持續。

本技術檔概述一些常見的陰影深度對應演算法和常見的成品，並說明數種技術（範圍從基本到中級的困難），可用來提高標準陰影對應的品質。 將基本陰影對應新增至標題通常很簡單，但瞭解陰影成品的細微程度可能很困難。 這項技術檔是針對已實行遮蔽的中繼圖形開發人員所撰寫，但不完全瞭解特定構件的出現原因，並不確定如何解決這些問題。

選取正確的技巧來緩和特定的成品，是重要。 當您解決陰影對應的缺點時，品質的差異可能相當令人印象深刻 (圖 1) 。 正確實施這些技術可大幅改善標準陰影。 本文中所述的技術是在 DirectX SDK 的範例 CascadedShadowMaps11 中執行。

**圖1。具有重大成品的陰影 (在執行本文中所述的技巧之後，將) 和陰影 (正確)**

![具有重大成品的陰影 (在執行本文中所述的技巧之後，將) 和陰影 (正確) ](images/shadows-before-and-after.jpg)

## <a name="shadow-depth-maps-review"></a>地圖評論的陰影深度

陰影深度對應演算法是雙通路演算法。 第一個階段會在光線空間中產生深度對應。 在第二個階段中，這個對應會用來比較光線空間中的每個圖元深度與光源間距深度地圖中的對應深度。

**[圖 2]陰影場景的主要部分**

![陰影場景的主要部分](images/key-parts-of-shadow-scene.jpg)

### <a name="pass-1"></a>Pass 1

場景如 [圖 2] 所示。 在第一次通過 ([圖 3]) 中，幾何會轉譯成從光線的觀點來看的深度緩衝區。 更具體來說，頂點著色器會將幾何轉換成淺色間距。

第一個階段的最終結果是深度緩衝區，其中包含來自光線觀點的場景深度資訊。 現在可用於傳遞2，以判斷哪些圖元從燈光 pixels occluded。

**圖3。基本陰影對應的第一次傳遞**

![基本陰影對應的第一次傳遞](images/first-pass-of-basic-hadow-mapping.png)

### <a name="pass-2"></a>Pass 2

在第二次通過 ([圖 4]) 中，頂點著色器會將每個頂點轉換兩次。 每個頂點都會轉換成相機的視圖空間，並傳遞至圖元著色器作為位置。 光線的視圖投射紋理矩陣也會轉換每個頂點，並以紋理座標的形式傳遞至圖元著色器。 視圖投射紋理矩陣是用來在傳遞1中使用一個額外轉換來呈現場景的相同矩陣。 它是一種轉換，它會從 view space ( –1到1（X 和 Y) ）轉換成1，並將 y) 中的材質空間 (0 到1，也就是 Y 中的1到0。

圖元著色器會接收插補位置和插補材質座標。 執行深度測試所需的所有專案現在都在此材質座標中。 您現在可以使用 X 和 Y 材質座標，從第一次行程中編制深度緩衝區的索引，並比較所產生的深度值與 Z 紋理座標，來執行深度測試。

**[圖 4]基本陰影對應的第二次傳遞**

![基本陰影對應的第二次傳遞](images/second-pass-of-basic-shadow-mapping.png)

## <a name="shadow-map-artifacts"></a>陰影地圖 Artifacts

陰影深度對應演算法是最廣泛使用的即時遮蔽演算法，但仍會產生數個需要緩和的構件。 接下來會摘要說明可能發生的構件類型。

### <a name="perspective-aliasing"></a>觀點別名

[圖 5] 顯示了一般構件的觀點別名。 當陰影地圖中要材質的圖元間距不是一對一比例時，就會發生此情況。 這是因為接近接近平面的圖元會緊密合在一起，而且需要較高的陰影地圖解析度。

[圖 6] 顯示陰影地圖和視圖的截錐。 接近眼睛，圖元會緊密在一起，而許多圖元會對應到相同的陰影材質。 遠平面的圖元會散佈出來，藉此減少透視圖的別名。

**[圖 5]。高度觀點的別名 (左) 與低觀點的別名 (右)**

![高度觀點的別名 (左) 與低觀點的別名 (右) ](images/high-perspective-aliasing-vs-low-perspective-aliasing.jpg)

若為左邊的影像，則會有較高的透視圖別名;太多的眼睛空間圖元都對應到相同的陰影對應材質。 在右邊的影像中，因為眼睛空間圖元與陰影地圖材質之間有1:1 的對應，所以透視失真鋸齒很低。

**[圖 6]。使用陰影對應來查看截錐**

![使用陰影對應來查看截錐](images/view-frustum-with-shadow-map.jpg)

最深的平面中的淺色圖元代表低度的別名，而接近平面的深圖元則代表高度透視圖的別名。

陰影地圖解析度也可能太高。 雖然較高的解析度較不明顯，但它可能會導致小型物件（例如電話線路），而不會轉換陰影。 此外，解析度過高可能會導致嚴重的效能問題，因為材質存取模式。

透視圖陰影地圖 (PSMs) 和淺色空間透視圖陰影地圖 (LSPSMs) 嘗試透過扭曲光源的投射矩陣來處理透視別名，以將更多材質置於接近需求的地方。 可惜的是，這兩種技術都無法解決觀點的別名。 將眼睛間距圖元對應到陰影地圖中材質所需的轉換參數化，無法由線性誤差來系結。 需要對數參數化。 PSMs 會將太多詳細資料放在眼睛附近，導致遠處陰影的品質低或甚至消失。 LSPSMs 可讓您更妥善地找出不斷增加解析度的中間，並留下足夠的物件詳細資料。 這兩種技術都是在某些場景設定中退化為正向陰影。 您可以針對視圖的每個臉部呈現不同的陰影地圖來 counteracted 這個 degeneration，不過這很昂貴。 對數透視圖 (LogPSMs) 也會針對視圖的每個臉部呈現不同的地圖。 這項技術使用非線性柵格化來放置更多材質。 D3D10 和 D3D11 類別的硬體不支援非線性柵格化。 如需這些技術和演算法的詳細資訊，請參閱參考一節。

串聯陰影地圖 (網，) 是處理觀點別名的最受歡迎技術。 雖然網 PSMs 與 LSPSMs 可以合併，但這是不必要的。 協助工具文章、[串聯陰影地圖](/windows/desktop/DxTechArts/cascaded-shadow-maps)中，使用網達器修正透視圖的問題。

### <a name="projective-aliasing"></a>Projective 別名

Projective 別名比透視圖別名更難顯示。 [圖 7] 中反白顯示的 distended 陰影會示範 projective 混淆錯誤。 當相機空間中材質之間的對應 Projective 小於1的比率時，就會發生別名;這是因為幾何的方向與燈光鏡頭有關。 當幾何的正切平面變成平行至光線時，就會發生 Projective 的別名。

**[圖 7]。高 projective 的別名與低 projective 別名**

![高 projective 的別名與低 projective 別名](images/high-projective-aliasing-vs-low%20projective-aliasing.jpg)

用來減輕觀點混淆錯誤的技巧也會降低 projective 的別名。 Projective 別名會在表面法線與光線垂直時發生;這些表面應該會以擴散光源方能以較少的光線為依據。

### <a name="shadow-acne-and-erroneous-self-shadowing"></a>陰影 Acne 和錯誤 Self-Shadowing

陰影 acne (圖 8) （與錯誤自我遮蔽同義的詞彙）會在陰影對應 quantizes 整個材質的深度時發生。 當著色器將實際深度與此值進行比較時，可能會因為未遮蔽而自行遮蔽。

陰影 acne 的另一個原因是，亮空間中的材質會接近深度對應中對應材質的深度，精確度錯誤會導致深度測試錯誤地發生錯誤。 此精確度差異的其中一個原因是，深度對應是由固定函式的點陣化硬體所計算，而比較深度則是由著色器所計算。 Projective 別名也會導致影子 acne。

**圖8。陰影 acne 成品**

![陰影 acne 成品](images/shadow-acne-artifact.jpg)

如左側影像所示，部分圖元無法通過深度測試，並建立了 speckled 成品和波紋模式。 為了減少錯誤的自我遮蔽，接近平面的界限和淺色空間視圖的最大平面應該盡可能地以最緊密的方式計算。 以斜率調整為基礎的深度偏差和其他類型的偏差，都是用來減緩陰影 acne 的其他解決方案。

### <a name="peter-panning"></a>Peter 移動

*Peter 移動* 字是從子女的書籍字元（其陰影變成卸離，以及誰可以飛出）來衍生其名稱。 此成品會讓具有遺失陰影的物件中斷連結，並將其浮在表面上方（ ([圖 9]) ）。

**[圖 9]。Peter 移動構件**

![peter 移動構件](images/peter-panning-artifact.jpg)

在左邊的影像中，陰影會從物件卸離，並建立浮動效果。

移除 surface acne 的其中一項技術是將某個值加入至亮空間的圖元位置;這稱為新增深度位移。 當使用的深度位移太大時，Peter 移動結果。 在此情況下，深度位移會導致深度測試錯誤地傳遞。 如同陰影 acne，當深度緩衝區中的有效位數沒有足夠時，Peter 移動就會而不耐煩。 計算緊密接近的平面和目前的平面，也有助於避免 Peter 的移動。

## <a name="techniques-to-improve-shadow-maps"></a>改進影子地圖的技巧

將遮蔽新增至標題是一種處理常式。 第一個步驟是讓基本的影子地圖運作。 第二個是確保所有基本計算都能以最佳方式執行： frusta 盡可能緊密地調整、接近/遠的平面緊密地調整、使用斜率調整偏差等。 當基本的陰影已啟用，而且看起來越好，開發人員就可以更清楚地瞭解需要哪些演算法才能讓陰影獲得足夠的精確度。 本節會提供基本的提示，讓基本的影子地圖能以最理想的方式查看。

### <a name="slope-scale-depth-bias"></a>Slope-Scale 深度偏差

如先前所述，自我遮蔽可能會導致陰影 acne。 新增過多偏差可能會導致 Peter 移動。 此外，具有陡 (的多邊形，相較于光線) ，相較于淺色傾斜 (的多邊形，相較于燈光) ，會有更多 projective 的別名。 因此，每個深度對應值可能需要不同的位移，視多邊形的斜率相對於光線而定。

Direct3D 10 硬體可以根據視圖方向來偏差多邊形的斜率。 這項功能的作用是將大型偏差套用至多邊形，以向下邊緣觀看，但不會直接將任何偏差套用至面向光線的多邊形。 [圖 10] 說明在針對相同非偏誤斜率進行測試時，陰影和未遮蔽之間有兩個連續的圖元可以交替。

**[圖 10]斜率縮放深度-相較于非偏誤深度的偏差**

![斜率縮放深度-相較于非偏誤深度的偏差](images/slope-scaled-depth-bias-compared-to-unbiased-depth.png)

### <a name="calculating-a-tight-projection"></a>計算緊密投射

將光源的投射緊密地調整成視圖的範圍，會增加陰影地圖的涵蓋範圍。 [圖 11] 說明使用任意投射或調整投射到場景界限，會產生更高的透視圖別名。

**[圖 11]任意陰影的縮排和陰影截紙可符合場景**

![任意陰影的縮排和陰影截紙可符合場景](images/arbitrary-shadow-frustum-and-shadow-frustum-fit-to-scene.jpg)

視圖是從光線的觀點來看。 梯形表示觀看攝影機的錐截。 在影像上繪製的方格代表陰影地圖。 右邊的影像會顯示相同的解析度陰影地圖在更緊密地配合場景時，會建立更材質的涵蓋範圍。

[圖 12] 說明適當的 frustums。 若要計算投影，構成視圖的分割區的八個點會轉換成輕量。 接下來，會找到 X 和 Y 中的最小值和最大值。 這些值組成正向投射的範圍。

**[圖 12]陰影投射符合視圖的截縮圖**

![陰影投射符合視圖的截縮圖](images/shadow-projection-fit-to-view-frustum.jpg)

您也可以將錐裁剪成場景 AABB，以取得更緊密的系結。 在所有情況下都不建議這麼做，因為這可能會將燈泡投影的大小從框架變更為框架。 許多技術（例如，將燈光 Texel-Sized 遞增一節中所述的技巧）在每個畫面格的光線投射大小都保持不變時，會提供更好的結果。

### <a name="calculating-the-near-plane-and-far-plane"></a>計算接近平面和遠平面

接近平面和目前的平面是計算投影矩陣所需的最後一個片段。 平面越緊密，深度緩衝區中的值愈精確。

深度緩衝區可以是16位、24位或32位，其值介於0和1之間。 一般而言，深度緩衝區是固定的點，而接近接近平面的值會比接近最接近平面的值更緊密地分組在一起。 深度緩衝區可用的精確度程度，取決於接近平面到最遠平面的比率。 使用嚴謹可能的近乎/far 平面可能會允許使用16位的深度緩衝區。 16位深度緩衝區可以減少記憶體的使用，同時提高處理速度。

### <a name="aabb-based-near-plane-and-far-plane"></a>AABB-Based 近平面和目前的平面

計算接近平面和目前平面的簡單簡單方式，就是將場景的周框磁片區轉換成輕量空間。 最小的 Z 座標值是近平面，最大的 Z 座標值是最大的平面。 針對場景和燈光的許多設定，此方法就已足夠。 但是最糟的情況可能會導致深度緩衝區的精確度大幅遺失;[圖 13] 顯示這類案例。 在這裡，最遠的平面範圍會比所需的四倍長。

[圖 13] 中的 [視圖] 會刻意選擇較小。 小型視圖的截量圖會顯示在非常大的場景中，其中包含從 view 相機擴充的支柱。 對近和遠的平面使用場景 AABB 不是最佳的。 在[串聯陰影地圖](/windows/desktop/DxTechArts/cascaded-shadow-maps)技術檔中所述的 CSM 演算法，必須針對非常小的 frustums，計算接近或遠的平面。

**[圖 13]根據場景 AABB 的近和遠平面**

![根據場景 aabb 的近和遠平面](images/near-far-%20planes-based-on-scene-aabb.jpg)

### <a name="frustum-based-near-plane-and-far-plane"></a>Frustum-Based 近平面和目前的平面

計算近和遠平面的另一項技巧，就是將分割區轉換成輕量，並使用 Z 的最小值和最大值，分別是接近和遠的平面。 [圖 14] 說明這兩種方法的問題。 首先，計算太保守，如同當錐延伸超過場景的幾何時所示。 其次，接近的平面可能太過嚴格，因此會裁剪陰影輪子。

**圖14。接近或遠的平面只以視圖的截錐為基礎**

![接近或遠的平面只以視圖的截錐為基礎](images/near-far-planes-based-solely-on-view-frustum.jpg)

### <a name="light-frustum-intersected-with-scene-to-calculate-near-and-far-planes"></a>淺截量與場景相交，以計算近和遠的平面

[圖 15] 顯示計算近和遠的平面的適當方式。 正向淺截量的四個平面是使用視圖的 X 和 Y 座標的最小值和最大值來計算。 正向視圖的最後兩個平面是近和遠的平面。 若要尋找這些平面，場景的範圍會針對四個已知的輕量截量平面裁剪。 新裁剪界限的最小和最大 Z 值分別代表近平面和遠平面。

執行這項作業的程式碼位於 CascadedShadowMaps11 範例中。 組成世界 AABB 的八個點會轉換成輕量空間。 將點轉換成光線空間可簡化裁剪測試。 淺截量的四個已知平面現在可以線條表示。 輕量空間中的場景周框磁片區可以表示為六個 quadrilaterals。 然後，您可以將這些6個 quadrilaterals 轉換成12個三角形，以進行以三角形為基礎的裁剪。 三角形會根據視圖的已知平面來裁剪， (這些是在亮空間) 的 X 和 Y 中的水準和垂直線條。 在 X 和 Y 中找到交集點時，會在該點裁剪3D 三角形。 所有裁剪三角形的最小和最大 Z 值都是接近平面和目前的平面。 CascadedShadowMaps11 範例會示範如何在 **ComputeNearAndFar** 函式中執行這項剪輯。

有兩個以上的技巧可用來計算嚴謹可能接近和遠的平面。 這些技術並不會顯示在 CascadedShadowMaps 範例中。

-   您可以透過將場景的階層或場景中的個別物件與淺截量隔開，來計算更緊密的平面。 這會是更複雜的計算。 雖然 CascadedShadowMaps11 範例中未說明，但這可能是某些圖格的有效技術。
-   最少可以計算最小的平面：

    -   視圖的最大深度會在淺色空間中被截量。
    -   視圖的錐交叉和場景 AABB 交集的最大深度。

這種方法在搭配使用串聯陰影地圖使用時可能會造成問題，您可以在 view （view）的外部建立索引。 在此情況下，陰影對應可能遺失幾何。

**[圖 15]根據燈光的四個計算平面和場景之周框幾何交集的最接近平面**

![根據燈光的四個計算平面和場景之周框幾何交集的最接近平面](images/near-far-plane-based-on-intersection-of-four.jpg)

### <a name="moving-the-light-in-texel-sized-increments"></a>以 Texel-Sized 增量移動燈光

陰影地圖中的常見成品是 shimmering edge 效果。 隨著攝影機的移動，陰影邊緣的圖元會變亮和變暗。 這種情況不會出現在靜止的影像中，但會很明顯，並且會即時分散。 [圖 16] 強調這個問題，[圖 17] 顯示陰影邊緣的外觀。

發生 shimmering edge 錯誤的原因是，每次相機移動時都會重新計算燈光投射矩陣。 這會在產生的陰影對應中產生微小的差異。 下列所有因素都可能影響為了系結場景所建立的矩陣。

-   視圖截量的大小
-   視圖截量的方向
-   光線的位置
-   攝影機的位置

每次此矩陣變更時，陰影邊緣都可能會變更。

**[圖 16]Shimmering 陰影邊緣**

![shimmering 陰影邊緣](images/shimmering-shadow-edges.jpg)

當相機從左至右移動時，陰影框線的圖元就會跟著遮蔽。

**[圖 17]不含 shimmering 邊緣的陰影**

![不含 shimmering 邊緣的陰影](images/shadows-without-shimmering-edges.jpg)

當相機從左至右移動時，陰影邊緣會保持不變。

針對方向光源，此問題的解決方法是將 X 和 Y (中的最小值/最大值舍入，以使正向的投射界限) 為圖元大小遞增。 這可以透過除法運算、樓層運算和乘來完成。


```C++
        vLightCameraOrthographicMin /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMin = XMVectorFloor( vLightCameraOrthographicMin );
        vLightCameraOrthographicMin *= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax = XMVectorFloor( vLightCameraOrthographicMax );
        vLightCameraOrthographicMax *= vWorldUnitsPerTexel;
```



VWorldUnitsPerTexel 值的計算方式是取得 view 分割區的界限，並除以緩衝區大小。


```C++
        FLOAT fWorldUnitsPerTexel = fCascadeBound /
        (float)m_CopyOfCascadeConfig.m_iBufferSize;
        vWorldUnitsPerTexel = XMVectorSet( fWorldUnitsPerTexel, fWorldUnitsPerTexel,                            0.0f, 0.0f );
```



將視圖的大小上限設為較鬆散，使其符合正向投射的範圍。

請務必注意，使用這項技術時，材質的寬度和高度為1圖元以上。 這會將陰影座標與陰影對應外的索引編制保持一致。

### <a name="back-face-and-front-face"></a>背面和正面臉部

陰影對應應使用標準背面剔除來進行轉譯，此程式會略過檢視器無法查看的物件，並加速呈現場景。 另一個常見的選項是在已啟用 front 臉部剔除的情況下轉譯陰影對應，這表示會刪除面向檢視器的物件。 這項功能的引數是有助於自我遮蔽，因為組成物件背面的幾何會稍微位移。 這種想法有兩個問題。

-   任何具有不當前端或後置臉部幾何的物件都會導致陰影地圖中的成品。 但是，如果不正確的正面臉部或背面的幾何會造成其他問題，就可以放心地假設正面臉部和正面臉部幾何已正確完成。 為 sprite 型幾何（例如 foliage）建立背景臉部可能不切實際。
-   如果陰影深度差異太小，則很可能會發生像是牆壁等物件基底的 Peter 移動和陰影間距。

### <a name="shadow-mapfriendly-geometry"></a>陰影對應–易記幾何

建立可在陰影對應中妥善運作的幾何，可在對抗像是 Peter 移動和陰影 acne 的構件時獲得更大的彈性。

固定邊緣對於自我遮蔽有問題。 靠近 edge 尖端的深度差異很小。 即使是較小的位移，還是會導致物件失去其陰影 (圖 18) 。

**[圖 18]。尖邊會造成從低深度差異與位移的構件詞幹分析**

![尖邊會造成從低深度差異與位移的構件詞幹分析](images/sharp-edges-cause%20artifacts.jpg)

小物件（例如牆壁）應該要有備份，即使它們永遠看不見。 這會增加深度差異。

也請務必確定幾何的面向方向是正確的;也就是，物件的外部應該會向外，而且物件內的內部應該是正面的。 這對於使用恢復臉部剔除進行轉譯，以及對抗深度偏差的效果而言很重要。

## <a name="summary"></a>摘要

本文所述的技巧可用於提高標準陰影對應的品質。 下一步是查看可搭配標準陰影對應使用的技術。 我們建議使用網達網，作為對抗觀點別名的絕佳技術。 接近篩選或變異數陰影對應的百分比可用於將陰影邊緣柔化。 如需詳細資訊，請參閱[串聯陰影地圖](/windows/desktop/DxTechArts/cascaded-shadow-maps)技術文章。

Donnelly、W 和 Lauritzen，A.[差異陰影地圖](https://portal.acm.org/citation.cfm?doid=1111411.1111440)。 互動式3d 圖形上的 Symposium，以及互動式3D 圖形和遊戲的 2006 Symposium 的訴訟。 2006、pp. 161-165。

Engel，Woflgang f. 第4節。 串聯陰影地圖。 ShaderX5， *Advanced 轉譯技巧*，Wolfgang Engel，Ed。 麻塞諸塞州波士頓 Charles 河媒體。 2006。 pp. 197 –206。

Stamminger、Marc 和 Drettakis、George。 [透視圖陰影地圖](https://portal.acm.org/citation.cfm?id=566616)。 電腦圖形和互動式技術的國際會議， *在電腦圖形和互動式技術上有29年的研討會*。 2002、pp 557 –562個。

Wimmer、M.、Scherzer、d. 和 Purgathofer、W.[淺空間透視圖陰影地圖](https://www.cg.tuwien.ac.at/research/vr/lispsm/shadows_egsr2004_revised.pdf)。 轉譯時的 Eurographics Symposium。 2004。 2005年6月10日修訂。 [技術 Universität Wien](https://www.cg.tuwien.ac.at/research/vr/lispsm/)。

 

 
