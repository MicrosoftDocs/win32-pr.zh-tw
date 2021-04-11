---
description: 您可以在頂點資料中提供 Alpha 資料。 若要啟用頂點 Alpha，請將 D3DRS \_ DIFFUSEMATERIALSOURCE 設定為 D3DMCS \_ COLOR1，讓 Direct3D 執行時間從擴散色彩（而非材質）取得擴散值。
ms.assetid: 2b0d842d-ee7d-4633-846d-96697153adc7
title: " (Direct3D 9) 的頂點 Alpha"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f661c013e324a0bf209b4faca41d1974a41e81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108833"
---
# <a name="vertex-alpha-direct3d-9"></a> (Direct3D 9) 的頂點 Alpha

您可以在頂點資料中提供 Alpha 資料。 若要啟用頂點 Alpha，請將 D3DRS \_ DIFFUSEMATERIALSOURCE 設定為 D3DMCS \_ COLOR1，讓 Direct3D 執行時間從擴散色彩（而非材質）取得擴散值。


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE,  
                                D3DMCS_COLOR1 );
```



然後，在漫射色彩中提供 Alpha 值。 AddAlphaToASphere 函式會將 Alpha 新增至球體的頂點。 以下是如何提供 Alpha 資訊給函數的範例。


```
AddAlphaToASphere( m_pObstacleVertices, 12,  
                    D3DRGBA(light.dcvDiffuse.r, light.dcvDiffuse.g, 
                            light.dcvDiffuse.b, vAlpha ));
```



這就是函式看起來的樣子。


```
 
void AddAlphaToASphere(D3DLVERTEX* pVertices, DWORD dwNumRings, D3DCOLOR lightcolor)
{
    WORD x, y;
    // rings around
    for( y=0; y < dwNumRings; y++ )
        for( x=0; x < (dwNumRings*2)+1; x++ )
            (pVertices++)->color = lightcolor;

    // top and bottom
    (pVertices++)->color = lightcolor;
    (pVertices++)->color = lightcolor;
}
```



AddAlphaToASphere 只會修改 D3DLVERTEX 類型的每個頂點的色彩成員，以包含 Alpha 資訊。

D3DLVERTEX 看起來會像這樣。


```
 
// Lit vertex
typedef struct {
    D3DVALUE x, y, z;
    DWORD dwReserved;
    D3DCOLOR color, specular;
    D3DVALUE tu, tv;
} D3DLVERTEX, *LPD3DLVERTEX;
```



繪製球體，


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

//...

// Draw the lit sphere
m_pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX,
                                    m_pObstacleVertices, m_dwNumObstacleVertices,
                                    m_pObstacleIndices,  m_dwNumObstacleIndices, 0 );
```



使用頂點 Alpha 產生透明球體。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Alpha 混色](alpha-blending.md)
</dt> </dl>

 

 



