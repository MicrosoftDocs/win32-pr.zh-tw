---
description: 定義每一階段的材質混合作業。
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: 'D3DTEXTUREOP 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322783"
---
# <a name="d3dtextureop-enumeration"></a>D3DTEXTUREOP 列舉

定義每一階段的材質混合作業。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP \_ DISABLE**
</dt> <dd>

停用此材質階段的輸出，以及索引較高的所有階段。 若要停用材質對應，請將此設定為第一個材質階段的色彩運算 (階段 0) 。 啟用色彩作業時，無法停用 Alpha 作業。 當色彩混合啟用時，將 Alpha 作業設定為 D3DTOP \_ 停用會導致未定義的行為。

</dd> <dt>

<span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**
</dt> <dd>

使用這個紋理階段的第一個色彩或 Alpha 引數（未修改）作為輸出。 當搭配使用 D3DTSS COLOROP 材質階段狀態時，此作業會影響 color 引數 \_ ，而當搭配 D3DTSS ALPHAOP 使用時，則會影響 Alpha 引數 \_ 。

![此引數的方程式 (s (rgba) = arg1) ](images/topfrm1.png)

</dd> <dt>

<span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**
</dt> <dd>

使用這個紋理階段的第二個色彩或 Alpha 引數（未修改）作為輸出。 當搭配使用 D3DTSS COLOROP 材質階段狀態時，此作業會影響 color 引數 \_ ，而當搭配 D3DTSS ALPHAOP 使用時，則會影響 Alpha 引數 \_ 。

![此引數的方程式 (s (rgba) = arg2) ](images/topfrm2.png)

</dd> <dt>

<span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP \_ lambert**
</dt> <dd>

將引數的元件相乘。

![lambert 作業的方程式 (s (rgba) = arg1 x arg 2) ](images/topfrm3.png)

</dd> <dt>

<span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**
</dt> <dd>

將引數的元件相乘，並將產品移至左邊的1位 (有效地將它們乘以 2) 以進行 brightening。

![modulate2x 作業的方程式 (s (rgba) = (arg1 x arg 2) 然後左移 1) ](images/topfrm4.png)

</dd> <dt>

<span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**
</dt> <dd>

將引數的元件相乘，並將產品移至左邊的2位 (有效地將它們乘以 4) 以進行 brightening。

![modulate4x 作業的方程式 (s (rgba) = (arg1 x arg 2) 然後左移 2) ](images/topfrm5.png)

</dd> <dt>

<span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ 新增**
</dt> <dd>

加入引數的元件。

