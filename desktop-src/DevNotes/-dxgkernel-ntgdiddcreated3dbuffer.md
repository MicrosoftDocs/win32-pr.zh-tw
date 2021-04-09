---
description: 用來建立指定之描述的驅動程式層級命令或頂點緩衝區。
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: 'NtGdiDdCreateD3DBuffer 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2d402a70822fba094d22c82b8767ee3298b86374
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936097"
---
# <a name="ntgdiddcreated3dbuffer-function"></a><span data-ttu-id="1278f-103">NtGdiDdCreateD3DBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="1278f-103">NtGdiDdCreateD3DBuffer function</span></span>

<span data-ttu-id="1278f-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="1278f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1278f-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="1278f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1278f-106">用來建立指定之描述的驅動程式層級命令或頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1278f-106">Used to create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1278f-107">語法</span><span class="sxs-lookup"><span data-stu-id="1278f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="1278f-108">參數</span><span class="sxs-lookup"><span data-stu-id="1278f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1278f-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1278f-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1278f-110">代表驅動程式之 [**DD \_ DIRECTDRAW \_ 全域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1278f-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="1278f-111">*hSurface* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1278f-111">*hSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1278f-112">介面控點陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1278f-112">Pointer to an array of surface handles.</span></span> <span data-ttu-id="1278f-113">如果在模式切換之後重新建立介面，呼叫端可以將這些控制碼設定為先前的控制碼值。</span><span class="sxs-lookup"><span data-stu-id="1278f-113">The caller can set these handles to the previous handle values if the surfaces are being re-created after a mode switch.</span></span> <span data-ttu-id="1278f-114">此程式在 DirectDraw 檔中稱為「還原」。</span><span class="sxs-lookup"><span data-stu-id="1278f-114">This process is called "restoring" in the DirectDraw documentation.</span></span>

</dd> <dt>

<span data-ttu-id="1278f-115">*puSurfaceDescription* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1278f-115">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1278f-116">描述驅動程式應建立之介面或緩衝區的 [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="1278f-116">Pointer to a [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="1278f-117">*puSurfaceGlobalData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1278f-117">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1278f-118">[**DD \_ 介面 \_ 全域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global)結構的指標，其中包含與多個表面共用的介面資料。</span><span class="sxs-lookup"><span data-stu-id="1278f-118">Pointer to a [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="1278f-119">*puSurfaceLocalData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1278f-119">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1278f-120">[**DD \_ 介面 \_ 本機**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構清單的指標，描述驅動程式所建立的介面物件。</span><span class="sxs-lookup"><span data-stu-id="1278f-120">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span> <span data-ttu-id="1278f-121">此陣列中通常只有一個專案。</span><span class="sxs-lookup"><span data-stu-id="1278f-121">There is usually only one entry in this array.</span></span>

</dd> <dt>

<span data-ttu-id="1278f-122">*puSurfaceMoreData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1278f-122">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1278f-123">[**DD \_ 介面 \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more)的指標，此結構包含額外的本機介面資料。</span><span class="sxs-lookup"><span data-stu-id="1278f-123">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="1278f-124">*puCreateSurfaceData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1278f-124">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1278f-125">[**DD \_ CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata)結構的指標，其中包含建立緩衝區所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="1278f-125">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1278f-126">*puhSurface* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1278f-126">*puhSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1278f-127">供 DirectDraw API 使用，而且不應該由驅動程式填入。</span><span class="sxs-lookup"><span data-stu-id="1278f-127">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1278f-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="1278f-128">Return value</span></span>

<span data-ttu-id="1278f-129">**NtGdiDdCreateD3DBuffer** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="1278f-129">**NtGdiDdCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="1278f-130">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1278f-130">Return code</span></span>                                                                                              | <span data-ttu-id="1278f-131">Description</span><span class="sxs-lookup"><span data-stu-id="1278f-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1278f-132"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="1278f-132"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="1278f-133">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="1278f-133">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="1278f-134">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="1278f-134">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="1278f-135">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="1278f-135">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="1278f-136"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="1278f-136"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="1278f-137">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="1278f-137">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="1278f-138">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="1278f-138">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="1278f-139">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="1278f-139">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1278f-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="1278f-140">Requirements</span></span>



| <span data-ttu-id="1278f-141">需求</span><span class="sxs-lookup"><span data-stu-id="1278f-141">Requirement</span></span> | <span data-ttu-id="1278f-142">值</span><span class="sxs-lookup"><span data-stu-id="1278f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1278f-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1278f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1278f-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1278f-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1278f-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1278f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1278f-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1278f-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1278f-147">標頭</span><span class="sxs-lookup"><span data-stu-id="1278f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="1278f-148"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1278f-148"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1278f-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1278f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1278f-150">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="1278f-150">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
