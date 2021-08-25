---
description: 磁片區材質是三維的圖元集合 (材質) ，可用來繪製二維琪本類型，例如三角形或線條。
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: " (Direct3D 9) 的音量材質資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17e72448fd1fd4856cf81a344f5c176fdb6272546468126975edbff8b20218d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984351"
---
# <a name="volume-texture-resources-direct3d-9"></a> (Direct3D 9) 的音量材質資源

磁片區材質是三維的圖元集合 (材質) ，可用來繪製二維琪本類型，例如三角形或線條。 需要三個元素的材質座標，才能以磁片區作為紋理的每個頂點。 繪製基本型別時，每個包含的圖元都會根據類似于二維材質案例的規則，填滿磁片區中某個圖元的色彩值。 磁片區不會直接轉譯，因為沒有可與其繪製的三維琪本專案。

您可以使用磁片區紋理來取得特殊效果，例如 patchy 霧化、爆炸等等。

磁片區會組織成配量，並可將寬度 x 高度2D 介面視為堆疊，以使寬度 x 高度 x 深度量。 每個配量都是單一資料列。 磁片區可以有後續層級，其中每個層級的維度會截斷為前一個層級的一半。 下圖顯示具有多個層級的音量材質看起來是什麼樣子。

![具有8x2x4、4x1x2 和 2x1x1 cube 標記法之磁片區材質的圖表](images/level123.png)

## <a name="creating-a-volume-texture"></a>建立磁片區材質

下列程式碼範例顯示使用磁片區材質所需的步驟。

首先，請針對每個頂點指定具有三個材質座標的自訂頂點型別，如下列程式碼範例所示。


```
struct VOLUMEVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu, tv, tw;
};

#define D3DFVF_VOLUMEVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|
                             D3DFVF_TEX1|D3DFVF_TEXCOORDSIZE3(0))
```



接下來，使用資料填滿頂點。


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



現在，建立頂點緩衝區，並將頂點中的資料填入其中。

下一步是使用 [**IDirect3DDevice9：： CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) 方法來建立磁片區材質，如下列程式碼範例所示。


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



轉譯原始物件之前，請先將目前材質設定為上面建立的音量材質。 下列程式碼範例會顯示一條三角形的整個轉譯程式。


```
if( SUCCEEDED( d3dDevice->BeginScene() ) )
{
    // Draw the quad, with the volume texture.
    d3dDevice->SetTexture( 0, pVolumeTexture );
    d3dDevice->SetFVF( D3DFVF_VOLUMEVERTEX );
    d3dDevice->SetStreamSource( 0, pVB, sizeof(VOLUMEVERTEX) );
    d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 2);

   // End the scene.
   d3dDevice->EndScene();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 紋理](direct3d-textures.md)
</dt> </dl>

 

 
