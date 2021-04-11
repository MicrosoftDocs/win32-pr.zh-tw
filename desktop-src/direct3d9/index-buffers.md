---
description: IDirect3DIndexBuffer9 介面所代表的索引緩衝區是包含索引資料的記憶體緩衝區。
ms.assetid: baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784
title: " (Direct3D 9) 的索引緩衝區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7151fae6deb72a0c569d269c80e5b13bf946f9d0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845964"
---
# <a name="index-buffers-direct3d-9"></a><span data-ttu-id="b5c21-103"> (Direct3D 9) 的索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="b5c21-103">Index Buffers (Direct3D 9)</span></span>

<span data-ttu-id="b5c21-104">[**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)介面所代表的索引緩衝區是包含索引資料的記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b5c21-104">Index buffers, represented by the [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, are memory buffers that contain index data.</span></span> <span data-ttu-id="b5c21-105">索引資料（或索引）是頂點緩衝區的整數位移，可用來使用 [**IDirect3DDevice9：:D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 方法來呈現基本資料。</span><span class="sxs-lookup"><span data-stu-id="b5c21-105">Index data, or indices, are integer offsets into vertex buffers and are used to render primitives using the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method.</span></span>

<span data-ttu-id="b5c21-106">頂點緩衝包含頂點，因此，您可以使用或不使用索引的基本類型來繪製頂點緩衝。</span><span class="sxs-lookup"><span data-stu-id="b5c21-106">A vertex buffer contains vertices; therefore, you can draw a vertex buffer either with or without indexed primitives.</span></span> <span data-ttu-id="b5c21-107">不過，因為索引緩衝包含索引，您無法使用無對應頂點緩衝的索引緩衝。</span><span class="sxs-lookup"><span data-stu-id="b5c21-107">However, because an index buffer contains indices, you cannot use an index buffer without a corresponding vertex buffer.</span></span> <span data-ttu-id="b5c21-108"> (為 [**IDirect3DDevice9：:D rawindexedprimitiveup**](/windows/desktop/api) 和 [**IDirect3DDevice9：:D rawprimitiveup**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup) 是唯一繪製沒有索引或頂點緩衝區的繪圖方法。 ) </span><span class="sxs-lookup"><span data-stu-id="b5c21-108">(As a side note, [**IDirect3DDevice9::DrawIndexedPrimitiveUP**](/windows/desktop/api) and [**IDirect3DDevice9::DrawPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup) are the only draw methods that draw without an index or a vertex buffer.)</span></span>

## <a name="index-buffer-description"></a><span data-ttu-id="b5c21-109">索引緩衝描述</span><span class="sxs-lookup"><span data-stu-id="b5c21-109">Index Buffer Description</span></span>

<span data-ttu-id="b5c21-110">索引緩衝是依照其能力來描述，例如存在於記憶體中的哪裡、是否支援讀取和寫入，以及可包含的索引類型以數目。</span><span class="sxs-lookup"><span data-stu-id="b5c21-110">An index buffer is described in terms of its capabilities, such as where it exists in memory, whether it supports reading and writing, and the type and number of indices it can contain.</span></span> <span data-ttu-id="b5c21-111">這些特性會保留在 [**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md) 結構中。</span><span class="sxs-lookup"><span data-stu-id="b5c21-111">These traits are held in a [**D3DINDEXBUFFER\_DESC**](d3dindexbuffer-desc.md) structure.</span></span>

<span data-ttu-id="b5c21-112">索引緩衝描述會告訴您的應用程式現有緩衝區是如何建立的。</span><span class="sxs-lookup"><span data-stu-id="b5c21-112">Index buffer descriptions tell your application how an existing buffer was created.</span></span> <span data-ttu-id="b5c21-113">您為系統提供空描述結構，以填入先前建立的索引緩衝功能。</span><span class="sxs-lookup"><span data-stu-id="b5c21-113">You provide an empty description structure for the system to fill with the capabilities of a previously created index buffer.</span></span>

