---
description: 當燈光來源發亮時，會有發亮的物件，也就是使用高度反光材質的物件-接收高光。
ms.assetid: cea53131-1e2e-4389-80fd-ef5a0d068703
title: 地圖 (Direct3D 9) 的鏡面光
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05362eb4c0b79ebb980a6c0acb1607713765a446c0ef27823ae0e648cef88d68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026098"
---
# <a name="specular-light-maps-direct3d-9"></a>地圖 (Direct3D 9) 的鏡面光

當燈光來源發亮時，會有發亮的物件，也就是使用高度反光材質的物件-接收高光。 在某些情況下，光源模組所產生的反射醒目顯示不正確。 為了產生更吸引人的醒目提示，許多 Direct3D 應用程式都會將反射光線對應至基本專案。

若要執行反射光線對應，將反射光線對應新增至基本類型的紋理，然後調變（將結果乘以）RGB 光線對應。

下列程式碼範例將說明 c + + 中的這個程式。


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexSpecLightMap is a valid pointer to a texture that contains RGB
// specular light map data.
// lptexLightMap is a valid pointer to a texture that contains RGB
// light map data.

// Set the base texture.
d3dDevice->SetTexture(0, lptexBaseTexture );

// Set the base texture operation and arguments.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the specular light map.
d3dDevice->SetTexture(1, lptexSpecLightMap);

// Set the specular light map operation and args.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Set the RGB light map.
d3dDevice->SetTexture(2, lptexLightMap);

// Set the RGB light map operation and arguments.
d3dDevice->SetTextureStageState(2,D3DTSS_COLOROP, D3DTOP_MODULATE);
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用紋理的燈光對應](light-mapping-with-textures.md)
</dt> </dl>

 

 



