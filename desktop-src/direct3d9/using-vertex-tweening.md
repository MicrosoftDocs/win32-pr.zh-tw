---
description: 若要判斷 Direct3D 是否支援頂點補間，請檢查 \_ D3DCAPS9 結構的 VertexProcessingCaps 成員中是否有 D3DVTXPCAPS 補間旗標。
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: 使用 (Direct3D 9) 的頂點補間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ca56cc521b5bff01a5d6af5c2d4ab6b02cd49e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846167"
---
# <a name="using-vertex-tweening-direct3d-9"></a><span data-ttu-id="27ce4-103">使用 (Direct3D 9) 的頂點補間</span><span class="sxs-lookup"><span data-stu-id="27ce4-103">Using Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="27ce4-104">若要判斷 Direct3D 是否支援頂點補間，請檢查 \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 VertexProcessingCaps 成員中是否有 D3DVTXPCAPS 補間旗標。</span><span class="sxs-lookup"><span data-stu-id="27ce4-104">To determine if Direct3D supports vertex tweening, check for the D3DVTXPCAPS\_TWEENING flag in the VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="27ce4-105">下列程式碼範例會使用 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) 方法來判斷是否支援補間。</span><span class="sxs-lookup"><span data-stu-id="27ce4-105">The following code example uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to determine if tweening is supported.</span></span>


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



<span data-ttu-id="27ce4-106">若要使用向量補間，您必須先設定使用第二個一般或第二個位置的自訂頂點型別。</span><span class="sxs-lookup"><span data-stu-id="27ce4-106">To use vector tweening, you must first set up a custom vertex type that uses a second normal or a second position.</span></span> <span data-ttu-id="27ce4-107">下列程式碼範例顯示包含第二個點和第二個位置的範例宣告。</span><span class="sxs-lookup"><span data-stu-id="27ce4-107">The following code example shows a sample declaration that includes both a second point and a second position.</span></span>


```
struct TEX_VERTEX
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DVECTOR position2;
    D3DVECTOR normal2;
};

//Create a vertex buffer with the type TEX_VERTEX.
```



<span data-ttu-id="27ce4-108">下一步是設定目前的宣告。</span><span class="sxs-lookup"><span data-stu-id="27ce4-108">The next step is to set the current declaration.</span></span> <span data-ttu-id="27ce4-109">下列程式碼範例示範如何進行此動作。</span><span class="sxs-lookup"><span data-stu-id="27ce4-109">The code example below shows how to do this.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    { 0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 1 },
    { 0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 1 },
    D3DDECL_END()
};
```



<span data-ttu-id="27ce4-110">如需有關建立自訂頂點型別和頂點緩衝區的詳細資訊，請參閱 [建立 (Direct3D 9) 的頂點緩衝區 ](creating-a-vertex-buffer.md)。</span><span class="sxs-lookup"><span data-stu-id="27ce4-110">For more information about creating a custom vertex type and a vertex buffer, see [Creating a Vertex Buffer (Direct3D 9)](creating-a-vertex-buffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="27ce4-111">啟用頂點補間時，目前的宣告中必須有第二個位置或第二個。</span><span class="sxs-lookup"><span data-stu-id="27ce4-111">When vertex tweening is enabled, a second position or a second normal must be present in the current declaration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="27ce4-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="27ce4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27ce4-113">頂點 Tweening</span><span class="sxs-lookup"><span data-stu-id="27ce4-113">Vertex Tweening</span></span>](vertex-tweening.md)
</dt> </dl>

 

 
