---
description: 瞭解 D3DX_FILTER 旗標，這些旗標可用來指定材質中要操作的通道，例如 D3DX_FILTER_TRIANGLE。
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7580749eca2134f899356c4632d8171b147aa7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408221"
---
# <a name="d3dx_filter"></a>D3DX \_ 篩選

下列旗標用來指定要在材質中操作的通道。



| \#定義                | 描述                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ 篩選 \_ 無      | 不會進行調整或篩選。 來源影像界限外的圖元會假設為透明的黑色。                                                                                 |
| D3DX \_ 篩選 \_ 點     | 每個目的地圖元都是從來源影像取樣最接近的圖元來計算。                                                                                                                     |
| D3DX \_ 篩選 \_ 線性    | 每個目的地圖元都是從來源影像取樣四個最接近的圖元來計算。 當兩個軸的刻度小於2時，此篩選器的效果最佳。                                          |
| D3DX \_ 篩選 \_ 三角形  | 來源影像中的每個圖元平均占目的地映射。 這是篩選器的最慢。                                                                                           |
| D3DX \_ 篩選 \_ 方塊       | 每個圖元的計算方式是將來源影像中的 2x2 (x2) box 圖元平均。 只有當目的地的維度為來源的一半時，此篩選才會運作，如同 mipmap 的情況。 |
| D3DX \_ 篩選 \_ 鏡像 \_ U | U 軸上材質邊緣的圖元應進行鏡像，而不會換行。                                                                                                                           |
| D3DX \_ 篩選 \_ 鏡像 \_ V | 在 v 軸上紋理邊緣的圖元應進行鏡像，而不會換行。                                                                                                                           |
| D3DX \_ 篩選 \_ 鏡像 \_ W | 在 w 軸上紋理邊緣的圖元應進行鏡像，而不會換行。                                                                                                                           |
| D3DX \_ 篩選 \_ 鏡像    | 指定此旗標與指定 D3DX \_ 濾波器 \_ 鏡像 \_ U、D3DX \_ FILTER \_ 鏡像 \_ V 和 D3DX \_ 濾波器 \_ mirror （ \_ W 旗標）相同。                                                                     |
| D3DX \_ 篩選 \_ 遞色    | 產生的影像必須使用4x4 排序的遞色量演算法進行遞色。                                                                                                                                  |
| D3DX \_ FILTER \_ SRGB \_ IN  | 輸入資料位於 sRGB (gamma 2.2) 色彩空間中。                                                                                                                                                              |
| D3DX \_ FILTER \_ SRGB \_ OUT | 輸出資料位於 sRGB (gamma 2.2) 色彩空間中。                                                                                                                                                         |
| D3DX \_ 篩選 \_ SRGB      | 與 \_ \_ \_ 在 \| D3DX \_ 篩選 \_ srgb 中 \_ 指定 D3DX 篩選 srgb 的方式相同。                                                                                                                                       |



 

每個有效的篩選都必須只包含下列其中一個旗標： D3DX \_ filter \_ NONE、D3DX \_ FILTER \_ POINT、D3DX \_ filter \_ 線性、D3DX \_ filter \_ 三角形或 D3DX \_ filter \_ BOX。 此外，您可以使用或運算子，以有效的篩選準則來指定下列一個或多個選擇性旗標： D3DX \_ filter \_ mirror \_ U、D3DX \_ FILTER \_ mirror \_ V、D3DX \_ filter \_ mirror \_ W、D3DX \_ filter \_ 鏡像、D3DX \_ filter \_ 遞色、D3DX \_ filter \_ srgb \_ IN、D3DX filter \_ \_ srgb \_ OUT 或 D3DX \_ filter \_ srgb。

指定 \_ 這個參數的 D3DX 預設值，通常相當於指定 D3DX \_ 濾波器 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。 不過，D3DX \_ 預設值可以有不同的意義，視使用篩選的方法而定。 例如：

-   使用 [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)時，D3DX \_ 預設對應至 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。
-   使用 [**D3DXFilterTexture**](d3dxfiltertexture.md)時， \_ \_ \_ 如果紋理大小是2的乘冪，D3DX 預設會對應到 D3DX 篩選方塊，否則會使用 D3DX \_ 篩選方塊 \_ \| D3DX \_ 篩選 \_ 遞色。

參考每個方法，以查看如何對應 D3DX \_ 預設篩選的相關資訊。

## <a name="constant-information"></a>常數資訊



| 需求                         | 值           |
|--------------------------|------------|
| 標頭                   | d3dx9tex。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DX 常數](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



