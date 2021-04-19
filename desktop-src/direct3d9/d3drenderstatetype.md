---
description: 轉譯狀態會定義各種頂點和圖元處理的設定狀態。
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: 'D3DRENDERSTATETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2386762eaa45f1eefbccac97723c3ad71c3a76fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974845"
---
# <a name="d3drenderstatetype-enumeration"></a>D3DRENDERSTATETYPE 列舉

轉譯狀態會定義各種頂點和圖元處理的設定狀態。 某些轉譯狀態會設定頂點處理，而某些設定圖元處理 (查看 [ (Direct3D 9) ](render-states.md)) 的轉譯狀態。 您可以使用 stateblocks 來儲存和還原轉譯狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**
</dt> <dd>

深度緩衝處理狀態，作為 [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) 列舉型別的其中一個成員。 將此狀態設定為 D3DZB \_ TRUE，以啟用 z 緩衝、D3DZB \_ USEW 來啟用 w 緩衝，或 D3DZB \_ FALSE 以停用深度緩衝。

\_如果已將 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)結構的 EnableAutoDepthStencil 成員設為 **TRUE**，則此呈現狀態的預設值為 D3DZB TRUE， \_ 否則為 FALSE。

</dd> <dt>

<span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**
</dt> <dd>

[**D3DFILLMODE**](./d3dfillmode.md)列舉型別的一或多個成員。 預設值為 D3DFILL \_ 固態。

</dd> <dt>

<span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**
</dt> <dd>

[**D3DSHADEMODE**](./d3dshademode.md)列舉型別的一或多個成員。 預設值為 D3DSHADE \_ GOURAUD。

</dd> <dt>

<span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**
</dt> <dd>

**TRUE** 表示讓應用程式寫入深度緩衝區。 預設值為 **TRUE**。 此成員可讓應用程式防止系統以新的深度值更新深度緩衝區。 如果 **為 FALSE**，則會根據轉譯狀態 D3DRS \_ ZFUNC （假設深度緩衝處理已發生）進行深度比較，但不會將深度值寫入緩衝區。

</dd> <dt>

<span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**
</dt> <dd>

**TRUE** 表示啟用每圖元 Alpha 測試。 如果測試通過，則會由框架緩衝區來處理圖元。 否則，就會略過圖元的所有框架緩衝區處理。

使用 D3DRS ALPHAFUNC 轉譯狀態所提供的比較函式，藉由比較輸入的 Alpha 值與參考 Alpha 值來完成測試 \_ 。 參考 Alpha 值是由針對 D3DRS ALPHAREF 所設定的值所決定 \_ 。 如需詳細資訊，請參閱 [ (Direct3D 9 的 Alpha 測試狀態) ](alpha-testing-state.md)。

此參數的預設值為 **FALSE**。

</dd> <dt>

<span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**
</dt> <dd>

預設值為 **TRUE**，可讓您繪製線條中的最後一個圖元。 若要防止繪製最後一個圖元，請將此值設定為 **FALSE**。 如需詳細資訊，請參閱 [ (Direct3D 9) 的大綱和填滿狀態 ](outline-and-fill-state.md)。

</dd> <dt>

<span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**
</dt> <dd>

[**D3DBLEND**](./d3dblend.md)列舉型別的其中一個成員。 預設值為 D3DBLEND \_ 一個。

</dd> <dt>

<span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**
</dt> <dd>

[**D3DBLEND**](./d3dblend.md)列舉型別的其中一個成員。 預設值為 D3DBLEND \_ 零。

</dd> <dt>

<span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**
</dt> <dd>

指定回溯三角形的挑選方式（如果有的話）。 這可以設定為 [**D3DCULL**](./d3dcull.md) 列舉型別的其中一個成員。 預設值為 D3DCULL \_ CCW。

</dd> <dt>

<span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ ZFUNC**
</dt> <dd>

[**D3DCMPFUNC**](./d3dcmpfunc.md)列舉型別的其中一個成員。 預設值為 D3DCMP \_ LESSEQUAL。 此成員可讓應用程式根據與相機之間的距離來接受或拒絕圖元。

圖元的深度值會與深度緩衝區值進行比較。 如果圖元的深度值通過比較函數，則會寫入圖元。

