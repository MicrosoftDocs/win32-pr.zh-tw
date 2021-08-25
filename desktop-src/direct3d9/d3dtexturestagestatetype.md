---
description: 材質階段狀態會定義多 blender 材質作業。
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: 'D3DTEXTURESTAGESTATETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4879009f603a6943302f0595f37176ec5edf8e1a1d3212efedb66c923d775104
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894148"
---
# <a name="d3dtexturestagestatetype-enumeration"></a>D3DTEXTURESTAGESTATETYPE 列舉

材質階段狀態會定義多 blender 材質作業。 某些取樣器狀態會設定頂點處理，以及某些設定的圖元處理。 您可以使用 stateblocks 來儲存和還原材質階段狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ COLOROP**
</dt> <dd>

材質階段狀態是由 [**D3DTEXTUREOP**](./d3dtextureop.md) 列舉型別之一成員所識別的材質色彩混合作業。 第一個材質階段的預設值 (階段 0) 是 D3DTOP \_ lambert; 針對所有其他階段，預設值為 D3DTOP \_ DISABLE。

</dd> <dt>

<span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**
</dt> <dd>

材質階段狀態是階段的第一個色彩引數，由其中一個 [D3DTA](d3dta.md)來識別。 預設引數為 D3DTA \_ 材質。

指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。 \_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。 註冊的預設值是 (0.0、0.0、0.0、0.0) 。

</dd> <dt>

<span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**
</dt> <dd>

材質階段狀態是階段的第二個色彩引數，由 [D3DTA](d3dta.md)識別。 預設引數為 D3DTA \_ CURRENT。 指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。 \_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。 註冊的預設值是 (0.0、0.0、0.0、0.0) 

</dd> <dt>

<span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**
</dt> <dd>

材質階段狀態是由 [**D3DTEXTUREOP**](./d3dtextureop.md) 列舉型別之一成員所識別的材質 Alpha 混色運算。 第一個材質階段的預設值 (階段 0) 是 D3DTOP \_ SELECTARG1，而針對所有其他階段，預設值為 D3DTOP \_ DISABLE。

</dd> <dt>

<span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**
</dt> <dd>

材質階段狀態是此階段的第一個 Alpha 引數，由 [D3DTA](d3dta.md)所識別。 預設引數為 D3DTA \_ 材質。 如果未針對這個階段設定材質，則預設引數為 D3DTA \_ 擴散。 指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。 \_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。 註冊的預設值是 (0.0、0.0、0.0、0.0) 。

</dd> <dt>

<span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**
</dt> <dd>

材質階段狀態是階段的第二個 Alpha 引數，由 [D3DTA](d3dta.md)所識別。 預設引數為 D3DTA \_ CURRENT。 指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。 \_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。 註冊的預設值是 (0.0、0.0、0.0、0.0) 。

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**
</dt> <dd>

材質階段狀態是浮動 \[ \] \[ \] 對應矩陣中 0 0 係數的浮點值。 預設值為 0.0。

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**
</dt> <dd>

材質階段狀態是浮動 \[ \] \[ \] 對應矩陣中 0 1 係數的浮點值。 預設值為 0.0。

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**
</dt> <dd>

材質階段狀態是浮動 \[ \] \[ \] 對應矩陣中的 1 0 係數的浮點值。 預設值為 0.0。

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**
</dt> <dd>

材質階段狀態是浮動 \[ \] \[ \] 對應矩陣中1個係數的浮點值。 預設值為 0.0。

</dd> <dt>

<span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**
</dt> <dd>

要搭配此材質階段使用之材質座標集的索引。 您最多可以為每個頂點指定八組紋理座標。 如果頂點未在指定的索引中包含一組紋理座標，系統就會預設為您和 v 座標 (0，0) 。

使用頂點著色器進行轉譯時，每個階段的材質座標索引都必須設定為其預設值。 每個階段的預設索引等於階段索引。 針對這個紋理階段使用的每個頂點，將此狀態設定為以零為基底的座標集索引。

