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
# <a name="using-indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="b5f72-103">使用 (Direct3D 9) 的索引頂點混合</span><span class="sxs-lookup"><span data-stu-id="b5f72-103">Using Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="b5f72-104">轉換狀態256-511 會保留為最多可儲存256矩陣，可使用8位索引來編制索引。</span><span class="sxs-lookup"><span data-stu-id="b5f72-104">Transform states 256-511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span> <span data-ttu-id="b5f72-105">使用宏 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) ，將索引0-255 對應至對應的轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="b5f72-105">Use the macro [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) to map indices 0-255 to the corresponding transform states.</span></span> <span data-ttu-id="b5f72-106">下列程式碼範例示範如何使用 [**IDirect3DDevice9：： SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) 方法，將在轉換狀態編號256的矩陣設定為識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="b5f72-106">The following code example shows how to use the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the matrix at transform state number 256 to an identity matrix.</span></span>


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



<span data-ttu-id="b5f72-107">若要啟用或停用索引頂點混合，請將 D3DRS \_ INDEXEDVERTEXBLENDENABLE 轉譯狀態設為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="b5f72-107">To enable or disable indexed vertex blending, set the D3DRS\_INDEXEDVERTEXBLENDENABLE render state to **TRUE**.</span></span> <span data-ttu-id="b5f72-108">當轉譯狀態為 [已啟用] 時，您必須使用每個頂點傳遞矩陣索引作為封裝的 Dword。</span><span class="sxs-lookup"><span data-stu-id="b5f72-108">When the render state is enabled ,you must pass matrix indices as packed DWORDs with every vertex.</span></span> <span data-ttu-id="b5f72-109">當此轉譯狀態已停用且已啟用頂點混色時，就相當於在每個頂點中都有矩陣索引0、1、2和3。</span><span class="sxs-lookup"><span data-stu-id="b5f72-109">When this render state is disabled and vertex blending is enabled, it is equivalent to having the matrix indices 0, 1, 2, and 3 in every vertex.</span></span> <span data-ttu-id="b5f72-110">下列程式碼範例使用 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法來啟用索引頂點的混合。</span><span class="sxs-lookup"><span data-stu-id="b5f72-110">The code example below uses the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method to enable indexed vertex blending.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



<span data-ttu-id="b5f72-111">若要啟用或停用頂點混合，請將 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 轉譯狀態設定為 [D3DRS \_ 停用] 以外的值（ [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 列舉型別）。</span><span class="sxs-lookup"><span data-stu-id="b5f72-111">To enable or disable vertex blending, set the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) render state to a value other than D3DRS\_DISABLE from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="b5f72-112">如果此轉譯狀態未設定為 [停用 D3DRS] \_ ，則您必須針對每個頂點傳遞所需的加權數目。</span><span class="sxs-lookup"><span data-stu-id="b5f72-112">If this render state is not set to D3DRS\_DISABLE, then you must pass the required number of weights for each vertex.</span></span> <span data-ttu-id="b5f72-113">下列程式碼範例會使用 **IDirect3DDevice9：： graphicsdevice** 來針對每個頂點啟用具有三個加權的頂點混合。</span><span class="sxs-lookup"><span data-stu-id="b5f72-113">The following code example uses **IDirect3DDevice9::SetRenderState** to enable vertex blending with three weights for each vertex.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a><span data-ttu-id="b5f72-114">判斷索引頂點混合支援</span><span class="sxs-lookup"><span data-stu-id="b5f72-114">Determining Indexed Vertex Blending Support</span></span>

<span data-ttu-id="b5f72-115">若要判斷索引頂點混色矩陣的大小上限，請檢查 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 MaxVertexBlendMatrixIndex 成員。</span><span class="sxs-lookup"><span data-stu-id="b5f72-115">To determine the maximum size for the indexed vertex blending matrix, check the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's MaxVertexBlendMatrixIndex member.</span></span> <span data-ttu-id="b5f72-116">下列程式碼範例會使用 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) 方法來取得此大小。</span><span class="sxs-lookup"><span data-stu-id="b5f72-116">The code example below uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to retrieve this size.</span></span>


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



<span data-ttu-id="b5f72-117">如果在 MaxVertexBlendMatrixIndex 中設定的值為0，則裝置不支援索引矩陣。</span><span class="sxs-lookup"><span data-stu-id="b5f72-117">If the value set in MaxVertexBlendMatrixIndex is 0, the device does not support indexed matrices.</span></span>

