---
title: texkill-ps
description: 如果紋理座標 (UVW) 的前三個元件中有任何一個小於零，則取消轉譯目前的圖元。
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 462549a9caba9b4b49ca5b5ac088e41320b3d6f731a78a0251d5191cc601a2e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284026"
---
# <a name="texkill---ps"></a>texkill-ps

如果紋理座標 (UVW) 的前三個元件中有任何一個小於零，則取消轉譯目前的圖元。

## <a name="syntax"></a>Syntax



| texkill dst |
|-------------|



 

其中

-   dst 是目的地註冊

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texkill               | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

此指令對應于 HLSL 的 [**剪輯**](dx-graphics-hlsl-clip.md) 函數。

texkill 不會取樣任何材質。 它會在目的地暫存器編號所指定紋理座標的前三個元件上運作。 針對 ps \_ 1 \_ 4，texkill 會操作目的地登錄的前三個元件中的資料。

您可以使用此指令在轉譯器中執行任意的剪輯平面。

使用頂點著色器時，應用程式會負責套用「透視圖」轉換。 這可能會造成任意裁剪平面的問題，因為如果它包含 anisomorphic 縮放比例，也需要轉換剪輯平面。 因此，最好提供要用於任意 clipper 的 unprojected 頂點位置，也就是由 texkill 運算子識別的材質座標集合。

此指令的使用方式如下：

<dl> texkill tn  
圖元遮罩的完成方式如下：  
如果 ( TextureCoordinates 的 x、y、z 元件 (階段 n) <sub>UVWQ</sub>< 0 )   
取消圖元呈現
</dl>

針對圖元著色器 1 \_ 1、1 \_ 2 和 1 \_ 3，texkill 會在目的地暫存器編號所指定的材質座標設定上運作。 不過，在第1版中， \_ texkill 會針對 [材質座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) 暫存器中包含的資料 (tn) 或在已指定為目的地的暫存登錄 (rn) 中操作。

當啟用取樣時，由於會在 texkill 所產生的任何邊緣上，對多邊形邊緣所達成的任何消除鋸齒效果，都不會沿著任何邊緣達成。 圖元著色器每圖元執行一次。

這個範例只供說明。

此範例會遮罩具有負材質座標的圖元。 圖元色彩會從頂點資料中提供的頂點色彩插補。


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



紋理座標的範圍是從-0.5 到0.5 （u），以及 v 中的0.0 到1.0。 此指示會使負 u 值遭到遮罩。下圖顯示套用至四個未套用 texkill 指令之四色的頂點色彩。 下圖顯示 texkill 指令的結果。 紋理座標中的圖元色彩會以 0 (，其中 x 從-0.5 到 0.0) 會被遮罩。背景色彩 (白色) 用來遮罩圖元色彩。

![將頂點色彩套用至不含 texkill 指令之四色輸出的圖例](images/pstexkill-in.jpg)![已套用 texkill 指令的輸出圖例](images/pstexkill-out.jpg)

紋理座標資料會在此範例中的頂點資料宣告中宣告。


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




