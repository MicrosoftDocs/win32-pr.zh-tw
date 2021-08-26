---
title: '常數 float register (HLSL 與參考) '
description: 四個元件浮點常數的頂點著色器輸入暫存器。 使用 def-vs 或 SetVertexShaderConstantF 設定常數暫存器。
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c81cc05a40ebb7ede53fb14c957584f289a14a15045a2b69f557072c6885c9ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949928"
---
# <a name="constant-float-register-hlsl-vs-reference"></a>常數 float register (HLSL 與參考) 

四個元件浮點常數的頂點著色器輸入暫存器。 使用 [def-vs](def---vs.md) 或 [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)設定常數暫存器。

常數暫存器檔案是唯讀的，從頂點著色器的角度來看。 任何單一指令都只能存取一個常數暫存器。 不過，該指令中的每個來源可能會獨立 swizzle，並在讀取時對該向量進行否定。

在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。

-   針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。 使用 defx 宣告之常數的存留期只限于該著色器的執行。 相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。 在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。
-   針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。 每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。

常數暫存器會指定為絕對或相對：


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



您可以使用絕對索引或從位址暫存器中的相對索引，讀取常數暫存器。 從超出範圍的暫存器讀取會傳回 (0.0、0.0、0.0、0.0) 。

## <a name="examples"></a>範例

以下是在著色器中宣告兩個浮點常數的範例。


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



每次呼叫 [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) 時，就會載入這些常數。

以下是使用 API 的範例。


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



如果您要使用 API 來設定常數值，則不需要著色器宣告。



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| 常數暫存器      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 