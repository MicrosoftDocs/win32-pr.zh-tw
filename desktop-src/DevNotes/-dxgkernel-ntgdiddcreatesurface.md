---
description: NtGdiDdCreateSurface 函式-將介面附加至另一個介面。
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: 'NtGdiDdCreateSurface 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bf8e13cff80ddea4e102c045c174565e7e835274
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085776"
---
# <a name="ntgdiddcreatesurface-function"></a><span data-ttu-id="55643-103">NtGdiDdCreateSurface 函式</span><span class="sxs-lookup"><span data-stu-id="55643-103">NtGdiDdCreateSurface function</span></span>

<span data-ttu-id="55643-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="55643-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="55643-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="55643-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="55643-106">將介面附加至另一個介面。</span><span class="sxs-lookup"><span data-stu-id="55643-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="55643-107">語法</span><span class="sxs-lookup"><span data-stu-id="55643-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="55643-108">參數</span><span class="sxs-lookup"><span data-stu-id="55643-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55643-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55643-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55643-110">代表驅動程式之 [**DD \_ DIRECTDRAW \_ 全域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="55643-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="55643-111">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55643-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55643-112">相同介面的先前控制碼。</span><span class="sxs-lookup"><span data-stu-id="55643-112">Previous handle to the same surface.</span></span> <span data-ttu-id="55643-113">如果介面是在模式切換之後重新建立，則會使用。</span><span class="sxs-lookup"><span data-stu-id="55643-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="55643-114">*puSurfaceDescription* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="55643-114">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55643-115">描述驅動程式應建立之介面或緩衝區的 [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="55643-115">Pointer to the [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="55643-116">*puSurfaceGlobalData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="55643-116">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55643-117">[**DD \_ 介面 \_ 全域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global)結構的指標，其中包含與多個表面全域共用的表面資料。</span><span class="sxs-lookup"><span data-stu-id="55643-117">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="55643-118">*puSurfaceLocalData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="55643-118">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55643-119">[**DD \_ 介面 \_ 本機**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構清單的指標，描述驅動程式所建立的介面物件。</span><span class="sxs-lookup"><span data-stu-id="55643-119">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="55643-120">*puSurfaceMoreData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="55643-120">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55643-121">[**DD \_ 介面 \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more)的指標，此結構包含額外的本機介面資料。</span><span class="sxs-lookup"><span data-stu-id="55643-121">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="55643-122">*puCreateSurfaceData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="55643-122">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55643-123">[**DD \_ CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata)結構的指標，其中包含建立表面所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="55643-123">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create a surface.</span></span>

</dd> <dt>

<span data-ttu-id="55643-124">*puhSurface* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="55643-124">*puhSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55643-125">供 DirectDraw API 使用，而且不應該由驅動程式填入。</span><span class="sxs-lookup"><span data-stu-id="55643-125">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55643-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="55643-126">Return value</span></span>

<span data-ttu-id="55643-127">**NtGdiDdCreateSurface** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="55643-127">**NtGdiDdCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="55643-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="55643-128">Return code</span></span>                                                                                              | <span data-ttu-id="55643-129">Description</span><span class="sxs-lookup"><span data-stu-id="55643-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55643-130"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="55643-130"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="55643-131">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="55643-131">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="55643-132">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="55643-132">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="55643-133">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="55643-133">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="55643-134"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="55643-134"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="55643-135">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="55643-135">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="55643-136">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="55643-136">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="55643-137">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="55643-137">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55643-138">備註</span><span class="sxs-lookup"><span data-stu-id="55643-138">Remarks</span></span>

<span data-ttu-id="55643-139">建議您的應用程式呼叫 [IDirectDraw7：： CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) ，而不是使用此函數。</span><span class="sxs-lookup"><span data-stu-id="55643-139">It is recommended that your application call [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) instead of using this function.</span></span>

<span data-ttu-id="55643-140">建立一連串的連接表面（例如交換鏈或鏈或 mipmap）時，應該先針對每個介面呼叫 [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) 。</span><span class="sxs-lookup"><span data-stu-id="55643-140">When creating a chain of attached surfaces, such as a swap chain or chain or mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) should be called for each surface first.</span></span> <span data-ttu-id="55643-141">然後呼叫 [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) 來附加它們。</span><span class="sxs-lookup"><span data-stu-id="55643-141">Then call [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) to attach them.</span></span> <span data-ttu-id="55643-142">最後，只針對鏈中的第一個介面呼叫 **NtGdiDdCreateSurface** 。</span><span class="sxs-lookup"><span data-stu-id="55643-142">Finally, call **NtGdiDdCreateSurface** for the first surface in the chain only.</span></span> <span data-ttu-id="55643-143">在此情況下， *hSurface* 會是 **NtGdiDdCreateSurfaceObject** 針對鏈中第一個介面所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="55643-143">In this case, *hSurface* would be the handle returned by **NtGdiDdCreateSurfaceObject** for the first surface in the chain.</span></span>

<span data-ttu-id="55643-144">只應呼叫 **NtGdiDdCreateSurface** ，以在本機和非本機視訊記憶體中建立介面。</span><span class="sxs-lookup"><span data-stu-id="55643-144">**NtGdiDdCreateSurface** should only be called to create surfaces in local and non-local video memory.</span></span> <span data-ttu-id="55643-145">永遠不應該呼叫它來建立系統記憶體表面。</span><span class="sxs-lookup"><span data-stu-id="55643-145">It should never be called to create system memory surfaces.</span></span> <span data-ttu-id="55643-146">若要建立系統記憶體表面，請改用 [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) 。</span><span class="sxs-lookup"><span data-stu-id="55643-146">To create system memory surfaces, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="55643-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="55643-147">Requirements</span></span>



| <span data-ttu-id="55643-148">需求</span><span class="sxs-lookup"><span data-stu-id="55643-148">Requirement</span></span> | <span data-ttu-id="55643-149">值</span><span class="sxs-lookup"><span data-stu-id="55643-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55643-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55643-150">Minimum supported client</span></span><br/> | <span data-ttu-id="55643-151">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55643-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="55643-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55643-152">Minimum supported server</span></span><br/> | <span data-ttu-id="55643-153">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55643-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="55643-154">標頭</span><span class="sxs-lookup"><span data-stu-id="55643-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="55643-155"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="55643-155"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55643-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55643-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55643-157">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="55643-157">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