只有當轉譯狀態為 **TRUE** 時，才會將 depth 值寫入深度緩衝區。

如果深度測試失敗，軟體 rasterizers 和許多硬體加速器的運作速度會更快，因為不需要在圖元呈現時篩選和 lambert 材質。

</dd> <dt>

<span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**
</dt> <dd>

值，指定在啟用 Alpha 測試時測試圖元的參考 Alpha 值。 這是8位值，放在 DWORD 轉譯狀態值的低8位中。 值的範圍可以從0x00000000 到0x000000FF。 預設值為 0。

</dd> <dt>

<span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**
</dt> <dd>

[**D3DCMPFUNC**](./d3dcmpfunc.md)列舉型別的其中一個成員。 預設值為 [永遠 D3DCMP] \_ 。 此成員可讓應用程式根據其 Alpha 值來接受或拒絕圖元。

</dd> <dt>

<span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**
</dt> <dd>

**TRUE** 表示啟用遞色。 預設值為 **FALSE**。

</dd> <dt>

<span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**
</dt> <dd>

**TRUE** 表示啟用 Alpha 混合透明度。 預設值為 **FALSE**。

Alpha 混色的類型取決於 D3DRS \_ SRCBLEND 和 D3DRS \_ DESTBLEND 轉譯狀態。

</dd> <dt>

<span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ FOGENABLE**
</dt> <dd>

**TRUE** 表示啟用霧化混色。 預設值為 **FALSE**。 如需使用霧化混合的詳細資訊，請參閱 [霧化](fog.md)。

</dd> <dt>

<span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**
</dt> <dd>

**TRUE** 表示啟用高光。 預設值為 **FALSE**。

高光的計算方式，就像物件的每個頂點都在物件的原點一樣。 只要物件是以原點建立模型，而且從光線到物件的距離相對較大，這就會提供預期的結果。 在其他情況下，結果會是未定義的。

當這個成員設定為 **TRUE** 時，會在紋理重迭之後，但在 Alpha 混合之前，將反射色彩新增至基底色彩。

</dd> <dt>

<span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ FOGCOLOR**
</dt> <dd>

型別為 [**D3DCOLOR**](d3dcolor.md)的值。 預設值為 0。 如需有關霧化色彩的詳細資訊，請參閱 [ (Direct3D 9) 的霧化色彩 ](fog-color.md)。

</dd> <dt>

<span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ FOGTABLEMODE**
</dt> <dd>

要用於圖元霧化的霧化公式。 設定為 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別的其中一個成員。 預設值為 [無] D3DFOG \_ 。 如需圖元霧化的詳細資訊，請參閱 [ (Direct3D 9) 的圖元霧化 ](pixel-fog.md)。

</dd> <dt>

<span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ FOGSTART**
</dt> <dd>

圖元或頂點霧化效果開始于線性霧化模式的深度。 預設值為 0.0 f。 深度會在世界空間中指定，用於頂點霧化以及裝置空間 \[ 0.0、1.0 \] 或世界空間，以進行圖元霧化。 針對圖元霧化，當系統使用 z 進行霧化計算，而當系統使用眼睛相關的霧化 (w-霧) 時，這些值就會在裝置空間中。 如需詳細資訊，請參閱 [ (Direct3D 9 的霧化參數) ](fog-parameters.md) 和 [眼睛相關的 Vs. Z 深度](pixel-fog.md)。

此呈現狀態的值為浮點值。 因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ FOGEND**
</dt> <dd>

線性霧化模式的圖元或頂點霧化效果結束的深度。 預設值為 1.0 f。 深度會在世界空間中指定，用於頂點霧化以及裝置空間 \[ 0.0、1.0 \] 或世界空間，以進行圖元霧化。 若為圖元霧化，當系統使用 z 進行霧化計算，而當系統使用眼睛相關的霧化 (w-霧化) 時，這些值就會在裝置空間中。 如需詳細資訊，請參閱 [ (Direct3D 9 的霧化參數) ](fog-parameters.md) 和 [眼睛相關的 Vs. Z 深度](pixel-fog.md)。

此呈現狀態的值為浮點值。 因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS \_ FOGDENSITY**
</dt> <dd>

