---
description: 查詢先前為其功能建立的 Microsoft DirectDraw 物件之核心模式標記法。
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: 'NtGdiDdQueryDirectDrawObject 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 557854f70f4f1a55022b16d1bfe045efbc017a13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847469"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a><span data-ttu-id="2ef75-103">NtGdiDdQueryDirectDrawObject 函式</span><span class="sxs-lookup"><span data-stu-id="2ef75-103">NtGdiDdQueryDirectDrawObject function</span></span>

<span data-ttu-id="2ef75-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="2ef75-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="2ef75-105">相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="2ef75-106">查詢先前為其功能建立的 Microsoft DirectDraw 物件之核心模式標記法。</span><span class="sxs-lookup"><span data-stu-id="2ef75-106">Queries a previously created kernel-mode representation of a Microsoft DirectDraw object for its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef75-107">語法</span><span class="sxs-lookup"><span data-stu-id="2ef75-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a><span data-ttu-id="2ef75-108">參數</span><span class="sxs-lookup"><span data-stu-id="2ef75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef75-109">*hDirectDrawLocal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef75-110">先前建立之核心模式 DirectDraw 裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2ef75-110">Handle to the previously-created kernel-mode DirectDraw device.</span></span>

</dd> <dt>

<span data-ttu-id="2ef75-111">*pHalInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-111">*pHalInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef75-112">將填入裝置功能之 [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2ef75-112">Pointer to a [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) structure that will be filled with the device's capabilities.</span></span> <span data-ttu-id="2ef75-113">請參閱 DDK 檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2ef75-113">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="2ef75-114">*pCallBackFlags*</span><span class="sxs-lookup"><span data-stu-id="2ef75-114">*pCallBackFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2ef75-115">呼叫端提供之緩衝區的指標，此緩衝區會儲存驅動程式回報的回呼旗標。</span><span class="sxs-lookup"><span data-stu-id="2ef75-115">Pointer to a caller-provided buffer that stores driver-reported callback flags.</span></span> <span data-ttu-id="2ef75-116">緩衝區的大小應為3個 \* sizeof (DWORD) ，並以下列順序儲存回呼旗標： pCallBackFlags \[ 0 \] 用於 [**dd \_ 回呼**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks)中的旗標，pCallBackFlags 1 用於 dd SURFACECALLBACKS 中的旗標， \[ \] 而 pCallBackFlags [**\_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks) \[ 2 \] 用於 [**dd \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks)中的旗標。</span><span class="sxs-lookup"><span data-stu-id="2ef75-116">The buffer should be of size 3\*sizeof(DWORD) and stores callback flags in the following order: pCallBackFlags\[0\] for flags in [**DD\_CALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), pCallBackFlags\[1\] for flags in [**DD\_SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks), and pCallBackFlags\[2\] for flags in [**DD\_PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks).</span></span> <span data-ttu-id="2ef75-117">請參閱 DDK 檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2ef75-117">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="2ef75-118">*puD3dCallbacks* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-118">*puD3dCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef75-119">Direct3D 回呼指標的資料表指標。</span><span class="sxs-lookup"><span data-stu-id="2ef75-119">Pointer to a table of Direct3D callback pointers.</span></span> <span data-ttu-id="2ef75-120">資料表會填入 Gdi32.dll 內模仿 Direct3D 顯示驅動程式的函式指標。</span><span class="sxs-lookup"><span data-stu-id="2ef75-120">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="2ef75-121">此回呼資料表與 \_ DDK 檔中所討論的 D3DHAL D3DCALLBACKS 結構相同。</span><span class="sxs-lookup"><span data-stu-id="2ef75-121">This callback table is identical to the D3DHAL\_D3DCALLBACKS structure discussed in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="2ef75-122">*puD3dDriverData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-122">*puD3dDriverData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef75-123">[**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata)資料的指標，如 DDK 檔中所述。</span><span class="sxs-lookup"><span data-stu-id="2ef75-123">Pointer to [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) data, as described in the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="2ef75-124">*puD3dBufferCallbacks* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-124">*puD3dBufferCallbacks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef75-125">回呼指標資料表的指標。</span><span class="sxs-lookup"><span data-stu-id="2ef75-125">Pointer to a table of callback pointers.</span></span> <span data-ttu-id="2ef75-126">資料表會填入 Gdi32.dll 內模仿 Direct3D 顯示驅動程式的函式指標。</span><span class="sxs-lookup"><span data-stu-id="2ef75-126">The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver.</span></span> <span data-ttu-id="2ef75-127">此回呼資料表與 DDHAL \_ DDEXEBUFCALLBACKS 結構相同，它會對應至 DDK 檔中所討論的 [**DD \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) 結構，不同之處在于 **DD \_ D3DBUFCALLBACKS** 中 XxxD3DBuffer 的成員會取代為 XxxExecuteBuffer DDHAL 中的 DDEXEBUFCALLBACKS \_ 。</span><span class="sxs-lookup"><span data-stu-id="2ef75-127">This callback table is identical to the DDHAL\_DDEXEBUFCALLBACKS structure, which maps to the [**DD\_D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) structure discussed in the DDK documentation, except that members XxxD3DBuffer in **DD\_D3DBUFCALLBACKS** are replaced with XxxExecuteBuffer in DDHAL\_DDEXEBUFCALLBACKS.</span></span>

</dd> <dt>

<span data-ttu-id="2ef75-128">*puD3dTextureFormats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-128">*puD3dTextureFormats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef75-129">[**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85))結構陣列的指標，定義一組允許的材質格式。</span><span class="sxs-lookup"><span data-stu-id="2ef75-129">Pointer to an array of [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structures that define the set of permissible texture formats.</span></span>

</dd> <dt>

<span data-ttu-id="2ef75-130">*puNumHeaps* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-130">*puNumHeaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef75-131">[**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)的 **dwNumHeaps** 成員指標。**vmiData**。</span><span class="sxs-lookup"><span data-stu-id="2ef75-131">Pointer to the **dwNumHeaps** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**.</span></span> <span data-ttu-id="2ef75-132">**DwNumHeaps** 成員會指定 *puvmList* 中的記憶體堆積數目。</span><span class="sxs-lookup"><span data-stu-id="2ef75-132">The **dwNumHeaps** member specifies the number of memory heaps in *puvmList*.</span></span> <span data-ttu-id="2ef75-133">請參閱 DDK 檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2ef75-133">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="2ef75-134">*puvmList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-134">*puvmList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef75-135">影片記憶體堆積描述項清單的指標。</span><span class="sxs-lookup"><span data-stu-id="2ef75-135">Pointer to a list of video memory heap descriptors.</span></span> <span data-ttu-id="2ef75-136">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2ef75-136">Can be **NULL**.</span></span> <span data-ttu-id="2ef75-137">未使用此參數，因為影片記憶體管理完全是在核心模式中處理。</span><span class="sxs-lookup"><span data-stu-id="2ef75-137">This parameter is not used because video memory management is handled entirely within kernel mode.</span></span>

</dd> <dt>

<span data-ttu-id="2ef75-138">*puNumFourCC* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-138">*puNumFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef75-139">[**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)的 **puNumFourCCCodes** 成員指標。**ddCaps**。</span><span class="sxs-lookup"><span data-stu-id="2ef75-139">Pointer to the **puNumFourCCCodes** member of [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.</span></span> <span data-ttu-id="2ef75-140">**PuNumFourCCCodes** 成員會指定驅動程式支援的 [四個字元碼 (FOURCC)](../directshow/fourcc-codes.md)碼數目。</span><span class="sxs-lookup"><span data-stu-id="2ef75-140">The **puNumFourCCCodes** member specifies the number of [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) codes that the driver supports.</span></span> <span data-ttu-id="2ef75-141">請參閱 DDK 檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2ef75-141">See DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="2ef75-142">*puFourCC* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-142">*puFourCC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef75-143">支援的 [四個字元代碼清單的指標 (FOURCC) ](../directshow/fourcc-codes.md) 介面格式。</span><span class="sxs-lookup"><span data-stu-id="2ef75-143">Pointer to a list of supported [Four-Character Codes (FOURCC)](../directshow/fourcc-codes.md) surface formats.</span></span> <span data-ttu-id="2ef75-144">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2ef75-144">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef75-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ef75-145">Return value</span></span>

<span data-ttu-id="2ef75-146">如果成功，此函式會傳回 **TRUE**;否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2ef75-146">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef75-147">備註</span><span class="sxs-lookup"><span data-stu-id="2ef75-147">Remarks</span></span>

<span data-ttu-id="2ef75-148">這個函式的呼叫是設計成在兩個步驟的進程中進行。</span><span class="sxs-lookup"><span data-stu-id="2ef75-148">A call to this function is designed to be made in a two-step process.</span></span> <span data-ttu-id="2ef75-149">在第一個步驟中， *puFourCC*、 *puvmList* 和 *puD3dTextureFormats* 應該是 **Null**，而 [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) 會填入 [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)。**ddCaps**。**dwNumFourCCCodes**、 **DD \_ HALINFO**。**vmiData**。**dwNumHeaps** 和 [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata)。**dwNumTextureFormats** ，其中包含要傳回的專案數。</span><span class="sxs-lookup"><span data-stu-id="2ef75-149">In the first step, *puFourCC*, *puvmList* and *puD3dTextureFormats* should be **NULL**, and [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) will fill in [**DD\_HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**.**dwNumFourCCCodes**, **DD\_HALINFO**.**vmiData**.**dwNumHeaps**, and [**D3DHAL\_GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** with the number of entries that are to be returned.</span></span> <span data-ttu-id="2ef75-150">在第二個呼叫中，呼叫端應配置指定大小的陣列，並傳遞這些指標，而不是 *puFourCC*、 *puvmList* 和 *puD3dTextureFormats* 參數中的 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="2ef75-150">In the second call, the caller should allocate arrays of the indicated size and pass those pointers instead of **NULL** values in the *puFourCC*, *puvmList* and *puD3dTextureFormats* parameters.</span></span> <span data-ttu-id="2ef75-151">陣列接著會填入適當的資料。</span><span class="sxs-lookup"><span data-stu-id="2ef75-151">The arrays will then be populated with appropriate data.</span></span>

<span data-ttu-id="2ef75-152">建議應用程式使用 DirectDraw 和 [Direct3D](../direct3d10/d3d10-graphics-reference.md) api 來建立和管理圖形裝置物件。</span><span class="sxs-lookup"><span data-stu-id="2ef75-152">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="2ef75-153">這些結構以簡化與作業系統無關的方式來抽象化裝置建立程式。</span><span class="sxs-lookup"><span data-stu-id="2ef75-153">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef75-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ef75-154">Requirements</span></span>



| <span data-ttu-id="2ef75-155">需求</span><span class="sxs-lookup"><span data-stu-id="2ef75-155">Requirement</span></span> | <span data-ttu-id="2ef75-156">值</span><span class="sxs-lookup"><span data-stu-id="2ef75-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef75-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ef75-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2ef75-158">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2ef75-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ef75-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2ef75-160">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ef75-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2ef75-161">標頭</span><span class="sxs-lookup"><span data-stu-id="2ef75-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ef75-162"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ef75-162"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ef75-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ef75-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef75-164">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="2ef75-164">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="2ef75-165">**DdQueryDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="2ef75-165">**DdQueryDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[<span data-ttu-id="2ef75-166">**NtGdiDdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="2ef75-166">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