> [!Note]  
> <span data-ttu-id="b5f72-118">使用軟體頂點處理時，256矩陣可用於已編制索引的頂點混色（不論是否有一般混合）。</span><span class="sxs-lookup"><span data-stu-id="b5f72-118">When software vertex processing is used, 256 matrices can be used for indexed vertex blending, with or without normal blending.</span></span>

 

## <a name="passing-matrix-indices-to-direct3d"></a><span data-ttu-id="b5f72-119">將矩陣索引傳遞給 Direct3D</span><span class="sxs-lookup"><span data-stu-id="b5f72-119">Passing Matrix Indices to Direct3D</span></span>

<span data-ttu-id="b5f72-120">全球矩陣索引可以使用舊版頂點著色器（FVF 或宣告）傳遞給 Direct3D。</span><span class="sxs-lookup"><span data-stu-id="b5f72-120">World matrix indices can be passed to Direct3D by using legacy vertex shaders - FVF - or declarations.</span></span>

<span data-ttu-id="b5f72-121">下列程式碼範例顯示如何使用舊版頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="b5f72-121">The code example below shows how to use legacy vertex shaders.</span></span>


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



<span data-ttu-id="b5f72-122">使用舊版頂點著色器時，矩陣索引會與使用 D3DFVF XYZBn 旗標的頂點位置一起傳遞 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b5f72-122">When a legacy vertex shader is used, matrix indices are passed together with vertex positions using D3DFVF\_XYZBn flags.</span></span> <span data-ttu-id="b5f72-123">矩陣索引會在 DWORD 內以位元組的形式傳遞，且必須緊接在最後一個頂點權數之後。</span><span class="sxs-lookup"><span data-stu-id="b5f72-123">Matrix indices are passed as bytes inside a DWORD and must be present immediately after the last vertex weight.</span></span> <span data-ttu-id="b5f72-124">您也可以使用 D3DFVF XYZBn 來傳遞頂點加權 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b5f72-124">Vertex weights are also passed using D3DFVF\_XYZBn.</span></span> <span data-ttu-id="b5f72-125">封裝的 DWORD 包含 index3、index2.cshtml.cs、>index1 和 index0，其中 index0 位於 DWORD 的最小位元組中。</span><span class="sxs-lookup"><span data-stu-id="b5f72-125">A packed DWORD contains index3, index2, index1, and index0, where index0 is located in the lowest byte of the DWORD.</span></span> <span data-ttu-id="b5f72-126">使用的世界矩陣索引數目等於傳遞給用來進行混色的矩陣數目（如 [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md)所定義）。</span><span class="sxs-lookup"><span data-stu-id="b5f72-126">The number of used world-matrix indices is equal to the number passed to the number of matrices used for blending as defined by [**D3DRS\_VERTEXBLEND**](./d3drenderstatetype.md).</span></span>

<span data-ttu-id="b5f72-127">使用宣告時，D3DVSDE BLENDINDICES 會 \_ 定義要從中取得矩陣索引的輸入頂點暫存器。</span><span class="sxs-lookup"><span data-stu-id="b5f72-127">When a declaration is used, D3DVSDE\_BLENDINDICES defines the input vertex register to get matrix indices from.</span></span> <span data-ttu-id="b5f72-128">矩陣索引必須以 D3DVSDT UBYTE4 的形式傳遞 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b5f72-128">Matrix indices must be passed as D3DVSDT\_UBYTE4.</span></span>

<span data-ttu-id="b5f72-129">下列程式碼範例顯示如何使用宣告。</span><span class="sxs-lookup"><span data-stu-id="b5f72-129">The code example below shows how to use declarations.</span></span> <span data-ttu-id="b5f72-130">請注意，除非使用固定函式頂點著色器，否則元件的順序不再重要。</span><span class="sxs-lookup"><span data-stu-id="b5f72-130">Note that the order of the components is no longer important unless using a fixed-function vertex shader.</span></span>

<span data-ttu-id="b5f72-131">以下是頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="b5f72-131">Here is the vertex declaration.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



<span data-ttu-id="b5f72-132">以下是對應的 register 宣告。</span><span class="sxs-lookup"><span data-stu-id="b5f72-132">Here is the corresponding register declaration.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b5f72-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5f72-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5f72-134">索引頂點混色</span><span class="sxs-lookup"><span data-stu-id="b5f72-134">Indexed Vertex Blending</span></span>](indexed-vertex-blending.md)
</dt> </dl>

 

 
