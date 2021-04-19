---
description: 本節說明可用於可程式化資料流程模型的著色器。
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: '將一或多個串流程式設計 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106997058"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a><span data-ttu-id="cd810-103">將一或多個串流程式設計 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="cd810-103">Programming One or More Streams (Direct3D 9)</span></span>

<span data-ttu-id="cd810-104">本節說明可用於可程式化資料流程模型的著色器。</span><span class="sxs-lookup"><span data-stu-id="cd810-104">This section describes shaders that can be used for the programmable stream model.</span></span>

## <a name="using-streams"></a><span data-ttu-id="cd810-105">使用資料流程</span><span class="sxs-lookup"><span data-stu-id="cd810-105">Using Streams</span></span>

<span data-ttu-id="cd810-106">DirectX 8 引進了串流的概念，可將資料系結至輸入暫存器以供著色器使用。</span><span class="sxs-lookup"><span data-stu-id="cd810-106">DirectX 8 introduced the notion of a stream to bind data to input registers for use by shaders.</span></span> <span data-ttu-id="cd810-107">資料流程是元件資料的統一陣列，其中每個元件都是由一或多個代表單一實體的元素組成，例如位置、正常、色彩等等。</span><span class="sxs-lookup"><span data-stu-id="cd810-107">A stream is a uniform array of component data, where each component consists of one or more elements that represent a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="cd810-108">資料流程可讓圖形晶片平行執行多個頂點緩衝區的直接記憶體存取，同時也提供應用程式資料更自然的對應。</span><span class="sxs-lookup"><span data-stu-id="cd810-108">Streams enable graphic chips to perform a direct memory access from multiple vertex buffers in parallel and also provide a more natural mapping from application data.</span></span> <span data-ttu-id="cd810-109">它們也啟用了簡單的多紋理與 multipass。</span><span class="sxs-lookup"><span data-stu-id="cd810-109">They also enable trivial multitexture versus multipass.</span></span> <span data-ttu-id="cd810-110">請將它想成：</span><span class="sxs-lookup"><span data-stu-id="cd810-110">Think of it like this:</span></span>

-   <span data-ttu-id="cd810-111">頂點由 n 個數據流所組成。</span><span class="sxs-lookup"><span data-stu-id="cd810-111">A vertex is composed of n streams.</span></span>
-   <span data-ttu-id="cd810-112">資料流程是由 m 元素組成。</span><span class="sxs-lookup"><span data-stu-id="cd810-112">A stream is composed of m elements.</span></span>
-   <span data-ttu-id="cd810-113">專案是 \[ 位置、色彩、標準、材質座標 \] 。</span><span class="sxs-lookup"><span data-stu-id="cd810-113">An element is \[position, color, normal, texture coordinate\].</span></span>

<span data-ttu-id="cd810-114">[**IDirect3DDevice9：： SetStreamSource**](/windows/desktop/api)方法會將頂點緩衝區系結至裝置資料流程，建立頂點資料與饋送基本處理函式的數個數據流埠之一之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="cd810-114">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="cd810-115">在呼叫 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)之類的繪圖方法之前，不會發生資料流程資料的實際參考。</span><span class="sxs-lookup"><span data-stu-id="cd810-115">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="cd810-116">輸入頂點元素與可程式化頂點著色器之頂點輸入暫存器的對應是在著色器宣告中定義，但輸入頂點元素沒有與其使用相關的特定語義。</span><span class="sxs-lookup"><span data-stu-id="cd810-116">The mapping of the input vertex elements to the vertex input registers for programmable vertex shaders is defined in the shader declaration, but the input vertex elements do not have specific semantics about their use.</span></span> <span data-ttu-id="cd810-117">輸入頂點元素的解讀是使用著色器指示進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="cd810-117">The interpretation of the input vertex elements is programmed using the shader instructions.</span></span> <span data-ttu-id="cd810-118">頂點著色器函式是由套用至每個頂點的指令陣列所定義。</span><span class="sxs-lookup"><span data-stu-id="cd810-118">The vertex shader function is defined by an array of instructions that are applied to each vertex.</span></span> <span data-ttu-id="cd810-119">您可以使用著色器函式中的指示，將頂點輸出暫存器明確寫入至。</span><span class="sxs-lookup"><span data-stu-id="cd810-119">The vertex output registers are explicitly written to, using instructions in the shader function.</span></span>

