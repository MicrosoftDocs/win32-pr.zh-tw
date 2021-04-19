---
description: 您可以藉由呼叫 IDirect3DDevice9：： CreateVertexBuffer 方法（可接受五個參數）來建立頂點緩衝區物件。
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: " (Direct3D 9) 建立頂點緩衝區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc831ab508f14d61b8e42861f75422ff6a04bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971972"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="cf239-103"> (Direct3D 9) 建立頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="cf239-103">Creating a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="cf239-104">您可以藉由呼叫 [**IDirect3DDevice9：： CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) 方法（可接受五個參數）來建立頂點緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="cf239-104">You create a vertex buffer object by calling the [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method, which accepts five parameters.</span></span> <span data-ttu-id="cf239-105">第一個參數會指定頂點緩衝區長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cf239-105">The first parameter specifies the vertex buffer length, in bytes.</span></span> <span data-ttu-id="cf239-106">使用 sizeof 運算子來判斷頂點格式的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cf239-106">Use the sizeof operator to determine the size of a vertex format, in bytes.</span></span> <span data-ttu-id="cf239-107">請考慮下列自訂頂點格式。</span><span class="sxs-lookup"><span data-stu-id="cf239-107">Consider the following custom vertex format.</span></span>


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



<span data-ttu-id="cf239-108">若要建立頂點緩衝區來保存四個 CUSTOMVERTEX 結構， \[ 請 \* \] 為 *Length* 參數指定 4 sizeof (CUSTOMVERTEX) 。</span><span class="sxs-lookup"><span data-stu-id="cf239-108">To create a vertex buffer to hold four CUSTOMVERTEX structures, specify \[4\*sizeof(CUSTOMVERTEX)\] for the *Length* parameter.</span></span>

<span data-ttu-id="cf239-109">第二個參數是一組使用方式控制項。</span><span class="sxs-lookup"><span data-stu-id="cf239-109">The second parameter is a set of usage controls.</span></span> <span data-ttu-id="cf239-110">此外，它的值會決定頂點緩衝區是否能夠包含剪切資訊（以剪輯旗標的形式），也就是存在於視圖區域外部的頂點。</span><span class="sxs-lookup"><span data-stu-id="cf239-110">Among other things, its value determines whether the vertex buffer is capable of containing clipping information - in the form of clip flags - for vertices that exist outside the viewing area.</span></span> <span data-ttu-id="cf239-111">若要建立不能包含剪輯旗標的頂點緩衝區，請包括 \_ *Usage* 參數的 D3DUSAGE DONOTCLIP 旗標。</span><span class="sxs-lookup"><span data-stu-id="cf239-111">To create a vertex buffer that cannot contain clip flags, include the D3DUSAGE\_DONOTCLIP flag for the *Usage* parameter.</span></span> <span data-ttu-id="cf239-112">\_只有當您也指出頂點緩衝區將包含已轉換的頂點時，才會套用 D3DUSAGE DONOTCLIP 旗標-D3DFVF \_ XYZRHW 旗標包含在 *FVF* 參數中。</span><span class="sxs-lookup"><span data-stu-id="cf239-112">The D3DUSAGE\_DONOTCLIP flag is applied only if you also indicate that the vertex buffer will contain transformed vertices - the D3DFVF\_XYZRHW flag is included in the *FVF* parameter.</span></span> <span data-ttu-id="cf239-113">[](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) \_ 如果您指出緩衝區將包含未轉換的頂點 (D3DFVF XYZ 旗標) ，IDirect3DDevice9：： CreateVertexBuffer 方法會忽略 D3DUSAGE DONOTCLIP 旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cf239-113">The [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method ignores the D3DUSAGE\_DONOTCLIP flag if you indicate that the buffer will contain untransformed vertices (the D3DFVF\_XYZ flag).</span></span> <span data-ttu-id="cf239-114">裁剪旗標佔用額外的記憶體，讓支援裁剪的頂點緩衝區稍微大於無法包含剪切旗標的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cf239-114">Clipping flags occupy additional memory, making a clipping-capable vertex buffer slightly larger than a vertex buffer incapable of containing clipping flags.</span></span> <span data-ttu-id="cf239-115">由於這些資源會在建立頂點緩衝區時配置，因此您必須事先要求支援裁剪的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cf239-115">Because these resources are allocated when the vertex buffer is created, you must request a clipping-capable vertex buffer ahead of time.</span></span>

<span data-ttu-id="cf239-116">第三個參數 *FVF* 是描述頂點緩衝區頂點格式的 [D3DFVF](d3dfvf.md) 組合。</span><span class="sxs-lookup"><span data-stu-id="cf239-116">The third parameter, *FVF*, is a combination of [D3DFVF](d3dfvf.md) that describe the vertex format of the vertex buffer.</span></span> <span data-ttu-id="cf239-117">如果您為此參數指定0，則頂點緩衝區為非 FVF 的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cf239-117">If you specify 0 for this parameter, then the vertex buffer is a non-FVF vertex buffer.</span></span> <span data-ttu-id="cf239-118">如需詳細資訊，請參閱 [FVF Direct3D 9 (的頂點緩衝區) ](fvf-vertex-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="cf239-118">For more information, see [FVF Vertex Buffers (Direct3D 9)](fvf-vertex-buffers.md).</span></span> <span data-ttu-id="cf239-119">第四個參數描述用來放置頂點緩衝區的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="cf239-119">The fourth parameter describes the memory class into which to place the vertex buffer.</span></span>

<span data-ttu-id="cf239-120">[**IDirect3DDevice9：： CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)所接受的最後一個參數是變數的位址，如果呼叫成功，將會以頂點緩衝區物件的新 [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)介面指標填滿。</span><span class="sxs-lookup"><span data-stu-id="cf239-120">The final parameter that [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) accepts is the address of a variable that will be filled with a pointer to the new [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface of the vertex buffer object, if the call succeeds.</span></span>

<span data-ttu-id="cf239-121">您無法產生不支援的頂點緩衝區的剪切旗標。</span><span class="sxs-lookup"><span data-stu-id="cf239-121">You cannot produce clip flags for a vertex buffer that was created without support for them.</span></span>

<span data-ttu-id="cf239-122">下列 c + + 程式碼範例示範如何在程式碼中建立頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cf239-122">The following C++ code example shows what creating a vertex buffer might look like in code.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cf239-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf239-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf239-124">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="cf239-124">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
