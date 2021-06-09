---
description: 許多轉譯和內容產生技巧都需要2D 信號 (的唯一、非重迭地圖，例如紋理) 到網格上。
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: '使用 UVAtlas (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826326"
---
# <a name="using-uvatlas-direct3d-9"></a>使用 UVAtlas (Direct3D 9) 

> [!NOTE]
> UVAtlas 最初是隨附于現已淘汰的 D3DX9 utilty 程式庫中。 您可以從 [UV 的 Command-Line 工具 (uvatlas.exe) ](https://github.com/Microsoft/UVAtlas)取得最新版本。

許多轉譯和內容產生技巧都需要2D 信號 (的唯一、非重迭地圖，例如紋理) 到網格上。 這類技術包括：

-   標準/置換對應
-   材質空間 PRT 模擬和燈光地圖
-   表面繪製
-   材質區域光源

手動產生唯一的 UV 對應通常很耗時且繁瑣。當輸入幾何很複雜，而且需要有效率/低扭曲的材質空間使用量時，更是如此。 下圖顯示範例網格及其對應的材質塔。

![顯示範例網格及其對應的材質塔。](images/uvatlas1.jpg)

此範例會在左邊的) 顯示網格 (，並在右) 上顯示對應的 UV 空間一般地圖 (。 請注意，材質塔包含數個群組或資料叢集;每個叢集都稱為「圖表」，而在上述範例中，顯示會包含網格部分的一般資料。

D3DX UVAtlas Api 會自動產生最佳、非重迭的材質塔。 Api 提供的輸入參數可讓您：

-   將材質延展、扭曲和 undersampling 降至最低。
-   最大化材質空間封裝密度，以有效率地使用記憶體。
-   提供跨網格的平均取樣，將取樣頻率的不連續降到最低。

## <a name="how-uvatlas-works"></a>UVAtlas 的運作方式

UVAtlas Api (查看 [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) 函式，) 透過將圖層分割成圖表並將圖表封裝成材質塔來產生材質塔。 使用 [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) 和 [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) 分別執行這些步驟;或者，您可以使用 [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) ，在單一呼叫中進行資料分割、參數化和套件。

-   [分割和參數化網格](#partitioning-and-parameterizing-a-mesh)
-   [使用整合式度量張量來控制參數化](#using-integrated-metric-tensors-to-control-parameterization)
-   [針對使用者指定的 Creases 使用相鄰資料](#using-adjacency-data-for-user-specified-creases)
-   [將圖表封裝到塔](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>分割和參數化網格

首先，網格會分割成圖表，然後每個圖表會參數化為自己的 \[ 0、1個 \] UV 空間。 圓柱可由一個圖表參數化;另一方面，球體將需要兩個圖表，如下圖所示。

![分割成兩個圖表之球體的圖例](images/uvatlas3.jpg)

可以使用單一圖表參數化的網格會分類為「homeomorphic 至磁片」，這表示您可以將無限彈性、可無限延伸的磁片分散到圖表上，並完全涵蓋幾何。 這種延展功能（稱為 homeomorphism）是雙向函式;這表示您可以從一個參數化移至另一個參數，而不會遺失資訊。

很少的真實世界網格可以參數化為兩個維度，而不需要將網格分隔成叢集或圖表。 下圖顯示另一個範例網格及其對應的材質塔。

![顯示具有不同圖形及其對應材質塔的範例網格。](images/uvatlas2.jpg)

有兩個參數可決定所建立的圖表數目：

-   可供塔使用的圖表數目上限
-   每個圖表允許的最大延展量

延展量將會決定所產生的圖表數目，以及取樣的整體品質。 從0.0 延展範圍 (不會) 到 1.0 (任何延展) 量。 D3DXUVAtlasCreate 和 D3DXUVAtlasPartition 會傳回演算法產生的最大延展。 下圖顯示另一個範例網格及其對應的材質塔。

![範例網格及其對應的材質塔圖](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>使用整合式度量張量來控制參數化

您可以根據每個三角形來指定材質間距的優先順序。 您可以提供整合的度量張量，以控制在產生的材質空間塔中如何伸展三角形。 您可以使用 D3DX IMT 計算函數，直接指定 IMT 的，也可以根據輸入信號來計算。 整合式計量 tensor (或 IMT) 是對稱的2x2 矩陣，描述如何在塔中將三角形伸展。 每個 IMT 都是由3個浮點數定義， (a，b，c) 來呼叫它們。 它們可以在對稱2x2 矩陣中排列，如下所示：


```
a b
b c
```



然後，IMT 可以用來尋找兩個向量之間的距離。 假設有兩個向量 v1 和 v2，其中：


```
vector v1
vector v2 = v1 + (s,t)
```



V1 與 v2 之間的距離可以計算如下：


```
sqrt((s, t) * M * (s, t)^T)
```



換句話說，向量 (s，t) 可能是以 u-v 空間的任意方向延展的大小。 在此情況下，s 向量是從第一個頂點到第二個頂點的方向，而 t 是標準和 s 的交叉乘積。 例如：


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



您可以使用 D3DX IMT 計算函數（D3DXComputeIMTFromPerVertexSignal、D3DXComputeIMTFromPerTexelSignal、D3DXComputeIMTFromSignal 和 D3DXComputeIMTFromTexture 圖形），直接指定 IMT 的或根據輸入信號來計算 \_ 。

如果您想要控制如何配置個別三角形的材質空間，請直接指定 IMT 資料。 如此一來，就能將塔中的更多區域配置至網格 (的重要區域，例如字元的臉部或胸標誌，或接近播放程式流覽路徑的場景區域) 。 藉由指定 IMT 做為識別矩陣的倍數，產生的三角形將會在材質空間中以一致的方式調整。

例如，假設有一個高解析度的一般地圖，您可以計算 IMT，以提供更多材質空間給標準地圖中較高頻率的範圍。 對應至原始一般地圖之固定區域的「一般」 (三角形) 將會收到較少的材質空間。 包含大量標準地圖詳細資料的三角形，在最終結果中會收到更多材質區域。 然後，您可以將一般地圖重新取樣為較小的材質，但維持詳細資料，或者您可以使用更理想的 UV 對應來重新計算一般地圖。

### <a name="using-adjacency-data-for-user-specified-creases"></a>針對使用者指定的 Creases 使用相鄰資料

您可以將使用者定義的相鄰資訊提供給資料分割函數，以描述網格中預先定義的 creases，從而定義相鄰臉部之間的圖表界限。 這是一個簡單的方法，可讓呼叫者將自己的圖表分割指定為演算法的輸入，這會進一步修改圖表，以在允許的最大值下顯示延展。

### <a name="example"></a>範例

此範例說明如何使用 UVAtlas Api 和 DirectX 檢視器 (Dxviewer.exe) 在您的模型中尋找並修正可能會大幅影響材質塔大小的不連續。 您可以從 DirectX SDK 取得 Dxviewer.exe 並瞭解它的相關資訊。 在2009年8月之後，Dxviewer.exe 已從 DirectX SDK 移除，因此若要取得此版本，您至少需要2009年8月的 DirectX SDK。 如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。

假設您在您最愛的內容產生軟體中開始使用一些模型 (此範例會使用 Maya) 中所建立的阻礙 head 模型。 將紋理模型匯出為. x 檔案，並使用 D3DXUVAtlasCreate 建立材質塔。 產生的材質塔看起來會像下圖。

![阻礙模型的塔圖](images/uvatlas5.jpg)

塔有22個圖表和最大延展值0.994。

現在，請查看多紋理的模型，以查看材質塔與幾何的對應程度。 若要這樣做，請將模型載入檢視器工具中：

-   從 DirectX 公用程式開啟檢視器工具。
-   按一下 [開啟] 按鈕，載入. x 檔案。
-   按一下 [流覽] 按鈕，然後從快顯視窗中選取 [Creases]，以啟用 [折痕] 觀看選項。

下圖顯示您應該會在檢視器工具中看到的內容。

![檢視器工具中的紋理網格圖](images/uvatlas6c.jpg)

每一行都是一個折痕，也就是紋理塔中兩個圖表之間的相鄰邊緣。 演算法所產生的圖表數目是因為法線中的不連續所造成的微小差異。 這些小差異可透過焊接資料來減少，也就是強制幾乎等於相等的資料。 若要焊接法線和 skinweights：

-   在網格上使用下列命令列來執行 DirectX Ops (dxops.exe) 工具 (以您的模型名稱取代 ' modelName. x ') ：
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

這會比較法線和 skinweights，而在值之間的差異小於2.01，則會將資料設為相等。 下圖顯示在) 左焊接 (之前的 creases，以及在右) 上焊接 (之後的 creases：

![焊接之前的 creases 圖例](images/uvatlas6a.jpg)![焊接之後的 creases 圖例](images/uvatlas6b.jpg)

圖7：使用焊接移除 creases

在此範例中，已從輸入網格移除86頂點。 在網格中使用較少的 creases 時，您可以重新產生塔，如下圖所示。

![已移除 creases 的新的塔圖](images/uvatlas8.jpg)

塔僅有7個圖表和大約0.0776 的最大延展。 新的塔現在適用于較小的材質 (此範例) 的大小大約為30%。

### <a name="packing-charts-into-an-atlas"></a>將圖表封裝到塔

一旦將網格分割成個別的參數化圖表，圖表就必須有效率地封裝成單一材質地圖。 這會以 D3DXUVAtlasCreate 的第二個步驟來執行，或可透過呼叫 D3DXUVAtlasPack 明確地叫用。

封裝的圖表會以使用者指定的裝訂邊寬度隔開。 裝訂邊寬度是圖表之間的區隔量，並允許雙線性插補和 mip 對應，以避免在圖表界限上呈現成品。 D3DX 會提供自動填入這些裝訂邊的介面，如需詳細資訊，請參閱 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 。

## <a name="integrating-uvatlas-into-your-pipeline"></a>將 UVAtlas 整合到您的管線

除了在紋理繪製之前被叫用的演出者之外，這些函式也可以整合到自動化的美工圖案中。 例如，在執行 PRT 模擬或正常對應傳遞之前，您可以在資產更新後自動發出 UVAtlas 呼叫。 如果已修改網狀拓朴，這可避免需要手動手動修復物件的 UV 對應。

如需 UVAtlas 函式的使用方式，請參閱 [ (uvatlas.exe) 的 UV Command-Line 工具 ](https://github.com/Microsoft/UVAtlas) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced 主題](advanced-topics.md)
</dt> </dl>

 

 
