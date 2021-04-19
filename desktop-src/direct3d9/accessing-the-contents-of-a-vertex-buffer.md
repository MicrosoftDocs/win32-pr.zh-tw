---
description: 頂點緩衝區物件可讓應用程式直接存取配置給頂點資料的記憶體。
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: '存取頂點緩衝區的內容 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973580"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="46cdc-103">存取頂點緩衝區的內容 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="46cdc-103">Accessing the Contents of a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="46cdc-104">頂點緩衝區物件可讓應用程式直接存取配置給頂點資料的記憶體。</span><span class="sxs-lookup"><span data-stu-id="46cdc-104">Vertex buffer objects enable applications to directly access the memory allocated for vertex data.</span></span> <span data-ttu-id="46cdc-105">您可以藉由呼叫 [**IDirect3DVertexBuffer9：： Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) 方法來取得頂點緩衝區記憶體的指標，然後視需要存取記憶體，以使用新的頂點資料填滿緩衝區，或讀取它已包含的任何資料。</span><span class="sxs-lookup"><span data-stu-id="46cdc-105">You can retrieve a pointer to vertex buffer memory by calling the [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) method, and then accessing the memory as needed to fill the buffer with new vertex data or to read any data it already contains.</span></span> <span data-ttu-id="46cdc-106">**IDirect3DVertexBuffer9：： Lock** 方法接受四個參數。</span><span class="sxs-lookup"><span data-stu-id="46cdc-106">The **IDirect3DVertexBuffer9::Lock** method accepts four parameters.</span></span> <span data-ttu-id="46cdc-107">第一個 *OffsetToLock* 是頂點資料中的位移。</span><span class="sxs-lookup"><span data-stu-id="46cdc-107">The first, *OffsetToLock*, is the offset into the vertex data.</span></span> <span data-ttu-id="46cdc-108">第二個參數是頂點資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="46cdc-108">The second parameter is the size, measured in bytes, of the vertex data.</span></span> <span data-ttu-id="46cdc-109">如果呼叫成功，則接受的第三個參數是指向頂點資料之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="46cdc-109">The third parameter accepted is the address of a pointer that points to the vertex data, if the call succeeds.</span></span>

<span data-ttu-id="46cdc-110">最後一個參數 *旗標* 會告知系統應該如何鎖定記憶體。</span><span class="sxs-lookup"><span data-stu-id="46cdc-110">The last parameter, *Flags*, tells the system how the memory should be locked.</span></span> <span data-ttu-id="46cdc-111">根據將存取頂點資料的方式，指定 *旗標* 參數的常數。</span><span class="sxs-lookup"><span data-stu-id="46cdc-111">Specify constants for the *Flags* parameter according to the way the vertex data will be accessed.</span></span> <span data-ttu-id="46cdc-112">請確定為 [**D3DUSAGE**](d3dusage.md) 選擇的值符合為 [D3DLOCK](d3dlock.md)選擇的值。</span><span class="sxs-lookup"><span data-stu-id="46cdc-112">Make sure the value chosen for [**D3DUSAGE**](d3dusage.md) matches the value chosen for [D3DLOCK](d3dlock.md).</span></span> <span data-ttu-id="46cdc-113">例如，如果您要建立僅具有寫入存取權的頂點緩衝區，請指定 D3DLOCK READONLY 來嘗試讀取資料並不合理 \_ 。</span><span class="sxs-lookup"><span data-stu-id="46cdc-113">For example, if you are creating a vertex buffer with write access only, it doesn't make sense to try to read the data by specifying D3DLOCK\_READONLY.</span></span> <span data-ttu-id="46cdc-114">明智地使用這些旗標，可讓驅動程式鎖定記憶體，並提供最佳效能，並提供所要求的存取類型。</span><span class="sxs-lookup"><span data-stu-id="46cdc-114">Wisely using these flags allows the driver to lock the memory and provide the best performance, given the requested access type.</span></span>