在指數霧化模式中使用之圖元或頂點霧化的霧化密度 (D3DFOG \_ EXP 和 D3DFOG \_ EXP2) 。 有效的密度值範圍從0.0 到1.0。 預設值為 1.0。 如需詳細資訊，請參閱 [ (Direct3D 9) 的霧化參數 ](fog-parameters.md)。

此呈現狀態的值為浮點值。 因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**
</dt> <dd>

**TRUE** 表示啟用以範圍為基礎的頂點霧化。 預設值為 **FALSE**，在這種情況下，系統會使用深度型的霧化。 在以範圍為基礎的霧化中，從檢視器物件的距離會用來計算霧化效果，而不是物件的深度 (也就是在場景中的 z 座標) 。 在以範圍為基礎的霧化中，所有的霧化方法都會正常運作，不同之處在于它們會在計算中使用範圍而非深度。

範圍是用於霧化計算的正確因素，但通常會使用深度，因為範圍是計算和深度的耗用時間，通常已可供使用。 使用深度來計算霧化有不想要的效果，讓周邊物件的 fogginess 隨著檢視器的眼睛變化而變更，在此情況下，深度變更和範圍會維持不變。

因為目前沒有硬體支援每個圖元範圍的霧化，所以範圍更正只會提供給頂點霧化。

如需詳細資訊，請參閱 [ (Direct3D 9) 的頂點霧化 ](vertex-fog.md)。

</dd> <dt>

<span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**
</dt> <dd>

**TRUE** 表示啟用 stenciling，否則為 **FALSE** 以停用 stenciling。 預設值為 **FALSE**。 如需詳細資訊，請參閱 [ (Direct3D 9) 的樣板緩衝區技術 ](stencil-buffer-techniques.md)。

</dd> <dt>

<span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**
</dt> <dd>

樣板測試失敗時要執行的樣板作業。 值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。 預設值為 [保留] D3DSTENCILOP \_ 。

</dd> <dt>

<span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**
</dt> <dd>

樣板測試通過時要執行的樣板作業，而且 (z 測試) 的深度測試失敗。 值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。 預設值為 [保留] D3DSTENCILOP \_ 。

</dd> <dt>

<span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**
</dt> <dd>

當樣板和深度 (z) 測試都通過時，要執行的樣板作業。 值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。 預設值為 [保留] D3DSTENCILOP \_ 。

</dd> <dt>

<span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**
</dt> <dd>

樣板測試的比較函數。 值是來自 [**D3DCMPFUNC**](./d3dcmpfunc.md) 列舉型別。 預設值為 [永遠 D3DCMP] \_ 。

比較函數是用來比較參考值與樣板緩衝區專案。 這項比較只適用于在樣板遮罩中設定的參考值和樣板緩衝區專案中的位， (由 D3DRS STENCILMASK 轉譯 \_ 狀態) 設定。 若 **為 TRUE**，則樣板測試會通過。

</dd> <dt>

<span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**
</dt> <dd>

樣板測試的 int 參考值。 預設值為 0。

</dd> <dt>

<span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**
</dt> <dd>

遮罩會套用至參考值和每個樣板緩衝區專案，以判斷樣板測試的有效位。 預設遮罩為0xFFFFFFFF。

</dd> <dt>

<span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**
</dt> <dd>

寫入遮罩會套用至寫入至樣板緩衝區的值。 預設遮罩為0xFFFFFFFF。

</dd> <dt>

<span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**
</dt> <dd>

用於多紋理混合的色彩，與 D3DTA \_ TFACTOR 材質混合引數或 D3DTOP \_ BLENDFACTORALPHA 材質混合作業。 相關聯的值是 [**D3DCOLOR**](d3dcolor.md) 變數。 預設值為不透明的白色 (0xFFFFFFFF) 。

</dd> <dt>

<span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**
</dt> <dd>

多組紋理座標的材質換行行為。 此轉譯狀態的有效值可以是 D3DWRAPCOORD \_ 0 (或 D3DWRAP \_ U) 、D3DWRAPCOORD \_ 1 (或 D3DWRAP \_ V) 、D3DWRAPCOORD \_ 2 (或 D3DWRAP \_ W) ，以及 D3DWRAPCOORD \_ 3 旗標的任意組合。 這些會導致系統將第一個、第二、第三和第四個維度的方向（有時稱為 s、t、r 和 q 指示）包裝給指定的材質。 此轉譯狀態的預設值為 0 (在) 的所有方向停用換行。

