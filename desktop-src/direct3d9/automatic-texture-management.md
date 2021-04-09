---
description: 材質管理是判斷在指定時間轉譯需要哪些材質的程式，並確保將這些材質載入視訊記憶體中。
ms.assetid: ea6d64ee-f570-49eb-b5fd-67fcde3f8ddc
title: '自動材質管理 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0eb14eede197661bc127a062229ebed31274ae8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847503"
---
# <a name="automatic-texture-management-direct3d-9"></a><span data-ttu-id="ab3c5-103">自動材質管理 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="ab3c5-103">Automatic Texture Management (Direct3D 9)</span></span>

<span data-ttu-id="ab3c5-104">材質管理是判斷在指定時間轉譯需要哪些材質的程式，並確保將這些材質載入視訊記憶體中。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-104">Texture management is the process of determining which textures are needed for rendering at a given time and ensuring that those textures are loaded into video memory.</span></span> <span data-ttu-id="ab3c5-105">如同任何演算法，材質管理配置會因複雜性而異，但任何材質管理方法都牽涉到下列重要工作。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-105">As with any algorithm, texture management schemes vary in complexity, but any approach to texture management involves the following key tasks.</span></span>

-   <span data-ttu-id="ab3c5-106">追蹤可用材質記憶體的數量。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-106">Tracking the amount of available texture memory.</span></span>
-   <span data-ttu-id="ab3c5-107">計算轉譯所需的材質，而不需要。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-107">Calculating which textures are needed for rendering, and which are not.</span></span>
-   <span data-ttu-id="ab3c5-108">判斷哪些現有的材質資源可以使用另一個材質影像重載，以及應終結哪些表面，並以新的材質資源取代。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-108">Determining which existing texture resources can be reloaded with another texture image, and which surfaces should be destroyed and replaced with new texture resources.</span></span>

<span data-ttu-id="ab3c5-109">Direct3D 會實行系統支援的材質管理，以確保載入紋理以獲得最佳效能。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-109">Direct3D implements system-supported texture management to ensure that textures are loaded for optimal performance.</span></span> <span data-ttu-id="ab3c5-110">Direct3D 管理的材質資源稱為 managed 紋理。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-110">Texture resources that Direct3D manages are referred to as managed textures.</span></span>

<span data-ttu-id="ab3c5-111">材質管理員會追蹤具有時間戳記的材質，以識別上次使用材質的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-111">The texture manager tracks textures with a time-stamp that identifies when the texture was last used.</span></span> <span data-ttu-id="ab3c5-112">然後，它會使用最少最近使用的演算法來判斷應該移除的材質。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-112">It then uses a least-recently-used algorithm to determine which textures should be removed.</span></span> <span data-ttu-id="ab3c5-113">當有兩個紋理的目標是要從記憶體中移除時，材質優先順序會用來做為系結器。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-113">Texture priorities are used as tie breakers when two textures are targeted for removal from memory.</span></span> <span data-ttu-id="ab3c5-114">如果兩個材質具有相同的優先順序值，則會移除最近最少使用的材質。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-114">If two textures have the same priority value, the least-recently-used texture is removed.</span></span> <span data-ttu-id="ab3c5-115">但是，如果兩個材質具有相同的時間戳記，則會先移除優先順序較低的材質。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-115">However, if two textures have the same time-stamp, the texture that has a lower priority is removed first.</span></span>

<span data-ttu-id="ab3c5-116">當您建立紋理介面時，會要求自動材質管理。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-116">You request automatic texture management for texture surfaces when you create them.</span></span> <span data-ttu-id="ab3c5-117">若要在 c + + 應用程式中取出 managed 材質，請呼叫 [**IDirect3DDevice9：： CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) 並指定為集區參數所管理的 D3DPOOL，以建立材質資源 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-117">To retrieve a managed texture in a C++ application, create a texture resource by calling [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) and specifying the D3DPOOL\_MANAGED for the Pool parameter.</span></span> <span data-ttu-id="ab3c5-118">您不能指定要建立紋理的位置。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-118">You are not allowed to specify where you want the texture created.</span></span> <span data-ttu-id="ab3c5-119">當您建立 managed 材質時，不能使用 D3DPOOL \_ DEFAULT 或 D3DPOOL \_ SYSTEMMEM 旗標。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-119">You cannot use the D3DPOOL\_DEFAULT or D3DPOOL\_SYSTEMMEM flags when creating a managed texture.</span></span> <span data-ttu-id="ab3c5-120">建立 managed 材質之後，您可以呼叫 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 方法，將其設定為轉譯裝置材質串聯中的階段。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-120">After creating the managed texture, you can call the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method to set it to a stage in the rendering device's texture cascade.</span></span>