<span data-ttu-id="46cdc-115">當您完成填滿或讀取頂點資料之後，請呼叫 [**IDirect3DVertexBuffer9：： Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) 方法，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="46cdc-115">After you finish filling or reading the vertex data, call the [**IDirect3DVertexBuffer9::Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) method, as shown in the following code example.</span></span>


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



<span data-ttu-id="46cdc-116">如果您使用 D3DUSAGE WRITEONLY 旗標建立頂點緩衝區 \_ ，請勿使用 D3DLOCK \_ READONLY 鎖定旗標。</span><span class="sxs-lookup"><span data-stu-id="46cdc-116">If you create a vertex buffer with the D3DUSAGE\_WRITEONLY flag, do not use the D3DLOCK\_READONLY locking flag.</span></span> <span data-ttu-id="46cdc-117">\_如果您的應用程式只會從頂點緩衝區記憶體讀取，請使用 D3DLOCK READONLY 旗標。</span><span class="sxs-lookup"><span data-stu-id="46cdc-117">Use the D3DLOCK\_READONLY flag if your application will read only from the vertex buffer memory.</span></span> <span data-ttu-id="46cdc-118">包含這個旗標可讓 Direct3D 將其內部程式優化，以改善效率（假設存取記憶體將會是唯讀的）。</span><span class="sxs-lookup"><span data-stu-id="46cdc-118">Including this flag enables Direct3D to optimize its internal procedures to improve efficiency, given that access to the memory will be read-only.</span></span>

<span data-ttu-id="46cdc-119">如 [](performance-optimizations.md)需針對 \_ \_ [**IDirect3DVertexBuffer9：： LOCK**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)的 FLAGS 參數使用 D3DLOCK 捨棄或 D3DLOCK NOOVERWRITE 的相關資訊，請參閱使用動態頂點和索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="46cdc-119">See [Using Dynamic Vertex and Index Buffers](performance-optimizations.md) for information about using D3DLOCK\_DISCARD or D3DLOCK\_NOOVERWRITE for the Flags parameter of [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).</span></span>

<span data-ttu-id="46cdc-120">在 c + + 中，因為您直接存取配置給頂點緩衝區的記憶體，請確定您的應用程式能正確地存取配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="46cdc-120">In C++, because you directly access the memory allocated for the vertex buffer, make sure your application properly accesses the allocated memory.</span></span> <span data-ttu-id="46cdc-121">否則，您會面臨轉譯記憶體不正確風險。</span><span class="sxs-lookup"><span data-stu-id="46cdc-121">Otherwise, you risk rendering that memory invalid.</span></span> <span data-ttu-id="46cdc-122">使用您的應用程式用來從配置緩衝區中的一個頂點移至另一個頂點的頂點格式跨距。</span><span class="sxs-lookup"><span data-stu-id="46cdc-122">Use the stride of the vertex format that your application uses to move from one vertex in the allocated buffer to another.</span></span> <span data-ttu-id="46cdc-123">頂點緩衝區記憶體是在 FVF 中指定的簡單頂點陣列。</span><span class="sxs-lookup"><span data-stu-id="46cdc-123">The vertex buffer memory is a simple array of vertices specified in FVF.</span></span> <span data-ttu-id="46cdc-124">使用您定義的任何頂點格式結構的 stride。</span><span class="sxs-lookup"><span data-stu-id="46cdc-124">Use the stride of whatever vertex format structure you define.</span></span> <span data-ttu-id="46cdc-125">您可以藉由檢查頂點緩衝區描述中包含的 [D3DFVF](d3dfvf.md) ，在執行時間計算每個頂點的 stride。</span><span class="sxs-lookup"><span data-stu-id="46cdc-125">You can calculate the stride of each vertex at run time by examining the [D3DFVF](d3dfvf.md) contained in the vertex buffer description.</span></span> <span data-ttu-id="46cdc-126">下表顯示每個頂點元件的大小。</span><span class="sxs-lookup"><span data-stu-id="46cdc-126">The following table shows the size for each vertex component.</span></span>