</dd> <dt>

<span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS \_ 剪切**
</dt> <dd>

**TRUE** 表示要啟用 Direct3D 的基本剪輯，或使用 **FALSE** 來停用它。 預設值為 **TRUE**。

</dd> <dt>

<span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS \_ 光源**
</dt> <dd>

**TRUE** 表示啟用 Direct3D 光源，或 **FALSE** 表示停用它。 預設值為 **TRUE**。 只有包含頂點標準的頂點會正確地發亮;未包含一般的頂點會在所有光源計算中採用0的點乘積。

</dd> <dt>

<span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ 環境**
</dt> <dd>

環境淺色色彩。 此值的類型為 [**D3DCOLOR**](d3dcolor.md)。 預設值為 0。

</dd> <dt>

<span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ FOGVERTEXMODE**
</dt> <dd>

要用於頂點模糊的霧化公式。 設定為 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別的其中一個成員。 預設值為 [無] D3DFOG \_ 。

</dd> <dt>

<span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**
</dt> <dd>

**TRUE** 表示啟用每個頂點的色彩，或使用 **FALSE** 來停用它。 預設值為 **TRUE**。 啟用每個頂點色彩可讓系統在其光源計算中包含為個別頂點定義的色彩。

如需詳細資訊，請參閱下列呈現狀態：

-   D3DRS \_ DIFFUSEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE
-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ EMISSIVEMATERIALSOURCE

</dd> <dt>

<span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**
</dt> <dd>

**TRUE** 表示啟用相機相關的高光，或為 **FALSE** 表示使用正向反射醒目顯示。 預設值為 **TRUE**。 使用正向投射的應用程式應指定 **FALSE**。

</dd> <dt>

<span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**
</dt> <dd>

**TRUE** 表示啟用頂點法線的自動正規化，或 **FALSE** 表示停用。 預設值為 **FALSE**。 啟用此功能會讓系統在將頂點轉換成相機空間之後，將頂點的頂點法線正規化，而這可能會耗費大量運算時間。

</dd> <dt>

<span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**
</dt> <dd>

光源計算的擴散色彩來源。 有效的值是 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 列舉型別的成員。 預設值為 D3DMCS \_ COLOR1。 只有當 D3DRS \_ COLORVERTEX 轉譯狀態設為 **TRUE** 時，才會使用此呈現狀態的值。

</dd> <dt>

<span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**
</dt> <dd>

光源計算的反射色彩來源。 有效的值是 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 列舉型別的成員。 預設值為 D3DMCS \_ COLOR2。

</dd> <dt>

<span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**
</dt> <dd>

光源計算的環境色彩來源。 有效的值是 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 列舉型別的成員。 預設值為 [D3DMCS \_ 材質]。

</dd> <dt>

<span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**
</dt> <dd>

光源計算的放射色彩來源。 有效的值是 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 列舉型別的成員。 預設值為 [D3DMCS \_ 材質]。

</dd> <dt>

<span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**
</dt> <dd>

