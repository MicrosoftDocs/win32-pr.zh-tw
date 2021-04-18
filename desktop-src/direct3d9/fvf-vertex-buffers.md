---
description: 將 IDirect3DDevice9：： CreateVertexBuffer 方法的 FVF 參數設定為非零值（必須是有效的 FVF 碼），表示緩衝區內容是以 FVF 程式碼為特徵。
ms.assetid: 7cab559f-3e9d-46bd-b00f-439e0922aeeb
title: FVF (Direct3D 9) 的頂點緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86201c3ddc1cab6d492539caccc61c1430b3a2c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971275"
---
# <a name="fvf-vertex-buffers-direct3d-9"></a><span data-ttu-id="31afa-103">FVF (Direct3D 9) 的頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="31afa-103">FVF Vertex Buffers (Direct3D 9)</span></span>

<span data-ttu-id="31afa-104">將 [**IDirect3DDevice9：： CreateVertexBuffer**](/windows/desktop/api) 方法的 FVF 參數設定為非零值（必須是有效的 FVF 碼），表示緩衝區內容是以 FVF 程式碼為特徵。</span><span class="sxs-lookup"><span data-stu-id="31afa-104">Setting the FVF parameter of the [**IDirect3DDevice9::CreateVertexBuffer**](/windows/desktop/api) method to a nonzero value, which must be a valid FVF code, indicates that the buffer content is to be characterized by an FVF code.</span></span> <span data-ttu-id="31afa-105">使用 FVF 程式碼建立的頂點緩衝區稱為 FVF 頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="31afa-105">A vertex buffer that is created with an FVF code is referred to as an FVF vertex buffer.</span></span> <span data-ttu-id="31afa-106">某些方法或使用 [**IDirect3DDevice9**](/windows/desktop/api) 需要 FVF 頂點緩衝區，而其他方法則需要非 FVF 的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="31afa-106">Some methods or uses of [**IDirect3DDevice9**](/windows/desktop/api) require FVF vertex buffers, and others require non-FVF vertex buffers.</span></span> <span data-ttu-id="31afa-107">FVF 頂點緩衝區必須是 [**IDirect3DDevice9：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices)的目的地頂點緩衝區引數。</span><span class="sxs-lookup"><span data-stu-id="31afa-107">FVF vertex buffers are required as the destination vertex buffer argument for [**IDirect3DDevice9::ProcessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).</span></span>

<span data-ttu-id="31afa-108">FVF 頂點緩衝區可以系結至任何資料流程編號的來源資料流。</span><span class="sxs-lookup"><span data-stu-id="31afa-108">FVF vertex buffers can be bound to a source data stream for any stream number.</span></span>

<span data-ttu-id="31afa-109">\_FVF 頂點緩衝區上的 D3DFVF XYZRHW 元件是否存在，表示該緩衝區中的頂點已經過處理。</span><span class="sxs-lookup"><span data-stu-id="31afa-109">The presence of the D3DFVF\_XYZRHW component on FVF vertex buffers indicates that the vertices in that buffer have been processed.</span></span> <span data-ttu-id="31afa-110">用於 IDirect3DDevice9 的頂點緩衝區 [**：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) 目的地頂點緩衝區必須經過後置處理。</span><span class="sxs-lookup"><span data-stu-id="31afa-110">Vertex buffers used for [**IDirect3DDevice9::ProcessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) destination vertex buffers must be post-processed.</span></span> <span data-ttu-id="31afa-111">用於固定函式著色器輸入的頂點緩衝區可以是前置處理或 postprocessed。</span><span class="sxs-lookup"><span data-stu-id="31afa-111">Vertex buffers used for fixed function shader inputs can be either preprocessed or postprocessed.</span></span> <span data-ttu-id="31afa-112">如果頂點緩衝區經過處理後，則會有效地略過著色器，並將資料直接傳遞至基本剪切和設定模組。</span><span class="sxs-lookup"><span data-stu-id="31afa-112">If the vertex buffer is post-processed, then the shader is effectively bypassed and the data is passed directly to the primitive clipping and setup module.</span></span>

<span data-ttu-id="31afa-113">FVF 頂點緩衝區可以搭配頂點著色器使用。</span><span class="sxs-lookup"><span data-stu-id="31afa-113">FVF vertex buffers can be used with vertex shaders.</span></span> <span data-ttu-id="31afa-114">此外，頂點資料流程也可以代表非 FVF 頂點緩衝區可以有的相同頂點格式。</span><span class="sxs-lookup"><span data-stu-id="31afa-114">Also, vertex streams can represent the same vertex formats that non-FVF vertex buffers can.</span></span> <span data-ttu-id="31afa-115">它們不需要用來輸入來自不同頂點緩衝區的資料。</span><span class="sxs-lookup"><span data-stu-id="31afa-115">They do not have to be used to input data from separate vertex buffers.</span></span> <span data-ttu-id="31afa-116">新頂點資料流程的額外彈性可讓需要保持資料不同的應用程式能夠更妥善地運作，但這並不是必要的。</span><span class="sxs-lookup"><span data-stu-id="31afa-116">The additional flexibility of the new vertex streams enables applications that need to keep their data separate to work better, but it is not required.</span></span> <span data-ttu-id="31afa-117">如果應用程式可以事先維護交錯的資料，就能提升效能。</span><span class="sxs-lookup"><span data-stu-id="31afa-117">If the application can maintain interleaved data in advance, then that is a performance boost.</span></span> <span data-ttu-id="31afa-118">如果應用程式只會在每次轉譯呼叫之前交錯資料，則應該啟用 API 或硬體以使用多個資料流程來進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="31afa-118">If the application will only interleave the data before every rendering call, then it should enable the API or hardware to do this with multiple streams.</span></span>

<span data-ttu-id="31afa-119">頂點效能最重要的事項是使用32位元組頂點，並維護良好的快取順序。</span><span class="sxs-lookup"><span data-stu-id="31afa-119">The most important things with vertex performance is to use a 32-byte vertex, and to maintain good cache ordering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31afa-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="31afa-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31afa-121">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="31afa-121">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
