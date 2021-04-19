---
description: 定義保存資源緩衝區的記憶體類別。
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: 'D3DPOOL 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985531"
---
# <a name="d3dpool-enumeration"></a><span data-ttu-id="35277-103">D3DPOOL 列舉</span><span class="sxs-lookup"><span data-stu-id="35277-103">D3DPOOL enumeration</span></span>

<span data-ttu-id="35277-104">定義保存資源緩衝區的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="35277-104">Defines the memory class that holds the buffers for a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="35277-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35277-105">Syntax</span></span>


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a><span data-ttu-id="35277-106">常數</span><span class="sxs-lookup"><span data-stu-id="35277-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="35277-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="35277-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="35277-108">資源會放在記憶體集區中，最適合指定資源所要求的一組使用方式。</span><span class="sxs-lookup"><span data-stu-id="35277-108">Resources are placed in the memory pool most appropriate for the set of usages requested for the given resource.</span></span> <span data-ttu-id="35277-109">這通常是視訊記憶體，包括本機視訊記憶體和 AGP 記憶體。</span><span class="sxs-lookup"><span data-stu-id="35277-109">This is usually video memory, including both local video memory and AGP memory.</span></span> <span data-ttu-id="35277-110">D3DPOOL \_ 預設集區與 D3DPOOL \_ MANAGED 和 D3DPOOL SYSTEMMEM 不同 \_ ，它指定將資源放在慣用的記憶體中，以供存取裝置。</span><span class="sxs-lookup"><span data-stu-id="35277-110">The D3DPOOL\_DEFAULT pool is separate from D3DPOOL\_MANAGED and D3DPOOL\_SYSTEMMEM, and it specifies that the resource is placed in the preferred memory for device access.</span></span> <span data-ttu-id="35277-111">請注意，D3DPOOL \_ 預設值絕對不會指出 \_ 應該選擇 D3DPOOL MANAGED 或 D3DPOOL \_ SYSTEMMEM 做為此資源的記憶體集區類型。</span><span class="sxs-lookup"><span data-stu-id="35277-111">Note that D3DPOOL\_DEFAULT never indicates that either D3DPOOL\_MANAGED or D3DPOOL\_SYSTEMMEM should be chosen as the memory pool type for this resource.</span></span> <span data-ttu-id="35277-112">放在 D3DPOOL 預設集區中的材質 \_ 無法鎖定，除非它們是動態紋理或私用、FOURCC、驅動程式格式。</span><span class="sxs-lookup"><span data-stu-id="35277-112">Textures placed in the D3DPOOL\_DEFAULT pool cannot be locked unless they are dynamic textures or they are private, FOURCC, driver formats.</span></span> <span data-ttu-id="35277-113">若要存取 unlockable 材質，您必須使用 [**IDirect3DDevice9：： UpdateSurface**](/windows/desktop/api)、 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)、 [**IDirect3DDevice9：： GetFrontBufferData**](/windows/desktop/api)和 [**IDirect3DDevice9：： GetRenderTargetData**](/windows/desktop/api)等函數。</span><span class="sxs-lookup"><span data-stu-id="35277-113">To access unlockable textures, you must use functions such as [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9::GetFrontBufferData**](/windows/desktop/api), and [**IDirect3DDevice9::GetRenderTargetData**](/windows/desktop/api).</span></span> <span data-ttu-id="35277-114">D3DPOOL \_ 受控的選擇可能比 \_ 大多數應用程式的 D3DPOOL 預設值更好。</span><span class="sxs-lookup"><span data-stu-id="35277-114">D3DPOOL\_MANAGED is probably a better choice than D3DPOOL\_DEFAULT for most applications.</span></span> <span data-ttu-id="35277-115">請注意，在驅動程式專屬像素格式中建立的某些紋理（Direct3D 執行時間不明）可以鎖定。</span><span class="sxs-lookup"><span data-stu-id="35277-115">Note that some textures created in driver-proprietary pixel formats, unknown to the Direct3D runtime, can be locked.</span></span> <span data-ttu-id="35277-116">另請注意，-不同于材質交換鏈回緩衝區、轉譯目標、頂點緩衝區和索引緩衝區都可以鎖定。</span><span class="sxs-lookup"><span data-stu-id="35277-116">Also note that - unlike textures - swap chain back buffers, render targets, vertex buffers, and index buffers can be locked.</span></span> <span data-ttu-id="35277-117">裝置遺失時，必須先釋出使用 D3DPOOL 預設建立的資源， \_ 然後再呼叫 [**IDirect3DDevice9：： Reset**](/windows/desktop/api)。</span><span class="sxs-lookup"><span data-stu-id="35277-117">When a device is lost, resources created using D3DPOOL\_DEFAULT must be released before calling [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="35277-118">如需詳細資訊，請參閱 [ (Direct3D 9) 的遺失裝置 ](lost-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="35277-118">For more information, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="35277-119">使用 D3DPOOL 建立資源時 \_ ，如果已認可視訊卡記憶體，將會收回 managed 資源以釋出足夠的記憶體來滿足要求。</span><span class="sxs-lookup"><span data-stu-id="35277-119">When creating resources with D3DPOOL\_DEFAULT, if video card memory is already committed, managed resources will be evicted to free enough memory to satisfy the request.</span></span>

