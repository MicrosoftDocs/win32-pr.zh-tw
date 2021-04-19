---
description: 效果狀態是用來初始化管線狀態，以準備頂點和圖元處理。
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: '效果狀態 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e208c0c7c14564a9967562ff2fd04a400cb7901
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314761"
---
# <a name="effect-states-direct3d-9"></a>效果狀態 (Direct3D 9) 

效果狀態是用來初始化管線狀態，以準備頂點和圖元處理。


```
effect state [ [index] ] = expression;
```



其中：

-   效果狀態-類似于傳統的固定函式管線狀態。 以下提供完整的狀態清單。
-   \[\[ \] 索引 \]-選擇性的整數索引。 索引會識別效果狀態陣列內的特定狀態。 外部括弧表示索引是選擇性的。 如果使用索引，請務必使用內部括弧。
-   運算式狀態指派運算式。 請參閱 [ (Direct3D 9) 的運算式 ](expressions.md)。

每個狀態都有原生資料類型。 這是當效果指派值時，狀態預期值的資料類型。 以下列出每個狀態所預期的資料類型。

請注意，效果介面會盡可能儘早地將值轉換成適當的類型。 常值可以在編譯時期轉換。 非常值 (亦即，當呼叫適當的 Set 方法時，) 需要轉換的一般變數。 例如，如有必要，效果介面會轉換使用 [**SetBool**](id3dxbaseeffect--setbool.md)、 [**SetValue**](id3dxbaseeffect--setvalue.md)和其他類似函式設定的值。 為了獲得更好的效能，請確定傳遞至效果介面的值已經是正確的類型，而且不需要轉換。 如果執行時間無法轉換值，則會傳回錯誤。

效果狀態可以分成下列類別：

