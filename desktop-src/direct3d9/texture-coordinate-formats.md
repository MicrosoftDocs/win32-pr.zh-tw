---
description: Direct3D 中的材質座標可以包含一個、兩個、三個或四個浮點數元素，以處理具有不同維度層級的材質。
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: " (Direct3D 9) 的材質座標格式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c48ec28b9c99357fe8825f5ff79da3c8869719389c4a4bc4874c5740fc71f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519881"
---
# <a name="texture-coordinate-formats-direct3d-9"></a> (Direct3D 9) 的材質座標格式

Direct3D 中的材質座標可以包含一個、兩個、三個或四個浮點數元素，以處理具有不同維度層級的材質。 一維材質-維度為1到 n 材質的材質介面，由一個材質座標定址。 最常見的案例（2D 材質）會使用兩個材質座標（通常稱為您和 v）來定址。 Direct3D 支援兩種類型的3D 紋理：三層環境對應和磁片區紋理。 三種環境對應不是真正的3D，但會使用3個元素的向量定址。 如需詳細資訊，請參閱 [ (Direct3D 9) 的三次環境對應 ](cubic-environment-mapping.md)。

如 [ (Direct3D 9) 的固定 ](fixed-function-fvf-codes.md)函式 FVF 程式碼中所述，應用程式會以頂點格式來編碼材質座標。 頂點格式可包含多組材質座標。 您可以使用 D3DFVF \_ TEX0，透過 D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) 來描述不含材質座標或最多8個集合的頂點格式。

每個材質座標集可以有一到四個元素。 D3DFVF \_ TEXTUREFORMAT1 到 D3DFVF \_ TEXTUREFORMAT4 旗標描述了集合中紋理座標內的元素數目，但這些旗標並不會單獨使用。 相反地， [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) 的巨集群組會使用這些旗標來建立位模式，以描述頂點格式的特定材質座標集合所使用的專案數目。 這些宏會接受單一參數，以識別要定義其元素數目之座標集的索引。 下列範例說明如何使用這些宏。


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> 除了立方環境對應和磁片區材質之外，rasterizers 無法使用兩個以上的元素來處理紋理。 應用程式可以針對材質座標提供最多三個元素，但只有在材質為立方體圖、磁片區材質或 D3DTTFF 投射的材質轉換旗標時才會 \_ 使用。 D3DTTFF \_ 投射旗標會讓轉譯器將前兩個元素除以第三個 (或 n 個) 元素。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質座標轉換 ](texture-coordinate-transformations.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質座標](texture-coordinates.md)
</dt> </dl>

 

 