![新增作業的方程式 (s (rgba) = arg1 + arg 2) ](images/topfrm6.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ ADDSIGNED**
</dt> <dd>

將引數的元件新增為-0.5 偏差，使值的有效範圍從-0.5 到0.5。

![新增簽署作業 (s 的方程式 (rgba) = arg1 + arg 2 – 0.5) ](images/topfrm7.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**
</dt> <dd>

將引數的元件新增為-0.5 偏差，然後將產品轉移至左方的1位。

![新增帶正負號之2x 作業 ( (s 的方程式 (rgba) = arg1 + arg 2-0.5) 然後左移 1) ](images/topfrm8.png)

</dd> <dt>

<span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP \_ 減**
</dt> <dd>

從第一個引數的元件減去第二個引數的元件。

![減法運算的方程式 (s (rgba) = arg1-arg 2) ](images/topfrm9.png)

</dd> <dt>

<span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ ADDSMOOTH**
</dt> <dd>

新增第一個和第二個引數;然後將其產品從總和減去。

![加入平滑作業 (s 的方程式 (rgba) = arg1 + arg 2 x (1-arg1) ) ](images/topfrm10.png)

</dd> <dt>

<span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ BLENDDIFFUSEALPHA**
</dt> <dd>

以線性方式混合此材質階段，使用每個頂點的插入 Alpha。

![blend 漫射 Alpha 運算的方程式 (s (rgba) = arg1 x Alpha + arg 2 x (1-Alpha) ) ](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ BLENDTEXTUREALPHA**
</dt> <dd>

使用這個階段材質的 Alpha，以線性方式混合此材質階段。

![blend 材質 Alpha 運算的方程式 (s (rgba) = arg1 x Alpha + arg 2 x (1-Alpha) ) ](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ BLENDFACTORALPHA**
</dt> <dd>

使用具有 D3DRS TEXTUREFACTOR 轉譯狀態的純量 Alpha 組，以線性方式混合此材質階段 \_ 。

![blend 因數 Alpha 運算的方程式 (s (rgba) = arg1 x Alpha + arg 2 x (1-Alpha) ) ](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ BLENDTEXTUREALPHAPM**
</dt> <dd>

以線性方式混合使用預乘 Alpha 的材質階段。

![blend 材質 Alpha pm 運算的方程式 (s (rgba) = arg1 + arg 2 x (1-Alpha) ) ](images/topfrm12.png)

</dd> <dt>

<span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ BLENDCURRENTALPHA**
</dt> <dd>

使用從上一個材質階段取得的 Alpha，以線性方式混合此材質階段。

![blend 目前 Alpha 運算的方程式 (s (rgba) = arg1 x Alpha + arg2 x (1-Alpha) ) ](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP \_ PREMODULATE**
</dt> <dd>

\_階段 n 中設定了 D3DTOP PREMODULATE。 階段 n 的輸出是 arg1。 此外，如果階段 n + 1 中有材質， \_ 階段 n + 1 中的任何 D3DTA 目前都會依階段 n + 1 中的材質預乘。

</dd> <dt>

<span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ MODULATEALPHA \_ ADDCOLOR**
</dt> <dd>

使用第一個引數的 Alpha lambert 第二個引數的色彩;然後將結果新增至引數1。 只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。

![add color lambert Alpha operation (s (rgba) = arg1 (rgb) + arg1 (rgb)  (x arg2) ) ](images/topfrm13.png)

</dd> <dt>

<span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ MODULATECOLOR \_ ADDALPHA**
</dt> <dd>

Lambert 引數;然後新增第一個引數的 Alpha。 只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。

![新增 Alpha lambert 色彩作業的方程式 (s (rgba) = arg1 (rgb) x arg2 (rgb) + arg1 (a) ) ](images/topfrm14.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ MODULATEINVALPHA \_ ADDCOLOR**
</dt> <dd>

類似于 D3DTOP \_ MODULATEALPHA \_ ADDCOLOR，但使用第一個引數之 Alpha 的反向。 只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。

![新增色彩 lambert 反向 Alpha 運算 (s (rgba) = (1-arg1 (x arg2) ) rgb (+ arg1) rgb (](images/topfrm15.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ MODULATEINVCOLOR \_ ADDALPHA**
</dt> <dd>

類似于 D3DTOP \_ MODULATECOLOR \_ ADDALPHA，但使用第一個引數的色彩反轉。 只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。

![新增 Alpha lambert 反向色彩作業 (s (rgba) = (1-arg1 (rgb) ) x arg2 (rgb) + arg1 (a) ) ](images/topfrm16.png)

</dd> <dt>

<span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ BUMPENVMAP**
</dt> <dd>

使用下一個材質階段中的環境對應（沒有亮度），執行每圖元的凹凸對應。 只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。

</dd> <dt>

<span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ BUMPENVMAPLUMINANCE**
</dt> <dd>

使用下一個材質階段中的環境對應，以亮度執行每個圖元的凹凸對應。 只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。

</dd> <dt>

<span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**
</dt> <dd>

將每個引數的元件 lambert 為帶正負號的元件，並新增其產品;然後，將總和複製到所有色彩通道，包括 Alpha。 這項操作支援色彩和 Alpha 運算。

![點乘積3作業的方程式 (s (rgba) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b) ) ](images/topfrm17.png)

在 DirectX 6 和 DirectX 7 中，多紋理作業會在用來模擬已簽署資料的一半 (y = x-0.5) 之前將上述輸入往下移動，並將純量結果自動壓制到正值，並複寫到所有三個輸出通道。 另外也請注意，做為色彩作業，這不會更新只是更新 RGB 元件的 Alpha。

不過，在 DirectX 8.1 著色器中，您可以指定將輸出路由傳送至 rgb 或元件，或是 (預設) 。 您也可以在 Alpha 通道上指定個別的純量運算。

</dd> <dt>

<span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MULTIPLYADD**
</dt> <dd>

執行乘法累積運算。 它會接受最後兩個引數，將它們相乘，並將其新增至其餘的輸入/來源引數，並將其放入結果中。

S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3

</dd> <dt>

<span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ LERP**
</dt> <dd>

以線性方式在第二個和第三個來源引數之間，以第一個來源引數指定的比例進行插補

S<sub>RGBA</sub> = (arg1) \* Arg2 + (1-arg1) \* Arg3。

</dd> <dt>

<span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

使用 D3DTSS \_ COLOROP 或 D3DTSS \_ ALPHAOP 值與 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 方法來設定色彩或 Alpha 運算時，會使用此類型的成員。

在上述公式中，S<sub>rgba</sub> 是紋理作業所產生的 rgba 色彩，而 Arg1、Arg2 和 Arg3 則代表材質引數的完整 RGBA 色彩。 引數的個別元件會以注標顯示。 例如，引數1的 Alpha 元件會顯示為 Arg1<sub>A</sub>。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