-   <span data-ttu-id="b5c21-114">格式成員描述索引緩衝區資料的介面格式。</span><span class="sxs-lookup"><span data-stu-id="b5c21-114">The Format member describes the surface format of the index buffer data.</span></span>
-   <span data-ttu-id="b5c21-115">此類型會識別索引緩衝區的資源類型。</span><span class="sxs-lookup"><span data-stu-id="b5c21-115">The Type identifies the resource type of the index buffer.</span></span>
-   <span data-ttu-id="b5c21-116">使用結構成員包含一般功能旗標。</span><span class="sxs-lookup"><span data-stu-id="b5c21-116">The Usage structure member contains general capability flags.</span></span> <span data-ttu-id="b5c21-117">D3DUSAGE \_ SOFTWAREPROCESSING 旗標表示索引緩衝區要與軟體頂點處理搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b5c21-117">The D3DUSAGE\_SOFTWAREPROCESSING flag indicates that the index buffer is to be used with software vertex processing.</span></span> <span data-ttu-id="b5c21-118">使用中的 D3DUSAGE WRITEONLY 旗標是否存在， \_ 表示索引緩衝區記憶體只用于寫入作業。</span><span class="sxs-lookup"><span data-stu-id="b5c21-118">The presence of the D3DUSAGE\_WRITEONLY flag in Usage indicates that the index buffer memory is used only for write operations.</span></span> <span data-ttu-id="b5c21-119">這樣就可以釋出驅動程式，將索引資料放在最佳的記憶體位置，以啟用快速處理和轉譯。</span><span class="sxs-lookup"><span data-stu-id="b5c21-119">This frees the driver to place the index data in the best memory location to enable fast processing and rendering.</span></span> <span data-ttu-id="b5c21-120">如果 \_ 未使用 D3DUSAGE WRITEONLY 旗標，驅動程式較不可能將資料放在讀取作業效率不佳的位置。</span><span class="sxs-lookup"><span data-stu-id="b5c21-120">If the D3DUSAGE\_WRITEONLY flag is not used, the driver is less likely to put the data in a location that is inefficient for read operations.</span></span> <span data-ttu-id="b5c21-121">這犧牲了一些處理和轉譯速度。</span><span class="sxs-lookup"><span data-stu-id="b5c21-121">This sacrifices some processing and rendering speed.</span></span> <span data-ttu-id="b5c21-122">如果未指定此旗標，則會假設應用程式會對索引緩衝區中的資料執行讀取和寫入作業。</span><span class="sxs-lookup"><span data-stu-id="b5c21-122">If this flag is not specified, it is assumed that applications perform read and write operations on the data in the index buffer.</span></span>
-   <span data-ttu-id="b5c21-123">集區會指定配置給索引緩衝區的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="b5c21-123">Pool specifies the memory class allocated for the index buffer.</span></span> <span data-ttu-id="b5c21-124">D3DPOOL \_ SYSTEMMEM 旗標表示系統已在系統記憶體中建立索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b5c21-124">The D3DPOOL\_SYSTEMMEM flag indicates that the system created the index buffer in system memory.</span></span>
-   <span data-ttu-id="b5c21-125">大小成員會儲存頂點緩衝區資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b5c21-125">The Size member stores the size, in bytes, of the vertex buffer data.</span></span>
-   <span data-ttu-id="b5c21-126">未使用最後一個參數 pSharedHandle。</span><span class="sxs-lookup"><span data-stu-id="b5c21-126">The last parameter pSharedHandle is not used.</span></span> <span data-ttu-id="b5c21-127">將它設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b5c21-127">Set it to **NULL**.</span></span>

## <a name="index-processing-requirements"></a><span data-ttu-id="b5c21-128">索引處理需求</span><span class="sxs-lookup"><span data-stu-id="b5c21-128">Index Processing Requirements</span></span>

