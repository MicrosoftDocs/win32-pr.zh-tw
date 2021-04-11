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
# <a name="vertex-alpha-direct3d-9"></a><span data-ttu-id="95d7f-104"> (Direct3D 9) 的頂點 Alpha</span><span class="sxs-lookup"><span data-stu-id="95d7f-104">Vertex Alpha (Direct3D 9)</span></span>

<span data-ttu-id="95d7f-105">您可以在頂點資料中提供 Alpha 資料。</span><span class="sxs-lookup"><span data-stu-id="95d7f-105">Alpha data can be supplied in the vertex data.</span></span> <span data-ttu-id="95d7f-106">若要啟用頂點 Alpha，請將 D3DRS \_ DIFFUSEMATERIALSOURCE 設定為 D3DMCS \_ COLOR1，讓 Direct3D 執行時間從擴散色彩（而非材質）取得擴散值。</span><span class="sxs-lookup"><span data-stu-id="95d7f-106">To enable vertex alpha, set the D3DRS\_DIFFUSEMATERIALSOURCE to D3DMCS\_COLOR1 so that the Direct3D runtime takes the diffuse value from the diffuse color rather than the material.</span></span>


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE,  
                                D3DMCS_COLOR1 );
```



<span data-ttu-id="95d7f-107">然後，在漫射色彩中提供 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="95d7f-107">Then, provide alpha values in the diffuse color.</span></span> <span data-ttu-id="95d7f-108">AddAlphaToASphere 函式會將 Alpha 新增至球體的頂點。</span><span class="sxs-lookup"><span data-stu-id="95d7f-108">The AddAlphaToASphere function, adds alpha to the vertices of a sphere.</span></span> <span data-ttu-id="95d7f-109">以下是如何提供 Alpha 資訊給函數的範例。</span><span class="sxs-lookup"><span data-stu-id="95d7f-109">Here's an example of how to provide the alpha information to the function.</span></span>


```
AddAlphaToASphere( m_pObstacleVertices, 12,  
                    D3DRGBA(light.dcvDiffuse.r, light.dcvDiffuse.g, 
                            light.dcvDiffuse.b, vAlpha ));
```



<span data-ttu-id="95d7f-110">這就是函式看起來的樣子。</span><span class="sxs-lookup"><span data-stu-id="95d7f-110">This is what the function looks like.</span></span>


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



<span data-ttu-id="95d7f-111">AddAlphaToASphere 只會修改 D3DLVERTEX 類型的每個頂點的色彩成員，以包含 Alpha 資訊。</span><span class="sxs-lookup"><span data-stu-id="95d7f-111">AddAlphaToASphere simply modifies the color member of each vertex, which are of type D3DLVERTEX, to include the alpha information.</span></span>

<span data-ttu-id="95d7f-112">D3DLVERTEX 看起來會像這樣。</span><span class="sxs-lookup"><span data-stu-id="95d7f-112">D3DLVERTEX looks like this.</span></span>


```
 
// Lit vertex
typedef struct {
    D3DVALUE x, y, z;
    DWORD dwReserved;
    D3DCOLOR color, specular;
    D3DVALUE tu, tv;
} D3DLVERTEX, *LPD3DLVERTEX;
```



<span data-ttu-id="95d7f-113">繪製球體，</span><span class="sxs-lookup"><span data-stu-id="95d7f-113">Drawing the sphere,</span></span>


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

//...

// Draw the lit sphere
m_pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX,
                                    m_pObstacleVertices, m_dwNumObstacleVertices,
                                    m_pObstacleIndices,  m_dwNumObstacleIndices, 0 );
```



<span data-ttu-id="95d7f-114">使用頂點 Alpha 產生透明球體。</span><span class="sxs-lookup"><span data-stu-id="95d7f-114">results in a transparent sphere using vertex alpha.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95d7f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="95d7f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95d7f-116">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="95d7f-116">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



