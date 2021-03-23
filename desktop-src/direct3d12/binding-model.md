---
title: 來自 Direct3D 11 的系結模型差異
description: DirectX12 系結背後的主要設計決策之一，是將它與其他管理工作分開。 這會在應用程式上放置一些需求，以管理特定潛在的風險。
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2785da6497fd4e775d9f88847928e7c4c08e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104034"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a><span data-ttu-id="eb31e-104">來自 Direct3D 11 的系結模型差異</span><span class="sxs-lookup"><span data-stu-id="eb31e-104">Differences in the Binding Model from Direct3D 11</span></span>

<span data-ttu-id="eb31e-105">DirectX12 系結背後的主要設計決策之一，是將它與其他管理工作分開。</span><span class="sxs-lookup"><span data-stu-id="eb31e-105">One of the main design decisions behind DirectX12 binding is to separate it from other management tasks.</span></span> <span data-ttu-id="eb31e-106">這會在應用程式上放置一些需求，以管理特定潛在的風險。</span><span class="sxs-lookup"><span data-stu-id="eb31e-106">This places some requirements on the app to manage certain potential hazards.</span></span>

<span data-ttu-id="eb31e-107">D3D12 系結模型的主要優點是，它可讓應用程式經常變更材質系結，而不會有很大的 CPU 效能成本。</span><span class="sxs-lookup"><span data-stu-id="eb31e-107">The main advantage of the D3D12 Binding Model is that it enables apps to change texture bindings frequently, without a huge CPU performance cost.</span></span> <span data-ttu-id="eb31e-108">其他優點是著色器可以存取非常大量的資源、著色器不需要事先知道要系結的資源數量，而且不論硬體或應用程式內容流程為何，都可以使用統一的資源系結模型。</span><span class="sxs-lookup"><span data-stu-id="eb31e-108">Other benefits are that shaders have access to a very large number of resources, shaders need not know in advance how many resources will be bound, and that a unified resource binding model can be used regardless of hardware or the apps content flow.</span></span>

<span data-ttu-id="eb31e-109">為了改善效能，系結模型不會要求系統追蹤應用程式要求 GPU 使用的系結，而且系結和多執行緒命令清單之間有乾淨的整合。</span><span class="sxs-lookup"><span data-stu-id="eb31e-109">To improve performance, the binding model does not require the system to keep track of what bindings an app has requested the GPU to use, and there is a clean integration between binding and multi-threaded command lists.</span></span>

<span data-ttu-id="eb31e-110">下列各節將列出自 D3D11 之後的一些資源系結模型變更。</span><span class="sxs-lookup"><span data-stu-id="eb31e-110">The following sections list some of the changes to the resource binding model since D3D11.</span></span>