</dd> <dt>

<span data-ttu-id="35277-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL \_ 受控**</span><span class="sxs-lookup"><span data-stu-id="35277-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="35277-121">系統會視需要自動將資源複製到裝置可存取的記憶體。</span><span class="sxs-lookup"><span data-stu-id="35277-121">Resources are copied automatically to device-accessible memory as needed.</span></span> <span data-ttu-id="35277-122">受管理的資源是由系統記憶體所支援，且不需要在裝置遺失時重新建立。</span><span class="sxs-lookup"><span data-stu-id="35277-122">Managed resources are backed by system memory and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="35277-123">如需詳細資訊，請參閱 [ (Direct3D 9 管理資源) ](managing-resources.md) 。</span><span class="sxs-lookup"><span data-stu-id="35277-123">See [Managing Resources (Direct3D 9)](managing-resources.md) for more information.</span></span> <span data-ttu-id="35277-124">受控資源可以鎖定。</span><span class="sxs-lookup"><span data-stu-id="35277-124">Managed resources can be locked.</span></span> <span data-ttu-id="35277-125">系統只會直接修改系統記憶體複製。</span><span class="sxs-lookup"><span data-stu-id="35277-125">Only the system-memory copy is directly modified.</span></span> <span data-ttu-id="35277-126">Direct3D 會視需要將您的變更複製到驅動程式可存取的記憶體。</span><span class="sxs-lookup"><span data-stu-id="35277-126">Direct3D copies your changes to driver-accessible memory as needed.</span></span>



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35277-127">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="35277-127">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="35277-128">D3DPOOL \_ MANAGED 適用于 [**IDirect3DDevice9**](/windows/desktop/api)，但它對 [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="35277-128">D3DPOOL\_MANAGED is valid with [**IDirect3DDevice9**](/windows/desktop/api); however, it is not valid with [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="35277-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="35277-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="35277-130">資源會放在通常不是由 Direct3D 裝置存取的記憶體中。</span><span class="sxs-lookup"><span data-stu-id="35277-130">Resources are placed in memory that is not typically accessible by the Direct3D device.</span></span> <span data-ttu-id="35277-131">此記憶體配置會耗用系統 RAM，但不會減少可分頁的 RAM。</span><span class="sxs-lookup"><span data-stu-id="35277-131">This memory allocation consumes system RAM but does not reduce pageable RAM.</span></span> <span data-ttu-id="35277-132">裝置遺失時，不需要重新建立這些資源。</span><span class="sxs-lookup"><span data-stu-id="35277-132">These resources do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="35277-133">此集區中的資源可以鎖定，並可作為 [**IDirect3DDevice9：： UpdateSurface**](/windows/desktop/api) 或 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) 作業的來源，以使用 D3DPOOL 預設建立的記憶體資源 \_ 。</span><span class="sxs-lookup"><span data-stu-id="35277-133">Resources in this pool can be locked and can be used as the source for a [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api) or [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) operation to a memory resource created with D3DPOOL\_DEFAULT.</span></span>

</dd> <dt>

<span data-ttu-id="35277-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ 臨時**</span><span class="sxs-lookup"><span data-stu-id="35277-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL\_SCRATCH**</span></span>
</dt> <dd>

<span data-ttu-id="35277-135">資源會放在系統 RAM 中，而且不需要在裝置遺失時重新建立。</span><span class="sxs-lookup"><span data-stu-id="35277-135">Resources are placed in system RAM and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="35277-136">這些資源不是依裝置大小或格式限制來系結。</span><span class="sxs-lookup"><span data-stu-id="35277-136">These resources are not bound by device size or format restrictions.</span></span> <span data-ttu-id="35277-137">因此，Direct3D 裝置無法存取這些資源，也無法將其設定為紋理或轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="35277-137">Because of this, these resources cannot be accessed by the Direct3D device nor set as textures or render targets.</span></span> <span data-ttu-id="35277-138">不過，您一律可以建立、鎖定和複製這些資源。</span><span class="sxs-lookup"><span data-stu-id="35277-138">However, these resources can always be created, locked, and copied.</span></span>

