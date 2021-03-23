---
title: 描述項總覽
description: 描述元是由 API 呼叫所建立，並識別資源。
ms.assetid: 64721226-5533-4816-865E-9429032FCC86
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d83b2fbfd5c5df2738c61aea4f1d1115d6c874
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548412"
---
# <a name="descriptors-overview"></a><span data-ttu-id="cadb8-103">描述項總覽</span><span class="sxs-lookup"><span data-stu-id="cadb8-103">Descriptors Overview</span></span>

<span data-ttu-id="cadb8-104">描述元是由 API 呼叫所建立，並識別資源。</span><span class="sxs-lookup"><span data-stu-id="cadb8-104">Descriptors are created by API calls and identify resources.</span></span>

-   [<span data-ttu-id="cadb8-105">描述中繼資料</span><span class="sxs-lookup"><span data-stu-id="cadb8-105">Descriptor data</span></span>](#descriptor-data)
-   [<span data-ttu-id="cadb8-106">描述項控制碼</span><span class="sxs-lookup"><span data-stu-id="cadb8-106">Descriptor handles</span></span>](#descriptor-handles)
-   [<span data-ttu-id="cadb8-107">Null 描述項</span><span class="sxs-lookup"><span data-stu-id="cadb8-107">Null descriptors</span></span>](#null-descriptors)
-   [<span data-ttu-id="cadb8-108">預設描述項</span><span class="sxs-lookup"><span data-stu-id="cadb8-108">Default descriptors</span></span>](#default-descriptors)
-   [<span data-ttu-id="cadb8-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="cadb8-109">Related topics</span></span>](#related-topics)

## <a name="descriptor-data"></a><span data-ttu-id="cadb8-110">描述中繼資料</span><span class="sxs-lookup"><span data-stu-id="cadb8-110">Descriptor data</span></span>

<span data-ttu-id="cadb8-111">描述項是相當小的資料區塊，可完整地以 GPU 特定的不透明格式來描述 GPU 的物件。</span><span class="sxs-lookup"><span data-stu-id="cadb8-111">A descriptor is a relatively small block of data that fully describes an object to the GPU, in a GPU-specific opaque format.</span></span> <span data-ttu-id="cadb8-112">有幾種不同類型的描述項會 &mdash; 呈現目標視圖 (RTVs) 、深度樣板視圖 (dsv) 、著色器資源檢視 (SRVs) 、未排序的存取視圖 (UAVs) 、常數緩衝區視圖 (CBVs) 和取樣器。</span><span class="sxs-lookup"><span data-stu-id="cadb8-112">There are several different types of descriptors&mdash;render target views (RTVs), depth stencil views (DSVs), shader resource views (SRVs), unordered access views (UAVs), constant buffer views (CBVs), and samplers.</span></span>

<span data-ttu-id="cadb8-113">描述項的大小視 GPU 硬體而異。</span><span class="sxs-lookup"><span data-stu-id="cadb8-113">Descriptors vary in size, depending on the GPU hardware.</span></span> <span data-ttu-id="cadb8-114">您可以藉由呼叫 [**ID3D12Device：： GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)，查詢 SRV、UAV 或 CBV 的大小。</span><span class="sxs-lookup"><span data-stu-id="cadb8-114">You can query for the size of an SRV, UAV, or CBV by calling [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize).</span></span> <span data-ttu-id="cadb8-115">此檔中顯示的描述項為不可分割單位;以下是範例。</span><span class="sxs-lookup"><span data-stu-id="cadb8-115">Descriptors are shown in this documentation as indivisible units; here's an example.</span></span>

![srv、cbv、uav 和取樣器](images/single-descriptor.png)

<span data-ttu-id="cadb8-117">描述項是由 API 呼叫所建立，而且會包含您希望描述項包含的資源和 mip 對應等資訊。</span><span class="sxs-lookup"><span data-stu-id="cadb8-117">Descriptors are created by API calls, and will include information such as the resource and mip-maps you want the descriptor to contain.</span></span>

<span data-ttu-id="cadb8-118">驅動程式不會追蹤或保存描述項的參考，而是由應用程式確保正確的描述項類型正在使用中，而且資訊是最新的。</span><span class="sxs-lookup"><span data-stu-id="cadb8-118">The driver does not track or hold references to descriptors, it is up to the app to ensure the correct descriptor type is in use, and that the information is current.</span></span> <span data-ttu-id="cadb8-119">有一個小例外狀況;驅動程式會檢查轉譯目標系結，以確保交換鏈能正常運作。</span><span class="sxs-lookup"><span data-stu-id="cadb8-119">There is one small exception to this; the driver does inspect render target bindings to ensure swap chains work correctly.</span></span>

<span data-ttu-id="cadb8-120">物件描述項不需要釋出或釋放。</span><span class="sxs-lookup"><span data-stu-id="cadb8-120">Object descriptors do not need to be freed or released.</span></span> <span data-ttu-id="cadb8-121">驅動程式不會將任何配置附加至描述項的建立。</span><span class="sxs-lookup"><span data-stu-id="cadb8-121">Drivers do not attach any allocations to the creation of a descriptor.</span></span> <span data-ttu-id="cadb8-122">不過，描述項可能會編碼應用程式擁有存留期之其他配置的參考。</span><span class="sxs-lookup"><span data-stu-id="cadb8-122">A descriptor may, however, encode references to other allocations for which the application owns the lifetime.</span></span> <span data-ttu-id="cadb8-123">比方說，SRV 的描述項必須包含 D3D 資源的虛擬位址 (例如 SRV 所參考的材質) 。</span><span class="sxs-lookup"><span data-stu-id="cadb8-123">For instance, a descriptor for an SRV must contain the virtual address of the D3D resource (e.g. a texture) that the SRV refers to.</span></span> <span data-ttu-id="cadb8-124">應用程式必須負責確保它在其相依的基礎 D3D 資源已損毀或遭到修改時，不會使用 SRV 描述項， (例如宣告為 nonresident) 。</span><span class="sxs-lookup"><span data-stu-id="cadb8-124">It is the application's responsibility to make sure that it does not use an SRV descriptor when the underlying D3D resource it depends on has been destroyed or is being modified (such as being declared as nonresident).</span></span>

<span data-ttu-id="cadb8-125">使用描述項的主要方式是將它們放在描述元堆積中，而這些專案是描述項的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cadb8-125">The primary way to use descriptors is to place them in descriptor heaps, which are backing memory for descriptors.</span></span>

## <a name="descriptor-handles"></a><span data-ttu-id="cadb8-126">描述項控制碼</span><span class="sxs-lookup"><span data-stu-id="cadb8-126">Descriptor handles</span></span>

<span data-ttu-id="cadb8-127">描述項控制碼是描述項的唯一位址。</span><span class="sxs-lookup"><span data-stu-id="cadb8-127">A descriptor handle is the unique address of the descriptor.</span></span> <span data-ttu-id="cadb8-128">它類似于指標，但不是不透明的，因為其實作為硬體特有。</span><span class="sxs-lookup"><span data-stu-id="cadb8-128">It is similar to a pointer, but is opaque as its implementation is hardware specific.</span></span> <span data-ttu-id="cadb8-129">控制碼在描述元堆積之間是唯一的，因此，例如，控制碼陣列可以參考多個堆積中的描述項。</span><span class="sxs-lookup"><span data-stu-id="cadb8-129">The handle is unique across descriptor heaps, so, for example, an array of handles can reference descriptors in multiple heaps.</span></span>

<span data-ttu-id="cadb8-130">CPU 控制碼可供立即使用，例如複製來源和目的地都需要識別。</span><span class="sxs-lookup"><span data-stu-id="cadb8-130">CPU handles are for immediate use, such as copying where both the source and destination need to be identified.</span></span> <span data-ttu-id="cadb8-131">在使用 (（例如，呼叫 [**ID3D12GraphicsCommandList：： OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)) 、可以重複使用，或可處置其基礎堆積）之後立即使用。</span><span class="sxs-lookup"><span data-stu-id="cadb8-131">Immediately after use (for example, a call to [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)), they can be reused, or their underlying heap can be disposed.</span></span>

<span data-ttu-id="cadb8-132">GPU 控制碼無法立即使用 &mdash; ，它們會從命令清單識別位置，以在 gpu 執行時間使用。</span><span class="sxs-lookup"><span data-stu-id="cadb8-132">GPU handles are not for immediate use&mdash;they identify locations from a command list, for use at GPU execution time.</span></span> <span data-ttu-id="cadb8-133">您必須保留它們，直到任何參考它們的命令清單完全執行為止。</span><span class="sxs-lookup"><span data-stu-id="cadb8-133">They must be preserved until any command lists referencing them have executed entirely.</span></span>

<span data-ttu-id="cadb8-134">若要建立堆積開頭的描述項控制碼，建立描述元堆積本身之後，請呼叫下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="cadb8-134">To create a descriptor handle for the start of a heap, after creating the descriptor heap itself, call one of the following methods:</span></span>

-   [<span data-ttu-id="cadb8-135">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="cadb8-135">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)
-   [<span data-ttu-id="cadb8-136">**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="cadb8-136">**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)

<span data-ttu-id="cadb8-137">這些方法會傳回下列結構：</span><span class="sxs-lookup"><span data-stu-id="cadb8-137">These methods return the following structures:</span></span>

-   [<span data-ttu-id="cadb8-138">**D3D12 \_ CPU \_ 描述項 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="cadb8-138">**D3D12\_CPU\_DESCRIPTOR\_HANDLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)
-   [<span data-ttu-id="cadb8-139">**D3D12 \_ GPU \_ 描述項 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="cadb8-139">**D3D12\_GPU\_DESCRIPTOR\_HANDLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

<span data-ttu-id="cadb8-140">由於描述項的大小會因硬體而異，因此可取得堆積中每個描述元之間的增量：</span><span class="sxs-lookup"><span data-stu-id="cadb8-140">As the size of the descriptors varies by hardware, to get the increment between each descriptor in a heap use:</span></span>

-   [<span data-ttu-id="cadb8-141">**ID3D12Device::GetDescriptorHandleIncrementSize**</span><span class="sxs-lookup"><span data-stu-id="cadb8-141">**ID3D12Device::GetDescriptorHandleIncrementSize**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)

<span data-ttu-id="cadb8-142">您可以使用數個增量、複製控制碼，以及將控制碼傳遞至 API 呼叫，以安全的方式來位移開始位置。</span><span class="sxs-lookup"><span data-stu-id="cadb8-142">It is safe to offset a starting location with a number of increments, to copy handles, and to pass handles into API calls.</span></span> <span data-ttu-id="cadb8-143">將控制碼取值為有效的 CPU 指標，也不能分析控制碼內的位，是不安全的。</span><span class="sxs-lookup"><span data-stu-id="cadb8-143">It is not safe to dereference a handle as if it was a valid CPU pointer, nor to analyze the bits within a handle.</span></span>

<span data-ttu-id="cadb8-144">已加入一些協助程式結構與初始化成員，以簡化管理處理程式的工作。</span><span class="sxs-lookup"><span data-stu-id="cadb8-144">Some helper structures have been added, with initialization members, to make managing handles a little easier.</span></span>

-   [<span data-ttu-id="cadb8-145">**CD3DX12 \_ CPU \_ 描述項 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="cadb8-145">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE**</span></span>](cd3dx12-cpu-descriptor-handle.md)
-   [<span data-ttu-id="cadb8-146">**CD3DX12 \_ GPU \_ 描述項 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="cadb8-146">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE**</span></span>](cd3dx12-gpu-descriptor-handle.md)

## <a name="null-descriptors"></a><span data-ttu-id="cadb8-147">Null 描述項</span><span class="sxs-lookup"><span data-stu-id="cadb8-147">Null descriptors</span></span>

<span data-ttu-id="cadb8-148">使用 API 呼叫建立描述項時，應用程式會針對描述項定義中的資源指標傳遞 Null，以達到著色器存取時沒有任何限制的效果。</span><span class="sxs-lookup"><span data-stu-id="cadb8-148">When creating descriptors using API calls, applications pass NULL for the resource pointer in the descriptor definition to achieve the effect of nothing bound when accessed by a shader.</span></span>

<span data-ttu-id="cadb8-149">其餘的描述項必須盡可能填入。</span><span class="sxs-lookup"><span data-stu-id="cadb8-149">The rest of the descriptor must be populated as much as possible.</span></span> <span data-ttu-id="cadb8-150">例如，在著色器資源檢視 (SRVs) 的情況下，可以使用描述元來區分它 (的檢視類型 Texture1D、Texture2D 等，) 。</span><span class="sxs-lookup"><span data-stu-id="cadb8-150">For example, in the case of Shader Resource Views (SRVs), the descriptor can be used to distinguish the type of view it is (Texture1D, Texture2D, and so on).</span></span> <span data-ttu-id="cadb8-151">視圖描述項中的數值參數（例如 mipmap 數目）必須全部設定為對資源有效的值。</span><span class="sxs-lookup"><span data-stu-id="cadb8-151">Numerical parameters in the view descriptor, such as the number of mipmaps, must all be set to values that are valid for a resource.</span></span>

<span data-ttu-id="cadb8-152">在許多情況下，有一個已定義的行為可存取未系結的資源，例如傳回預設值的 SRVs。</span><span class="sxs-lookup"><span data-stu-id="cadb8-152">In many cases, there is a defined behavior for accessing an unbound resource, such as SRVs which return default values.</span></span> <span data-ttu-id="cadb8-153">只要著色器存取的類型與描述元類型相容，就會在存取 Null 描述元時接受這些值。</span><span class="sxs-lookup"><span data-stu-id="cadb8-153">Those will be honored when accessing a NULL descriptor as long as the type of shader access is compatible with the descriptor type.</span></span> <span data-ttu-id="cadb8-154">例如，如果著色器預期 Texture2D SRV 並存取定義為 Texture1D 的 Null SRV，則行為會是未定義的，而且可能會導致裝置重設。</span><span class="sxs-lookup"><span data-stu-id="cadb8-154">For example, if a shader expects a Texture2D SRV and accesses a NULL SRV defined as a Texture1D, the behavior is undefined and could result in device reset.</span></span>

<span data-ttu-id="cadb8-155">總而言之，若要建立 null 描述項，請在 `null` 使用 [**CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)等方法建立視圖時傳遞 *pResource* 參數。</span><span class="sxs-lookup"><span data-stu-id="cadb8-155">In summary, to create a null descriptor, pass `null` for the *pResource* parameter when creating the view with methods such as [**CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview).</span></span> <span data-ttu-id="cadb8-156">針對 [view description] 參數 *pDesc*，設定當資源不是 null 時可運作的設定 (否則某些硬體) 可能會發生損毀。</span><span class="sxs-lookup"><span data-stu-id="cadb8-156">For the view description parameter *pDesc*, set a configuration that would work if the resource was not null (otherwise a crash may occur on some hardware).</span></span>

<span data-ttu-id="cadb8-157">不過，根描述項不應設為 null。</span><span class="sxs-lookup"><span data-stu-id="cadb8-157">Root descriptors however, should not be set to null.</span></span>

<span data-ttu-id="cadb8-158">在第1層硬體 (請參閱 [**硬體層**](./hardware-support.md)，透過描述項資料表系結 (的所有描述元) 都必須初始化為真實描述元或 null 描述項（即使硬體未存取），否則行為未定義。</span><span class="sxs-lookup"><span data-stu-id="cadb8-158">On Tier1 hardware (see [**Hardware Tiers**](./hardware-support.md), all descriptors that are bound (via descriptor tables) must be initialized, either as real descriptors or null descriptors, even if not accessed by the hardware, otherwise behaviour is undefined.</span></span>

<span data-ttu-id="cadb8-159">在第2層硬體上，這適用于系結 CBV 和 UAV 描述項，但不適用於 SRV 描述項。</span><span class="sxs-lookup"><span data-stu-id="cadb8-159">On Tier2 hardware, this applies to bound CBV and UAV descriptors, but not to SRV descriptors.</span></span>

<span data-ttu-id="cadb8-160">在 Tier3 硬體上，不會有任何限制，但前提是不會存取未初始化的描述項。</span><span class="sxs-lookup"><span data-stu-id="cadb8-160">On Tier3 hardware, there's no restriction on this, provided that uninitialized descriptors are never accessed.</span></span>

## <a name="default-descriptors"></a><span data-ttu-id="cadb8-161">預設描述項</span><span class="sxs-lookup"><span data-stu-id="cadb8-161">Default descriptors</span></span>

<span data-ttu-id="cadb8-162">若要建立特定視圖的預設描述項，請將有效的 *pResource* 參數傳遞至 create view 方法 (例如 [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)) ，但是針對 *pDesc* 參數傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="cadb8-162">To create a default descriptor for a particular view, pass in a valid *pResource* parameter to the create view method (such as [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)), but pass in **NULL** for the *pDesc* parameter.</span></span> <span data-ttu-id="cadb8-163">例如，如果資源包含14個 mips，則此視圖會包含14個 mips。</span><span class="sxs-lookup"><span data-stu-id="cadb8-163">For example, if the resource contained 14 mips, then the view would contain 14 mips.</span></span> <span data-ttu-id="cadb8-164">預設的案例涵蓋資源與觀點的最明顯對應。</span><span class="sxs-lookup"><span data-stu-id="cadb8-164">The default case covers the most obvious mapping of a resource to a view.</span></span> <span data-ttu-id="cadb8-165">這需要配置具有完整格式名稱的資源 (例如 **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB** ，而非 **DXGI_FORMAT_R8G8B8A8_TYPELESS**) 。</span><span class="sxs-lookup"><span data-stu-id="cadb8-165">This does require that the resource is allocated with a fully qualified format name (such as **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB** rather than **DXGI_FORMAT_R8G8B8A8_TYPELESS**).</span></span>

<span data-ttu-id="cadb8-166">因為提供的 *pResource* 參數必須是 **Null**，且必須透過 [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv) 傳遞位置，所以無法搭配使用預設描述項與 raytracing 加速結構視圖。</span><span class="sxs-lookup"><span data-stu-id="cadb8-166">Default descriptors can't be used with a raytracing acceleration structure view, because the provided *pResource* parameter must be **NULL**, and the location must be passed via a [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cadb8-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="cadb8-167">Related topics</span></span>

[<span data-ttu-id="cadb8-168">描述項</span><span class="sxs-lookup"><span data-stu-id="cadb8-168">Descriptors</span></span>](descriptors.md)