<span data-ttu-id="b5c21-129">索引處理作業指數的效能，大幅仰賴索引緩衝存在於記憶體中的位置，以及正在使用何種轉譯裝置。</span><span class="sxs-lookup"><span data-stu-id="b5c21-129">The performance of index processing operations depends heavily on where the index buffer exists in memory and what type of rendering device is being used.</span></span> <span data-ttu-id="b5c21-130">應用程式控制索引緩衝在建立時的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="b5c21-130">Applications control the memory allocation for index buffers when they are created.</span></span> <span data-ttu-id="b5c21-131">\_設定 D3DPOOL SYSTEMMEM memory 旗標時，會在系統記憶體中建立索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b5c21-131">When the D3DPOOL\_SYSTEMMEM memory flag is set, the index buffer is created in system memory.</span></span> <span data-ttu-id="b5c21-132">\_使用 D3DPOOL 預設記憶體旗標時，設備磁碟機會判斷索引緩衝區的記憶體最適合配置的位置，通常稱為驅動程式優化的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b5c21-132">When the D3DPOOL\_DEFAULT memory flag is used, the device driver determines where the memory for the index buffer is best allocated, often referred to as driver-optimal memory.</span></span> <span data-ttu-id="b5c21-133">驅動程式-最佳的記憶體可以是本機視訊記憶體、非本機視訊記憶體或系統記憶體。</span><span class="sxs-lookup"><span data-stu-id="b5c21-133">Driver-optimal memory can be local video memory, non-local video memory, or system memory.</span></span>

<span data-ttu-id="b5c21-134">\_在呼叫 [**IDirect3DDevice9：： CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)方法時設定 D3DUSAGE SOFTWAREPROCESSING 行為旗標，指定要搭配軟體頂點處理使用的索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b5c21-134">Setting the D3DUSAGE\_SOFTWAREPROCESSING behavior flag when calling the [**IDirect3DDevice9::CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) method specifies that the index buffer is to be used with software vertex processing.</span></span> <span data-ttu-id="b5c21-135">\_使用軟體頂點處理時，在混合模式頂點處理 (D3DCREATE 混合 VERTEXPROCESSING) 需要此旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b5c21-135">This flag is required in mixed mode vertex processing (D3DCREATE\_MIXED\_VERTEXPROCESSING) when software vertex processing is used.</span></span>

<span data-ttu-id="b5c21-136">應用程式可以直接將索引寫入驅動程式最佳化記憶體中配置的索引緩衝。</span><span class="sxs-lookup"><span data-stu-id="b5c21-136">The application can directly write indices to a index buffer allocated in driver-optimal memory.</span></span> <span data-ttu-id="b5c21-137">這項技術會防止稍後的冗餘複製作業。</span><span class="sxs-lookup"><span data-stu-id="b5c21-137">This technique prevents a redundant copy operation later.</span></span> <span data-ttu-id="b5c21-138">如果您的應用程式從索引緩衝讀回資料，這項技術無法正常運作，因為主機從驅動程式最佳化記憶體完成讀取作業的速度非常緩慢。</span><span class="sxs-lookup"><span data-stu-id="b5c21-138">This technique does not work well if your application reads data back from an index buffer, because read operations done by the host from driver-optimal memory can be very slow.</span></span> <span data-ttu-id="b5c21-139">因此，如果應用程式在不規律地處理或將資料寫入緩衝區期間需要讀取，系統記憶體索引緩衝則是較理想的選擇。</span><span class="sxs-lookup"><span data-stu-id="b5c21-139">Therefore, if your application needs to read during processing or writes data to the buffer erratically, a system-memory index buffer is a better choice.</span></span>

