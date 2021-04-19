---
description: 應用程式可以藉由指定 &\# 0034; 變更&\# 0034; 材質上的區域，優化複製材質的子集。
ms.assetid: 102081bc-d5d5-4ec1-b935-00d4eda8f470
title: " (Direct3D 9) 的材質中途區域"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e3f1ce350a2728c99c49455b5fb8b638c47d10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970694"
---
# <a name="texture-dirty-regions-direct3d-9"></a><span data-ttu-id="b06bb-103"> (Direct3D 9) 的材質中途區域</span><span class="sxs-lookup"><span data-stu-id="b06bb-103">Texture Dirty Regions (Direct3D 9)</span></span>

<span data-ttu-id="b06bb-104">應用程式可以在紋理上指定「已變更」區域，以優化材質的子集複製。</span><span class="sxs-lookup"><span data-stu-id="b06bb-104">Applications can optimize which subset of a texture is copied by specifying "dirty" regions on textures.</span></span> <span data-ttu-id="b06bb-105">只有標記為中途的區域會透過呼叫 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)來複製。</span><span class="sxs-lookup"><span data-stu-id="b06bb-105">Only those regions marked as dirty are copied by a call to [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span> <span data-ttu-id="b06bb-106">不過，可能會擴充中途區域以優化對齊。</span><span class="sxs-lookup"><span data-stu-id="b06bb-106">However, the dirty regions may be expanded to optimize alignment.</span></span> <span data-ttu-id="b06bb-107">建立材質時，會將整個材質視為中途變更。</span><span class="sxs-lookup"><span data-stu-id="b06bb-107">When a texture is created, the entire texture is considered dirty.</span></span> <span data-ttu-id="b06bb-108">只有下列作業會影響材質的變更狀態：</span><span class="sxs-lookup"><span data-stu-id="b06bb-108">Only the following operations affect the dirty state of a texture:</span></span>

-   <span data-ttu-id="b06bb-109">將中途區域新增至材質。</span><span class="sxs-lookup"><span data-stu-id="b06bb-109">Adding a dirty region to a texture.</span></span>
-   <span data-ttu-id="b06bb-110">鎖定材質中的一些緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b06bb-110">Locking some buffer in the texture.</span></span> <span data-ttu-id="b06bb-111">此作業會將鎖定的區域新增為中途區域。</span><span class="sxs-lookup"><span data-stu-id="b06bb-111">This operation adds the locked region as a dirty region.</span></span> <span data-ttu-id="b06bb-112">如果應用程式對實際的中途區域有更好的瞭解，就可以關閉此自動變更區域更新。</span><span class="sxs-lookup"><span data-stu-id="b06bb-112">The application can turn off this automatic dirty region update if it has better knowledge of the actual dirty regions.</span></span>
-   <span data-ttu-id="b06bb-113">使用紋理的介面層級做為 [**IDirect3DDevice9：： UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) 中的目的地，會將整個材質標示為中途。</span><span class="sxs-lookup"><span data-stu-id="b06bb-113">Using a surface level of the texture as a destination in [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) marks the entire texture as dirty.</span></span>
-   <span data-ttu-id="b06bb-114">在 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) 中使用材質作為來源，會清除來源材質上的所有中途區域。</span><span class="sxs-lookup"><span data-stu-id="b06bb-114">Using the texture as a source in [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) clears all the dirty regions on the source texture.</span></span>
-   <span data-ttu-id="b06bb-115">使用 [**IDirect3DSurface9：： GetDC**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc) 傳回裝置內容。</span><span class="sxs-lookup"><span data-stu-id="b06bb-115">Using [**IDirect3DSurface9::GetDC**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc) to return a device context.</span></span>
-   <span data-ttu-id="b06bb-116">呼叫 [**IDirect3DBaseTexture9：： GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) 會將整個材質標示為中途。</span><span class="sxs-lookup"><span data-stu-id="b06bb-116">Calling [**IDirect3DBaseTexture9::GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) marks the entire texture as dirty.</span></span>
-   <span data-ttu-id="b06bb-117">呼叫 [**IDirect3DBaseTexture9：： SetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype) 會將整個材質標示為中途。</span><span class="sxs-lookup"><span data-stu-id="b06bb-117">Calling [**IDirect3DBaseTexture9::SetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype) marks the entire texture as dirty.</span></span>

