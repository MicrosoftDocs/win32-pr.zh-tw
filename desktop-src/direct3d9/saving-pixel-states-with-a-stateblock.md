---
description: 狀態欄塊可以用來只捕獲圖元狀態 (請參閱 (Direct3D 9) ) 的狀態欄塊儲存和還原狀態。
ms.assetid: 30624c0a-e30f-4383-bc0c-b43f42403e72
title: 以 StateBlock (Direct3D 9) 儲存圖元狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80741d9f17939d5795163a3e84c58bcdb9003c70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510258"
---
# <a name="saving-pixel-state-with-a-stateblock-direct3d-9"></a>以 StateBlock (Direct3D 9) 儲存圖元狀態

狀態欄塊只能用來捕捉圖元狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。 以下是圖元狀態：

-   圖元呈現狀態 (請參閱 [圖元管線：轉譯狀態](#pixel-pipeline-render-state)) 。
-   圖元材質狀態 (請參閱 [圖元管線：材質狀態](#pixel-pipeline-texture-state)) 。
-   圖元取樣器狀態 (請參閱 [圖元管線：取樣器狀態](#pixel-pipeline-sampler-state)) 。
-   目前的圖元著色器和每個圖元著色器常數。

若要使用狀態欄塊來捕捉圖元狀態，請 \_ 在呼叫 [**IDirect3DDevice9：： CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)時，指定 D3DSBT PIXELSTATE。

## <a name="pixel-pipeline-render-state"></a>圖元管線：轉譯狀態

裝置轉譯狀態會影響管線幾乎所有元件的行為。 藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)來設定轉譯狀態。

下表包含所有設定圖元狀態的呈現狀態：



| 轉譯狀態                              | 預設值      |
|--------------------------------------------|--------------------|
| D3DRS \_ ZENABLE                             | D3DZB \_ FALSE       |
| D3DRS \_ SPECULARENABLE                      | **FALSE**          |
| [**D3DFILLMODE**](./d3dfillmode.md)   | D3DFILL \_ 固態     |
| [**D3DSHADEMODE**](./d3dshademode.md) | D3DSHADE \_ GOURAUD  |
| D3DRS \_ ZWRITEENABLE                        | **TRUE**           |
| D3DRS \_ ALPHATESTENABLE                     | **FALSE**          |
| D3DRS \_ LASTPIXEL                           | **TRUE**           |
| D3DRS \_ SRCBLEND                            | D3DBLEND \_ 一      |
| D3DRS \_ DESTBLEND                           | D3DBLEND \_ 零     |
| D3DRS \_ ZFUNC                               | D3DCMP \_ LESSEQUAL  |
| D3DRS \_ ALPHAREF                            | 0                  |
| D3DRS \_ ALPHAFUNC                           | \_一律 D3DCMP     |
| D3DRS \_ DITHERENABLE                        | **FALSE**          |
| D3DRS \_ FOGSTART                            | 0                  |
| D3DRS \_ FOGEND                              | 1                  |
| D3DRS \_ FOGDENSITY                          | 1                  |
| D3DRS \_ ALPHABLENDENABLE                    | **FALSE**          |
| D3DRS \_ DEPTHBIAS                           | 0                  |
| D3DRS \_ STENCILENABLE                       | **FALSE**          |
| D3DRS \_ STENCILFAIL                         | D3DSTENCILOP \_ 保留 |
| D3DRS \_ STENCILZFAIL                        | D3DSTENCILOP \_ 保留 |
| D3DRS \_ STENCILPASS                         | D3DSTENCILOP \_ 保留 |
| D3DRS \_ STENCILFUNC                         | \_一律 D3DCMP     |
| D3DRS \_ STENCILREF                          | 0                  |
| D3DRS \_ STENCILMASK                         | 0xffffffff         |
| D3DRS \_ STENCILWRITEMASK                    | 0xffffffff         |
| D3DRS \_ TEXTUREFACTOR                       | 0xffffffff         |
| D3DRS \_ WRAP0                               | 0                  |
| D3DRS \_ WRAP1                               | 0                  |
| D3DRS \_ WRAP2                               | 0                  |
| D3DRS \_ WRAP3                               | 0                  |
| D3DRS \_ WRAP4                               | 0                  |
| D3DRS \_ WRAP5                               | 0                  |
| D3DRS \_ WRAP6                               | 0                  |
| D3DRS \_ WRAP7                               | 0                  |
| D3DRS \_ WRAP8                               | 0                  |
| D3DRS \_ WRAP9                               | 0                  |
| D3DRS \_ WRAP10                              | 0                  |
| D3DRS \_ WRAP11                              | 0                  |
| D3DRS \_ WRAP12                              | 0                  |
| D3DRS \_ WRAP13                              | 0                  |
| D3DRS \_ WRAP14                              | 0                  |
| D3DRS \_ WRAP15                              | 0                  |
| D3DRS \_ LOCALVIEWER                         | **TRUE**           |
| D3DRS \_ EMISSIVEMATERIALSOURCE              | D3DMCS \_ 材質   |
| D3DRS \_ AMBIENTMATERIALSOURCE               | D3DMCS \_ 材質   |
| D3DRS \_ DIFFUSEMATERIALSOURCE               | D3DMCS \_ COLOR1     |
| D3DRS \_ SPECULARMATERIALSOURCE              | D3DMCS \_ COLOR2     |
| D3DRS \_ COLORWRITEENABLE                    | 0x0000000f         |
| [**D3DBLENDOP**](./d3dblendop.md)     | D3DBLENDOP \_ 新增    |
| D3DRS \_ SCISSORTESTENABLE                   | **FALSE**          |
| D3DRS \_ SLOPESCALEDEPTHBIAS                 | 0                  |
| D3DRS \_ ANTIALIASEDLINEENABLE               | **FALSE**          |
| D3DRS \_ TWOSIDEDSTENCILMODE                 | **FALSE**          |
| D3DRS \_ CCW \_ STENCILFAIL                    | D3DSTENCILOP \_ 保留 |
| D3DRS \_ CCW \_ STENCILZFAIL                   | D3DSTENCILOP \_ 保留 |
| D3DRS \_ CCW \_ STENCILPASS                    | D3DSTENCILOP \_ 保留 |
| D3DRS \_ CCW \_ STENCILFUNC                    | \_一律 D3DCMP     |
| D3DRS \_ COLORWRITEENABLE1                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE2                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE3                   | 0x0000000f         |
| D3DRS \_ BLENDFACTOR                         | 0xffffffff         |
| D3DRS \_ SRGBWRITEENABLE                     | 0                  |
| D3DRS \_ SEPARATEALPHABLENDENABLE            | **FALSE**          |
| D3DRS \_ SRCBLENDALPHA                       | D3DBLEND \_ 一      |
| D3DRS \_ DESTBLENDALPHA                      | D3DBLEND \_ 零     |
| D3DRS \_ BLENDOPALPHA                        | D3DBLENDOP \_ 新增    |



 

## <a name="pixel-pipeline-sampler-state"></a>圖元管線：取樣器狀態

取樣器狀態會控制取樣的相關主題，例如篩選、平平貼圖和材質座標位址模式。 使用 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 來設定取樣器狀態 (包括鑲嵌單位中用來取樣置換地圖) 的狀態。 取樣器狀態已重新命名為 "D3DSAMP \_ " 前置詞，以在從 DirectX 8 移植時啟用編譯時期錯誤偵測。

下表包含所有設定圖元狀態的取樣器狀態：



| 取樣器狀態         | 預設值     |
|------------------------|-------------------|
| D3DSAMP \_ ADDRESSU      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ ADDRESSV      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ ADDRESSW      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ 邊框   | 0x00000000        |
| D3DSAMP \_ MAGFILTER     | D3DTEXF \_ 點    |
| D3DSAMP \_ MINFILTER     | D3DTEXF \_ 點    |
| D3DSAMP \_ MIPFILTER     | D3DTEXF \_ 無     |
| D3DSAMP \_ MIPMAPLODBIAS | 0                 |
| D3DSAMP \_ MAXMIPLEVEL   | 0                 |
| D3DSAMP \_ MAXANISOTROPY | 1                 |
| D3DSAMP \_ SRGBTEXTURE   | 0                 |
| D3DSAMP \_ ELEMENTINDEX  | 0                 |



 

## <a name="pixel-pipeline-texture-state"></a>圖元管線：材質狀態

材質狀態控制多紋理 blender 的材質混合作業。 使用 [**IDirect3DDevice9：： SetTextureStageState**](/windows/desktop/api) 來設定材質階段狀態。 使用 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 將材質與取樣器階段產生關聯。

下表包含所有設定圖元狀態的材質狀態：



| 材質狀態                | 預設值    |
|-------------------------------|------------------|
| D3DTSS \_ COLOROP               | D3DTOP \_ DISABLE  |
| D3DTSS \_ COLORARG1             | D3DTA \_ 材質   |
| D3DTSS \_ COLORARG2             | D3DTA \_ 目前   |
| D3DTSS \_ ALPHAOP               | D3DTOP \_ DISABLE  |
| D3DTSS \_ ALPHAARG1             | D3DTA \_ 材質   |
| D3DTSS \_ ALPHAARG2             | D3DTA \_ 目前   |
| D3DTSS \_ BUMPENVMAT00          | 0                |
| D3DTSS \_ BUMPENVMAT01          | 0                |
| D3DTSS \_ BUMPENVMAT10          | 0                |
| D3DTSS \_ BUMPENVMAT11          | 0                |
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| D3DTSS \_ BUMPENVLSCALE         | 0                |
| D3DTSS \_ BUMPENVLOFFSET        | 0                |
| D3DTSS \_ TEXTURETRANSFORMFLAGS | D3DTTFF \_ DISABLE |
| D3DTSS \_ COLORARG0             | D3DTA \_ 目前   |
| D3DTSS \_ ALPHAARG0             | D3DTA \_ 目前   |
| D3DTSS \_ RESULTARG             | D3DTA \_ 目前   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[狀態欄塊儲存與還原狀態](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