-   [亮州](#light-states)
-   [材質狀態](#material-states)
-   [轉譯狀態](#render-states)
    -   [圖元管道呈現狀態](#pixel-pipe-render-states)
    -   [頂點管線呈現狀態](#vertex-pipe-render-states)
-   [取樣器狀態](#sampler-states)
-   [取樣器階段狀態](#sampler-stage-states)
-   [著色器狀態](#shader-states)
-   [著色器常數狀態](#shader-constant-states)
-   [材質狀態](#texture-states)
-   [材質階段狀態](#texture-stage-states)
-   [轉換狀態](#transform-states)

## <a name="light-states"></a>亮州

若要啟用效果的最佳效能，應該在效果檔案中指定燈光或材質的所有元件。 您無法宣告的狀態會設定為某個預設值，因為 Direct3D 無法個別設定燈的狀態。



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| 亮州            | 類型   | 值                                                                                                              |
| LightAmbient \[ n\]      | float4 | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的環境成員。                                                           |
| LightAttenuation0 \[ n\] | FLOAT  | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation0 成員。                                                      |
| LightAttenuation1 \[ n\] | FLOAT  | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation1 成員。                                                      |
| LightAttenuation2 \[ n\] | FLOAT  | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation2 成員。                                                      |
| LightDiffuse \[ n\]      | float4 | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的擴散成員。                                                           |
| LightDirection \[ n\]    | float3 | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的方向成員。                                                         |
| LightEnable \[ n\]       | bool   | **TRUE** 或 **FALSE**。 請參閱 [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)中的 bEnable 引數。            |
| LightFalloff \[ n\]      | FLOAT  | [**D3DCOLORVALUE**](d3dcolorvalue.md)。 請參閱 [**D3DLIGHT9**](d3dlight9.md)的衰減成員。                   |
| LightPhi \[ n\]          | FLOAT  | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Phi 成員。                                                               |
| LightPosition \[ n\]     | float3 | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的位置成員。                                                          |
| LightRange \[ n\]        | FLOAT  | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的範圍成員。                                                             |
| LightSpecular \[ n\]     | float4 | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的反射成員。                                                          |
| LightTheta \[ n\]        | FLOAT  | 請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Theta 成員。                                                             |
| LightType \[ n\]         | dword  | 與最多 n 個 [**D3DLIGHTTYPE**](./d3dlighttype.md) 值陣列相同的值，不含 D3DLIGHT \_ 前置詞。 |



 

範例：


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



這會啟用光源、將點光源設定為類型、將光線位置設定為 float3<10.0 f、1.0 f、23.0 f>，然後將環境色彩設定為 float4<0.7 f、0.0 f、0.0 f、1.0 f>。

## <a name="material-states"></a>材質狀態

因為 Direct3D 無法個別設定材質狀態，所以您無法宣告的狀態會設定為某些預設值。



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| 材質狀態   | 類型   | 值                                         |
| MaterialAmbient  | float4 | 與環境相同的值[ ](d3dmaterial9.md)  |
| >materialdiffuse  | float4 | 與漫射相同的值[ ](d3dmaterial9.md)  |
| MaterialEmissive | float4 | 與放射相同的值[ ](d3dmaterial9.md) |
| MaterialPower    | FLOAT  | 與電源相同的值[ ](d3dmaterial9.md)    |
| MaterialSpecular | float4 | 與反射的值相同[ ](d3dmaterial9.md) |



 

範例：


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



這會將擴散色彩設定為 float4<0.7 f、0.0 f、0.0 f、1.0 f>，並讓材質 3.0 f 的威力。

## <a name="render-states"></a>轉譯狀態

轉譯狀態有兩種類型：

-   [圖元管道呈現狀態](#pixel-pipe-render-states)
-   [頂點管線呈現狀態](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a>圖元管道呈現狀態

效果檔案轉譯狀態的名稱類似于固定函式管線狀態，通常會移除前置詞。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>轉譯狀態</td>
<td>類型</td>
<td>值</td>
</tr>
<tr class="even">
<td>AlphaBlendEnable</td>
<td>bool</td>
<td>是非題。 與 <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>中 D3DRS_ALPHABLENDENABLE 相同的值。</td>
</tr>
<tr class="odd">
<td>AlphaFunc</td>
<td>dword</td>
<td>與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。 請參閱 D3DRS_ALPHAFUNC。</td>
</tr>
<tr class="even">
<td>AlphaRef</td>
<td>dword</td>
<td>與 D3DRS_ALPHAREF 的值相同。</td>
</tr>
<tr class="odd">
<td>AlphaTestEnable</td>
<td>dword</td>
<td>是非題。 請參閱 D3DRS_ALPHATESTENABLE。</td>
</tr>
<tr class="even">
<td>BlendOp</td>
<td>dword</td>
<td>與沒有 D3DBLENDOP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> 相同的值。</td>
</tr>
<tr class="odd">
<td>ColorWriteEnable</td>
<td>dword</td>
<td>紅色的位元組合 |綠色 |藍色 |阿 爾 法。 請參閱 D3DRS_COLORWRITEENABLE。</td>
</tr>
<tr class="even">
<td>DepthBias</td>
<td>FLOAT</td>
<td>與 D3DRS_DEPTHBIAS 的值相同。</td>
</tr>
<tr class="odd">
<td>DestBlend</td>
<td>dword</td>
<td>與沒有 D3DBLEND_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> 相同的值。</td>
</tr>
<tr class="even">
<td>DitherEnable</td>
<td>bool</td>
<td>是非題。 與 D3DRS_DITHERENABLE 的值相同。</td>
</tr>
<tr class="odd">
<td>FillMode</td>
<td>dword</td>
<td>與沒有 D3DFILL_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> 相同的值。</td>
</tr>
<tr class="even">
<td>LastPixel</td>
<td>dword</td>
<td>是非題。 請參閱 D3DRS_LASTPIXEL。</td>
</tr>
<tr class="odd">
<td>ShadeMode</td>
<td>dword</td>
<td>與沒有 D3DSHADE_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> 相同的值。</td>
</tr>
<tr class="even">
<td>SlopeScaleDepthBias</td>
<td>FLOAT</td>
<td>與 D3DRS_SLOPESCALEDEPTHBIAS 的值相同。</td>
</tr>
<tr class="odd">
<td>SrcBlend</td>
<td>dword</td>
<td>與沒有 D3DBLEND_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> 相同的值。</td>
</tr>
<tr class="even">
<td>SRGBWriteEnable</td>
<td>bool</td>
<td>是非題。 與 D3DRS_SRGBWRITEENABLE 的值相同。</td>
</tr>
<tr class="odd">
<td>StencilEnable</td>
<td>bool</td>
<td>是非題。 與 D3DRS_STENCILENABLE 的值相同。</td>
</tr>
<tr class="even">
<td>StencilFail</td>
<td>dword</td>
<td>與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。 請參閱 D3DRS_STENCILFAIL。</td>
</tr>
<tr class="odd">
<td>StencilFunc</td>
<td>dword</td>
<td>與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。 請參閱 D3DRS_STENCILFUNC。</td>
</tr>
<tr class="even">
<td>StencilMask</td>
<td>dword</td>
<td>與 D3DRS_STENCILMASK 的值相同。</td>
</tr>
<tr class="odd">
<td>StencilPass</td>
<td>dword</td>
<td>與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。 請參閱 D3DRS_STENCILPASS。</td>
</tr>
<tr class="even">
<td>StencilRef</td>
<td>int</td>
<td>與 D3DRS_STENCILREF 的值相同。</td>
</tr>
<tr class="odd">
<td>StencilWriteMask</td>
<td>dword</td>
<td>與 D3DRS_STENCILWRITEMASK 的值相同。</td>
</tr>
<tr class="even">
<td>StencilZFail</td>
<td>dword</td>
<td>與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。 請參閱 D3DRS_STENCILZFAIL。</td>
</tr>
<tr class="odd">
<td>TextureFactor</td>
<td>dword</td>
<td>與 <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>相同的值。 與 D3DRS_TEXTUREFACTOR 的值相同。</td>
</tr>
<tr class="even">
<td>Wrap0 - Wrap15</td>
<td>dword</td>
<td>值與 D3DRS_WRAP0 所使用的值相同。 有效值為：
<ul>
<li>對應至 D3DWRAPCOORD_0 的 COORD0 () </li>
<li>對應至 D3DWRAPCOORD_1 的 COORD1 () </li>
<li>對應至 D3DWRAPCOORD_2 的 COORD2 () </li>
<li>對應至 D3DWRAPCOORD_3 的 COORD3 () </li>
<li>U (對應至 D3DWRAP_U) </li>
<li>對應至 D3DWRAP_V 的 V () </li>
<li>對應至 D3DWRAP_W 的 W () </li>
</ul></td>
</tr>
<tr class="odd">
<td>ZEnable</td>
<td>dword</td>
<td>與沒有 D3DZB_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> 相同的值。</td>
</tr>
<tr class="even">
<td>ZFunc</td>
<td>dword</td>
<td>與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。 請參閱 D3DRS_ZFUNC。</td>
</tr>
<tr class="odd">
<td>ZWriteEnable</td>
<td>bool</td>
<td>是非題。 請參閱 D3DRS_ZWRITEENABLE。</td>
</tr>
</tbody>
</table>



 

範例：


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



這會啟用 Alpha 混色，並讓所有幾何以線框呈現。

### <a name="vertex-pipe-render-states"></a>頂點管線呈現狀態

效果檔案轉譯狀態的名稱類似于固定函式管線狀態，通常會移除前置詞。



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 轉譯狀態             | 類型   | 值                                                                                                                                        |
| 環境                  | float4 | 與 D3DRS 環境相同的值 \_ 。                                                                                                                |
| AmbientMaterialSource    | dword  | 與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。 請參閱 D3DRS \_ AMBIENTMATERIALSOURCE。  |
| 裁剪                 | bool   | 是非題。 與 D3DRS 裁剪相同的值 \_ 。                                                                                                |
| ClipPlaneEnable          | dword  | D3DCLIPPLANE0-D3DCLIPPLANE5 宏的位元組合。 請參閱 [**D3DCLIPPLANEn**](d3dclipplanen.md) 和 D3DRS \_ CLIPPLANEENABLE。           |
| ColorVertex              | bool   | 是非題。 與 D3DRS COLORVERTEX 相同的值 \_ 。                                                                                             |
| CullMode                 | dword  | 與沒有 D3DCULL 前置詞的 [**D3DCULL**](./d3dcull.md) 相同的值 \_ 。                                                                 |
| DiffuseMaterialSource    | dword  | 與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。 請參閱 D3DRS \_ DIFFUSEMATERIALSOURCE。  |
| EmissiveMaterialSource   | dword  | 與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。 請參閱 D3DRS \_ EMISSIVEMATERIALSOURCE。 |
| FogColor                 | dword  | 與 [**D3DCOLOR**](d3dcolor.md)相同的值。 請參閱 D3DRS \_ FOGCOLOR。                                                                             |
| FogDensity               | FLOAT  | 與 D3DRS FOGDENSITY 相同的值 \_ 。                                                                                                             |
| FogEnable                | bool   | 是非題。 與 D3DRS FOGENABLE 相同的值 \_ 。                                                                                               |
| FogEnd                   | FLOAT  | 與 D3DRS FOGEND 相同的值 \_ 。                                                                                                                 |
| FogStart                 | FLOAT  | 與 D3DRS FOGSTART 相同的值 \_ 。                                                                                                               |
| FogTableMode             | dword  | 與 [**D3DFOGMODE**](./d3dfogmode.md)相同的值。 請參閱 \_ [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)中的 D3DRS FOGTABLEMODE。     |
| FogVertexMode            | dword  | 與沒有 D3DFOG 前置詞的 [**D3DFOGMODE**](./d3dfogmode.md) 相同的值 \_ 。                                                            |
| IndexedVertexBlendEnable | bool   | 是非題。 與 D3DRS INDEXEDVERTEXBLENDENABLE 相同的值 \_ 。                                                                                |
| 光源                 | bool   | 是非題。 與 D3DRS 光源相同的值 \_ 。                                                                                                |
| LocalViewer              | bool   | 是非題。 與 D3DRS LOCALVIEWER 相同的值 \_ 。                                                                                             |
| MultiSampleAntialias     | bool   | 與 D3DRS MULTISAMPLEANTIALIAS 相同的值 \_ 。                                                                                                   |
| MultiSampleMask          | dword  | 與 D3DRS MULTISAMPLEMASK 相同的值 \_ 。                                                                                                        |
| NormalizeNormals         | bool   | 是非題。 與 D3DRS NORMALIZENORMALS 相同的值 \_ 。                                                                                        |
| PatchSegments            | FLOAT  | 與 [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)中的 nSegments 相同的值。                                                         |
| PointScale \_            | FLOAT  | 與 D3DRS \_ POINTSCALE A 相同 \_ 的值。                                                                                                          |
| PointScale \_ B            | FLOAT  | 與 D3DRS POINTSCALE B 相同的值 \_ \_ 。                                                                                                          |
| PointScale \_ C            | FLOAT  | 與 D3DRS POINTSCALE C 相同的值 \_ \_ 。                                                                                                          |
| PointScaleEnable         | bool   | 與 D3DRS POINTSCALEENABLE 相同的值 \_ 。                                                                                                       |
| Dialog                | FLOAT  | 與 D3DRS dialog 相同的值 \_ 。                                                                                                              |
| Dialog \_ 分鐘           | FLOAT  | 與 D3DRS dialog MIN 相同的值 \_ \_ 。                                                                                                         |
| Dialog \_ Max           | FLOAT  | 與 D3DRS \_ dialog MAX 相同 \_ 的值，不含 D3DRS \_ 前置詞。                                                                              |
| PointSpriteEnable        | bool   | 是非題。 與 D3DRS POINTSPRITEENABLE 相同的值 \_ 。                                                                                       |
| RangeFogEnable           | bool   | 是非題。 與 D3DRS RANGEFOGENABLE 相同的值 \_ 。                                                                                          |
| SpecularEnable           | bool   | 是非題。 與 D3DRS SPECULARENABLE 相同的值 \_ 。                                                                                          |
| SpecularMaterialSource   | dword  | 與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。 請參閱 D3DRS \_ SPECULARMATERIALSOURCE。 |
| TweenFactor              | FLOAT  | 與 D3DRS TWEENFACTOR 相同的值 \_ 。                                                                                                            |
| VertexBlend              | dword  | 與沒有 D3DVBF 前置詞的 [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 相同的值 \_ 。 請參閱 D3DRS \_ VERTEXBLEND。                  |



 

範例：


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



這會使環境色彩 float4<0.7 f、0.0 f、0.0 f、1.0 f>、將背面剔除模式設定為逆時針方向，並將 [霧化色彩] 設定為紅色。

## <a name="sampler-states"></a>取樣器狀態

取樣器狀態代表取樣器物件。



|         |         |                                     |
|---------|---------|-------------------------------------|
| 狀態   | 類型    | 值                              |
| 取樣器 | 採樣 | **Null** 或取樣器狀態欄塊。 |



 

## <a name="sampler-stage-states"></a>取樣器階段狀態

取樣器階段狀態是用來取樣紋理。 取樣器狀態決定篩選類型和材質定址模式。



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 取樣器狀態       | 類型                         | 值                                                                                                                            |
| AddressU \[ 16\]      | dword                        | 與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。 請參閱 D3DSAMP \_ ADDRESSU。      |
| AddressV \[ 16\]      | dword                        | 與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。 請參閱 D3DSAMP \_ ADDRESSV。      |
| AddressW \[ 16\]      | dword                        | 與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。 請參閱 D3DSAMP \_ ADDRESSW。      |
| 邊框 \[ 16\]   | [**D3DCOLOR**](d3dcolor.md) | 與沒有 D3DTEXF 前置詞的 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 相同的值 \_ 。 請參閱 D3DSAMP \_ 邊框出。 |
| MagFilter \[ 16\]     | dword                        | 與沒有 D3DTEXF 前置詞的 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 相同的值 \_ 。 請參閱 D3DSAMP \_ MAGFILTER。   |
| MaxAnisotropy \[ 16\] | dword                        | 與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MAXANISOTROPY 相同的值 \_ 。                                                               |
| MaxMipLevel \[ 16\]   | int                          | 與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MAXMIPLEVEL 相同的值 \_ 。                                                                 |
| MinFilter \[ 16\]     | dword                        | 與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MINFILTER 相同的值 \_ 。                                                                   |
| MipFilter \[ 16\]     | dword                        | 與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MIPFILTER 相同的值 \_ 。                                                                   |
| MipMapLodBias \[ 16\] | FLOAT                        | 與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MIPMAPLODBIAS 相同的值 \_ 。                                                               |
| SRGBTexture         | bool                         | 與 D3DSAMP SRGBTEXTURE 的值相同， \_ 不含 D3DSAMP \_ 前置詞。                                                                   |



 

範例：


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



這個個會 UVW 值介於0和1之間。

## <a name="shader-states"></a>著色器狀態

只有兩種效果著色器狀態：一個與頂點著色器物件相關聯，另一個與圖元著色器物件相關聯。



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| 著色器狀態 | 類型         | 值                                                                      |
| 無效  | 無效  | **Null**、元件區塊、編譯目標或圖元著色器參數。 |
| VertexShader | vertexshader | **Null**、元件區塊、編譯目標或圖元著色器參數。 |



 

範例：


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



這會將 VSTexture （稍早在 fx 檔案中定義的頂點著色器）編譯為頂點著色器1.1 版，然後將該編譯的著色器設定為頂點著色器。 圖元著色器會指派給 **Null**。

## <a name="shader-constant-states"></a>著色器常數狀態

著色器常數狀態可用來存取著色器常數參數。



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| 著色器常數狀態 | 類型            | 值                                       |
| PixelShaderConstant   | float \[ m \[ n\]\] | m x n 浮點數的陣列;m 和 n 是選擇性的。 |
| PixelShaderConstant1  | float4          | 一個4D 浮點數。                                |
| PixelShaderConstant2  | float4x2        | 兩個4D 浮點數。                               |
| PixelShaderConstant3  | float4x3        | 三個4D 浮點數。                             |
| PixelShaderConstant4  | float4x4        | 四個4D 浮點數。                              |
| PixelShaderConstantB  | bool \[ m \[ n\]\]  | m x n bool 的陣列;m 和 n 是選擇性的。  |
| PixelShaderConstantI  | int \[ m \[ n\]\]   | m x n 的整數陣列。 m 和 n 是選擇性的。   |
| PixelShaderConstantF  | float \[ m \[ n\]\] | m x n 浮點數陣列。 m 和 n 是選擇性的。 |
| VertexShaderConstant  | float \[ m \[ n\]\] | m x n 浮點數陣列。 m 和 n 是選擇性的。 |
| VertexShaderConstant1 | float4          | 一個4D 浮點數。                                |
| VertexShaderConstant2 | float4x2        | 兩個4D 浮點數。                               |
| VertexShaderConstant3 | float4x3        | 三個4D 浮點數。                             |
| VertexShaderConstant4 | float4x4        | 四個4D 浮點數。                              |
| VertexShaderConstantB | bool \[ m \[ n\]\]  | m x n bool 陣列。 m 和 n 是選擇性的。  |
| VertexShaderConstantI | int \[ m \[ n\]\]   | m x n 的整數陣列。 m 和 n 是選擇性的。   |
| VertexShaderConstantF | float \[ m \[ n\]\] | m x n 浮點數陣列。 m 和 n 是選擇性的。 |



 

## <a name="texture-states"></a>材質狀態

材質狀態會初始化多紋理 blender 所使用的材質。



|               |         |                                   |
|---------------|---------|-----------------------------------|
| 材質狀態 | 類型    | 值                            |
| 材質 \[ 8\]  | 紋理 | **Null** 或紋理參數。 |



 

## <a name="texture-stage-states"></a>材質階段狀態

材質階段狀態會設定多紋理 blender 中的材質和紋理階段。



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 材質階段狀態        | 類型  | 值                                                                                                                                                    |
| AlphaOp \[ 8\]               | dword | 與沒有 D3DTOP 前置詞的 [**D3DTEXTUREOP**](./d3dtextureop.md) 相同 \_ 。 請參閱 D3DTSS \_ ALPHAOP。                                                      |
| AlphaArg0 \[ 8\]             | dword | 與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。 請參閱 D3DTSS \_ ALPHAARG0。                                                                             |
| AlphaArg1 \[ 8\]             | dword | 與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。 請參閱 D3DTSS \_ ALPHAARG1。                                                                             |
| AlphaArg2 \[ 8\]             | dword | 與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。 請參閱 D3DTSS \_ ALPHAARG2。                                                                             |
| ColorArg0 \[ 8\]             | dword | 與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。 請參閱 D3DTSS \_ COLORARG0。                                                                             |
| ColorArg1 \[ 8\]             | dword | 與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。 請參閱 D3DTSS \_ COLORARG1。                                                                             |
| ColorArg2 \[ 8\]             | dword | 與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。 請參閱 D3DTSS \_ COLORARG2。                                                                             |
| ColorOp \[ 8\]               | dword | 與沒有 D3DTOP 前置詞的 [**D3DTEXTUREOP**](./d3dtextureop.md) 相同 \_ 。 請參閱 D3DTSS \_ COLOROP。                                                      |
| BumpEnvLScale \[ 8\]         | FLOAT | 與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS BUMPENVLSCALE 相同的值 \_ 。                                                                                      |
| BumpEnvLOffset \[ 8\]        | FLOAT | 與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS BUMPENVLOFFSET 相同的值 \_ 。                                                                                     |
| BumpEnvMat00 \[ 8\]          | FLOAT | 與 D3DTSS BUMPENVMAT00 相同的值 \_ 。                                                                                                                      |
| BumpEnvMat01 \[ 8\]          | FLOAT | 與 D3DTSS BUMPENVMAT01 相同的值 \_ 。                                                                                                                      |
| BumpEnvMat10 \[ 8\]          | FLOAT | 與 D3DTSS BUMPENVMAT10 相同的值 \_ 。                                                                                                                      |
| BumpEnvMat11 \[ 8\]          | FLOAT | 與 D3DTSS BUMPENVMAT11 相同的值 \_ 。                                                                                                                      |
| ResultArg \[ 8\]             | dword | 與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。 請參閱 D3DTSS \_ RESULTARG。                                                                             |
| TexCoordIndex \[ 8\]         | dword | 與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS TEXCOORDINDEX 相同的值 \_ 。                                                                                      |
| TextureTransformFlags \[ 8\] | dword | 與沒有 D3DTTFF 前置詞的 [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) 值相同的值 \_ 。 請參閱 D3DTSS \_ TEXTURETRANSFORMFLAGS。 |



 

## <a name="transform-states"></a>轉換狀態

設定轉換狀態以初始化轉換矩陣。 效果會使用已轉置的矩陣來提高效率。 您可以將已轉換的矩陣提供給效果，或在使用矩陣之前自動變換矩陣。



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| 轉換狀態       | 類型     | 值                                                                                                                          |
| ProjectionTransform   | float4x4 | 浮點數的4x4 矩陣。 與 \_ 沒有 D3DTS 前置詞的 D3DTS 投射相同的值 \_ 。                                            |
| TextureTransform \[ 8\] | float4x4 | 浮點數的4x4 矩陣。 與沒有 D3DTS 前置詞的 [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) 相同的值 \_ 。 |
| ViewTransform         | float4x4 | 浮點數的4x4 矩陣。 D3DTS \_ VIEW 與沒有 D3DTS 前置詞的值相同 \_ 。                                                  |
| WorldTransform        | float4x4 | 浮點數的4x4 矩陣。                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