-   [<span data-ttu-id="eb31e-111">記憶體常駐管理與系結分開</span><span class="sxs-lookup"><span data-stu-id="eb31e-111">Memory Residency Management Separated From Binding</span></span>](#memory-residency-management-separated-from-binding)
-   [<span data-ttu-id="eb31e-112">物件存留期管理與系結分開</span><span class="sxs-lookup"><span data-stu-id="eb31e-112">Object Lifetime Management Separated From Binding</span></span>](#object-lifetime-management-separated-from-binding)
-   [<span data-ttu-id="eb31e-113">與系結分開的驅動程式資源狀態追蹤</span><span class="sxs-lookup"><span data-stu-id="eb31e-113">Driver Resource State Tracking Separated From Binding</span></span>](#driver-resource-state-tracking-separated-from-binding)
-   [<span data-ttu-id="eb31e-114">CPU GPU 對應記憶體同步處理與系結分開</span><span class="sxs-lookup"><span data-stu-id="eb31e-114">CPU GPU Mapped Memory Synchronization Separated From Binding</span></span>](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [<span data-ttu-id="eb31e-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb31e-115">Related topics</span></span>](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a><span data-ttu-id="eb31e-116">記憶體常駐管理與系結分開</span><span class="sxs-lookup"><span data-stu-id="eb31e-116">Memory Residency Management Separated From Binding</span></span>

<span data-ttu-id="eb31e-117">應用程式可以明確控制哪些表面必須可用來讓 GPU 直接使用 (稱為「常駐」 ) 。</span><span class="sxs-lookup"><span data-stu-id="eb31e-117">Applications have explicit control over which surfaces they need to be available for the GPU to use directly (called being "resident").</span></span> <span data-ttu-id="eb31e-118">相反地，他們可以在資源上套用其他狀態，例如明確地將它們設為非常駐，或讓作業系統選擇需要最少記憶體使用量的特定應用程式類別。</span><span class="sxs-lookup"><span data-stu-id="eb31e-118">Conversely, they can apply other states on resources such as explicitly making them not resident, or letting the OS choose for certain classes of applications that require a minimal memory footprint.</span></span> <span data-ttu-id="eb31e-119">這裡的重點是，應用程式的「常駐」管理與它如何提供資源的存取權給著色器完全分離。</span><span class="sxs-lookup"><span data-stu-id="eb31e-119">The important point here is that the application's management of what is resident is completely decoupled from how it gives access to resources to shaders.</span></span>

<span data-ttu-id="eb31e-120">從提供著色器存取資源的機制中分離常駐管理，可減少轉譯的系統/硬體成本，因為作業系統不需要持續檢查本機系結狀態，就能知道要做什麼。</span><span class="sxs-lookup"><span data-stu-id="eb31e-120">The decoupling of residency management from the mechanism for giving shaders access to resources reduces the system/hardware cost for rendering since the OS doesn't have to constantly inspect the local binding state to know what to make resident.</span></span> <span data-ttu-id="eb31e-121">此外，著色器不再需要知道它們可能需要參考的確切表面，只要經過一組可能可存取的資源，就會事先進行。</span><span class="sxs-lookup"><span data-stu-id="eb31e-121">Furthermore, shaders no longer have to know which exact surfaces they may need to reference, as long as the entire set of possibly accessible resources has been made resident ahead of time.</span></span>

## <a name="object-lifetime-management-separated-from-binding"></a><span data-ttu-id="eb31e-122">物件存留期管理與系結分開</span><span class="sxs-lookup"><span data-stu-id="eb31e-122">Object Lifetime Management Separated From Binding</span></span>

<span data-ttu-id="eb31e-123">不同于先前的 Api，系統不會再追蹤資源系結至管線。</span><span class="sxs-lookup"><span data-stu-id="eb31e-123">Unlike previous APIs, the system no longer tracks bindings of resources to the pipeline.</span></span> <span data-ttu-id="eb31e-124">這是用來讓系統維持應用程式發行的存留資源，因為這些資源仍是由未處理的 GPU 工作所參考。</span><span class="sxs-lookup"><span data-stu-id="eb31e-124">This used to enable the system to keep alive resources that the application has released because they are still referenced by outstanding GPU work.</span></span>

<span data-ttu-id="eb31e-125">在釋放任何資源（例如紋理）之前，應用程式現在必須確定 GPU 已完成參考。</span><span class="sxs-lookup"><span data-stu-id="eb31e-125">Before freeing any resource, such as a texture, applications now must make sure the GPU has completed referencing it.</span></span> <span data-ttu-id="eb31e-126">這表示在應用程式可以安全地釋放資源之前，GPU 必須已完成執行參考資源的命令清單。</span><span class="sxs-lookup"><span data-stu-id="eb31e-126">This means before an application can safely free a resource the GPU must have completed execution of the command list referencing the resource.</span></span>

## <a name="driver-resource-state-tracking-separated-from-binding"></a><span data-ttu-id="eb31e-127">與系結分開的驅動程式資源狀態追蹤</span><span class="sxs-lookup"><span data-stu-id="eb31e-127">Driver Resource State Tracking Separated From Binding</span></span>

<span data-ttu-id="eb31e-128">系統不會再檢查資源系結，以瞭解何時發生資源轉換，需要額外的驅動程式或 GPU 工作。</span><span class="sxs-lookup"><span data-stu-id="eb31e-128">The system no longer inspects resource bindings to understand when resource transitions have occurred which require additional driver or GPU work.</span></span> <span data-ttu-id="eb31e-129">許多 Gpu 和驅動程式的常見範例，都必須知道介面何時會轉換成轉譯目標視圖， (RTV) 至著色器資源檢視 (SRV) 。</span><span class="sxs-lookup"><span data-stu-id="eb31e-129">A common example for many GPUs and drivers is having to know when a surface transitions from being used as a Render Target View (RTV) to Shader Resource View (SRV).</span></span> <span data-ttu-id="eb31e-130">應用程式本身現在必須識別系統可能在意的任何資源轉換是透過專用的 Api 發生。</span><span class="sxs-lookup"><span data-stu-id="eb31e-130">Applications themselves must now identify when any resource transitions that the system might care about are happening via dedicated APIs.</span></span>

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a><span data-ttu-id="eb31e-131">CPU GPU 對應記憶體同步處理與系結分開</span><span class="sxs-lookup"><span data-stu-id="eb31e-131">CPU GPU Mapped Memory Synchronization Separated From Binding</span></span>

<span data-ttu-id="eb31e-132">系統不會再檢查資源系結，以瞭解轉譯是否需要延遲，因為它相依于已對應以進行 CPU 存取但尚未對應的資源。</span><span class="sxs-lookup"><span data-stu-id="eb31e-132">The system no longer inspects resource bindings to understand if rendering needs to be delayed because it depends on a resource that has been mapped for CPU access but has not been unmapped yet.</span></span> <span data-ttu-id="eb31e-133">應用程式現在必須負責同步處理 CPU 和 GPU 記憶體存取。</span><span class="sxs-lookup"><span data-stu-id="eb31e-133">Applications now have the responsibility to synchronize CPU and GPU memory accesses.</span></span> <span data-ttu-id="eb31e-134">為了協助解決這個情況，系統會提供機制讓應用程式要求睡眠中的 CPU 執行緒，直到工作完成為止。</span><span class="sxs-lookup"><span data-stu-id="eb31e-134">To help with this, the system provides mechanisms for the application to request the sleeping of a CPU thread until work completes.</span></span> <span data-ttu-id="eb31e-135">輪詢也可以完成，但效率可能較低。</span><span class="sxs-lookup"><span data-stu-id="eb31e-135">Polling could also be done, but can be less efficient.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb31e-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb31e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb31e-137">資源系結</span><span class="sxs-lookup"><span data-stu-id="eb31e-137">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 