<span data-ttu-id="ab3c5-121">您可以針對材質介面呼叫 [**IDirect3DResource9：： SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) 方法，將優先順序指派給 managed 紋理。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-121">You can assign a priority to managed textures by calling the [**IDirect3DResource9::SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) method for the texture surface.</span></span>

<span data-ttu-id="ab3c5-122">Direct3D 會視需要自動將材質下載至視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-122">Direct3D automatically downloads textures into video memory as needed.</span></span> <span data-ttu-id="ab3c5-123">系統可能會將受控紋理快取在本機或非本機的視訊記憶體中，視非本機視訊記憶體的可用性或其他因素而定。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-123">The system might cache managed textures in local or nonlocal video memory, depending on the availability of nonlocal video memory or other factors.</span></span> <span data-ttu-id="ab3c5-124">受控紋理的快取位置不會傳達給您的應用程式，也不需要使用自動材質管理的這項資訊。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-124">The cache location of your managed textures is not communicated to your application, nor is this information required to use automatic texture management.</span></span> <span data-ttu-id="ab3c5-125">如果您的應用程式使用的紋理多於可容納在視頻記憶體中的材質，Direct3D 會從視訊記憶體中移除較舊的材質，以騰出空間給新的材質。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-125">If your application uses more textures than can fit in video memory, Direct3D removes older textures from video memory to make room for the new textures.</span></span> <span data-ttu-id="ab3c5-126">如果您再次使用移除的材質，系統會使用原始的系統記憶體紋理介面，在視訊記憶體快取中重載紋理。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-126">If you use a removed texture again, the system uses the original system-memory texture surface to reload the texture in the video-memory cache.</span></span> <span data-ttu-id="ab3c5-127">雖然需要重載紋理，但它也會降低應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-127">Although reloading the texture is necessary, it also decreases the application's performance.</span></span>

<span data-ttu-id="ab3c5-128">您可以藉由更新或鎖定材質資源，以動態方式修改紋理的原始系統記憶體複本。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-128">You can dynamically modify the original system-memory copy of the texture by updating or locking the texture resource.</span></span> <span data-ttu-id="ab3c5-129">當系統偵測到中途的介面時，在更新完成之後或介面解除鎖定時，材質管理員會自動更新材質的視訊記憶體複本。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-129">When the system detects a dirty surface - after an update is completed, or when the surface is unlocked - the texture manager automatically updates the video-memory copy of the texture.</span></span> <span data-ttu-id="ab3c5-130">產生的效能影響類似于重載移除的材質。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-130">The performance hit incurred is similar to reloading a removed texture.</span></span>

<span data-ttu-id="ab3c5-131">在遊戲中輸入新的層級時，您的應用程式可能需要藉由呼叫 [**IDirect3DDevice9：： EvictManagedResources**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)) ，來排清視訊記憶體 (中的所有 managed 紋理。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-131">When entering a new level in a game, your application might need to flush all managed textures from video memory (by calling [**IDirect3DDevice9::EvictManagedResources**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)).</span></span>

<span data-ttu-id="ab3c5-132">如需資源管理的詳細資訊，請參閱 [管理資源 (Direct3D 9) ](managing-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="ab3c5-132">For more information about resource management, see [Managing Resources (Direct3D 9)](managing-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab3c5-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="ab3c5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab3c5-134">Direct3D 紋理</span><span class="sxs-lookup"><span data-stu-id="ab3c5-134">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
