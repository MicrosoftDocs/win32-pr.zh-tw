---
title: Direct3D 11 中的材質簡介
description: 紋理資源是設計來儲存紋素的結構化資料集合。
ms.assetid: d745093e-2d51-4d45-a88a-caa0ca58b2ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3bfd19f018ff3f3d9fc8eb1608212a93b4364de2cc24b6213763dfcda4ffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027898"
---
# <a name="introduction-to-textures-in-direct3d-11"></a>Direct3D 11 中的材質簡介

紋理資源是設計來儲存紋素的結構化資料集合。 紋素代表管線可讀取或寫入的最小紋理單位。 和緩衝區不同的是，紋理可依紋理樣本篩選，由著色器單位讀取。 紋理類型會影響篩選紋理的方式。 每個材質都包含1至4個元件，以 DXGI 格式列舉所定義的其中一個 DXGI 格式來排列 \_ 。

建立具已知大小的紋理為結構化資源。 不過，每個紋理在建立資源之後可能有型別或無型別，只要當紋理與管線繫結時使用檢視完全指定型別。

## <a name="texture-types"></a>材質類型

有數種紋理類型︰1D、2D、3D，每一個都可使用或不使用 Mipmap 建立。 Direct3D 11 也支援材質陣列和多重取樣材質。

-   [1D 紋理](#1d-textures)
-   [1D 紋理陣列](#1d-texture-arrays)
-   [2D 材質和2D 材質陣列](#2d-textures-and-2d-texture-arrays)
-   [3D 紋理](#3d-textures)

### <a name="1d-textures"></a>1D 紋理

最簡單形式的 1D 紋理所包含的紋理資料，可以使用單一紋理座標處理，它可以視覺化為紋素陣列，如下圖所示。 1D 紋理會以 [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) 介面表示。

![1D 紋理的圖例](images/d3d10-1d-texture.png)

每個紋素根據所儲存的資料格式包含許多色彩元件。 增加更多複雜度，您可以使用 Mipmap 層次建立 1D 紋理，如下圖所示。

![具有 Mipmap 層次之 1D 紋理的圖例](images/d3d10-resource-texture1d.png)

Mipmap 層次是比上層小二的 n 次方的紋理。 最上層包含大部分的細節，每個後續的層次較小。 對於 1D Mipmap，最小層級包含一個紋素。 此外，MIP 層級一律降至 1:1。 當專為特別尺寸紋理產生 Mipmap， 下一個較低層次一律為均勻大小 (除了最低層到達 1 以外)。 例如，圖表顯示 5x1 紋理，其下一個最低層為 2x1 紋理，其下一個 (和上一個) MIP 層是 1x1 大小的紋理。 由稱為 LOD (細節層次) 的索引識別的層次，會在呈現不是那麼靠近相機的幾何圖形時，用於存取較小的紋理。

### <a name="1d-texture-arrays"></a>1D 紋理陣列

Direct3D 11 也支援材質的陣列。 一維紋理陣列也會以 [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) 介面表示。 1D 紋理陣列概念上看起來像下圖。

![1d 紋理陣列的圖例](images/d3d10-resource-texture1darray.png)

這個紋理陣列包含三種紋理。 三個紋理的每一個都具有紋理寬度 5 (也就是第一層的元素數目)。 每個紋理也包含 3 層 Mipmap。

在 Direct3D 中的所有紋理陣列都是同質紋理陣列，這表示紋理陣列中的每種紋理必須有相同資料格式和大小 (包括紋理寬度和 Mipmap 層次數目)。 只要每一個紋理陣列中的所有紋理大小都相符，您可以建立不同大小的紋理陣列。

### <a name="2d-textures-and-2d-texture-arrays"></a>2D 紋理和 2D 紋理陣列

Texture2D 資源包含 2D 紋格。 每個紋素是由 u、v 向量定位。 因為是紋理資源，它可能包含 mipmap 層次和子資源。 2D 紋理會以 [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) 介面表示。 完全填充的 2D 紋理資源看起來如下圖。

![2D 紋理資源的圖例](images/d3d10-resource-texture2d.png)

這個紋理資源包含具三個 Mipmap 層次的單一 3x5 紋理。

2D 紋理陣列資源是同質 2D 紋理陣列，也就是每個紋理都有相同的資料格式和尺寸 (包括 Mipmap 層次)。 2D 材質陣列也會以 [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) 介面表示。 它有類似 1D 紋理的版面配置，現在包含 2D 資料的紋理除外，如下圖所示。

![2d 材質陣列的圖例](images/d3d10-resource-texture2darray.png)

這個紋理包含三個紋理，每個紋理為 3x5 含兩個 Mipmap 層次。

### <a name="using-a-2d-texture-array-as-a-texture-cube"></a>使用 2D 紋理陣列做為立體紋理

紋理立方體是包含 6 個紋理的 2D 紋理陣列，每個立方體表面一個紋理。 完全填充的紋理立方體如下圖所示。

![代表材質 cube 之2d 材質陣列的圖例](images/d3d10-resource-texturecube.png)

包含 6 個紋理的 2D 紋理陣列，在使用立方體紋理視圖結合管線後，可使用立方體內建功能從著色器內讀取。 使用從紋理立方體中心指出的 3D 向量，從著色器處理紋理。

> [!Note]  
> 您使用 [**10 個 \_ 功能等級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) （含）以上建立的裝置可以支援材質 cube 的陣列，其中紋理數目等於陣列中的材質 cube 數目（以六為限）。 您使用 [**10 個 \_ 功能層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 建立的裝置僅支援六個臉部的單一紋理 cube。 此外，Direct3D 11 不支援部分 cubemaps。

 

### <a name="3d-textures"></a>3D 紋理

3D 紋理資源 (也稱為容體紋理) 包含 3D 紋理元素量。 因為是紋理資源，所以可會包含 mipmap 層次。 3D 紋理會以 [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) 介面表示。 完全填充的 3D 紋理外觀如下圖所示。

![3D 紋理資源的圖例](images/d3d10-resource-texture3d.png)

3D 紋理 Mipmap 切片繫結為描繪目標輸出 (描繪目標視圖) 時，3D 紋理行為等同於具 n 切片的 2D 紋理陣列。 您可以透過將輸出資料的純量元件宣告為 SV RenderTargetArrayIndex 系統值，從 [幾何著色器] 階段選擇特定轉譯配量 \_ 。

沒有 3D 紋理陣列概念，因此 3D 紋理子資源是單一 Mipmap 層次。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[紋理](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




