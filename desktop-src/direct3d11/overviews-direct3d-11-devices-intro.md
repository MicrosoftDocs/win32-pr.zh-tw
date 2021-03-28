---
title: Direct3D 11 中的裝置簡介
description: Direct3D 11 物件模型會將資源建立和轉譯功能區分為裝置和一或多個內容。這項分隔是設計來協助多執行緒處理。
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b03333c6594f17d85fee28880e46928241e06c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971397"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a><span data-ttu-id="e4ba4-103">Direct3D 11 中的裝置簡介</span><span class="sxs-lookup"><span data-stu-id="e4ba4-103">Introduction to a Device in Direct3D 11</span></span>

<span data-ttu-id="e4ba4-104">Direct3D 11 物件模型會將資源建立和轉譯功能區分為裝置和一或多個內容。這項分隔是設計來協助多執行緒處理。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-104">The Direct3D 11 object model separates resource creation and rendering functionality into a device and one or more contexts; this separation is designed to facilitate multithreading.</span></span>

-   [<span data-ttu-id="e4ba4-105">裝置</span><span class="sxs-lookup"><span data-stu-id="e4ba4-105">Device</span></span>](#introduction-to-a-device-in-direct3d-11)
-   [<span data-ttu-id="e4ba4-106">裝置內容</span><span class="sxs-lookup"><span data-stu-id="e4ba4-106">Device Context</span></span>](#device-context)
    -   [<span data-ttu-id="e4ba4-107">立即內容</span><span class="sxs-lookup"><span data-stu-id="e4ba4-107">Immediate Context</span></span>](#immediate-context)
    -   [<span data-ttu-id="e4ba4-108">延後內容</span><span class="sxs-lookup"><span data-stu-id="e4ba4-108">Deferred Context</span></span>](#deferred-context)
-   [<span data-ttu-id="e4ba4-109">執行緒考量</span><span class="sxs-lookup"><span data-stu-id="e4ba4-109">Threading Considerations</span></span>](#threading-considerations)
-   [<span data-ttu-id="e4ba4-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4ba4-110">Related topics</span></span>](#related-topics)

## <a name="device"></a><span data-ttu-id="e4ba4-111">裝置</span><span class="sxs-lookup"><span data-stu-id="e4ba4-111">Device</span></span>

<span data-ttu-id="e4ba4-112">裝置可用來建立資源和列舉顯示介面卡的功能。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-112">A device is used to create resources and to enumerate the capabilities of a display adapter.</span></span> <span data-ttu-id="e4ba4-113">在 Direct3D 11 中，裝置會以 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-113">In Direct3D 11, a device is represented with an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface.</span></span>

<span data-ttu-id="e4ba4-114">每個應用程式必須至少有一個裝置，大部分的應用程式只能建立一個裝置。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-114">Each application must have at least one device, most applications only create one device.</span></span> <span data-ttu-id="e4ba4-115">藉由呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) ，為安裝在電腦上的其中一個硬體驅動程式建立裝置，並指定具有 [**D3D \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) 旗標的驅動程式類型。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-115">Create a device for one of the hardware drivers installed on your machine by calling [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and specify the driver type with the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) flag.</span></span> <span data-ttu-id="e4ba4-116">每個裝置可以使用一或多個裝置內容，視所需的功能而定。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-116">Each device can use one or more device contexts, depending on the functionality desired.</span></span>

## <a name="device-context"></a><span data-ttu-id="e4ba4-117">裝置內容</span><span class="sxs-lookup"><span data-stu-id="e4ba4-117">Device Context</span></span>

<span data-ttu-id="e4ba4-118">裝置內容包含使用裝置的情況或設定。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-118">A device context contains the circumstance or setting in which a device is used.</span></span> <span data-ttu-id="e4ba4-119">更具體來說，裝置內容會用來設定管線狀態，並使用裝置所擁有的資源來產生轉譯命令。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-119">More specifically, a device context is used to set pipeline state and generate rendering commands using the resources owned by a device.</span></span> <span data-ttu-id="e4ba4-120">Direct3D 11 會執行兩種類型的裝置內容，一個用於立即轉譯，另一個用於延遲轉譯;這兩個內容都以 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-120">Direct3D 11 implements two types of device contexts, one for immediate rendering and the other for deferred rendering; both contexts are represented with an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span>

### <a name="immediate-context"></a><span data-ttu-id="e4ba4-121">立即內容</span><span class="sxs-lookup"><span data-stu-id="e4ba4-121">Immediate Context</span></span>

<span data-ttu-id="e4ba4-122">立即內容直接呈現到驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-122">An immediate context renders directly to the driver.</span></span> <span data-ttu-id="e4ba4-123">每個裝置都只有一個可從 GPU 取出資料的立即內容。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-123">Each device has one and only one immediate context which can retrieve data from the GPU.</span></span> <span data-ttu-id="e4ba4-124">立即內容可以用來立即轉譯 (，或) [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)中播放。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-124">An immediate context can be used to immediately render (or play back) a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span>

<span data-ttu-id="e4ba4-125">有兩種方式可以取得立即內容：</span><span class="sxs-lookup"><span data-stu-id="e4ba4-125">There are two ways to get an immediate context:</span></span>

-   <span data-ttu-id="e4ba4-126">藉由呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-126">By calling either [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>
-   <span data-ttu-id="e4ba4-127">藉由呼叫 [**ID3D11Device：： GetImmediateCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext)。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-127">By calling [**ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span></span>

### <a name="deferred-context"></a><span data-ttu-id="e4ba4-128">延後內容</span><span class="sxs-lookup"><span data-stu-id="e4ba4-128">Deferred Context</span></span>

<span data-ttu-id="e4ba4-129">延後的內容會將 GPU 命令記錄到 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)中。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-129">A deferred context records GPU commands into a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="e4ba4-130">延遲的內容主要用於多執行緒，而且對單一執行緒應用程式而言並不是必要的。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-130">A deferred context is primarily used for multithreading and is not necessary for a single-threaded application.</span></span> <span data-ttu-id="e4ba4-131">延遲的內容通常會由工作者執行緒（而非主要轉譯執行緒）使用。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-131">A deferred context is generally used by a worker thread instead of the main rendering thread.</span></span> <span data-ttu-id="e4ba4-132">當您建立延遲的內容時，它不會繼承來自立即內容的任何狀態。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-132">When you create a deferred context, it does not inherit any state from the immediate context.</span></span>

<span data-ttu-id="e4ba4-133">若要取得延遲的內容，請呼叫 [**ID3D11Device：： CreateDeferredCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext)。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-133">To get a deferred context, call [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

<span data-ttu-id="e4ba4-134">任何內容--immediate 或延後--可以在任何執行緒上使用，只要一次只在一個執行緒中使用內容即可。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-134">Any context -- immediate or deferred -- can be used on any thread as long as the context is only used in one thread at a time.</span></span>

## <a name="threading-considerations"></a><span data-ttu-id="e4ba4-135">執行緒考量</span><span class="sxs-lookup"><span data-stu-id="e4ba4-135">Threading Considerations</span></span>

<span data-ttu-id="e4ba4-136">下表強調 Direct3D 11 中的執行緒模型與舊版 Direct3D 之間的差異。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-136">This table highlights the differences in the threading model in Direct3D 11 from prior versions of Direct3D.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4ba4-137">Direct3D 11 與舊版 Direct3D 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="e4ba4-137">Differences between Direct3D 11 and previous versions of Direct3D:</span></span><br/> <span data-ttu-id="e4ba4-138">所有 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> 介面方法都是無限制執行緒，這表示可以安全地讓多個執行緒同時呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-138">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> interface methods are free-threaded, which means it is safe to have multiple threads call the functions at the same time.</span></span><br/>
<ul>
<li><span data-ttu-id="e4ba4-139">所有 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>衍生介面 (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>、 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>等 ) 都是無限制執行緒。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-139">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>-derived interfaces (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) are free-threaded.</span></span></li>
<li><span data-ttu-id="e4ba4-140">Direct3D 11 會將建立和轉譯的資源分割成兩個介面。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-140">Direct3D 11 splits resource creating and rendering into two interfaces.</span></span> <span data-ttu-id="e4ba4-141">Map、取消對應、Begin、End 和 >id3d11devicecoNtext 會在<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong></strong></a>上執行，因為<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>會強定義作業的順序。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-141">Map, Unmap, Begin, End, and GetData are implemented on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> because <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> strongly defines the order of operations.</span></span> <span data-ttu-id="e4ba4-142"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> 和 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> 介面也會針對自由執行緒作業執行方法。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-142"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> and <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> interfaces also implement methods for free-threaded operations.</span></span></li>
<li><span data-ttu-id="e4ba4-143">除了存在於<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) 上的<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>>id3d11devicecoNtext</strong></a>方法 (不是無限制執行緒，也就是需要單一執行緒。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-143">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> methods (except for those that exist on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) are not free-threaded, that is, they require single threading.</span></span> <span data-ttu-id="e4ba4-144">每次只有一個執行緒可以安全地呼叫其任何方法 (繪製、複製、對應等 ) 。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-144">Only one thread may safely be calling any of its methods (Draw, Copy, Map, etc.) at a time.</span></span></li>
<li><span data-ttu-id="e4ba4-145">一般情況下，無限制執行緒會將使用的同步處理原始物件數目以及其持續時間降到最低。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-145">In general, free-threading minimizes the number of synchronization primitives used as well as their duration.</span></span> <span data-ttu-id="e4ba4-146">不過，使用長期同步處理的應用程式可能會直接影響應用程式可預期達到的並行程度。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-146">However, an application that uses synchronization held for a long time can directly impact how much concurrency an application can expect to achieve.</span></span></li>
</ul>
<span data-ttu-id="e4ba4-147">ID3D10Device 介面方法並非設計成可自由執行緒。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-147">ID3D10Device interface methods are not designed to be free-threaded.</span></span> <span data-ttu-id="e4ba4-148">ID3D10Device 會 (與 Direct3D 9) 中的 ID3D9Device 一樣來實行所有建立和轉譯功能。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-148">ID3D10Device implements all create and rendering functionality (as does ID3D9Device in Direct3D 9).</span></span> <span data-ttu-id="e4ba4-149">對應和取消對應會在衍生於 ID3D10Asynchronous 衍生介面的 ID3D10Resource 衍生介面、Begin、End 和上執行。</span><span class="sxs-lookup"><span data-stu-id="e4ba4-149">Map and Unmap are implemented on ID3D10Resource-derived interfaces, Begin, End, and GetData are implemented on ID3D10Asynchronous-derived interfaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e4ba4-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4ba4-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4ba4-151">裝置</span><span class="sxs-lookup"><span data-stu-id="e4ba4-151">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





