---
description: 下列使用者定義結構可以用於將在兩個矩陣之間混合的頂點。
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: 使用 (Direct3D 9) 的幾何混合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991590"
---
# <a name="using-geometry-blending-direct3d-9"></a>使用 (Direct3D 9) 的幾何混合

下列使用者定義結構可以用於將在兩個矩陣之間混合的頂點。


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



Blend 權數必須出現在 FVF 中的位置和 RHW 資料之後，以及頂點正常之前。

請注意，前一個頂點格式只包含一個混合加權值。 這是因為會有兩個世界矩陣，定義于 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (0) 和 **D3DTS \_ WORLDMATRIX** (1) 轉換狀態。 系統會使用單一權數值來混合這兩個矩陣之間的每個頂點。 針對三個矩陣，只需要兩個加權，依此類推。

> [!Note]
>
> 定義外觀權數很簡單。 使用接點之間距離的線性功能是不錯的起點，但是更平滑的 sigmoid 函式看起來更好。 如果想要的話，選擇外觀權重分佈函式可能會導致 creases 的接點，並在短距離內使用較大的外觀權數變化。

 

## <a name="setting-blending-matrices"></a>設定混色矩陣

您可以藉由呼叫 [**IDirect3DDevice9：： SetTransform**](/windows/desktop/api) 方法，來設定系統混合的轉換矩陣。 將第一個參數設定為 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) 巨集定義的值，並將第二個參數設定為要設定之矩陣的位址。

下列 c + + 程式碼範例會設定兩個世界矩陣，在這兩個矩陣之間混合幾何來建立 double-jointed arm 的假像。


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



設定混色矩陣只會讓系統快取矩陣以供稍後使用。它不會指示系統開始混合頂點。

## <a name="enabling-geometry-blending"></a>啟用幾何混合

幾何混合預設為停用。 若要啟用幾何混合，請呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/desktop/api) 方法，將 D3DRS \_ VERTEXBLEND 轉譯狀態設定為 [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 列舉類型的值。 下列程式碼範例顯示在兩個世界矩陣之間設定 blend 的呈現狀態時，此呼叫可能會顯示的樣子。


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



當 D3DRS \_ VERTEXBLEND 設定為 D3DVBF DISABLE 以外的任何值時 \_ ，系統會假設頂點格式會包含適當的混色加權數目。 您必須負責提供符合規範的頂點格式，以及提供該格式對 Direct3D 轉譯方法的適當描述。

啟用時，系統會針對 DrawPrimitive 轉譯方法所呈現的所有物件執行幾何混合。

## <a name="see-also"></a>另請參閱

[修正 (Direct3D 9) 的函式 FVF 碼 ](fixed-function-fvf-codes.md)


## <a name="related-topics"></a>相關主題

<dl> <dt>

[幾何混合](geometry-blending.md)
</dt> </dl>

 

 
