---
description: Direct3D 管線使用的所有資源都衍生自兩個基本資源類型︰緩衝區和紋理。 緩衝區是原始資料 (元素) 的集合，紋理是紋素 (紋理元素) 的集合。
ms.assetid: c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69
title: " (Direct3D 10) 的資源類型"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0f757eac93fac8c0ffd49641441fa4570824670dfcca9c3d271f954054548b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120102"
---
# <a name="resource-types-direct3d-10"></a> (Direct3D 10) 的資源類型

Direct3D 管線使用的所有資源都衍生自兩個基本資源類型︰[緩衝區](#buffer-resources)和[紋理](#texture-resources)。 緩衝區是原始資料 (元素) 的集合，紋理是紋素 (紋理元素) 的集合。

-   [緩衝區資源](#buffer-resources)
    -   [緩衝區類型](#buffer-types)
-   [材質資源](#texture-resources)
    -   [材質類型](#texture-types)
    -   [子資源](#subresources)
    -   [強式與弱式類型](#strong-vs-weak-typing)
-   [相關主題](#related-topics)

有兩種方式可以完整指定資源的配置 (或記憶體使用量)︰



| 項目                                                                                                 | 描述                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="Typed"></span><span id="typed"></span><span id="TYPED"></span>類型<br/>             | 建立資源時完整指定類型。<br/>               |
| <span id="Typeless"></span><span id="typeless"></span><span id="TYPELESS"></span>無<br/> | 資源繫結到管線時完整指定類型。<br/> |



 

## <a name="buffer-resources"></a>緩衝區資源

緩衝資源是完整具類型的資料的集合，緩衝區則包含元素。 一個元素由 1 到 4 個元件組成。 元素資料類型的範例包括︰封裝資料值 (例如 R8G8B8A8)、單一的 8 位元整數、四個 32 位元浮點值。 這些資料類型是用來儲存資料，例如位置向量、一般向量、頂點緩衝區中的紋理座標、索引緩衝區中的索引，或者裝置狀態。

建立緩衝區做為未結構化的資源。 因為未建構，所以緩衝區無法包含任何 Mipmap 層次，在讀取時不會篩選，而且無法多重取樣。

### <a name="buffer-types"></a>緩衝區類型

-   [頂點緩衝區](#vertex-buffer)
-   [索引緩衝區](#index-buffer)
-   [常數緩衝區](#constant-buffer)

### <a name="vertex-buffer"></a>頂點緩衝區

緩衝區是元素的集合；頂點緩衝區包含每個頂點資料。 最簡單的範例是包含一種類型資料的頂點緩衝區，例如位置資料。 它可以像下圖一樣視覺化。

![包含位置資料的頂點緩衝區圖例](images/d3d10-resources-single-element-vb2.png)

頂點緩衝區經常包含可完整指定 3D 頂點所需的所有資料。 例如，可能會包含每個頂點位置、一般及紋理座標的頂點緩衝區。 此資料通常組織成每個頂點元素集，如下圖所示。

![頂點緩區的圖例，其包含位置、一般和紋理資料](images/d3d10-vertex-buffer-element.png)

這個頂點緩衝區包含八個頂點的每個頂點資料；每個頂點儲存三個元素 (位置、一般和紋理座標)。 位置和一般都是使用 3 32 位浮點數 (DXGI \_ 格式 \_ R32G32B32 \_ FLOAT) 和材質座標（使用 2 32 位浮點數 (\_ \_ float 格式 R32G32 \_ FLOAT) ）來指定。

若要存取頂點緩衝區的資料，您必須知道要存取哪個頂點以及這些其他緩衝區參數︰

-   位移 - 從緩衝區的起始到第一個頂點資料的位元組數目。 提供給 [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)的位移。
-   BaseVertexLocation-相對於適當繪製呼叫所使用之第一個頂點之位移的位元組數目 (參閱 [繪製方法](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)) 。

建立頂點緩衝區之前，您必須建立 [**輸入設定物件**](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout)來定義其配置;這是藉由呼叫 [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)來完成。 一旦建立了輸入設定物件，請呼叫 [**IASetInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetinputlayout)，將它系結至輸入組合語言階段。

若要建立頂點緩衝區，請呼叫 [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer)。

### <a name="index-buffer"></a>索引緩衝區

索引緩衝區包含連續的 16 位元或 32 位元索引集，而每個索引用來識別頂點緩衝區中的頂點。 使用具有一個或多個頂點緩衝區的索引緩衝區，來提供資料給 IA 階段即稱為編製索引。 索引緩衝區可以視覺化，如下圖所示。

![索引緩衝區的圖例](images/d3d10-index-buffer.png)

儲存在索引緩衝區中的循序索引，使用以下參數尋找︰

-   位移 - 從緩衝區的起始到第一個索引的位元組數目。 提供給 [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)的位移。
-   StartIndexLocation-相對於適當繪製呼叫所使用之第一個頂點之位移的位元組數目 (參閱 [繪製方法](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)) 。
-   IndexCount - 要呈現的索引數目。

若要建立索引緩衝區，請呼叫 [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer)。

索引緩衝區可以將多行或三角形的分隔線，藉由分隔每個 [線條或三角形](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) 的分隔線來將它們拼接在一起。 區域切割索引允許使用單一繪製呼叫來繪製多行或三角形連環。 區域剪下索引只是索引的最大可能值 (0xffff 的16位索引，0xffffffff 用於32位的索引) 。 區域切割索引會重設已編制索引的基本類型的捲繞順序，並且可以用來消除對於變質三角形的需求，否則可能需要先維護適當的三角形連環的捲繞順序。 下列圖例顯示區域切割索引的範例。

![區域切割索引的圖例](images/d3d10-ia-strips-cut-value.png)

### <a name="constant-buffer"></a>常數緩衝區

Direct3D 10 引進了新的緩衝區，以提供稱為著色器常數緩衝區或單純常數緩衝區的著色器常數。 就概念而言，它看起來就像單一元素的頂點緩衝區，如下圖所示。

![著色器常數緩衝區的圖例](images/d3d10-shader-resource-buffer.png)

每個元素會儲存 1 到 4 個元件常數，取決於儲存的資料格式。

常數緩衝區透過允許著色器常數群組在一起並且同時認可，而不是進行個別呼叫以分別認可每一個常數，來減少更新著色器常數所需的頻寬。

若要建立著色器常數緩衝區，請呼叫 [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) 並指定常數緩衝區系結旗標 D3D10 系結 \_ \_ 常數 \_ 緩衝區 (參閱 D3D10 系結 [**\_ \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) 標) 。

若要將著色器常數緩衝區系結至管線，請呼叫下列其中一種方法： [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers)、 [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers)或 [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers)。

請注意，使用 [**ID3D10Effect 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) 介面時， **ID3D10Effect 介面** 實例會處理建立、系結和 comitting 常數緩衝區的進程。 在這種情況下，只會 nescesary 使用其中一個 GetVariable 方法（例如 [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) ）來從效果中取得變數，並使用其中一個 SetVariable 方法（例如 [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix)）來更新變數。 如需使用 **ID3D10Effect 介面** 管理常數緩衝區的範例，請參閱 [教學課程 07](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx)。

著色器會繼續以不是常數緩衝區一部分的變數的相同方式，按照變數名稱直接讀取常數緩衝區中的變數。

每個著色器階段允許最多 15 個著色器常數緩衝區，而每個緩衝區可保留最多 4096 個常數。

使用常數緩衝區來儲存資料流輸出階段的結果。

如需在著色器中宣告常數緩衝區的範例，請參閱[著色器常數 (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-constants.md)。

## <a name="texture-resources"></a>材質資源

紋理資源是設計來儲存紋素的結構化資料集合。 和緩衝區不同的是，紋理可依紋理樣本篩選，由著色器單位讀取。 紋理類型會影響篩選紋理的方式。 紋素代表管線可讀取或寫入的最小紋理單位。 每個材質都包含1至4個元件，以其中一個 DXGI 格式排列 (請參閱 [**dxgi \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。

紋裡會建立結構化資源，以便得知其大小。 不過，只要在材質系結至管線時使用 view 完全指定型別，就可以在資源建立時間輸入每個材質或輸入較少的材質。

-   [材質類型](#texture-types)
-   [子資源](#subresources)
-   [強式與弱式類型](#strong-vs-weak-typing)

### <a name="texture-types"></a>材質類型

有數種紋理類型︰1D、2D、3D，每一個都可使用或不使用 Mipmap 建立。 Direct3D 10 也支援材質陣列和多重取樣材質。

-   [1D 材質](#1d-texture)
-   [1D 材質陣列](#1d-texture-array)
-   [2D 材質和2D 材質陣列](#2d-texture-and-2d-texture-array)
-   [3D 材質](#3d-texture)

### <a name="1d-texture"></a>1D 紋理

最簡單形式的 1D 紋理所包含的紋理資料，可以使用單一紋理座標處理，它可以視覺化為紋素陣列，如下圖所示。

![1D 紋理的圖例](images/d3d10-1d-texture.png)

每個紋素根據所儲存的資料格式包含許多色彩元件。 增加更多複雜度，您可以使用 Mipmap 層次建立 1D 紋理，如下圖所示。

![具有 Mipmap 層次之 1D 紋理的圖例](images/d3d10-resource-texture1d.png)

Mipmap 層次是比上層小二的 n 次方的紋理。 最上層包含大部分的詳細資料，每個後續層級較小；若是 1D 的 Mipmap，最小層級包含一個紋素。 不同層級是以稱為 LOD (詳細層級) 的索引來識別；您可以在呈現不是那麼靠近相機的幾何圖形時，使用 LOD 存取較小的紋理。

### <a name="1d-texture-array"></a>1D 材質陣列

Direct3D 10 對於紋理陣列也有新的資料結構。 1D 紋理陣列概念上看起來像下圖。

![1d 紋理陣列的圖例](images/d3d10-resource-texture1darray.png)

這個紋理陣列包含三種紋理。 三個紋理的每一個都具有紋理寬度 5 (也就是第一層的元素數目)。 每個紋理也包含 3 層 Mipmap。

在 Direct3D 中的所有紋理陣列都是同質紋理陣列，這表示紋理陣列中的每種紋理必須有相同資料格式和大小 (包括紋理寬度和 Mipmap 層次數目)。 只要每一個紋理陣列中的所有紋理大小都相符，您可以建立不同大小的紋理陣列。

### <a name="2d-texture-and-2d-texture-array"></a>2D 紋理和 2D 紋理陣列

Texture2D 資源包含 2D 紋格。 每個紋素是由 u、v 向量定位。 因為是紋理資源，它可能包含 Mipmap 層次和子資源。 完全填充的 2D 紋理資源看起來如下圖。

![2D 紋理資源的圖例](images/d3d10-resource-texture2d.png)

這個紋理資源包含具三個 Mipmap 層次的單一 3x5 紋理。

Texture2DArray 資源是同質 2D 紋理陣列；也就是每個紋理都有相同的資料格式和維度 (包括 Mipmap 層次)。 它與 1D 紋理陣列具有類似的配置，除了紋理現在包含 2D 資料以外，因此其外觀如下圖所示。

![2D 紋理資源陣列的圖例](images/d3d10-resource-texture2darray.png)

這個紋理包含三個紋理，每個紋理為 3x5 含兩個 Mipmap 層次。

### <a name="using-a-texture2darray-as-a-texture-cube"></a>使用 Texture2DArray 做為紋理立方體

紋理立方體是包含 6 個紋理的 2D 紋理陣列，每個立方體表面一個紋理。 完全填充的紋理立方體如下圖所示。

![代表紋理立方體之 2D 紋理資源的圖例](images/d3d10-resource-texturecube.png)

包含 6 個紋理的 2D 紋理陣列，在使用立方體紋理視圖結合管線後，可使用立方體內建功能從著色器內讀取。 使用從紋理立方體中心指出的 3D 向量，從著色器處理紋理。

### <a name="3d-texture"></a>3D 紋理

Texture3D 資源 (也稱為容積紋理) 包含 3D 容積的紋素。 因為是紋理資源，所以可能包含 Mipmap 層次。 完整填入的 [**3d 紋理**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) 看起來如下圖所示。

![3D 紋理資源的圖例](images/d3d10-resource-texture3d.png)

3D 紋理 Mipmap 切片繫結為描繪目標輸出 (描繪目標視圖) 時，3D 紋理行為等同於具 n 切片的 2D 紋理陣列。 您可以透過將輸出資料的純量元件宣告為 SV RenderTargetArrayIndex 系統值，從 [幾何著色器] 階段選擇特定轉譯配量 \_ 。

沒有 3D 紋理陣列概念，因此 3D 紋理子資源是單一 Mipmap 層次。

### <a name="subresources"></a>子資源

Direct3D 10 API 會參考整個資源或資源子集。 為了指定部分資源，Direct3D 已創造字詞子資源，這表示資源的子集。

緩衝區定義為單一的子資源。 紋理則稍微複雜，因為有數種不同紋理類型 (1D、2D 等)，其中部分支援 Mipmap 層次和/或紋理陣列。 從最簡單的案例開始，1D 紋理定義為單一子資源，如下圖所示。

![1D 紋理的圖例](images/d3d10-1d-texture.png)

這表示組成 1D 紋理的紋理陣列包含在單一子資源中。

如果展開含有三個 Mipmap 層次的 1D 紋理，它可以視覺化如下。

![具有 Mipmap 層次之 1D 紋理的圖例](images/d3d10-resource-texture1d.png)

將此視為三個子紋理組成的單一紋理。 每個子紋理計算為一個子資源，所以這個 1D 紋理包含 3 個子資源。 子紋理 (或子資源) 可以對單一紋理使用詳細層級 (LOD) 編制索引。 使用紋理陣列時，存取特定子紋理需要 LOD 和特定紋理二者。 或者，API 結合這兩個資訊為單一以零起始的子資源索引，如此處所示。

![以零起始的子資源索引的圖例](images/d3d10-resource-texture1darray-sub-indexing.png)

### <a name="selecting-subresources"></a>選取子資源

某些 API 會存取整個資源 (例如 [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)) ，其他人會存取一部分的資源 (例如 [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource) 或 [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) 。 存取部分資源的 API 通常會使用 view description (例如 [**D3D10 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)) 來指定要存取的子資源。

這些圖闡述檢視描述在存取紋理陣列時使用的詞彙。

### <a name="array-slice"></a>陣列切片

提供紋理陣列，每個紋理含有 Mipmap，陣列切片 (以白色矩形代表) 則包含一個紋理及其所有子紋理，如下圖所示。

![陣列切片的圖例](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Mip 切片

Mip 切片 (以白色矩形代表) 對於陣列中的每個紋理包含一個 Mipmap 層次，如下圖所示。

![Mip 切片的圖例](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>選取單一子資源

您可以使用這兩種切片來選擇單一子資源，如下圖所示。

![使用陣列切片和 Mip 切片選擇子資源的圖例](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>選取多個子資源

或者，您也可以使用含有數個 Mipmap 層次和/或數個紋理的這兩種切片，來選取多個子資源。

![選取多個子資源的圖例](images/d3d10-resource-subresources-2.png)

無論您使用何種材質類型（不論是否有 mipmap），不論是否有材質陣列，您都可以使用 helper 函數 [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)來計算特定 subresource 的索引。

### <a name="strong-vs-weak-typing"></a>強輸入與弱輸入

建立完整具類型的資源會限制資源為其建立時使用的格式。 這可讓執行時間將存取優化，特別是在建立資源時，其旗標表示應用程式無法 [對應](d3d10-graphics-programming-guide-resources-mapping.md) 。 使用特定類型建立的資源無法使用檢視機制重新解譯。

在類型較少的資源中，第一次建立資源時，資料類型是未知的。 應用程式必須從可用的類型格式較少選擇 (查看 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。 您必須指定要配置的記憶體大小，以及執行階段是否需要在 Mipmap 中產生子紋理。 不過，確實的資料格式 (記憶體是否解釋為整數、浮點值、未簽署的整數等) 要到資源使用檢視繫結到管線時才能確定。 因為直到紋理繫結到管線，紋理格式均維持彈性，所以資源稱為弱輸入的儲存空間。 弱輸入儲存空間的優點，是可以重複使用或重新解譯 (使用另一種格式)，只要新格式的元件位元符合舊格式的位元計數。

單一資源可以繫結至多個管線階段，只要每一個都有唯一檢視，而這完全符合每個位置的格式。 例如，使用格式 DXGI 格式 R32G32B32A32 的資源， \_ \_ 可以當做 \_ dxgi \_ 格式 \_ R32G32B32A32 \_ FLOAT，也可以在 \_ \_ \_ 管線中的不同位置同時使用 dxgi 格式 R32G32B32A32 UINT。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的資源 ](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
