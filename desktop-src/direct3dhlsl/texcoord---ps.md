---
title: texcoord-ps
description: 將材質座標資料 (UVW1)  (RGBA) 的色彩資料來解讀。
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682547"
---
# <a name="texcoord---ps"></a>texcoord-ps

將材質座標資料 (UVW1)  (RGBA) 的色彩資料來解讀。

## <a name="syntax"></a>Syntax



| texcoord dst |
|--------------|



 

其中

-   dst 是目的地註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcoord              | x    | x    | x    |      |      |      |       |      |       |



 

此指令會將材質座標集 (UVW1) 對應至目的地暫存器號碼，以 (RGBA) 的色彩資料。 如果材質座標集包含三個以上的元件，則遺漏的元件會設定為0。 第四個元件一律設定為1。 所有值都壓制介於0和1之間。

Texcoord 的優點是，它提供一種方式，將頂點資料以高精確度的方式直接傳遞至圖元著色器。 不過，當資料寫入目的地暫存器時，將會遺失某些精確度，視暫存器的硬體使用的位數而定。

此指令未取樣任何紋理。 只有在此材質階段設定的材質座標是相關的。

任何材質資料 (例如位置、標準和光源方向) 都可由頂點著色器對應至材質座標。 這是藉由使用 [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) 將材質與材質暫存器產生關聯，以及指定如何使用 [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)來完成紋理取樣來完成。 如果使用了 fixed 函數管線，請務必提供 TSS \_ TEXCOORDINDEX 旗標。

此指令的使用方式如下：


```
texcoord tn
```



[材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) 包含四個色彩值 (RGBA) 。 您也可以將資料視為向量資料 (xyzw) 。 texcoord 將會從紋理座標集 x (xyz) 取得這些值的三個值，而第四個元件 (w) 會設定為1。 紋理位址會從紋理座標集合 n 複製。 結果為0和1之間的壓制。

這個範例只供說明。 著色器隨附的 C 程式碼尚未針對效能進行優化。

以下是使用 texcoord 的範例著色器。


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



圖元著色器所呈現的輸出如下圖所示。  (u，v，w，1) 座標值會對應至 (rgb) 通道。 Alpha 色板設定為1。 在圖的角落，座標 (0、0、0、1) 會轉譯為黑色; (1、0、0、1) 為紅色; (0、1、0、1) 為綠色; (1、1、0、1) 包含綠色和紅色，產生黃色。

![範例圖元著色器的呈現輸出圖例](images/pstexcoord.jpg)

需要額外的程式碼才能使用此著色器，而範例案例如下所示。


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 