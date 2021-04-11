---
description: 建立核心模式介面物件，此物件表示 puSurfaceLocal 所參考的使用者模式介面物件。
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: 'NtGdiDdCreateSurfaceObject 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025839"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a><span data-ttu-id="bda2b-103">NtGdiDdCreateSurfaceObject 函式</span><span class="sxs-lookup"><span data-stu-id="bda2b-103">NtGdiDdCreateSurfaceObject function</span></span>

<span data-ttu-id="bda2b-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="bda2b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="bda2b-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="bda2b-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="bda2b-106">建立核心模式介面物件，此物件表示 *puSurfaceLocal* 所參考的使用者模式介面物件。</span><span class="sxs-lookup"><span data-stu-id="bda2b-106">Creates a kernel-mode surface object that represents the user-mode surface object referenced by *puSurfaceLocal*.</span></span>

## <a name="syntax"></a><span data-ttu-id="bda2b-107">語法</span><span class="sxs-lookup"><span data-stu-id="bda2b-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a><span data-ttu-id="bda2b-108">參數</span><span class="sxs-lookup"><span data-stu-id="bda2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda2b-109">*hDirectDrawLocal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bda2b-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda2b-110">核心模式 DirectDraw 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bda2b-110">Handle to the kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="bda2b-111">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bda2b-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda2b-112">相同介面的先前控制碼。</span><span class="sxs-lookup"><span data-stu-id="bda2b-112">Previous handle to the same surface.</span></span> <span data-ttu-id="bda2b-113">如果介面是在模式切換之後重新建立，則會使用。</span><span class="sxs-lookup"><span data-stu-id="bda2b-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="bda2b-114">*puSurfaceLocal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bda2b-114">*puSurfaceLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda2b-115">[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的指標，代表要與配置的記憶體相關聯的 DirectDraw 使用者模式介面物件。</span><span class="sxs-lookup"><span data-stu-id="bda2b-115">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw user-mode surface object with which to associate the allocated memory.</span></span> <span data-ttu-id="bda2b-116">請參閱 DDK 檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bda2b-116">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="bda2b-117">*puSurfaceMore* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bda2b-117">*puSurfaceMore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda2b-118">[**DD 介面的指標 \_ \_ 更多**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more)結構，其中包含每個個別介面物件的額外本機資料。</span><span class="sxs-lookup"><span data-stu-id="bda2b-118">Pointer to the [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local data for each individual surface object.</span></span> <span data-ttu-id="bda2b-119">請參閱 DDK 檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bda2b-119">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="bda2b-120">*puSurfaceGlobal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bda2b-120">*puSurfaceGlobal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda2b-121">[**DD \_ 介面 \_ 全域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global)結構的指標，其中包含全域與多個表面共用的介面資料。</span><span class="sxs-lookup"><span data-stu-id="bda2b-121">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure that contains surface data shared globally with multiple surfaces.</span></span> <span data-ttu-id="bda2b-122">請參閱 DDK 檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bda2b-122">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="bda2b-123">*bComplete* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bda2b-123">*bComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda2b-124">核心模式物件完成旗標。</span><span class="sxs-lookup"><span data-stu-id="bda2b-124">Kernel-mode object completion flag.</span></span> <span data-ttu-id="bda2b-125">可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bda2b-125">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="bda2b-126"> (TRUE) </span><span class="sxs-lookup"><span data-stu-id="bda2b-126">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="bda2b-127">完成有關核心模式表示的所有處理。</span><span class="sxs-lookup"><span data-stu-id="bda2b-127">Complete all processing concerning the kernel-mode representation.</span></span>

</dd> <dt>



 <span data-ttu-id="bda2b-128"> (FALSE) </span><span class="sxs-lookup"><span data-stu-id="bda2b-128">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="bda2b-129">建立物件，但不設定內部資料，例如記憶體指標。</span><span class="sxs-lookup"><span data-stu-id="bda2b-129">Create the object, but do not set up internal data such as the memory pointer.</span></span> <span data-ttu-id="bda2b-130">使用 **FALSE** 建立的物件可以使用 [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) 來附加，而且是透過呼叫 [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)來完成。</span><span class="sxs-lookup"><span data-stu-id="bda2b-130">Objects created using **FALSE** can be attached using [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) and are completed by a call to [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda2b-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="bda2b-131">Return value</span></span>

<span data-ttu-id="bda2b-132">如果成功，此函式會傳回核心模式介面標記法的控制碼;否則，它會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bda2b-132">If successful, this function returns a handle to the kernel-mode surface representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bda2b-133">備註</span><span class="sxs-lookup"><span data-stu-id="bda2b-133">Remarks</span></span>

<span data-ttu-id="bda2b-134">建議應用程式使用 DirectDraw 和 [Direct3D](../direct3d10/d3d10-graphics-reference.md) api 來建立和管理圖形裝置物件。</span><span class="sxs-lookup"><span data-stu-id="bda2b-134">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="bda2b-135">這些結構以簡化與作業系統無關的方式來抽象化裝置建立程式。</span><span class="sxs-lookup"><span data-stu-id="bda2b-135">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda2b-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="bda2b-136">Requirements</span></span>



| <span data-ttu-id="bda2b-137">需求</span><span class="sxs-lookup"><span data-stu-id="bda2b-137">Requirement</span></span> | <span data-ttu-id="bda2b-138">值</span><span class="sxs-lookup"><span data-stu-id="bda2b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bda2b-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bda2b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="bda2b-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bda2b-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bda2b-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bda2b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="bda2b-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bda2b-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bda2b-143">標頭</span><span class="sxs-lookup"><span data-stu-id="bda2b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda2b-144"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="bda2b-144"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bda2b-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bda2b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda2b-146">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="bda2b-146">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="bda2b-147">**DdCreateSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="bda2b-147">**DdCreateSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[<span data-ttu-id="bda2b-148">**NtGdiDdDeleteSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="bda2b-148">**NtGdiDdDeleteSurfaceObject**</span></span>](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[<span data-ttu-id="bda2b-149">**NtGdiDdAttachSurface**</span><span class="sxs-lookup"><span data-stu-id="bda2b-149">**NtGdiDdAttachSurface**</span></span>](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[<span data-ttu-id="bda2b-150">**NtGdiDdCreateSurface**</span><span class="sxs-lookup"><span data-stu-id="bda2b-150">**NtGdiDdCreateSurface**</span></span>](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
