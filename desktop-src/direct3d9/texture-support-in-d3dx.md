---
description: 深入瞭解 D3DX 中的材質支援。 D3DX 是提供 helper 服務的公用程式庫。 它是 Direct3D 元件之上的一層。
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: 'D3DX 中的材質支援 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ba518a5e9158c0337d45485852675d4ab91ef3585f027bd78fc51164c40466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026018"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a>D3DX 中的材質支援 (Direct3D 9) 

D3DX 是提供 helper 服務的公用程式庫。 它是 Direct3D 元件之上的一層。

## <a name="textures"></a>紋理

下列主題支援許多不同的材質。

-   標準 mipmapped 材質支援。 請參閱 [自動產生 mipmap (Direct3D 9) ](automatic-generation-of-mipmaps.md)。
-   Cube 地圖支援。 請參閱 [ (Direct3D 9) 的三次環境對應 ](cubic-environment-mapping.md)。
-   磁片區材質支援。 請參閱 [ (Direct3D 9) 的音量材質資源 ](volume-texture-resources.md)。
-   環境對應支援。 請參閱 [ (Direct3D 9) 的環境對應 ](environment-mapping.md)。
-   凹凸對應支援。 請參閱 [ (Direct3D 9) 的 [凹凸對應 ](bump-mapping.md)]。

### <a name="texture-color-conversion"></a>材質色彩轉換

使用任何 D3DXLoadSurfacexxx、D3DXLoadVolumexxx、D3DXCreateTexturexxx、D3DXCreateCubeTexturexxx 或 D3DXCreateVolumeTexturexxx 函數時，可能需要執行色彩轉換。 例如，一個介面可能是 RGBA 類型，另一個則可能是 UVWQ。 針對不同格式的案例，轉換順序如下所示：

### <a name="mapping-rgba-to-uvwq"></a>將 RGBA 對應至 UVWQ

-   R <-> U，R 通道會對應至 U 通道，反之亦然。
-   G <-> V、G 通道會對應至 V 通道，反之亦然。
-   B <-> W，B 通道會對應至 W 通道，反之亦然。
-   < > Q/L，通道會對應至 Q 或 L 通道 (，視目的地格式的可用版本) ，反之亦然。


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a>將 UV 對應到 RGBA

-   U <-> R、U 通道會對應至 R 通道，反之亦然。
-   V <-> G，V 通道會對應至 G 通道，反之亦然。
-   1 <-> B，1對應至 B 通道，反之亦然。
-   1 <-> A、1對應至通道，反之亦然。

如果來源中沒有一個通道，則會假設為 1 (但 A8 除外，其中 R、G、B 假設為 0) 。 例如：


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



