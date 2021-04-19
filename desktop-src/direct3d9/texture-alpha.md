---
description: 紋理也可以提供 Alpha 值。
ms.assetid: b9f53783-d4d8-4339-8cf3-5ad8305ff627
title: " (Direct3D 9) 的材質 Alpha"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694f8a72d3faede36c3e69ce1b6841b8f6450a3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970900"
---
# <a name="texture-alpha-direct3d-9"></a><span data-ttu-id="f36f1-103"> (Direct3D 9) 的材質 Alpha</span><span class="sxs-lookup"><span data-stu-id="f36f1-103">Texture Alpha (Direct3D 9)</span></span>

<span data-ttu-id="f36f1-104">紋理也可以提供 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="f36f1-104">Alpha values can also be provided by textures.</span></span> <span data-ttu-id="f36f1-105">首先，必須建立紋理。</span><span class="sxs-lookup"><span data-stu-id="f36f1-105">First, the texture must be created.</span></span> <span data-ttu-id="f36f1-106">其次，Alpha 值必須新增至材質。</span><span class="sxs-lookup"><span data-stu-id="f36f1-106">Second, the alpha values must be added to the texture.</span></span> <span data-ttu-id="f36f1-107">若要以材質呈現，請將材質設定為材質階段，然後選取適當的材質階段作業和運算元。</span><span class="sxs-lookup"><span data-stu-id="f36f1-107">To render with the texture, set the texture to a texture stage and select the appropriate texture stage operation and operands.</span></span> <span data-ttu-id="f36f1-108">呼叫 draw 時，將會以透明的方式呈現基本。</span><span class="sxs-lookup"><span data-stu-id="f36f1-108">When draw is called, the primitive will be rendered with transparency.</span></span> <span data-ttu-id="f36f1-109">這個範例會建立材質資源，然後載入 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="f36f1-109">This example creates a texture resource, and then loads the alpha channel.</span></span>


```
LPDIRECT3DTEXTURE9 m_pTexture;

// Create an alpha texture
D3DXCreateTexture(m_d3dDevice, 128, 128, 0, D3DUSAGE_RENDERTARGET, 
    D3DFMT_A8R8G8B8, D3DPOOL_MANAGED, &m_pTexture);

// Initialize the alpha channel
int  yGrad, xGrad;
D3DLOCKED_RECT lockedRect;

if(SUCCEEDED(pTexture->LockRect(0, &lockedRect, NULL, D3DLOCK_DISCARD )))
{
    m_pRGBAData = new DWORD[128*128];
    if( m_pRGBAData != NULL )
    {
        for( DWORD y=0; y < m_dwHeight; y++ )
        {   
            DWORD dwOffset = y*m_dwWidth;
            yGrad = (int)(((float)y/(float)m_dwWidth) * 255.0f);
            
            for( DWORD x=0; x < m_dwWidth; x )
            {
                xGrad = (int)(((float)x/(float)m_dwWidth) * 255.0f);

                DWORD b = (DWORD)(xGrad + (255 - yGrad))/2 & 0xFF;
                DWORD g = (DWORD)((255 - xGrad) + yGrad)/2 & 0xFF;
                DWORD r = (DWORD)(xGrad + yGrad)/2 & 0xFF;
                DWORD a = (DWORD)(xGrad + yGrad)/2 & 0xFF;

                lockedRect.pBits[dwOffset+x] = ((a<<24L)+(r<<16L)+(g<<8L)+(b));
                x++;
            }
        }
    }
    pTexture->UnlockRect(&lockedRect);
}
```



<span data-ttu-id="f36f1-110">Alpha 值是根據紋理大小中目前圖元的相對 x/y 位置計算。</span><span class="sxs-lookup"><span data-stu-id="f36f1-110">The alpha value is calculated based on the current pixel's relative x/y position within the texture size.</span></span> <span data-ttu-id="f36f1-111">接下來，將材質指派給紋理階段，並設定材質階段。</span><span class="sxs-lookup"><span data-stu-id="f36f1-111">Next, assign the texture to a texture stage and set up the texture stage.</span></span>


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

// Assign texture
m_pd3dDevice->SetTexture(0, m_pTexture);

// Texture stage states
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);  

m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE);

m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE);
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG2, D3DTA_DIFFUSE);

m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAOP, D3DTOP_MODULATE);

```



<span data-ttu-id="f36f1-112">這會產生具有透明度漸層的基本物件。</span><span class="sxs-lookup"><span data-stu-id="f36f1-112">This results in a primitive with a transparency gradient.</span></span> <span data-ttu-id="f36f1-113">漸層是透明的，其中 x = 0，而不是不透明，其中 x 是其最大值。</span><span class="sxs-lookup"><span data-stu-id="f36f1-113">The gradient is transparent where x = 0, and opaque where x is its maximum value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f36f1-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="f36f1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f36f1-115">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="f36f1-115">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



