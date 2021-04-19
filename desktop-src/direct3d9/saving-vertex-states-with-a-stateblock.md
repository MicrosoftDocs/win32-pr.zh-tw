---
description: 狀態欄塊只能用來捕捉頂點狀態 (請參閱 (Direct3D 9) ) 的狀態欄塊儲存和還原狀態。
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: 以 StateBlock (Direct3D 9) 儲存頂點狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970901"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a>以 StateBlock (Direct3D 9) 儲存頂點狀態

狀態欄塊只能用來捕捉頂點狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。 下列狀態為頂點狀態：

-   頂點呈現狀態 (請參閱 [頂點管線：轉譯狀態](#vertex-pipeline-render-state)) 。
-   頂點取樣器狀態 (請參閱 [頂點管線：取樣器狀態](#vertex-pipeline-sampler-state)) 。
-   頂點材質狀態 (請參閱 [頂點管線：材質狀態](#vertex-pipeline-texture-state)) 。
-   來自 [**IDirect3DDevice9：： SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)的 NPatch 模式區段。
-   [**IDirect3DDevice9：： SetLight**](/windows/desktop/api)的每個光線，以及是否使用 [**IDirect3DDevice9：： LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)來啟用光線。
-   目前的頂點著色器和每個頂點著色器常數。
-   針對每個頂點資料流程，儲存 [**IDirect3DDevice9：： SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq)的分隔值。
-   目前的頂點宣告。

若要使用狀態欄塊來捕捉頂點狀態，請 \_ 在呼叫 [**IDirect3DDevice9：： CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)時，指定 D3DSBT VERTEXSTATE。

## <a name="vertex-pipeline-render-state"></a>頂點管線：轉譯狀態

裝置轉譯狀態會影響管線幾乎所有元件的行為。 藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)來設定轉譯狀態。

下表包含設定頂點狀態的所有呈現狀態：



| 轉譯狀態                           | 預設值          |
|-----------------------------------------|------------------------|
| D3DRS \_ CULLMODE                         | D3DCULL \_ CCW           |
| D3DRS \_ FOGCOLOR                         | 0                      |
| D3DRS \_ FOGTABLEMODE                     | D3DFOG \_ 無           |
| D3DRS \_ FOGSTART                         | 0                      |
| D3DRS \_ FOGEND                           | 1                      |
| D3DRS \_ FOGDENSITY                       | 1                      |
| D3DRS \_ RANGEFOGENABLE                   | **FALSE**              |
| D3DRS \_ 環境                          | 0                      |
| D3DRS \_ COLORVERTEX                      | **TRUE**               |
| D3DRS \_ FOGVERTEXMODE                    | D3DFOG \_ 無           |
| D3DRS \_ 剪切                         | **TRUE**               |
| D3DRS \_ 光源                         | **TRUE**               |
| D3DRS \_ LOCALVIEWER                      | **TRUE**               |
| D3DRS \_ EMISSIVEMATERIALSOURCE           | D3DMCS \_ 材質       |
| D3DRS \_ AMBIENTMATERIALSOURCE            | D3DMCS \_ 材質       |
| D3DRS \_ DIFFUSEMATERIALSOURCE            | D3DMCS \_ COLOR1         |
| D3DRS \_ SPECULARMATERIALSOURCE           | D3DMCS \_ COLOR2         |
| D3DRS \_ VERTEXBLEND                      | D3DVBF \_ DISABLE        |
| D3DRS \_ CLIPPLANEENABLE                  | 0                      |
| D3DRS \_ dialog                        | 驅動程式相依       |
| D3DRS \_ dialog \_ MIN                   | 1                      |
| D3DRS \_ POINTSPRITEENABLE                | **FALSE**              |
| D3DRS \_ POINTSCALEENABLE                 | **FALSE**              |
| D3DRS \_ POINTSCALE \_                    | 1                      |
| D3DRS \_ POINTSCALE \_ B                    | 0                      |
| D3DRS \_ POINTSCALE \_ C                    | 0                      |
| D3DRS \_ MULTISAMPLEANTIALIAS             | **TRUE**               |
| D3DRS \_ MULTISAMPLEMASK                  | 0xffffffff             |
| D3DRS \_ PATCHEDGESTYLE                   | D3DPATCHEDGE \_ 離散 |
| D3DRS \_ dialog \_ MAX                   | 1                      |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE         | **FALSE**              |
| D3DRS \_ TWEENFACTOR                      | 0                      |
| D3DRS \_ POSITIONDEGREE                   | D3DDEGREE \_ 立方       |
| D3DRS \_ NORMALDEGREE                     | D3DDEGREE \_ 線性      |
| D3DRS \_ MINTESSELLATIONLEVEL             | 1                      |
| D3DRS \_ MAXTESSELLATIONLEVEL             | 1                      |
| D3DRS \_ ADAPTIVETESS \_ X                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Y                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Z                  | 1                      |
| D3DRS \_ ADAPTIVETESS \_ W                  | 0                      |
| D3DRS \_ ENABLEADAPTIVETESSELLATION "/> | **FALSE**              |



 

## <a name="vertex-pipeline-sampler-state"></a>頂點管線：取樣器狀態

取樣器狀態會控制取樣的相關主題，例如篩選、平平貼圖和材質座標位址模式。 使用 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 來設定取樣器狀態 (包括鑲嵌單位中用來取樣置換地圖) 的狀態。 取樣器狀態已重新命名為 "D3DSAMP \_ " 前置詞，以在從 DirectX 8 移植時啟用編譯時期錯誤偵測。

下表包含所有設定頂點狀態的取樣器狀態：



| 取樣器狀態      | 預設值 |
|---------------------|---------------|
| D3DSAMP \_ DMAPOFFSET | 256           |



 

## <a name="vertex-pipeline-texture-state"></a>頂點管線：材質狀態

材質狀態控制多紋理 blender 的材質混合作業。 使用 [**IDirect3DDevice9：： SetTextureStageState**](/windows/desktop/api) 來設定材質狀態。 使用 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 將材質與取樣器階段產生關聯。

下表包含所有設定頂點狀態的材質狀態：



| 材質狀態                | 預設值    |
|-------------------------------|------------------|
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| D3DTSS \_ TEXTURETRANSFORMFLAGS | D3DTTFF \_ DISABLE |



 

D3DTSS \_ TEXCOORDINDEX 是固定的函式頂點處理狀態。 如果使用可程式化的頂點著色器，則會忽略此狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[狀態欄塊儲存與還原狀態](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
