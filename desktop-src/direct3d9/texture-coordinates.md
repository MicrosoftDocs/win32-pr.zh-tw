---
description: 大部分紋理（像是點陣圖）都是一維的色彩值陣列。
ms.assetid: vs|directx_sdk|~\texture_coordinates.htm
title: " (Direct3D 9) 的材質座標"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff2c2c86eebac77d910b5dc6c583df380f0bbb2ccb3dca2fc65b9e929e7abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519792"
---
# <a name="texture-coordinates-direct3d-9"></a> (Direct3D 9) 的材質座標

大部分紋理（像是點陣圖）都是一維的色彩值陣列。 三種環境對應紋理是例外狀況。 如需詳細資訊，請參閱 [ (Direct3D 9) 的三次環境對應 ](cubic-environment-mapping.md)。 個別的色彩值稱為材質元素或材質。 每個材質在材質中都有唯一的位址。 您可以將位址視為資料行和資料列編號，在下圖中分別標示為您和 v。

![材質位址作為資料行和資料列編號的圖例](images/uvcoordinates.jpg)

材質座標位於材質空間中。 也就是說，它們是相對於材質中的位置 (0、0) 。 當材質套用至3D 空間中的基本時，其材質位址必須對應到物件座標。 然後，必須將它們轉譯為螢幕座標或圖元位置。

## <a name="mapping-texels-to-screen-space"></a>將材質對應至螢幕空間

Direct3D 會將材質空間中的材質直接對應至螢幕空間中的圖元，而略過中繼步驟以提高效率。 這個對應程式實際上是反向對應。 也就是說，針對螢幕空間中的每個圖元，會計算材質空間中對應的材質位置。 取樣點上或周圍的材質色彩。 取樣進程稱為材質篩選。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質篩選 ](texture-filtering.md)。

材質中的每個材質都可以透過其材質座標來指定。 不過，為了將材質對應至基本專案，Direct3D 需要所有紋理中所有材質的統一位址範圍。 因此，它會使用泛型定址配置，其中所有的材質位址都在0.0 到1.0 （含）的範圍內。 Direct3D 應用程式會以您的角度指定紋理座標，v 值與2D 笛卡兒座標一樣，是以 x、y 座標來指定。 技術上來說，系統可以實際處理0.0 和1.0 範圍之外的材質座標，並使用您針對材質定址所設定的參數來執行此作業。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質定址模式 ](texture-addressing-modes.md)。

結果是，相同的材質位址可以對應到不同材質中的不同材質座標。 在下圖中，材質位址是 (0.5，1.0) 。 不過，因為材質的大小不同，所以材質位址會對應至不同的材質。 在左邊的材質1是5x5。 材質位址 (0.5，1.0) 對應至材質 (2，4) 。 右側的材質2是7x7。 材質位址 (0.5，1.0) 對應至材質 (3，6) 。

![與不同材質上不同材質的相同材質位址對應圖例](images/texadr1.png)

材質對應程式的簡化版本如下圖所示。 無可否認地，此範例非常簡單。 如需詳細資訊，請參閱 [直接將材質對應至 (Direct3D 9) 的圖元 ](directly-mapping-texels-to-pixels.md)。

![圖元的圖例 (對應至物件空間的色彩) 正方形](images/texadr2.png)

在此範例中，顯示在圖左邊的圖元會理想化成色彩的正方形。 圖元四個角落的位址會對應至物件空間中的3D 基本物件。 圖元的形狀通常會因為3D 空間中的基本圖形，以及視圖角度而失真。 基本型別上的介面區的邊角會對應到圖元的邊角，然後對應到材質空間。 對應程式會再次扭曲圖元的形狀，這是很常見的。 圖元的最終色彩值是從圖元對應之區域中的材質計算而得。 您可以在設定材質篩選方法時，判斷 Direct3D 用來到達圖元色彩的方法。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質篩選 ](texture-filtering.md)。

您的應用程式可以直接將材質座標指派給頂點。 這項功能可讓您控制材質的哪些部分對應至基本。 例如，假設您建立的矩形基本型別與下圖中的材質大小完全相同。 在此範例中，您想要讓應用程式將整個材質對應到整個牆上。 您的應用程式指派給基本物件頂點的材質座標為 (0.0、0.0) 、 (1.0、0.0) 、 (1.0、1.0) 和 (0.0、1.0) 。

![材質對應牆的圖例](images/texadr3.png)

如果您決定將牆壁的高度減少一半，可以扭曲紋理以放到較小的牆上，或者您可以指派紋理座標，讓 Direct3D 使用材質的下半部。

如果您決定扭曲或調整材質以符合較小的牆，您使用的材質篩選方法將會影響影像的品質。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質篩選 ](texture-filtering.md)。

相反地，如果您決定要指派材質座標，讓 Direct3D 使用較小牆的材質下半部，則在此範例中，您的應用程式指派給原始物件頂點的材質座標為 (0.0、0.5) 、 (1.0、0.5) 、 (1.0、1.0) 和 (0.0、1.0) 。 Direct3D 會將材質的下半部套用至牆壁。

頂點的材質座標有可能大於1.0。 當您將材質座標指派給不在0.0 到1.0 （含）範圍內的頂點時，您也應該設定材質定址模式。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質定址模式 ](texture-addressing-modes.md)。

## <a name="texture-coordinates-and-texture-stages"></a>材質座標和材質階段

材質座標會透過材質階段與材質相關聯。 使用 SetTexture (stageIndex、pTexture) 將材質指派給紋理階段。 請參閱 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)。

彈性頂點格式 (FVF) 程式碼最多可定義八組紋理座標。 材質座標資料是由使用者在頂點資料中提供。 以零為基底的索引參考資料： 0-7。 最多有8個材質混合階段。 材質與使用 SetTexture ( stageIndex，pTexture) 的特定階段相關聯。

完成這項操作之後，任何階段都可以使用任何紋理座標集合。 每一組座標都與使用 SetTextureStageState ( stageIndex、D3DTSS \_ TEXCOORDINDEX、textureCoordinateIndex ) 的階段相關聯。 請參閱 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)。 如此一來，就可以將混合階段設定為使用任何材質和材質座標。 一個以上的階段可以使用相同的紋理或材質座標。

下列主題包含其他資訊。

-   [ (Direct3D 9) 的材質座標格式 ](texture-coordinate-formats.md)
-   [ (Direct3D 9) 的材質座標處理 ](texture-coordinate-processing.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 紋理](direct3d-textures.md)
</dt> </dl>

 

 
