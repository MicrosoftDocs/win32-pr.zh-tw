---
description: 從頂點緩衝區轉譯頂點資料需要執行幾個步驟。 首先，您必須呼叫 IDirect3DDevice9：： SetStreamSource 方法來設定資料流程來源，如下列範例所示。
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: '從頂點緩衝區轉譯 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108453"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="10c96-104">從頂點緩衝區轉譯 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="10c96-104">Rendering from a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="10c96-105">從頂點緩衝區轉譯頂點資料需要執行幾個步驟。</span><span class="sxs-lookup"><span data-stu-id="10c96-105">Rendering vertex data from a vertex buffer requires a few steps.</span></span> <span data-ttu-id="10c96-106">首先，您必須呼叫 [**IDirect3DDevice9：： SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) 方法來設定資料流程來源，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="10c96-106">First, you need to set the stream source by calling the [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) method, as shown in the following example.</span></span>


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



<span data-ttu-id="10c96-107">[**IDirect3DDevice9：： SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)的第一個參數會告訴 Direct3D 該裝置資料流程的來源。</span><span class="sxs-lookup"><span data-stu-id="10c96-107">The first parameter of [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) tells Direct3D the source of the device data stream.</span></span> <span data-ttu-id="10c96-108">第二個參數是要系結至資料流程的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="10c96-108">The second parameter is the vertex buffer to bind to the data stream.</span></span> <span data-ttu-id="10c96-109">第三個參數是從資料流程開頭到頂點資料開頭的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="10c96-109">The third parameter is the offset from the beginning of the stream to the beginning of the vertex data, in bytes.</span></span> <span data-ttu-id="10c96-110">第四個參數是元件的 stride （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="10c96-110">The fourth parameter is the stride of the component, in bytes.</span></span> <span data-ttu-id="10c96-111">在上述的範例程式碼中，CUSTOMVERTEX 的大小會用於元件的 stride。</span><span class="sxs-lookup"><span data-stu-id="10c96-111">In the sample code above, the size of a CUSTOMVERTEX is used for the stride of the component.</span></span>

<span data-ttu-id="10c96-112">下一步是透過呼叫 [**IDirect3DDevice9：： SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) 方法，通知 Direct3D 要使用哪個頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="10c96-112">The next step is to inform Direct3D which vertex shader to use by calling the [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) method.</span></span> <span data-ttu-id="10c96-113">下列範例程式碼會設定頂點著色器的 FVF 碼。</span><span class="sxs-lookup"><span data-stu-id="10c96-113">The following sample code sets an FVF code for the vertex shader.</span></span> <span data-ttu-id="10c96-114">這會通知 Direct3D 其正在處理的頂點類型。</span><span class="sxs-lookup"><span data-stu-id="10c96-114">This informs Direct3D of the types of vertices it is dealing with.</span></span>


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



<span data-ttu-id="10c96-115">設定資料流程來源和頂點著色器之後，任何繪製方法都將使用頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="10c96-115">After setting the stream source and vertex shader, any draw methods will use the vertex buffer.</span></span> <span data-ttu-id="10c96-116">下列程式碼範例顯示如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 方法，從頂點緩衝區轉譯頂點。</span><span class="sxs-lookup"><span data-stu-id="10c96-116">The code example below shows how to render vertices from a vertex buffer with the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method.</span></span>


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



<span data-ttu-id="10c96-117">[**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)所接受的第二個參數是要載入之頂點緩衝區中第一個向量的索引。</span><span class="sxs-lookup"><span data-stu-id="10c96-117">The second parameter that [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepts is the index of the first vector in the vertex buffer to load.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10c96-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="10c96-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10c96-119">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="10c96-119">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> <dt>

[<span data-ttu-id="10c96-120">從頂點和索引緩衝區轉譯 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="10c96-120">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
