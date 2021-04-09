---
description: 零或多個鎖定選項的組合，用來描述要執行的鎖定類型。
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3a60318aad8ae0fadcf02d5dea76f6aa62548
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689043"
---
# <a name="d3dlock"></a><span data-ttu-id="182fa-103">D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="182fa-103">D3DLOCK</span></span>

<span data-ttu-id="182fa-104">零或多個鎖定選項的組合，用來描述要執行的鎖定類型。</span><span class="sxs-lookup"><span data-stu-id="182fa-104">A combination of zero or more locking options that describe the type of lock to perform.</span></span>



|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="182fa-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="182fa-105">\#define</span></span>                   | <span data-ttu-id="182fa-106">Description</span><span class="sxs-lookup"><span data-stu-id="182fa-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="182fa-107">D3DLOCK \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="182fa-107">D3DLOCK\_DISCARD</span></span>           | <span data-ttu-id="182fa-108">應用程式會捨棄鎖定區域內的所有記憶體。</span><span class="sxs-lookup"><span data-stu-id="182fa-108">The application discards all memory within the locked region.</span></span> <span data-ttu-id="182fa-109">針對頂點和索引緩衝區，將會捨棄整個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="182fa-109">For vertex and index buffers, the entire buffer will be discarded.</span></span> <span data-ttu-id="182fa-110">只有在使用動態使用方式建立資源時，此選項才有效 (請參閱 [D3DUSAGE](d3dusage.md)) 。</span><span class="sxs-lookup"><span data-stu-id="182fa-110">This option is only valid when the resource is created with dynamic usage (see [D3DUSAGE](d3dusage.md)).</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="182fa-111">D3DLOCK \_ DONOTWAIT</span><span class="sxs-lookup"><span data-stu-id="182fa-111">D3DLOCK\_DONOTWAIT</span></span>         | <span data-ttu-id="182fa-112">允許應用程式在驅動程式無法立即鎖定介面時，取回 CPU 週期。</span><span class="sxs-lookup"><span data-stu-id="182fa-112">Allows an application to gain back CPU cycles if the driver cannot lock the surface immediately.</span></span> <span data-ttu-id="182fa-113">如果設定此旗標，且驅動程式無法立即鎖定介面，則鎖定呼叫會傳回 D3DERR \_ WASSTILLDRAWING。</span><span class="sxs-lookup"><span data-stu-id="182fa-113">If this flag is set and the driver cannot lock the surface immediately, the lock call will return D3DERR\_WASSTILLDRAWING.</span></span> <span data-ttu-id="182fa-114">只有在鎖定使用 [**CreateOffscreenPlainSurface**](/windows/desktop/api)、 [**CreateRenderTarget**](/windows/desktop/api)或 [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)所建立的介面時，才能使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="182fa-114">This flag can only be used when locking a surface created using [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api), or [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span></span> <span data-ttu-id="182fa-115">此旗標也可以與背景緩衝區一起使用。</span><span class="sxs-lookup"><span data-stu-id="182fa-115">This flag can also be used with a back buffer.</span></span>            |
| <span data-ttu-id="182fa-116">D3DLOCK \_ 沒有 \_ 中途 \_ 更新</span><span class="sxs-lookup"><span data-stu-id="182fa-116">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span> | <span data-ttu-id="182fa-117">根據預設，資源的鎖定會將中途區域新增至該資源。</span><span class="sxs-lookup"><span data-stu-id="182fa-117">By default, a lock on a resource adds a dirty region to that resource.</span></span> <span data-ttu-id="182fa-118">此選項可防止變更資源的變更狀態。</span><span class="sxs-lookup"><span data-stu-id="182fa-118">This option prevents any changes to the dirty state of the resource.</span></span> <span data-ttu-id="182fa-119">當應用程式具有在鎖定操作期間變更之區域集合的其他資訊時，應使用此選項。</span><span class="sxs-lookup"><span data-stu-id="182fa-119">Applications should use this option when they have additional information about the set of regions changed during the lock operation.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="182fa-120">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="182fa-120">D3DLOCK\_NOOVERWRITE</span></span>       | <span data-ttu-id="182fa-121">表示在鎖定期間，不會修改在繪圖呼叫中所參考的記憶體，因為沒有此旗標的最後一個鎖定將不會修改。</span><span class="sxs-lookup"><span data-stu-id="182fa-121">Indicates that memory that was referred to in a drawing call since the last lock without this flag will not be modified during the lock.</span></span> <span data-ttu-id="182fa-122">當應用程式將資料附加至資源時，這可以啟用優化。</span><span class="sxs-lookup"><span data-stu-id="182fa-122">This can enable optimizations when the application is appending data to a resource.</span></span> <span data-ttu-id="182fa-123">如果資源正在使用中，則指定這個旗標可讓驅動程式立即傳回，否則，驅動程式必須在從鎖定傳回之前完成使用資源。</span><span class="sxs-lookup"><span data-stu-id="182fa-123">Specifying this flag enables the driver to return immediately if the resource is in use, otherwise, the driver must finish using the resource before returning from locking.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="182fa-124">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="182fa-124">D3DLOCK\_NOSYSLOCK</span></span>         | <span data-ttu-id="182fa-125">視訊記憶體鎖定的預設行為是保留整個系統的重要區段，以保證鎖定期間不會發生任何顯示模式變更。</span><span class="sxs-lookup"><span data-stu-id="182fa-125">The default behavior of a video memory lock is to reserve a system-wide critical section, guaranteeing that no display mode changes will occur for the duration of the lock.</span></span> <span data-ttu-id="182fa-126">此選項會導致鎖定期間不保留整個系統的重要區段。</span><span class="sxs-lookup"><span data-stu-id="182fa-126">This option causes the system-wide critical section not to be held for the duration of the lock.</span></span><br/> <span data-ttu-id="182fa-127">鎖定作業相當耗時，但可以讓系統執行其他任務，例如移動滑鼠游標。</span><span class="sxs-lookup"><span data-stu-id="182fa-127">The lock operation is time consuming, but can enable the system to perform other duties, such as moving the mouse cursor.</span></span> <span data-ttu-id="182fa-128">此選項適用于長時間持續的鎖定，例如鎖定軟體轉譯的背景緩衝區，否則會對系統回應性造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="182fa-128">This option is useful for long-duration locks, such as the lock of the back buffer for software rendering that would otherwise adversely affect system responsiveness.</span></span><br/> |
| <span data-ttu-id="182fa-129">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="182fa-129">D3DLOCK\_READONLY</span></span>          | <span data-ttu-id="182fa-130">應用程式不會寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="182fa-130">The application will not write to the buffer.</span></span> <span data-ttu-id="182fa-131">這可讓以非原生格式儲存的資源在解除鎖定時儲存 recompression 步驟。</span><span class="sxs-lookup"><span data-stu-id="182fa-131">This enables resources stored in non-native formats to save the recompression step when unlocking.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="182fa-132">常數資訊</span><span class="sxs-lookup"><span data-stu-id="182fa-132">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="182fa-133">標頭</span><span class="sxs-lookup"><span data-stu-id="182fa-133">Header</span></span>                   | <span data-ttu-id="182fa-134">d3d9types。h</span><span class="sxs-lookup"><span data-stu-id="182fa-134">d3d9types.h</span></span> |
| <span data-ttu-id="182fa-135">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="182fa-135">Minimum operating system</span></span> | <span data-ttu-id="182fa-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="182fa-136">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="182fa-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="182fa-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="182fa-138">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="182fa-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="182fa-139">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="182fa-139">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="182fa-140">**鎖定**</span><span class="sxs-lookup"><span data-stu-id="182fa-140">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="182fa-141">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="182fa-141">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="182fa-142">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="182fa-142">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="182fa-143">**鎖定**</span><span class="sxs-lookup"><span data-stu-id="182fa-143">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="182fa-144">**LockBox**</span><span class="sxs-lookup"><span data-stu-id="182fa-144">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="182fa-145">**LockBox**</span><span class="sxs-lookup"><span data-stu-id="182fa-145">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="182fa-146">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="182fa-146">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="182fa-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="182fa-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

<span data-ttu-id="182fa-148">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="182fa-148">**LockVertexBuffer**</span></span>
</dt> <dt>

[<span data-ttu-id="182fa-149">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="182fa-149">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="182fa-150">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="182fa-150">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="182fa-151">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="182fa-151">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="182fa-152">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="182fa-152">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
