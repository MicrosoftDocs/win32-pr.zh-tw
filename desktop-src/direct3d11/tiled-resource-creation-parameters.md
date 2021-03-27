---
title: 磚資源建立參數
description: 您可以使用 D3D11 資源其他並排顯示旗標建立的 Direct3D 資源類型有一些 \_ 限制 \_ \_ 。 本節提供用來建立磚資源的有效參數。
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b912325371c59bd46a6cc4245289b2fe5d32a924
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/13/2019
ms.locfileid: "103679087"
---
# <a name="tiled-resource-creation-parameters"></a><span data-ttu-id="14368-104">磚資源建立參數</span><span class="sxs-lookup"><span data-stu-id="14368-104">Tiled resource creation parameters</span></span>

<span data-ttu-id="14368-105">您可以使用 [**D3D11 \_ 資源 \_ 其他 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 並排顯示旗標建立的 Direct3D 資源類型有一些限制。</span><span class="sxs-lookup"><span data-stu-id="14368-105">There are some constraints on the type of Direct3D resources that you can create with the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> <span data-ttu-id="14368-106">本節提供用來建立磚資源的有效參數。</span><span class="sxs-lookup"><span data-stu-id="14368-106">This section provides the valid parameters for creating tiled resources.</span></span>

<dl> <dt>

<span data-ttu-id="14368-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**支援的資源類型**</span><span class="sxs-lookup"><span data-stu-id="14368-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Supported Resource Type**</span></span>
</dt> <dd>

<span data-ttu-id="14368-108">Texture2D \[ 陣列 \] (包括 TextureCube \[ 陣列 \] ，這是 Texture2D \[ 陣列 \]) 或緩衝區的變異。</span><span class="sxs-lookup"><span data-stu-id="14368-108">Texture2D\[Array\] (including TextureCube\[Array\], which is a variant of Texture2D\[Array\]) or Buffer.</span></span>

<span data-ttu-id="14368-109">**不支援：** Texture1D \[ 陣列 \] 或 Texture3D，但未來可能會支援 Texture3D。</span><span class="sxs-lookup"><span data-stu-id="14368-109">**NOT supported:** Texture1D\[Array\] or Texture3D, but Texture3D might be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="14368-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**支援的資源使用方式**</span><span class="sxs-lookup"><span data-stu-id="14368-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="14368-111">D3D11 \_ 使用 \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="14368-111">D3D11\_USAGE\_DEFAULT.</span></span>

<span data-ttu-id="14368-112">**不支援：** D3D11 \_ 使用 \_ 動態、D3D11 \_ 使用 \_ 暫存或 D3D11 \_ 使用量 \_ 不可變。</span><span class="sxs-lookup"><span data-stu-id="14368-112">**NOT supported:** D3D11\_USAGE\_DYNAMIC, D3D11\_USAGE\_STAGING, or D3D11\_USAGE\_IMMUTABLE.</span></span>

</dd> <dt>

<span data-ttu-id="14368-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**支援的資源其他旗標**</span><span class="sxs-lookup"><span data-stu-id="14368-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="14368-114">D3D11 \_ \_ \_ 由定義) 、 \_ 其他 \_ TEXTURECUBE、DRAWINDIRECT 引數 \_ \_ 、 \_ 緩衝區 \_ 允許 \_ 原始 \_ 的視圖、 \_ 緩衝區 \_ 結構化、 \_ 資源資源區 \_ ，或 \_ 產生 \_ MIPS 的資源其他 (並排顯示的。</span><span class="sxs-lookup"><span data-stu-id="14368-114">D3D11\_RESOURCE\_MISC\_TILED (by definition), \_MISC\_TEXTURECUBE, \_DRAWINDIRECT\_ARGS, \_BUFFER\_ALLOW\_RAW\_VIEWS, \_BUFFER\_STRUCTURED, \_RESOURCE\_CLAMP, or \_GENERATE\_MIPS.</span></span>

<span data-ttu-id="14368-115">**不支援：** \_共用、 \_ 共用 \_ KEYEDMUTEX、 \_ GDI \_ 相容、 \_ 共用 \_ NTHANDLE、 \_ 受限 \_ 的內容、 \_ 限制 \_ 共用 \_ 資源、 \_ 限制 \_ 共用 \_ 資源 \_ 驅動程式、受防護 \_ 或 \_ 磚集區 \_ 。</span><span class="sxs-lookup"><span data-stu-id="14368-115">**NOT supported:** \_SHARED, \_SHARED\_KEYEDMUTEX, \_GDI\_COMPATIBLE, \_SHARED\_NTHANDLE, \_RESTRICTED\_CONTENT, \_RESTRICT\_SHARED\_RESOURCE, \_RESTRICT\_SHARED\_RESOURCE\_DRIVER, \_GUARDED, or \_TILE\_POOL.</span></span>

</dd> <dt>

<span data-ttu-id="14368-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**支援的系結旗標**</span><span class="sxs-lookup"><span data-stu-id="14368-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Supported Bind Flags**</span></span>
</dt> <dd>

<span data-ttu-id="14368-117">D3D11 系結 \_ \_ 著色器 \_ 資源、轉譯 \_ \_ 目標、 \_ 深度樣板或未 \_ \_ 排序 \_ 的存取。</span><span class="sxs-lookup"><span data-stu-id="14368-117">D3D11\_BIND\_SHADER\_RESOURCE, \_RENDER\_TARGET, \_DEPTH\_STENCIL, or \_UNORDERED\_ACCESS.</span></span>

<span data-ttu-id="14368-118">**不支援：** \_常數 \_ 緩衝區、 \_ 頂點緩衝區附注，將並排緩衝區系結 \_ \[ 為 SRV/UAV/RTV 仍然是正常的 \] 、 \_ 索引 \_ 緩衝區、 \_ 串流輸出、系結解碼器或系結 \_ \_ \_ \_ \_ 影片 \_ 編碼器。</span><span class="sxs-lookup"><span data-stu-id="14368-118">**NOT supported:** \_CONSTANT\_BUFFER, \_VERTEX\_BUFFER \[note that binding a tiled Buffer as an SRV/UAV/RTV is still ok\], \_INDEX\_BUFFER, \_STREAM\_OUTPUT, \_BIND\_DECODER, or \_BIND\_VIDEO\_ENCODER.</span></span>

</dd> <dt>

<span data-ttu-id="14368-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**支援的格式**</span><span class="sxs-lookup"><span data-stu-id="14368-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Supported Formats**</span></span>
</dt> <dd>

<span data-ttu-id="14368-120">特定設定的所有格式 (不管它是區塊式)，但有一些例外。</span><span class="sxs-lookup"><span data-stu-id="14368-120">All formats that would be available for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="14368-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**支援的 SampleDesc (的高取樣計數、品質)**</span><span class="sxs-lookup"><span data-stu-id="14368-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Supported SampleDesc (Multisample count, quality)**</span></span>
</dt> <dd>

<span data-ttu-id="14368-122">特定設定的所有描述都會受支援 (不管它是區塊式)，但有一些例外。</span><span class="sxs-lookup"><span data-stu-id="14368-122">Whatever would be supported for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="14368-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**支援的寬度/高度/MipLevels/ArraySize**</span><span class="sxs-lookup"><span data-stu-id="14368-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Supported Width/Height/MipLevels/ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="14368-124">Direct3D 11 支援的完整範圍。</span><span class="sxs-lookup"><span data-stu-id="14368-124">Full extents supported by Direct3D 11.</span></span> <span data-ttu-id="14368-125">並排顯示的資源並不會限制非並排顯示資源上的總記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="14368-125">Tiled resources don't have the restriction on total memory size imposed on non-tiled resources.</span></span> <span data-ttu-id="14368-126">磚的資源只會受到整體虛擬位址空間限制的限制。</span><span class="sxs-lookup"><span data-stu-id="14368-126">Tiled resources are only constrained by overall virtual address space limits.</span></span> <span data-ttu-id="14368-127">如需詳細資訊，請參閱 [適用于並排資源的位址空間](address-space-available-for-tiled-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="14368-127">For info, see [Address space available for tiled resources](address-space-available-for-tiled-resources.md).</span></span>

</dd> </dl>

<span data-ttu-id="14368-128">磚集區記憶體的初始內容未定義。</span><span class="sxs-lookup"><span data-stu-id="14368-128">The initial contents of tile pool memory are undefined.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14368-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="14368-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14368-130">建立磚資源</span><span class="sxs-lookup"><span data-stu-id="14368-130">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