<span data-ttu-id="cd810-120">不過，在此討論中，比較不在意專案的語義對應，並更在意使用資料流程的原因，以及使用資料流程解決的問題。</span><span class="sxs-lookup"><span data-stu-id="cd810-120">For this discussion, though, be less concerned with the semantic mapping of elements to registers and more concerned with the reason for using streams and what problem is solved by using streams.</span></span> <span data-ttu-id="cd810-121">資料流程的主要優點是，它們會移除先前與 multitexturing 相關聯的頂點資料成本。</span><span class="sxs-lookup"><span data-stu-id="cd810-121">The main benefit of streams is that they remove the vertex data costs previously associated with multitexturing.</span></span> <span data-ttu-id="cd810-122">在串流之前，使用者必須複製頂點資料集來處理沒有未使用之資料元素的單一和多紋理案例，或包含不會在多紋理案例中使用的資料元素。</span><span class="sxs-lookup"><span data-stu-id="cd810-122">Before streams, a user had to either duplicate vertex data sets to handle the single and multitexture case with no unused data elements, or carry data elements that would be unused except in the multitexture case.</span></span>

<span data-ttu-id="cd810-123">以下是使用兩組頂點資料的範例，一個用於單一材質，另一個用於 multitexturing。</span><span class="sxs-lookup"><span data-stu-id="cd810-123">Here is an example of using two sets of vertex data, one for single texture and one for multitexturing.</span></span>


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="cd810-124">替代方法是具有包含兩組材質座標的單一頂點元素。</span><span class="sxs-lookup"><span data-stu-id="cd810-124">The alternative was to have a single vertex element that contained both sets of texture coordinates.</span></span>


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="cd810-125">使用這個頂點資料，只會在記憶體中攜帶一個位置和色彩資料複本，因為即使是在單一材質案例中，仍會有這兩組紋理座標，以供轉譯之用。</span><span class="sxs-lookup"><span data-stu-id="cd810-125">With this vertex data, only one copy of the position and color data are carried in memory, at the expense of carrying both sets of texture coordinates around for rendering even in the single texture case.</span></span>

<span data-ttu-id="cd810-126">現在，我們已清楚地解決此問題，資料流程為此難題提供簡潔的修正。</span><span class="sxs-lookup"><span data-stu-id="cd810-126">Now that the tradeoff is clear, streams provide an elegant fix to this dilemma.</span></span> <span data-ttu-id="cd810-127">以下是支援三個數據流的一組頂點定義：一個具有位置和色彩，一個具有一組紋理座標，另一個則是第二組材質座標。</span><span class="sxs-lookup"><span data-stu-id="cd810-127">Here is a set of vertex definitions to support three streams: one with position and color, one with the first set of texture coordinates, and one with the second set of texture coordinates.</span></span>


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



<span data-ttu-id="cd810-128">頂點宣告如下所示：</span><span class="sxs-lookup"><span data-stu-id="cd810-128">The vertex declaration would be as follows:</span></span>


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



<span data-ttu-id="cd810-129">現在建立頂點宣告物件，並加以設定，如下所示：</span><span class="sxs-lookup"><span data-stu-id="cd810-129">Now create the vertex declaration object and set it as shown:</span></span>


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a><span data-ttu-id="cd810-130">組合範例</span><span class="sxs-lookup"><span data-stu-id="cd810-130">Examples of Combinations</span></span>

### <a name="one-stream-diffuse-color"></a><span data-ttu-id="cd810-131">一個資料流程擴散色彩</span><span class="sxs-lookup"><span data-stu-id="cd810-131">One Stream Diffuse Color</span></span>

<span data-ttu-id="cd810-132">用於擴散色彩轉譯的頂點宣告和資料流程設定看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="cd810-132">The vertex declaration and stream settings for diffuse color rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a><span data-ttu-id="cd810-133">具有色彩和材質的兩個數據流</span><span class="sxs-lookup"><span data-stu-id="cd810-133">Two Streams with Color and Texture</span></span>

<span data-ttu-id="cd810-134">單一材質轉譯的頂點宣告和資料流程設定看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="cd810-134">The vertex declaration and stream settings for single texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a><span data-ttu-id="cd810-135">兩個具有色彩和兩個材質的資料流程</span><span class="sxs-lookup"><span data-stu-id="cd810-135">Two Streams with Color and two Textures</span></span>

<span data-ttu-id="cd810-136">兩紋理多紋理轉譯的頂點宣告和資料流程設定看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="cd810-136">The vertex declaration and stream settings for two-texture multi-texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



<span data-ttu-id="cd810-137">在每個案例中，下列 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 調用尾碼。</span><span class="sxs-lookup"><span data-stu-id="cd810-137">In every case, the following [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) invocation suffices.</span></span>


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



<span data-ttu-id="cd810-138">這會顯示資料流程的彈性，可解決跨匯流排 (的資料複製/重復資料傳輸問題，也就是浪費頻寬) 。</span><span class="sxs-lookup"><span data-stu-id="cd810-138">This shows the flexibility of streams in solving the problem of data duplication/redundant data transmission across the bus (that is, of wasting bandwidth).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd810-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd810-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd810-140">頂點宣告</span><span class="sxs-lookup"><span data-stu-id="cd810-140">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