| <span data-ttu-id="46cdc-127">頂點格式旗標</span><span class="sxs-lookup"><span data-stu-id="46cdc-127">Vertex Format Flag</span></span> | <span data-ttu-id="46cdc-128">大小</span><span class="sxs-lookup"><span data-stu-id="46cdc-128">Size</span></span>              |
|--------------------|-------------------|
| <span data-ttu-id="46cdc-129">D3DFVF \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="46cdc-129">D3DFVF\_DIFFUSE</span></span>    | <span data-ttu-id="46cdc-130">sizeof (DWORD) </span><span class="sxs-lookup"><span data-stu-id="46cdc-130">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="46cdc-131">D3DFVF \_ 正常</span><span class="sxs-lookup"><span data-stu-id="46cdc-131">D3DFVF\_NORMAL</span></span>     | <span data-ttu-id="46cdc-132">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="46cdc-132">sizeof(float) x 3</span></span> |
| <span data-ttu-id="46cdc-133">D3DFVF \_ 反光</span><span class="sxs-lookup"><span data-stu-id="46cdc-133">D3DFVF\_SPECULAR</span></span>   | <span data-ttu-id="46cdc-134">sizeof (DWORD) </span><span class="sxs-lookup"><span data-stu-id="46cdc-134">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="46cdc-135">D3DFVF \_ TEXn</span><span class="sxs-lookup"><span data-stu-id="46cdc-135">D3DFVF\_TEXn</span></span>       | <span data-ttu-id="46cdc-136">sizeof (float) x n</span><span class="sxs-lookup"><span data-stu-id="46cdc-136">sizeof(float) x n</span></span> |
| <span data-ttu-id="46cdc-137">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="46cdc-137">D3DFVF\_XYZ</span></span>        | <span data-ttu-id="46cdc-138">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="46cdc-138">sizeof(float) x 3</span></span> |
| <span data-ttu-id="46cdc-139">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="46cdc-139">D3DFVF\_XYZRHW</span></span>     | <span data-ttu-id="46cdc-140">sizeof (float) x 4</span><span class="sxs-lookup"><span data-stu-id="46cdc-140">sizeof(float) x 4</span></span> |



 

<span data-ttu-id="46cdc-141">頂點格式所呈現的材質座標數目是由 D3DFVF \_ TEX n 旗標所描述， (其中 n 是介於0到 8) 的值。</span><span class="sxs-lookup"><span data-stu-id="46cdc-141">The number of texture coordinates present in the vertex format is described by the D3DFVF\_TEX n flags (where n is a value from 0 to 8).</span></span> <span data-ttu-id="46cdc-142">將材質座標集合的數目乘以一組材質座標的大小，其範圍從一到四個浮點數，以計算該紋理座標數目所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="46cdc-142">Multiply the number of texture coordinate sets by the size of one set of texture coordinates, which can range from one to four floats, to calculate the memory required for that number of texture coordinates.</span></span>

<span data-ttu-id="46cdc-143">使用總頂點跨距來視需要遞增和遞減記憶體指標，以存取特定頂點。</span><span class="sxs-lookup"><span data-stu-id="46cdc-143">Use the total vertex stride to increment and decrement the memory pointer as needed to access particular vertices.</span></span>

## <a name="retrieving-vertex-buffer-descriptions"></a><span data-ttu-id="46cdc-144">正在抓取頂點緩衝區描述</span><span class="sxs-lookup"><span data-stu-id="46cdc-144">Retrieving Vertex Buffer Descriptions</span></span>

<span data-ttu-id="46cdc-145">您可以藉由呼叫 [**IDirect3DVertexBuffer9：： GetDesc**](/windows/desktop/api) 方法，來取得頂點緩衝區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="46cdc-145">You can retrieve information about a vertex buffer by calling the [**IDirect3DVertexBuffer9::GetDesc**](/windows/desktop/api) method.</span></span> <span data-ttu-id="46cdc-146">這個方法會以頂點緩衝區的相關資訊來填滿 [**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="46cdc-146">This method fills the members of the [**D3DVERTEXBUFFER\_DESC**](d3dvertexbuffer-desc.md) structure with information about the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46cdc-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="46cdc-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46cdc-148">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="46cdc-148">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