此外，應用程式也可以包含要設定之索引的邏輯 OR，其中一個常數會要求 Direct3D 自動產生材質轉換的輸入材質座標。 如需所有常數的清單，請參閱 [D3DTSS \_ TCI](d3dtss-tci.md)。

除了 D3DTSS \_ TCI \_ PASSTHRU （解析為零）之外，如果有下列任何值包含在要設定的索引中，系統會嚴格地使用索引來判斷材質包裝模式。 這些旗標最適合用來執行環境對應。

</dd> <dt>

<span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**
</dt> <dd>

凹凸地圖亮度的浮點刻度值。 預設值為 0.0。

</dd> <dt>

<span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ BUMPENVLOFFSET**
</dt> <dd>

凹凸地圖亮度的浮點位移值。 預設值為 0.0。

</dd> <dt>

<span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ TEXTURETRANSFORMFLAGS**
</dt> <dd>

[**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md)列舉型別的成員，可控制此材質階段之材質座標的轉換。 預設值為 [停用] D3DTTFF \_ 。

</dd> <dt>

<span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**
</dt> <dd>

Triadic 作業的第三個色彩運算元設定 (乘、加入和線性插補) （由[D3DTA](d3dta.md)所識別）。 如果 \_ 有 D3DTEXOPCAPS MULTIPLYADD 或 D3DTEXOPCAPS LERP 裝置功能，則支援此設定 \_ 。 預設引數為 D3DTA \_ CURRENT。 指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。 \_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。 註冊的預設值是 (0.0、0.0、0.0、0.0) 。

</dd> <dt>

<span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**
</dt> <dd>

Triadic 作業的 Alpha 通道選取器運算元設定 (乘、加入和線性插補) （由[D3DTA](d3dta.md)所識別）。 如果 \_ 有 D3DTEXOPCAPS MULTIPLYADD 或 D3DTEXOPCAPS LERP 裝置功能，則支援此設定 \_ 。 預設引數為 D3DTA \_ CURRENT。 指定 D3DTA \_ TEMP 以選取用於讀取或寫入的臨時暫存器色彩。 \_如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援 D3DTA TEMP。 預設引數是 (0.0、0.0、0.0、0.0) 。

</dd> <dt>

<span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**
</dt> <dd>

設定為針對此階段的結果選取目的地註冊，由 [D3DTA](d3dta.md)識別。 您可以將此值設定為 D3DTA \_ 目前 (預設值) 或 D3DTA \_ TEMP，也就是可讀入後續階段做為輸入引數的單一臨時暫存器。 傳遞至霧化 blender 和框架緩衝區的最終色彩是取自 D3DTA \_ CURRENT，因此最後一個作用中的材質階段狀態必須設定為 [寫入至最新狀態]。 如果 \_ 有 D3DPMISCCAPS TSSARGTEMP 裝置功能，則支援此設定。

</dd> <dt>

<span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS \_ 常數**
</dt> <dd>

每個階段的常數色彩。 若要查看裝置是否支援每一階段的常數色彩，請參閱 \_ [D3DPMISCCAPS](d3dpmisccaps.md)中的 D3DPMISCCAPS PERSTAGECONSTANT 常數。 \_D3DTA 常數會使用 D3DTSS 常數 \_ 。 請參閱 [D3DTA](d3dta.md)。

</dd> <dt>

<span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉類型的成員會搭配 [**IDirect3DDevice9：： GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) 和 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 方法使用，以抓取並設定材質狀態值。

D3DTSS \_ BUMPENVMAT00、D3DTSS \_ BUMPENVMAT01、D3DTSS \_ BUMPENVMAT10 和 D3DTSS \_ BUMPENVMAT11 凸塊對應矩陣係數的有效值範圍大於或等於-8.0 且小於8.0。 以數學標記法表示的這個範圍是 (-8.0，8.0) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