<span data-ttu-id="b06bb-118">中途區域是在 mipmapped 材質的最上層設定，而 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) 可將中途區域展開至 mip 鏈，以將每個子層級複製的位元組數目降至最低。</span><span class="sxs-lookup"><span data-stu-id="b06bb-118">Dirty regions are set on the top level of a mipmapped texture, and [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) can expand the dirty region down the mip chain in order to minimize the number of bytes copied for each sublevel.</span></span> <span data-ttu-id="b06bb-119">請注意，子層中途區域座標會向外舍入，也就是說，其小數部分會舍入至最接近紋理的邊緣。</span><span class="sxs-lookup"><span data-stu-id="b06bb-119">Note that the sublevel dirty region coordinates are rounded outward, that is, their fractional parts are rounded toward the nearest edge of the texture.</span></span>

<span data-ttu-id="b06bb-120">由於每種材質類型都有不同類型的中途區域，因此每個材質類型都有方法。</span><span class="sxs-lookup"><span data-stu-id="b06bb-120">Because each type of texture has different types of dirty regions, there are methods on each texture type.</span></span> <span data-ttu-id="b06bb-121">2D 紋理使用中途矩形，以及大量紋理使用方塊。</span><span class="sxs-lookup"><span data-stu-id="b06bb-121">2D textures use dirty rectangle, and volume textures use boxes.</span></span>

-   [<span data-ttu-id="b06bb-122">**IDirect3DCubeTexture9::AddDirtyRect**</span><span class="sxs-lookup"><span data-stu-id="b06bb-122">**IDirect3DCubeTexture9::AddDirtyRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
-   [<span data-ttu-id="b06bb-123">**IDirect3DTexture9::AddDirtyRect**</span><span class="sxs-lookup"><span data-stu-id="b06bb-123">**IDirect3DTexture9::AddDirtyRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect)
-   [<span data-ttu-id="b06bb-124">**IDirect3DVolumeTexture9::AddDirtyBox**</span><span class="sxs-lookup"><span data-stu-id="b06bb-124">**IDirect3DVolumeTexture9::AddDirtyBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox)

<span data-ttu-id="b06bb-125">針對上述方法傳遞 **Null** 作為 PDirtyRect 或 pDirtyBox 參數，會展開中途區域以涵蓋整個材質。</span><span class="sxs-lookup"><span data-stu-id="b06bb-125">Passing **NULL** for the pDirtyRect or pDirtyBox parameters for the above methods expands the dirty region to cover the entire texture.</span></span>

<span data-ttu-id="b06bb-126">每個鎖定方法都可以 D3DLOCK \_ 沒有中途 \_ \_ 更新，這可防止材質的變更狀態變更。</span><span class="sxs-lookup"><span data-stu-id="b06bb-126">Each lock method can take D3DLOCK\_NO\_DIRTY\_UPDATE, which prevents any changes to the dirty state of the texture.</span></span> <span data-ttu-id="b06bb-127">如需詳細資訊，請參閱 [ (Direct3D 9) 的鎖定資源 ](locking-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="b06bb-127">For more information, see [Locking Resources (Direct3D 9)](locking-resources.md).</span></span>

<span data-ttu-id="b06bb-128">如果有關于在鎖定作業期間變更之真組區域的詳細資訊，應用程式應該使用 D3DLOCK \_ NO \_ DIRTY \_ UPDATE。</span><span class="sxs-lookup"><span data-stu-id="b06bb-128">When more information about the true set of regions that are changed during a lock operation is available, applications should use D3DLOCK\_NO\_DIRTY\_UPDATE.</span></span> <span data-ttu-id="b06bb-129">請注意，只有在不鎖定或複製到最上層) 的情況下，才會鎖定或複製材質子層 (也不會更新該材質的中途區域。</span><span class="sxs-lookup"><span data-stu-id="b06bb-129">Note that a lock or a copy to a texture sublevel only (that is, without locking or copying to the top level) does not update the dirty regions for that texture.</span></span> <span data-ttu-id="b06bb-130">當應用程式鎖定較低的層級，而不鎖定最上層時，應用程式會採用相同的責任來更新中途區域。</span><span class="sxs-lookup"><span data-stu-id="b06bb-130">Applications assume the same responsibility for updating dirty regions when they lock lower levels without locking the topmost level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b06bb-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="b06bb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b06bb-132">基本紋理概念</span><span class="sxs-lookup"><span data-stu-id="b06bb-132">Basic Texturing Concepts</span></span>](basic-texturing-concepts.md)
</dt> </dl>

 

 
