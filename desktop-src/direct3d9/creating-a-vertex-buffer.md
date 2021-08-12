---
description: 您可以藉由呼叫 IDirect3DDevice9：： CreateVertexBuffer 方法（可接受五個參數）來建立頂點緩衝區物件。
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: " (Direct3D 9) 建立頂點緩衝區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c12cb50d7879ef73d4c760ac61a0698651cb9ed7d334c90475bd2e8ee4148db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527672"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a> (Direct3D 9) 建立頂點緩衝區

您可以藉由呼叫 [**IDirect3DDevice9：： CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) 方法（可接受五個參數）來建立頂點緩衝區物件。 第一個參數會指定頂點緩衝區長度（以位元組為單位）。 使用 sizeof 運算子來判斷頂點格式的大小（以位元組為單位）。 請考慮下列自訂頂點格式。


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



若要建立頂點緩衝區來保存四個 CUSTOMVERTEX 結構， \[ 請 \* \] 為 *Length* 參數指定 4 sizeof (CUSTOMVERTEX) 。

第二個參數是一組使用方式控制項。 此外，它的值會決定頂點緩衝區是否能夠包含剪切資訊（以剪輯旗標的形式），也就是存在於視圖區域外部的頂點。 若要建立不能包含剪輯旗標的頂點緩衝區，請包括 \_ *Usage* 參數的 D3DUSAGE DONOTCLIP 旗標。 \_只有當您也指出頂點緩衝區將包含已轉換的頂點時，才會套用 D3DUSAGE DONOTCLIP 旗標-D3DFVF \_ XYZRHW 旗標包含在 *FVF* 參數中。 [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) \_ 如果您指出緩衝區將包含未轉換的頂點 (D3DFVF XYZ 旗標) ，IDirect3DDevice9：： CreateVertexBuffer 方法會忽略 D3DUSAGE DONOTCLIP 旗標 \_ 。 裁剪旗標佔用額外的記憶體，讓支援裁剪的頂點緩衝區稍微大於無法包含剪切旗標的頂點緩衝區。 由於這些資源會在建立頂點緩衝區時配置，因此您必須事先要求支援裁剪的頂點緩衝區。

第三個參數 *FVF* 是描述頂點緩衝區頂點格式的 [D3DFVF](d3dfvf.md) 組合。 如果您為此參數指定0，則頂點緩衝區為非 FVF 的頂點緩衝區。 如需詳細資訊，請參閱 [FVF Direct3D 9 (的頂點緩衝區) ](fvf-vertex-buffers.md)。 第四個參數描述用來放置頂點緩衝區的記憶體類別。

[**IDirect3DDevice9：： CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)所接受的最後一個參數是變數的位址，如果呼叫成功，將會以頂點緩衝區物件的新 [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)介面指標填滿。

您無法產生不支援的頂點緩衝區的剪切旗標。

下列 c + + 程式碼範例示範如何在程式碼中建立頂點緩衝區。


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點緩衝區](vertex-buffers.md)
</dt> </dl>

 

 