</dd> <dt>

<span data-ttu-id="35277-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="35277-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="35277-140">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="35277-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="35277-141">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="35277-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="35277-142">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="35277-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35277-143">備註</span><span class="sxs-lookup"><span data-stu-id="35277-143">Remarks</span></span>

<span data-ttu-id="35277-144">所有的集區類型都適用于所有資源，包括：頂點緩衝區、索引緩衝區、材質和表面。</span><span class="sxs-lookup"><span data-stu-id="35277-144">All pool types are valid with all resources including: vertex buffers, index buffers, textures, and surfaces.</span></span>

<span data-ttu-id="35277-145">下表指出針對轉譯目標、深度樣板和動態和 mipmap 使用方式的集區類型限制。</span><span class="sxs-lookup"><span data-stu-id="35277-145">The following tables indicate restrictions on pool types for render targets, depth stencils, and dynamic and mipmap usages.</span></span> <span data-ttu-id="35277-146">X 表示相容的組合;缺少 x 表示不相容。</span><span class="sxs-lookup"><span data-stu-id="35277-146">An x indicates a compatible combination; lack of an x indicates incompatibility.</span></span>



| <span data-ttu-id="35277-147">集區</span><span class="sxs-lookup"><span data-stu-id="35277-147">Pool</span></span>               | <span data-ttu-id="35277-148">D3DUSAGE \_ RENDERTARGET</span><span class="sxs-lookup"><span data-stu-id="35277-148">D3DUSAGE\_RENDERTARGET</span></span> | <span data-ttu-id="35277-149">D3DUSAGE \_ DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="35277-149">D3DUSAGE\_DEPTHSTENCIL</span></span> |
|--------------------|------------------------|------------------------|
| <span data-ttu-id="35277-150">D3DPOOL \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="35277-150">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="35277-151">x</span><span class="sxs-lookup"><span data-stu-id="35277-151">x</span></span>                      | <span data-ttu-id="35277-152">x</span><span class="sxs-lookup"><span data-stu-id="35277-152">x</span></span>                      |
| <span data-ttu-id="35277-153">D3DPOOL \_ 受控</span><span class="sxs-lookup"><span data-stu-id="35277-153">D3DPOOL\_MANAGED</span></span>   |                        |                        |
| <span data-ttu-id="35277-154">D3DPOOL \_ 臨時</span><span class="sxs-lookup"><span data-stu-id="35277-154">D3DPOOL\_SCRATCH</span></span>   |                        |                        |
| <span data-ttu-id="35277-155">D3DPOOL \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="35277-155">D3DPOOL\_SYSTEMMEM</span></span> |                        |                        |



 



| <span data-ttu-id="35277-156">集區</span><span class="sxs-lookup"><span data-stu-id="35277-156">Pool</span></span>               | <span data-ttu-id="35277-157">D3DUSAGE \_ 動態</span><span class="sxs-lookup"><span data-stu-id="35277-157">D3DUSAGE\_DYNAMIC</span></span> | <span data-ttu-id="35277-158">D3DUSAGE \_ AUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="35277-158">D3DUSAGE\_AUTOGENMIPMAP</span></span> |
|--------------------|-------------------|-------------------------|
| <span data-ttu-id="35277-159">D3DPOOL \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="35277-159">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="35277-160">x</span><span class="sxs-lookup"><span data-stu-id="35277-160">x</span></span>                 | <span data-ttu-id="35277-161">x</span><span class="sxs-lookup"><span data-stu-id="35277-161">x</span></span>                       |
| <span data-ttu-id="35277-162">D3DPOOL \_ 受控</span><span class="sxs-lookup"><span data-stu-id="35277-162">D3DPOOL\_MANAGED</span></span>   |                   | <span data-ttu-id="35277-163">x</span><span class="sxs-lookup"><span data-stu-id="35277-163">x</span></span>                       |
| <span data-ttu-id="35277-164">D3DPOOL \_ 臨時</span><span class="sxs-lookup"><span data-stu-id="35277-164">D3DPOOL\_SCRATCH</span></span>   |                   |                         |
| <span data-ttu-id="35277-165">D3DPOOL \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="35277-165">D3DPOOL\_SYSTEMMEM</span></span> | <span data-ttu-id="35277-166">x</span><span class="sxs-lookup"><span data-stu-id="35277-166">x</span></span>                 |                         |



 

<span data-ttu-id="35277-167">如需使用類型的詳細資訊，請參閱 [**D3DUSAGE**](d3dusage.md)。</span><span class="sxs-lookup"><span data-stu-id="35277-167">For more information about usage types, see [**D3DUSAGE**](d3dusage.md).</span></span>

