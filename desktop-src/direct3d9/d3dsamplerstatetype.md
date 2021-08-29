---
description: 取樣器狀態定義紋理取樣作業，例如紋理定址和材質篩選。
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: 'D3DSAMPLERSTATETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 55e8efe80390f64f2376fd3995e414fed604ec8cb854c14b94f71922e146a32e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988878"
---
# <a name="d3dsamplerstatetype-enumeration"></a>D3DSAMPLERSTATETYPE 列舉

取樣器狀態定義紋理取樣作業，例如紋理定址和材質篩選。 某些取樣器狀態設定頂點處理，以及一些設定圖元處理。 您可以使用 stateblocks 來儲存和還原取樣器狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP \_ ADDRESSU**
</dt> <dd>

U 座標的材質位址模式。 預設值為 D3DTADDRESS \_ WRAP。 如需詳細資訊，請參閱 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)。

</dd> <dt>

<span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ ADDRESSV**
</dt> <dd>

V 座標的材質位址模式。 預設值為 D3DTADDRESS \_ WRAP。 如需詳細資訊，請參閱 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)。

</dd> <dt>

<span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ ADDRESSW**
</dt> <dd>

W 座標的材質位址模式。 預設值為 D3DTADDRESS \_ WRAP。 如需詳細資訊，請參閱 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)。

</dd> <dt>

<span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ 邊框**
</dt> <dd>

框線色彩或類型 [**D3DCOLOR**](d3dcolor.md)。 預設色彩為0x00000000。

</dd> <dt>

<span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ MAGFILTER**
</dt> <dd>

[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)類型的放大篩選。 預設值為 D3DTEXF \_ 點。

</dd> <dt>

<span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MINFILTER**
</dt> <dd>

[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)類型的縮制篩選。 預設值為 D3DTEXF \_ 點。

</dd> <dt>

<span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MIPFILTER**
</dt> <dd>

要在縮制期間使用的 Mipmap 篩選準則。 請參閱 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)。 預設值為 [無] D3DTEXF \_ 。

</dd> <dt>

<span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ MIPMAPLODBIAS**
</dt> <dd>

Mipmap 詳細資料偏差。 預設值為零。

</dd> <dt>

<span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MAXMIPLEVEL**
</dt> <dd>

要使用的最大地圖的詳細層級索引。 值的範圍是從0到 (n-1-1) 其中0是最大值。 預設值為零。

</dd> <dt>

<span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MAXANISOTROPY**
</dt> <dd>

DWORD 最大 anisotropy。 值的範圍是從1到 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)結構的 **MaxAnisotropy** 成員中指定的值。 預設值為 1。

</dd> <dt>

<span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ SRGBTEXTURE**
</dt> <dd>

Gamma 修正值。 預設值為0，表示 gamma 為1.0，且不需要任何更正。 否則，此值表示取樣器在內容上應該採用2.2 的 gamma，並將其轉換為線性 (gamma 1.0) ，然後再呈現給圖元著色器。

</dd> <dt>

<span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ ELEMENTINDEX**
</dt> <dd>

將 multielement 材質指派給取樣器時，這會指出要使用的元素索引。 預設值為 0。

</dd> <dt>

<span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ DMAPOFFSET**
</dt> <dd>

Presampled 置換地圖中的頂點位移。 這是鑲嵌所使用的常數，其預設值為0。

</dd> <dt>

<span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
