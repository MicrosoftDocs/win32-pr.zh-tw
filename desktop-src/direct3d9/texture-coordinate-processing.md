---
description: 下圖顯示紋理座標與其來源之間的路徑，以及處理常式和轉譯器所採用的路徑。
ms.assetid: a6126946-8f75-4b3a-b017-d1014e917e9c
title: " (Direct3D 9) 的材質座標處理"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a161d3675a5859702368a62719124aa029ee455
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025770"
---
# <a name="texture-coordinate-processing-direct3d-9"></a> (Direct3D 9) 的材質座標處理

下圖顯示紋理座標與其來源之間的路徑，以及處理常式和轉譯器所採用的路徑。

![從來源到轉譯器之材質座標路徑的圖表](images/tex-processing.png)

有兩個來源可供系統用來繪製材質座標。 針對給定的材質階段，您可以使用頂點格式所包含的材質座標 (D3DFVF \_ TEX1 至 D3DFVF \_ TEX8) ，也可以使用 Direct3D 自動產生的材質座標。 如需第二個案例的詳細資訊，請參閱 [自動產生的材質座標 (Direct3D 9) ](automatically-generated-texture-coordinates.md)。 如果 \_ 目前材質階段的 D3DTSS TEXTURETRANSFORMFLAGS 材質階段狀態設定為 [D3DTTFF 停用] \_ (預設設定) ，則不會轉換輸入座標。 如果 D3DTSS \_ TEXTURETRANSFORMFLAGS> 設定為任何其他值，則會將該階段的轉換矩陣套用至輸入座標。

[**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md)列舉型別會定義 D3DTSS \_ TEXTURETRANSFORMFLAGS 材質階段狀態的有效值。 除了 \_ 略過材質座標轉換的 D3DTTFF DISABLE 旗標以外，在此列舉中定義的值會設定系統傳遞給轉譯器的輸出座標數目。 D3DTTFF \_ COUNT1 到 D3DTTFF \_ COUNT4 旗標會指示系統將一個、兩個、三個或四個元素從輸出座標傳遞到轉譯器。

D3DTTFF \_ 投射旗標是特殊的：它會告訴系統紋理座標適用于投射的材質。 將 D3DTTFF \_ 投影旗標與 [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) 的另一個成員結合，以指示轉譯器將所有元素除以最後一個元素，然後再進行點陣化。 例如，明確使用三個元素的材質座標，或當轉換產生三個元素的材質座標時，您可以結合 D3DTTFF \_ COUNT3 和 D3DTTFF \_ 投射旗標，讓轉譯器將前兩個專案除以最後一個元素，產生定址2d 材質所需的2d 材質座標。

> [!Note]  
> 除了立方環境對應和磁片區材質之外，rasterizers 無法使用具有兩個以上專案的材質座標來定址紋理。 如果您指定的專案數超過可以用來處理該階段目前材質的數目，則會忽略多餘的元素。 這也適用于使用2D 材質座標進行一維材質。

 

下列主題包含其他資訊。

-   [自動產生的材質座標 (Direct3D 9) ](automatically-generated-texture-coordinates.md)
-   [ (Direct3D 9) 的材質座標轉換 ](texture-coordinate-transformations.md)
-   [ (Direct3D 9) 的特殊效果 ](special-effects.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質座標](texture-coordinates.md)
</dt> </dl>

 

 