用來執行幾何混合的矩陣數目（如果有的話）。 有效的值是 [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 列舉型別的成員。 預設值為 [停用] D3DVBF \_ 。

</dd> <dt>

<span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**
</dt> <dd>

啟用或停用使用者定義裁剪平面。 有效值為任何 DWORD，其中每個位的狀態 (設定或未設定) 切換對應使用者定義裁剪平面的啟用狀態。 最不重要的位 (位 0) 控制位於索引0的第一個裁剪平面，而後續的位則控制較高索引的裁剪平面啟用。 如果設定了位，系統會在場景轉譯期間套用適當的裁剪平面。 預設值為 0。

系統會定義 [**D3DCLIPPLANEn**](d3dclipplanen.md) 宏，以提供便利的方式來啟用裁剪平面。

</dd> <dt>

<span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ dialog**
</dt> <dd>

浮點值，如果未指定每個頂點的點大小，則指定用於點大小計算的大小。 當頂點包含點大小時，不會使用這個值。 如果 D3DRS POINTSCALEENABLE 為 FALSE，則此值為螢幕空間單位 \_ ; 否則，此值會在全球空間單位中。  預設值是驅動程式傳回的值。 如果驅動程式傳回0或1，則預設值為64，這可允許軟體點大小模擬。 因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ dialog \_ MIN**
</dt> <dd>

指定點基本的最小大小的 float 值。 在轉譯期間，點基本類型會壓制為此大小。 將此值設定為小於1.0 的值，會在點未涵蓋圖元中心時捨棄點，並停用消除鋸齒，或在啟用消除鋸齒功能時以降低濃度呈現消除鋸齒。 預設值為 1.0 f。 此值的範圍大於或等於 0.0 f。 因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ POINTSPRITEENABLE**
</dt> <dd>

bool 值。 若 **為 TRUE**，則會設定點基本的材質座標，以便在每個點上對應完整紋理。 若為 **FALSE**，則會將頂點材質座標用於整個點。 預設值為 **FALSE**。 您可以將 D3DRS \_ POINTSCALEENABLE 設定為 **FALSE** ，並將 D3DRS dialog 設定為 \_ 1.0 （這是預設值），以達到 DirectX 7 樣式的單一圖元點。

</dd> <dt>

<span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**
</dt> <dd>

此為布林值，可控制點基本的大小計算。 若 **為 TRUE**，則會將點大小解釋為相機空間值，並以距離函式和等距至區 y 軸縮放比例進行調整，以計算最終的螢幕空間大小。 若 **為 FALSE**，則會將點大小轉譯為螢幕空間，並直接使用。 預設值為 **FALSE**。

</dd> <dt>

<span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_**
</dt> <dd>

浮點值，可控制點基本的距離型大小衰減。 只有在 D3DRS \_ POINTSCALEENABLE 為 **TRUE** 時才會啟用。 預設值為 1.0 f。 此值的範圍大於或等於 0.0 f。 因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**
</dt> <dd>

浮點值，可控制點基本的距離型大小衰減。 只有在 D3DRS \_ POINTSCALEENABLE 為 **TRUE** 時才會啟用。 預設值為 0.0 f。 此值的範圍大於或等於 0.0 f。 因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**
</dt> <dd>

浮點值，可控制點基本的距離型大小衰減。 只有在 D3DRS \_ POINTSCALEENABLE 為 **TRUE** 時才會啟用。 預設值為 0.0 f。 此值的範圍大於或等於 0.0 f。 因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**
</dt> <dd>

此為布林值，可決定使用多型呈現目標緩衝區時，如何計算個別樣本。 如果設定為 **TRUE**，則會計算多個範例，以便在每個多個範例的不同取樣位置取樣，以執行完整場景消除鋸齒。 當設定為 **FALSE** 時，會使用相同的樣本值寫入多個範例，在圖元中心進行取樣，以允許非反鋸齒的轉譯成多層式緩衝區。 轉譯為單一範例緩衝區時，此轉譯狀態不會有任何作用。 預設值為 **TRUE**。

</dd> <dt>

<span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**
</dt> <dd>

這個遮罩中的每個位（從最 (LSB) 的最小位開始）會控制多取樣轉譯目標中其中一個範例的修改。 因此，對於8樣本轉譯目標，低位元組包含八個範例的每個寫入。 轉譯為單一範例緩衝區時，此轉譯狀態不會有任何作用。 預設值為 0xFFFFFFFF。

此轉譯狀態可讓您使用多重取樣緩衝區做為累積緩衝區，並在每次傳遞更新範例子集的情況下進行 multipass 轉譯。

如果已啟用 n 個 multisamples 和 k 個樣本，則轉譯影像的結果濃度應該是 k/n。 每個圖元的每個元件 RGB 都是由 k/n 組成。

</dd> <dt>

<span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**
</dt> <dd>

設定修補程式邊緣是否會使用 float 樣式鑲嵌。 可能的值是由 [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) 列舉類型所定義。 預設值為 D3DPATCHEDGE \_ 離散。

</dd> <dt>

<span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**
</dt> <dd>

僅針對監視進行設定。 可能的值是由 [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) 列舉類型所定義。 請注意，如果 \_ 設定了 D3DRS DEBUGMONITORTOKEN，則會將呼叫視為將權杖傳遞至「偵錯工具」監視。 例如，如果 \_ 將 D3DDMT ENABLE 或 D3DDMT \_ DISABLE 傳遞至 D3DRS \_ DEBUGMONITORTOKEN-其他標記值會傳入，則偵錯工具的 (啟用或停用) 狀態仍會保存。

此狀態只適用于偵錯工具組建。 Debug monitor 預設為啟用 D3DDMT \_ 。

</dd> <dt>

<span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ dialog \_ MAX**
</dt> <dd>

浮點數值，指定要壓制點 sprite 的最大大小。 值必須小於或等於 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 的 MaxPointSize 成員，且大於或等於 D3DRS \_ dialog \_ MIN。 預設值為64.0。 因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**
</dt> <dd>

啟用或停用索引頂點混合的 bool 值。 預設值為 **FALSE**。 如果設定為 **TRUE**，則會啟用索引頂點混色。 當設定為 **FALSE** 時，就會停用索引頂點的混合。 如果已啟用此轉譯狀態，則使用者必須傳遞矩陣索引做為每個頂點的封裝 DWORDwith。 當轉譯狀態已停用，而且透過 D3DRS VERTEXBLEND 狀態啟用了頂點混色時 \_ ，它相當於在每個頂點中具有矩陣索引0、1、2、3。

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**
</dt> <dd>

UINT 值，可針對轉譯目標色彩緩衝區啟用每個通道的寫入。 設定的位會導致在3D 轉譯期間更新顏色通道。 明確的一點會導致色彩頻道不受影響。 如果在 \_ 裝置 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 PrimitiveMiscCaps 成員中設定 D3DPMISCCAPS COLORWRITEENABLE 功能位，則可以使用這項功能。 此呈現狀態不會影響清除作業。 預設值為0x0000000F。

此轉譯狀態的有效值可以是 D3DCOLORWRITEENABLE \_ ALPHA、D3DCOLORWRITEENABLE \_ BLUE、D3DCOLORWRITEENABLE \_ 綠或 D3DCOLORWRITEENABLE \_ RED 旗標的任何組合。

</dd> <dt>

<span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**
</dt> <dd>

控制補間因數的浮點值。 預設值為 0.0 f。 因為 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法接受 DWORD 值，所以您的應用程式必須轉換包含值的變數，如下列程式碼範例所示。


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**
</dt> <dd>

當 Alpha 混色轉譯狀態（D3DRS \_ ALPHABLENDENABLE）設為 **TRUE** 時，用來選取所套用算數運算的值。 有效的值是由 [**D3DBLENDOP**](./d3dblendop.md) 列舉類型所定義。 預設值為 D3DBLENDOP \_ ADD。

如果 \_ 不支援 D3DPMISCCAPS BLENDOP 裝置功能，則 \_ 會執行 D3DBLENDOP ADD。

</dd> <dt>

<span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**
</dt> <dd>

N-修補位置插補程度。 值可以是 D3DDEGREE \_ 三 (預設) 或 D3DDEGREE \_ 線性。 如需詳細資訊，請參閱 [**D3DDEGREETYPE**](./d3ddegreetype.md)。

</dd> <dt>

<span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**
</dt> <dd>

N-修補正常插補的程度。 值可以是 D3DDEGREE \_ 線性 (預設) 或 D3DDEGREE \_ 二次。 如需詳細資訊，請參閱 [**D3DDEGREETYPE**](./d3ddegreetype.md)。

</dd> <dt>

<span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**
</dt> <dd>

**TRUE** 表示啟用剪式測試，而 **FALSE** 則會停用。 預設值為 **FALSE**。

</dd> <dt>

<span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ SLOPESCALEDEPTHBIAS**
</dt> <dd>

用來決定要將多少偏差套用至共同平面基本專案，以減少 z 減少。 預設值為 0。

偏差 = (max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS。

其中 max 是所呈現三角形的最大深度斜率。

</dd> <dt>

<span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**
</dt> <dd>

**TRUE** 表示啟用行消除鋸齒， **FALSE** 可停用行消除鋸齒功能。 預設值為 **FALSE**。

當轉譯為多取樣轉譯目標時， \_ 會忽略 D3DRS ANTIALIASEDLINEENABLE，並將所有的行呈現為別名。 在多重取樣轉譯目標中使用 [**ID3DXLine**](id3dxline.md) 來呈現反鋸齒線條。

</dd> <dt>

<span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**
</dt> <dd>

最小鑲嵌層級。 預設值為 1.0 f。 請參閱 [鑲嵌式 (Direct3D 9) ](tessellation.md)。

</dd> <dt>

<span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**
</dt> <dd>

最大鑲嵌層級。 預設值為 1.0 f。 請參閱 [鑲嵌式 (Direct3D 9) ](tessellation.md)。

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**
</dt> <dd>

以 x 方向 tessellate 的自我調整數量。 預設值為 0.0 f。 請參閱 [適應性鑲嵌](tessellation.md)。

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**
</dt> <dd>

以 y 方向 tessellate 的數量。 預設值為 0.0 f。 請參閱 [適應性 \_ 鑲嵌](tessellation.md)。

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**
</dt> <dd>

依 z 方向的 tessellate 量。 預設值為 1.0 f。 請參閱 [適應性 \_ 鑲嵌](tessellation.md)。

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**
</dt> <dd>

依 w 方向的 tessellate 量。 預設值為 0.0 f。 請參閱 [適應性 \_ 鑲嵌](tessellation.md)。

</dd> <dt>

<span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**
</dt> <dd>

**TRUE** 表示啟用調適型鑲嵌， **FALSE** 則停用。 預設值為 **FALSE**。 請參閱 [適應性 \_ 鑲嵌](tessellation.md)。

</dd> <dt>

<span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**
</dt> <dd>

**TRUE** 會啟用雙面 Stenciling， **FALSE** 會停用它。 預設值為 **FALSE**。 應用程式應該將 D3DRS \_ CULLMODE 設定為 D3DCULL \_ NONE，以啟用雙面樣板模式。 如果三角形的纏繞順序是順時針的， \_ 則 \* 會使用 D3DRS 樣板作業。 如果是逆時針順序，則 \_ 會使用 D3DRS CCW \_ 樣板 \* 作業。

若要查看是否支援雙面樣板，請檢查 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS TWOSIDED 的 StencilCaps 成員 \_ 。 另請參閱 [D3DSTENCILCAPS](d3dstencilcaps.md)。

</dd> <dt>

<span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**
</dt> <dd>

如果 CCW 樣板測試失敗，則為要執行的樣板運算。 值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。 預設值為 [保留] D3DSTENCILOP \_ 。

</dd> <dt>

<span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**
</dt> <dd>

如果 CCW 樣板測試通過和 z 測試失敗，要執行的樣板作業。 值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。 預設值為 [保留] D3DSTENCILOP \_ 。

</dd> <dt>

<span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**
</dt> <dd>

當 CCW 樣板和 z 測試都通過時，要執行的樣板作業。 值是來自 [**D3DSTENCILOP**](./d3dstencilop.md) 列舉型別。 預設值為 [保留] D3DSTENCILOP \_ 。

</dd> <dt>

<span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**
</dt> <dd>

比較函數。 如果 ( (ref & mask) 樣板函式 (樣板 & mask) ) 為 **TRUE**，則會通過 CCW 樣板測試。 值是來自 [**D3DCMPFUNC**](./d3dcmpfunc.md) 列舉型別。 預設值為 [永遠 D3DCMP] \_ 。

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**
</dt> <dd>

裝置的其他 ColorWriteEnable 值。 請參閱 D3DRS \_ COLORWRITEENABLE。 如果在 \_ 裝置 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 PrimitiveMiscCaps 成員中設定 D3DPMISCCAPS INDEPENDENTWRITEMASKS 功能位，則可以使用這項功能。 預設值為0x0000000f。

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**
</dt> <dd>

裝置的其他 ColorWriteEnable 值。 請參閱 D3DRS \_ COLORWRITEENABLE。 如果在 \_ 裝置 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 PrimitiveMiscCaps 成員中設定 D3DPMISCCAPS INDEPENDENTWRITEMASKS 功能位，則可以使用這項功能。 預設值為0x0000000f。

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**
</dt> <dd>

裝置的其他 ColorWriteEnable 值。 請參閱 D3DRS \_ COLORWRITEENABLE。 如果在 \_ 裝置 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 PrimitiveMiscCaps 成員中設定 D3DPMISCCAPS INDEPENDENTWRITEMASKS 功能位，則可以使用這項功能。 預設值為0x0000000f。

</dd> <dt>

<span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**
</dt> <dd>

[**D3DCOLOR**](d3dcolor.md) 用於 Alpha 混合期間的常數 blend 因素。 如果 D3DPBLENDCAPS \_ BLENDFACTOR 功能位是在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 的 SrcBlendCaps 成員或 **DestBlendCaps** 的 D3DCAPS9 成員中設定，就可以使用這項功能。 請參閱 [**D3DRENDERSTATETYPE**]()。 預設值為0xffffffff。

</dd> <dt>

<span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**
</dt> <dd>

啟用轉譯目標寫入，以將 gamma 更正為 sRGB。 格式必須公開 D3DUSAGE \_ SRGBWRITE。 預設值為 0。

</dd> <dt>

<span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**
</dt> <dd>

用來比較深度值的浮點值。 請參閱 [ (Direct3D 9) 的深度偏差 ](depth-bias.md)。 預設值為 0。

</dd> <dt>

<span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**
</dt> <dd>

請參閱 D3DRS \_ WRAP0。

</dd> <dt>

<span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**
</dt> <dd>

**TRUE** 會啟用 Alpha 色板的不同 blend 模式。 預設值為 **FALSE**。

當設定為 **FALSE** 時，會強制將套用至 Alpha 的轉譯目標混色因數和作業與針對色彩定義的相同。 在未設定 cap D3DPMISCCAPS SEPARATEALPHABLEND 的實執行上，此模式實際上會寫死為 **FALSE** \_ 。 請參閱 [D3DPMISCCAPS](d3dpmisccaps.md)。

個別 Alpha 混色的類型取決於 D3DRS \_ SRCBLENDALPHA 和 D3DRS \_ DESTBLENDALPHA 轉譯狀態。

</dd> <dt>

<span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**
</dt> <dd>

[**D3DBLEND**](./d3dblend.md)列舉型別的其中一個成員。 除非 D3DRS \_ SEPARATEALPHABLENDENABLE 為 **TRUE**，否則會忽略此值。 預設值為 D3DBLEND \_ 一個。

</dd> <dt>

<span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**
</dt> <dd>

[**D3DBLEND**](./d3dblend.md)列舉型別的其中一個成員。 除非 D3DRS \_ SEPARATEALPHABLENDENABLE 為 **TRUE**，否則會忽略此值。 預設值為 D3DBLEND \_ 零。

</dd> <dt>

<span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**
</dt> <dd>

當轉譯狀態（D3DRS \_ SEPARATEALPHABLENDENABLE）設為 **TRUE** 時，用來選取套用至個別 Alpha 混色之算數運算的值。

有效的值是由 [**D3DBLENDOP**](./d3dblendop.md) 列舉類型所定義。 預設值為 D3DBLENDOP \_ ADD。

如果 \_ 不支援 D3DPMISCCAPS BLENDOP 裝置功能，則 \_ 會執行 D3DBLENDOP ADD。 請參閱 [D3DPMISCCAPS](d3dpmisccaps.md)。

</dd> <dt>

<span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註



| 轉譯狀態        |                    |
|----------------------|--------------------|
| ps \_ 1 \_ 1 到 ps \_ 1 \_ 3 | 4紋理取樣器 |



 

Direct3D 定義了 D3DRENDERSTATE \_ WRAPBIAS 常數，方便讓應用程式根據紋理座標集的以零為起始的整數來啟用或停用材質換行 (而不是明確地使用其中一個 D3DRS \_ WRAP n 狀態值) 。 將 D3DRENDERSTATE \_ WRAPBIAS 值新增至材質座標集的以零為起始的索引，以計算 \_ 對應至該索引的 D3DRS 換行 n 值，如下列範例所示。


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
