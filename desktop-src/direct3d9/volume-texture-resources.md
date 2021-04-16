---
description: 磁片區材質是三維的圖元集合 (材質) ，可用來繪製二維琪本類型，例如三角形或線條。
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: " (Direct3D 9) 的音量材質資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c66ff97d04e3c7c6c0a032f9a230dfd511b38c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551211"
---
# <a name="volume-texture-resources-direct3d-9"></a><span data-ttu-id="02124-103"> (Direct3D 9) 的音量材質資源</span><span class="sxs-lookup"><span data-stu-id="02124-103">Volume Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="02124-104">磁片區材質是三維的圖元集合 (材質) ，可用來繪製二維琪本類型，例如三角形或線條。</span><span class="sxs-lookup"><span data-stu-id="02124-104">Volume textures are three-dimensional collections of pixels (texels) that can be used to paint a two-dimensional primitive such as a triangle or a line.</span></span> <span data-ttu-id="02124-105">需要三個元素的材質座標，才能以磁片區作為紋理的每個頂點。</span><span class="sxs-lookup"><span data-stu-id="02124-105">Three-element texture coordinates are required for each vertex of a primitive that is to be textured with a volume.</span></span> <span data-ttu-id="02124-106">繪製基本型別時，每個包含的圖元都會根據類似于二維材質案例的規則，填滿磁片區中某個圖元的色彩值。</span><span class="sxs-lookup"><span data-stu-id="02124-106">As the primitive is drawn, each contained pixel is filled with the color value from some pixel within the volume, in accordance with rules analogous to the two-dimensional texture case.</span></span> <span data-ttu-id="02124-107">磁片區不會直接轉譯，因為沒有可與其繪製的三維琪本專案。</span><span class="sxs-lookup"><span data-stu-id="02124-107">Volumes are not rendered directly because there are no three-dimensional primitives that can be painted with them.</span></span>

<span data-ttu-id="02124-108">您可以使用磁片區紋理來取得特殊效果，例如 patchy 霧化、爆炸等等。</span><span class="sxs-lookup"><span data-stu-id="02124-108">You can use volume textures for special effects such as patchy fog, explosions, and so on.</span></span>

<span data-ttu-id="02124-109">磁片區會組織成配量，並可將寬度 x 高度2D 介面視為堆疊，以使寬度 x 高度 x 深度量。</span><span class="sxs-lookup"><span data-stu-id="02124-109">Volumes are organized into slices and can be thought of as width x height 2D surfaces stacked to make a width x height x depth volume.</span></span> <span data-ttu-id="02124-110">每個配量都是單一資料列。</span><span class="sxs-lookup"><span data-stu-id="02124-110">Each slice is a single row.</span></span> <span data-ttu-id="02124-111">磁片區可以有後續層級，其中每個層級的維度會截斷為前一個層級的一半。</span><span class="sxs-lookup"><span data-stu-id="02124-111">Volumes can have subsequent levels in which the dimensions of each level are truncated to half the dimensions of the previous level.</span></span> <span data-ttu-id="02124-112">下圖顯示具有多個層級的音量材質看起來是什麼樣子。</span><span class="sxs-lookup"><span data-stu-id="02124-112">The following diagram shows what a volume texture with multiple levels looks like.</span></span>

![具有8x2x4、4x1x2 和 2x1x1 cube 標記法之磁片區材質的圖表](images/level123.png)

## <a name="creating-a-volume-texture"></a><span data-ttu-id="02124-114">建立磁片區材質</span><span class="sxs-lookup"><span data-stu-id="02124-114">Creating a Volume Texture</span></span>

<span data-ttu-id="02124-115">下列程式碼範例顯示使用磁片區材質所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="02124-115">The code examples below show the steps required to use a volume texture.</span></span>

<span data-ttu-id="02124-116">首先，請針對每個頂點指定具有三個材質座標的自訂頂點型別，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="02124-116">First, specify a custom vertex type that has three texture coordinates for each vertex, as shown in this code example.</span></span>


```
struct VOLUMEVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu, tv, tw;
};

#define D3DFVF_VOLUMEVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|
                             D3DFVF_TEX1|D3DFVF_TEXCOORDSIZE3(0))
```



<span data-ttu-id="02124-117">接下來，使用資料填滿頂點。</span><span class="sxs-lookup"><span data-stu-id="02124-117">Next, fill the vertices with data.</span></span>


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



<span data-ttu-id="02124-118">現在，建立頂點緩衝區，並將頂點中的資料填入其中。</span><span class="sxs-lookup"><span data-stu-id="02124-118">Now, create a vertex buffer and fill it with data from the vertices.</span></span>

<span data-ttu-id="02124-119">下一步是使用 [**IDirect3DDevice9：： CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) 方法來建立磁片區材質，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="02124-119">The next step is to use the [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) method to create a volume texture, as shown in this code example.</span></span>


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



<span data-ttu-id="02124-120">轉譯原始物件之前，請先將目前材質設定為上面建立的音量材質。</span><span class="sxs-lookup"><span data-stu-id="02124-120">Before rendering the primitive, set the current texture to the volume texture created above.</span></span> <span data-ttu-id="02124-121">下列程式碼範例會顯示一條三角形的整個轉譯程式。</span><span class="sxs-lookup"><span data-stu-id="02124-121">The code example below shows the entire rendering process for a strip of triangles.</span></span>


```
if( SUCCEEDED( d3dDevice->BeginScene() ) )
{
    // Draw the quad, with the volume texture.
    d3dDevice->SetTexture( 0, pVolumeTexture );
    d3dDevice->SetFVF( D3DFVF_VOLUMEVERTEX );
    d3dDevice->SetStreamSource( 0, pVB, sizeof(VOLUMEVERTEX) );
    d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 2);

   // End the scene.
   d3dDevice->EndScene();
}
```



## <a name="related-topics"></a><span data-ttu-id="02124-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="02124-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02124-123">Direct3D 紋理</span><span class="sxs-lookup"><span data-stu-id="02124-123">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
