---
description: 三層環境對應（有時稱為 cube 對應）是包含代表物件周圍場景之影像資料的材質，如同物件位於 cube 中央一樣。
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: " (Direct3D 9) 的三次環境對應"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecac83db067224195883485bcbd282aa82ae4b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386000"
---
# <a name="cubic-environment-mapping-direct3d-9"></a> (Direct3D 9) 的三次環境對應

三層環境對應（有時稱為 cube 對應）是包含代表物件周圍場景之影像資料的材質，如同物件位於 cube 中央一樣。 每個三面的環境對應都涵蓋水準和垂直的90度視野，而且每個立方體圖都有六個臉部。 臉部的方向如下圖所示。

![具有垂直于 cube 臉部之中央座標軸的 cube 圖例](images/cubemap-cube.png)

Cube 的每個臉部都是在世界空間中的 x/y、y/z 或 x/z 平面垂直方向。 下圖顯示每個平面如何對應至臉部。

![使用平面座標投射的 cube 臉部圖例](images/cube-faces.png)

三層環境對應會實作為一系列的材質物件。 應用程式可以使用靜態映射進行三次環境對應，也可以轉譯成 cube 對應的臉部，以執行動態環境對應。 這項技術會要求 cube 對應介面必須是有效的呈現目標介面，並已設定 D3DUSAGE \_ RENDERTARGET 旗標。

立方體圖的臉部不需要包含周圍場景的極詳細轉譯。 在大部分的情況下，會將環境對應套用至曲線表面。 由於大多數應用程式使用的曲率數量，產生的反射失真會在環境對應中大幅詳細地顯示記憶體和轉譯的額外負荷。

## <a name="mipmapped-cubic-environment-maps"></a>Mipmapped 立方環境對應

Cube 對應可以是 mipmapped 的。 若要建立 mipmapped cube 對應，請將 [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) 方法的 [層級] 參數設定為您想要的層級數目。 您可以想像這些表面的拓撲，如下圖所示。

![具有 n 個 mip 層級之 mipmapped cube 地圖的圖表](images/cubemap-mipped.png)

建立 mipmapped 立方環境對應的應用程式，可以藉由呼叫 [**GetCubeMapSurface**](/windows/desktop/api) 方法來存取每個臉部。 從 [**D3DCUBEMAP \_ 臉部**](./d3dcubemap-faces.md) 列舉型別設定適當的值開始，如 [)  (Direct3D 9 中建立三種環境的地圖](creating-cubic-environment-map-surfaces.md)介面所述。 接下來，將 **GetCubeMapSurface** 層級參數設定為您想要的 mipmap 層級，以選取要抓取的層級。 請記住，0會對應到最上層影像。

## <a name="texture-coordinates-for-cubic-environment-maps"></a>三層環境對應的材質座標

使用標準紋理套用時，以三種方式建立索引三種環境對應的材質座標不是簡單的 u、v 樣式座標。 事實上，三層環境對應根本不會使用材質座標。 為了取代一組紋理座標，三層環境對應需要3D 向量。 您必須小心指定適當的頂點格式。 除了告訴系統您的應用程式所使用的材質座標集合數目之外，您還必須提供每個集合中有多少個元素的相關資訊。 基於這個目的，Direct3D 提供了 [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) 的宏集。 這些宏會接受單一參數，以識別要描述其大小的材質座標集合的索引。 在3D 向量的案例中，您會包含 D3DFVF TEXCOORDSIZE3 宏所建立的位模式 \_ 。 下列程式碼範例顯示如何使用這個宏。


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



在某些情況下（例如漫射燈光對應），您可以使用向量的相機空間頂點。 在其他情況下（例如反射環境對應），您會使用反映向量。 由於可廣泛瞭解轉換的頂點法線，此處的資訊著重于計算反映向量。

您必須瞭解每個頂點的位置，以及從視點到該頂點的向量，才能自行計算反映向量。 Direct3D 可以自動計算您幾何的反射向量。 使用這項功能可節省記憶體，因為您不需要包含環境對應的材質座標。 它也會減少頻寬，而在 T&L HAL 裝置的情況下，它可能會比您的應用程式本身所能產生的計算速度快很多。 若要使用這項功能，請在包含三層環境對應的材質階段中，將 [D3DTSS \_ TEXCOORDINDEX 材質階段] 狀態設定為 \_ CAMERASPACEREFLECTIONVECTOR 的 D3DTSS TCI \_ D3DTEXTURESTAGESTATETYPE 成員和紋理座標集合的索引組合。 [](./d3dtexturestagestatetype.md) 在某些情況下（例如，擴散燈光對應），您可以使用 D3DTEXTURESTAGESTATETYPE 的 D3DTSS \_ TCI \_ CAMERASPACENORMAL 成員，這會導致系統使用轉換的相機空間、頂點標準作為材質的定址向量。  索引僅供系統用來判斷材質的包裝模式。

下列程式碼範例顯示如何使用此值。


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



當您啟用自動材質座標產生時，系統會使用兩個公式中的一個來計算每個頂點的反射向量。 當 D3DRS \_ LOCALVIEWER 轉譯狀態設為 **TRUE** 時，會使用下列公式。

![反映向量的公式 (r = 2 (exn) n-e) ](images/reflection-vector-local.png)

在上述公式中，R 是正在計算的反映向量，E 是正規化的位置向量，而 N 是相機空間頂點正常。

當 D3DRS \_ LOCALVIEWER 轉譯狀態設為 **FALSE** 時，系統會使用下列公式。

![反映向量 (r = 2nzn-i) 的公式](images/reflection-vector-nonlocal.png)

此公式中的 R 和 N 元素與先前的公式相同。 N<sub>Z</sub> 的元素是頂點法線的世界空間 Z，而 I 是 (0，0，1) 無限遠的觀點。 系統會從任一公式使用反映向量，以選取並處理 cube 地圖的適當臉部。

> [!Note]  
> 在大多數情況下，應用程式應該啟用頂點法線的自動正規化。 若要這樣做，請將 D3DRS \_ NORMALIZENORMALS 設定為 **TRUE**。 如果您未啟用此呈現狀態，則環境對應的外觀會與您預期的不同。

 

下列主題包含其他資訊。

-   [ (Direct3D 9) 建立三個環境的地圖表面 ](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[環境對應](environment-mapping.md)
</dt> </dl>

 

 
