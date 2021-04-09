---
description: 轉換狀態256-511 會保留為最多可儲存256矩陣，可使用8位索引來編制索引。
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: 使用 (Direct3D 9) 的索引頂點混合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120362e4a86081ff51aee9053d1526a9a08f014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845956"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>使用 (Direct3D 9) 的索引頂點混合

轉換狀態256-511 會保留為最多可儲存256矩陣，可使用8位索引來編制索引。 使用宏 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) ，將索引0-255 對應至對應的轉換狀態。 下列程式碼範例示範如何使用 [**IDirect3DDevice9：： SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) 方法，將在轉換狀態編號256的矩陣設定為識別矩陣。


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



若要啟用或停用索引頂點混合，請將 D3DRS \_ INDEXEDVERTEXBLENDENABLE 轉譯狀態設為 **TRUE**。 當轉譯狀態為 [已啟用] 時，您必須使用每個頂點傳遞矩陣索引作為封裝的 Dword。 當此轉譯狀態已停用且已啟用頂點混色時，就相當於在每個頂點中都有矩陣索引0、1、2和3。 下列程式碼範例使用 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法來啟用索引頂點的混合。


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



若要啟用或停用頂點混合，請將 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 轉譯狀態設定為 [D3DRS \_ 停用] 以外的值（ [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 列舉型別）。 如果此轉譯狀態未設定為 [停用 D3DRS] \_ ，則您必須針對每個頂點傳遞所需的加權數目。 下列程式碼範例會使用 **IDirect3DDevice9：： graphicsdevice** 來針對每個頂點啟用具有三個加權的頂點混合。


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>判斷索引頂點混合支援

若要判斷索引頂點混色矩陣的大小上限，請檢查 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 MaxVertexBlendMatrixIndex 成員。 下列程式碼範例會使用 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) 方法來取得此大小。


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



如果在 MaxVertexBlendMatrixIndex 中設定的值為0，則裝置不支援索引矩陣。

> [!Note]  
> 使用軟體頂點處理時，256矩陣可用於已編制索引的頂點混色（不論是否有一般混合）。

 

## <a name="passing-matrix-indices-to-direct3d"></a>將矩陣索引傳遞給 Direct3D

全球矩陣索引可以使用舊版頂點著色器（FVF 或宣告）傳遞給 Direct3D。

下列程式碼範例顯示如何使用舊版頂點著色器。


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



使用舊版頂點著色器時，矩陣索引會與使用 D3DFVF XYZBn 旗標的頂點位置一起傳遞 \_ 。 矩陣索引會在 DWORD 內以位元組的形式傳遞，且必須緊接在最後一個頂點權數之後。 您也可以使用 D3DFVF XYZBn 來傳遞頂點加權 \_ 。 封裝的 DWORD 包含 index3、index2.cshtml.cs、>index1 和 index0，其中 index0 位於 DWORD 的最小位元組中。 使用的世界矩陣索引數目等於傳遞給用來進行混色的矩陣數目（如 [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md)所定義）。

使用宣告時，D3DVSDE BLENDINDICES 會 \_ 定義要從中取得矩陣索引的輸入頂點暫存器。 矩陣索引必須以 D3DVSDT UBYTE4 的形式傳遞 \_ 。

下列程式碼範例顯示如何使用宣告。 請注意，除非使用固定函式頂點著色器，否則元件的順序不再重要。

以下是頂點宣告。


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



以下是對應的 register 宣告。


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[索引頂點混色](indexed-vertex-blending.md)
</dt> </dl>

 

 