> [!Note]  
> <span data-ttu-id="b5c21-140">\_除非您不想要在驅動程式將頂點或索引緩衝區放置於 AGP 記憶體時使用影片記憶體或使用大量頁面鎖定 RAM，否則請一律使用 D3DPOOL 預設值。</span><span class="sxs-lookup"><span data-stu-id="b5c21-140">Always use D3DPOOL\_DEFAULT, except when you don't want to use video memory or use large amounts of page-locked RAM when the driver is putting vertex or index buffers into AGP memory.</span></span>

 

## <a name="create-an-index-buffer"></a><span data-ttu-id="b5c21-141">建立索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="b5c21-141">Create an Index Buffer</span></span>

<span data-ttu-id="b5c21-142">藉由呼叫 [**IDirect3DDevice9：： CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) 方法（可接受六個參數）來建立索引緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="b5c21-142">Create an index buffer object by calling the [**IDirect3DDevice9::CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) method, which accepts six parameters.</span></span>

-   <span data-ttu-id="b5c21-143">第一個參數會指定索引緩衝區長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b5c21-143">The first parameter specifies the index buffer length, in bytes.</span></span>
-   <span data-ttu-id="b5c21-144">第二個參數是一組使用方式控制項。</span><span class="sxs-lookup"><span data-stu-id="b5c21-144">The second parameter is a set of usage controls.</span></span> <span data-ttu-id="b5c21-145">此外，它的值會決定索引所參考的頂點是否能夠包含剪切資訊。</span><span class="sxs-lookup"><span data-stu-id="b5c21-145">Among other things, its value determines whether the vertices being referred to by the indices are capable of containing clipping information.</span></span> <span data-ttu-id="b5c21-146">若要改善效能，請 \_ 在不需要剪切時指定 D3DUSAGE DONOTCLIP。</span><span class="sxs-lookup"><span data-stu-id="b5c21-146">To improve performance, specify D3DUSAGE\_DONOTCLIP when clipping is not required.</span></span>

    <span data-ttu-id="b5c21-147">當您 \_ 針對該裝置啟用混合模式或軟體頂點處理 (D3DCREATE \_ mixed \_ VERTEXPROCESSING/D3DCREATE \_ software \_ VERTEXPROCESSING) 時，可以設定 D3DUSAGE SOFTWAREPROCESSING 旗標。</span><span class="sxs-lookup"><span data-stu-id="b5c21-147">The D3DUSAGE\_SOFTWAREPROCESSING flag can be set when mixed-mode or software vertex processing (D3DCREATE\_MIXED\_VERTEXPROCESSING / D3DCREATE\_SOFTWARE\_VERTEXPROCESSING) is enabled for that device.</span></span> <span data-ttu-id="b5c21-148">您 \_ 必須針對要在混合模式中使用軟體頂點處理的緩衝區設定 D3DUSAGE SOFTWAREPROCESSING，但不應針對在混合模式中使用硬體索引處理的最佳效能設定 (D3DCREATE \_ 硬體 \_ VERTEXPROCESSING) 。</span><span class="sxs-lookup"><span data-stu-id="b5c21-148">D3DUSAGE\_SOFTWAREPROCESSING must be set for buffers to be used with software vertex processing in mixed mode, but it should not be set for the best possible performance when using hardware index processing in mixed mode (D3DCREATE\_HARDWARE\_VERTEXPROCESSING).</span></span> <span data-ttu-id="b5c21-149">不過， \_ 當單一緩衝區同時搭配硬體和軟體頂點處理使用時，設定 D3DUSAGE SOFTWAREPROCESSING 是唯一的選項。</span><span class="sxs-lookup"><span data-stu-id="b5c21-149">However, setting D3DUSAGE\_SOFTWAREPROCESSING is the only option when a single buffer is used with both hardware and software vertex processing.</span></span> <span data-ttu-id="b5c21-150">\_混合和軟體裝置允許 D3DUSAGE SOFTWAREPROCESSING。</span><span class="sxs-lookup"><span data-stu-id="b5c21-150">D3DUSAGE\_SOFTWAREPROCESSING is allowed for mixed and software devices.</span></span>

    <span data-ttu-id="b5c21-151">您可以指定 D3DPOOL SYSTEMMEM，將頂點和索引緩衝區強制到系統記憶體中 \_ ，即使是在硬體中完成索引處理也是一樣。</span><span class="sxs-lookup"><span data-stu-id="b5c21-151">It is possible to force vertex and index buffers into system memory by specifying D3DPOOL\_SYSTEMMEM, even when the index processing is being done in hardware.</span></span> <span data-ttu-id="b5c21-152">這是一種方法，可在驅動程式將這些緩衝區放入 AGP 記憶體時避免過度大量的頁面鎖定記憶體。</span><span class="sxs-lookup"><span data-stu-id="b5c21-152">This is a way to avoid overly large amounts of page-locked memory when a driver is putting these buffers into AGP memory.</span></span>