<span data-ttu-id="35277-168">集區無法針對 mipmap) 中一個資源 (mip 層級內包含的不同物件混合使用，而且當選擇集區時，就無法變更。</span><span class="sxs-lookup"><span data-stu-id="35277-168">Pools cannot be mixed for different objects contained within one resource (mip levels in a mipmap) and, when a pool is chosen, it cannot be changed.</span></span>

<span data-ttu-id="35277-169">應用程式應該 \_ 針對大部分靜態資源使用 D3DPOOL 管理，因為這可讓應用程式不需要處理遺失的裝置。</span><span class="sxs-lookup"><span data-stu-id="35277-169">Applications should use D3DPOOL\_MANAGED for most static resources because this saves the application from having to deal with lost devices.</span></span> <span data-ttu-id="35277-170">執行時間會還原 (的受控資源。 ) 這對 (UMA) 系統的統一記憶體架構特別有用。</span><span class="sxs-lookup"><span data-stu-id="35277-170">(Managed resources are restored by the runtime.) This is especially beneficial for unified memory architecture (UMA) systems.</span></span> <span data-ttu-id="35277-171">其他動態資源不適合用于 D3DPOOL \_ 管理。</span><span class="sxs-lookup"><span data-stu-id="35277-171">Other dynamic resources are not a good match for D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="35277-172">事實上，您無法使用 D3DPOOL \_ MANAGED 搭配 D3DUSAGE DYNAMIC 來建立索引緩衝區和頂點緩衝區 \_ 。</span><span class="sxs-lookup"><span data-stu-id="35277-172">In fact, index buffers and vertex buffers cannot be created using D3DPOOL\_MANAGED together with D3DUSAGE\_DYNAMIC.</span></span>

<span data-ttu-id="35277-173">若為動態紋理，有時會想要使用一對影片記憶體和系統記憶體材質，使用 D3DPOOL \_ 預設值和系統記憶體（使用 D3DPOOL SYSTEMMEM）配置視訊記憶體 \_ 。</span><span class="sxs-lookup"><span data-stu-id="35277-173">For dynamic textures, it is sometimes desirable to use a pair of video memory and system memory textures, allocating the video memory using D3DPOOL\_DEFAULT and the system memory using D3DPOOL\_SYSTEMMEM.</span></span> <span data-ttu-id="35277-174">您可以使用鎖定方法來鎖定和修改系統記憶體材質的位。</span><span class="sxs-lookup"><span data-stu-id="35277-174">You can lock and modify the bits of the system memory texture using a locking method.</span></span> <span data-ttu-id="35277-175">然後，您可以使用 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)來更新視訊記憶體材質。</span><span class="sxs-lookup"><span data-stu-id="35277-175">Then you can update the video memory texture using [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

## <a name="requirements"></a><span data-ttu-id="35277-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="35277-176">Requirements</span></span>



| <span data-ttu-id="35277-177">需求</span><span class="sxs-lookup"><span data-stu-id="35277-177">Requirement</span></span> | <span data-ttu-id="35277-178">值</span><span class="sxs-lookup"><span data-stu-id="35277-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35277-179">標頭</span><span class="sxs-lookup"><span data-stu-id="35277-179">Header</span></span><br/> | <dl> <span data-ttu-id="35277-180"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="35277-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35277-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35277-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35277-182">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="35277-182">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="35277-183">**D3DUSAGE**</span><span class="sxs-lookup"><span data-stu-id="35277-183">**D3DUSAGE**</span></span>](d3dusage.md)
</dt> <dt>

[<span data-ttu-id="35277-184">**IDirect3DDevice9::CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="35277-184">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[<span data-ttu-id="35277-185">**IDirect3DDevice9::CreateIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="35277-185">**IDirect3DDevice9::CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[<span data-ttu-id="35277-186">**IDirect3DDevice9::CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="35277-186">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[<span data-ttu-id="35277-187">**IDirect3DDevice9::CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="35277-187">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[<span data-ttu-id="35277-188">**IDirect3DDevice9::CreateVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="35277-188">**IDirect3DDevice9::CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[<span data-ttu-id="35277-189">**D3DINDEXBUFFER \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="35277-189">**D3DINDEXBUFFER\_DESC**</span></span>](d3dindexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="35277-190">**D3DSURFACE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="35277-190">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> <dt>

[<span data-ttu-id="35277-191">**D3DVERTEXBUFFER \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="35277-191">**D3DVERTEXBUFFER\_DESC**</span></span>](d3dvertexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="35277-192">**D3DVOLUME \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="35277-192">**D3DVOLUME\_DESC**</span></span>](d3dvolume-desc.md)
</dt> </dl>

 

 