-   <span data-ttu-id="b5c21-153">第三個參數是 \_ \_ [D3DFORMAT](d3dformat.md) 列舉型別的 D3DFMT INDEX16 或 D3DFMT INDEX32 成員，它會指定每個索引的大小。</span><span class="sxs-lookup"><span data-stu-id="b5c21-153">The third parameter is either the D3DFMT\_INDEX16 or D3DFMT\_INDEX32 member of the [D3DFORMAT](d3dformat.md) enumerated type that specifies the size of each index.</span></span>

-   <span data-ttu-id="b5c21-154">第四個參數是 [**D3DPOOL**](./d3dpool.md) 列舉型別的成員，它會告訴系統要將新的索引緩衝區放在記憶體中的哪個位置。</span><span class="sxs-lookup"><span data-stu-id="b5c21-154">The fourth parameter is a member of the [**D3DPOOL**](./d3dpool.md) enumerated type that tells the system where in memory to place the new index buffer.</span></span>

-   <span data-ttu-id="b5c21-155">[**IDirect3DDevice9：： CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)所接受的最後一個參數是變數的位址，這個變數會填入頂點緩衝區物件的新 [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)介面指標（如果呼叫成功）。</span><span class="sxs-lookup"><span data-stu-id="b5c21-155">The final parameter that [**IDirect3DDevice9::CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) accepts is the address of a variable that is filled with a pointer to the new [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface of the vertex buffer object, if the call succeeds.</span></span>

<span data-ttu-id="b5c21-156">下列 c + + 程式碼範例會示範如何在程式碼中建立索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b5c21-156">The following C++ code example shows what creating an index buffer might look like in code.</span></span>


```
/*
 * For the purposes of this example, the d3dDevice variable is the 
 * address of an IDirect3DDevice9 interface exposed by a 
 * Direct3DDevice object, g_IB is a variable of type 
 * LPDIRECT3DINDEXBUFFER9.
 */

if( FAILED( d3dDevice->CreateIndexBuffer( 16384 *sizeof(WORD),
           D3DUSAGE_WRITEONLY, D3DFMT_INDEX16, D3DPOOL_DEFAULT, 
           &g_IB, NULL ) ) )
    return E_FAIL;
```



## <a name="access-an-index-buffer"></a><span data-ttu-id="b5c21-157">存取索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="b5c21-157">Access an Index Buffer</span></span>

<span data-ttu-id="b5c21-158">索引緩衝區物件可讓應用程式直接存取配置給索引資料的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b5c21-158">Index buffer objects enable applications to directly access the memory allocated for index data.</span></span> <span data-ttu-id="b5c21-159">您可以藉由呼叫 [**IDirect3DIndexBuffer9：： Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) 方法來取得索引緩衝區記憶體的指標，然後視需要存取記憶體，以使用新的索引資料來填滿緩衝區或讀取其包含的任何資料。</span><span class="sxs-lookup"><span data-stu-id="b5c21-159">You can retrieve a pointer to index buffer memory by calling the [**IDirect3DIndexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) method, and then accessing the memory as needed to fill the buffer with new index data or to read any data it contains.</span></span> <span data-ttu-id="b5c21-160">鎖定方法接受四個參數。</span><span class="sxs-lookup"><span data-stu-id="b5c21-160">The Lock method accepts four parameters.</span></span> <span data-ttu-id="b5c21-161">第一個 *OffsetToLock* 是索引資料中的位移。</span><span class="sxs-lookup"><span data-stu-id="b5c21-161">The first, *OffsetToLock*, is the offset into the index data.</span></span> <span data-ttu-id="b5c21-162">第二個參數是索引資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b5c21-162">The second parameter is the size, measured in bytes, of the index data.</span></span> <span data-ttu-id="b5c21-163">**IDirect3DIndexBuffer9：： Lock** 方法（ *ppbData*）接受的第三個參數是在呼叫成功時，以索引資料指標填滿的位元組指標位址。</span><span class="sxs-lookup"><span data-stu-id="b5c21-163">The third parameter accepted by the **IDirect3DIndexBuffer9::Lock** method, *ppbData*, is the address of a BYTE pointer filled with a pointer to the index data, if the call succeeds.</span></span>

<span data-ttu-id="b5c21-164">最後一個參數 *旗標* 會告知系統應該如何鎖定記憶體。</span><span class="sxs-lookup"><span data-stu-id="b5c21-164">The last parameter, *Flags*, tells the system how the memory should be locked.</span></span> <span data-ttu-id="b5c21-165">您可以使用它來表示應用程式如何存取緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="b5c21-165">You can use it to indicate how the application accesses the data in the buffer.</span></span> <span data-ttu-id="b5c21-166">根據您的應用程式存取索引資料的方式，指定 *旗標* 參數的常數。</span><span class="sxs-lookup"><span data-stu-id="b5c21-166">Specify constants for the *Flags* parameter according to the way the index data will be accessed by your application.</span></span> <span data-ttu-id="b5c21-167">這可讓驅動程式鎖定記憶體，並提供所要求之存取類型的最佳效能。</span><span class="sxs-lookup"><span data-stu-id="b5c21-167">This allows the driver to lock the memory and provide the best performance given the requested access type.</span></span> <span data-ttu-id="b5c21-168">\_如果您的應用程式只會從索引緩衝區記憶體讀取，請使用 D3DLOCK READONLY 旗標。</span><span class="sxs-lookup"><span data-stu-id="b5c21-168">Use D3DLOCK\_READONLY flag if your application will read only from the index buffer memory.</span></span> <span data-ttu-id="b5c21-169">包含這個旗標可讓 Direct3D 將其內部程式優化，以改善效率（假設存取記憶體將會是唯讀的）。</span><span class="sxs-lookup"><span data-stu-id="b5c21-169">Including this flag enables Direct3D to optimize its internal procedures to improve efficiency, given that access to the memory will be read-only.</span></span>

<span data-ttu-id="b5c21-170">填滿或讀取索引資料之後，請呼叫 [**IDirect3DIndexBuffer9：： Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock) 方法，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="b5c21-170">After you fill or read the index data, call the [**IDirect3DIndexBuffer9::Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock) method, as shown in the following code example.</span></span>


```
// This code example assumes the m_pIndexBuffer is a variable of type 
// LPDIRECT3DINDEXBUFFER9 and that g_Indices has been properly 
// initialized with indices.

// To fill the index buffer, you must lock the buffer to gain 
// access to the indices. This mechanism is required because index
// buffers may be in device memory.

VOID* pIndices;

if( FAILED( m_pIndexBuffer->Lock( 
      0,                 // Fill from start of the buffer
      sizeof(g_Indices), // Size of the data to load
      BYTE**)&pIndices,  // Returned index data
      0 ) ) )            // Send default flags to the lock
{
    SAFE_RELEASE(m_pIndexBuffer);
    return E_FAIL;
}

memcpy( pIndices, g_Indices, sizeof(g_Indices) );
m_pIndexBuffer->Unlock();
```



> [!Note]
>
> <span data-ttu-id="b5c21-171">如果您使用 D3DUSAGE WRITEONLY 旗標建立索引緩衝區 \_ ，請勿使用 D3DLOCK \_ READONLY 鎖定旗標。</span><span class="sxs-lookup"><span data-stu-id="b5c21-171">If you create an index buffer with the D3DUSAGE\_WRITEONLY flag, do not use the D3DLOCK\_READONLY locking flag.</span></span> <span data-ttu-id="b5c21-172">\_如果您的應用程式只會從索引緩衝區記憶體讀取，請使用 D3DLOCK READONLY 旗標。</span><span class="sxs-lookup"><span data-stu-id="b5c21-172">Use the D3DLOCK\_READONLY flag if your application will read only from the index buffer memory.</span></span> <span data-ttu-id="b5c21-173">包含這個旗標可讓 Direct3D 將其內部程式優化，以改善效率（假設存取記憶體將會是唯讀的）。</span><span class="sxs-lookup"><span data-stu-id="b5c21-173">Including this flag enables Direct3D to optimize its internal procedures to improve efficiency, given that access to the memory will be read-only.</span></span>
>
> <span data-ttu-id="b5c21-174">如需針對 \_ \_ [**IDirect3DIndexBuffer9：： Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)方法的 *Flags* 參數使用 D3DLOCK 捨棄或 D3DLOCK NOOVERWRITE 的詳細資訊，請參閱 [ (Direct3D 9) 的效能優化](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="b5c21-174">For information about using D3DLOCK\_DISCARD or D3DLOCK\_NOOVERWRITE for the *Flags* parameter of the [**IDirect3DIndexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) method, see [Performance Optimizations (Direct3D 9)](performance-optimizations.md).</span></span>

 

<span data-ttu-id="b5c21-175">在 c + + 中，因為您直接存取為索引緩衝區配置的記憶體，請確定您的應用程式能夠正確地存取配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b5c21-175">In C++, because you directly access the memory allocated for the index buffer, make sure your application properly accesses the allocated memory.</span></span> <span data-ttu-id="b5c21-176">否則，您會面臨轉譯記憶體不正確風險。</span><span class="sxs-lookup"><span data-stu-id="b5c21-176">Otherwise, you risk rendering that memory invalid.</span></span> <span data-ttu-id="b5c21-177">使用您的應用程式用來從配置緩衝區中的一個索引移至另一個索引的索引格式的 stride。</span><span class="sxs-lookup"><span data-stu-id="b5c21-177">Use the stride of the index format your application uses to move from one index in the allocated buffer to another.</span></span>

<span data-ttu-id="b5c21-178">藉由呼叫 [**IDirect3DIndexBuffer9：： GetDesc**](/windows/desktop/api) 方法，取得索引緩衝區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b5c21-178">Retrieve information about an index buffer by calling the [**IDirect3DIndexBuffer9::GetDesc**](/windows/desktop/api) method.</span></span> <span data-ttu-id="b5c21-179">這個方法會使用索引緩衝區的相關資訊，填滿 [**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="b5c21-179">This method fills the members of the [**D3DINDEXBUFFER\_DESC**](d3dindexbuffer-desc.md) structure with information about the index buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5c21-180">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5c21-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5c21-181">Direct3D 資源</span><span class="sxs-lookup"><span data-stu-id="b5c21-181">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> <dt>

[<span data-ttu-id="b5c21-182">從頂點和索引緩衝區轉譯 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="b5c21-182">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[<span data-ttu-id="b5c21-183"> (Direct3D 9) 的頂點緩衝區 </span><span class="sxs-lookup"><span data-stu-id="b5c21-183">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
